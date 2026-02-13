# Teoria: 3.2 Kontit

Edellä käsittelimme `npm`-pakettienhallintatyökalua.

Npm:n muodostamat projektit ovat yleensä hyvin monimutkaisia, ja ne toimivat eri ympäristöissä eri tavalla.

Monet npm:n kautta käytetyt tiedostot vaativat järjestelmäkohtaisia versioita asennetuiksi toimiakseen, 
jolloin projekti saattaa toimia yhdellä koneella, kun taas toisella se ei välttämättä toimikaan.

Esimerkiksi projekti saattaa toimia hyvin yhden tiimiläisen linux-koneella, 
mutta toisen windows-koneella ja kolmannen mac-koneella se ei välttämättä toimikaan.
Vastaavasti yhdellä saattaa olla asennettuna noden versio 20, ja toisella 22, ja projekti toimiikin vain versiolla 20.

Tällöin apuun tulevat kontit (englanniksi containers).
Kontit ovat virtuaalikoneen kaltaisia, mutta kevyempiä virtuaalisia ympäristöjä,
joille määritellään tarkasti, mitä käyttöjärjestelmää niissä käytetään, ja mitä paketteja järjestelmästä löytyy.

Yleinen javascript-koodaajien käyttämä kontti käyttää esimerkiksi tiettyä alpine-linuxin versiota, 
yhdistettynä tiettyyn node.js:n versioon.
Nämä siis määritellään kontin sisällä.

Tällöin järjestelmävaatimukset siirretään kontin sisälle, 
ja projektin pitäisi toimia kaikilla laitteilla samalla tavalla,
kunhan kyseinen kontti vain saadaan käyntiin jokaisen koneella.

Eli jokainen ajaa tällöin virtuaaliympäristössä konttia omalla koneellaan.

Yleisimpiä konttiohjelmia ovat docker, podman ja kubernetes.
Näistä docker ja podman ovat pienempiin projekteihin tarkoitettuja, 
kun taas kubernetes on monimutkaisempien konttijärjestelmien orkesterointiin tarkoitettu työkalu.

Tässä sisällössä käytämme podman-työkalua, sillä se on lisenssiltään docker-sovellusta suopeampi.
Kubernetes on taas työkaluna paljon monimutkaisempi, eikä siksi kurssin sisällön puitteissa kovinkaan mielenkiintoinen.

## Podman

Podman:in pystyy lataamaan osoitteesta [podman.io](https://podman.io).
Siitä kannattaa asentaa sekä podman desktop -graafinen sovellus, että komentorivityökalu `podman`.

Podmanin graafinen sovellus on näppärä, erityisesti kun tarvitsee nopeasti nähdä listauksia konteista,
ja siitä mitkä niistä ovat ajossa, tai milloin ne on luotu.

Arkisessa käytössä podmanin komentorivityökalu on kuitenkin luultavasti se hyödyllisempi.
Toisaalta, molemmilla pitäisi onnistua samat asiat, joten lopulta kyse on siitä kumpaa tykkää enemmän käyttää.

### Podman tässä kurssissa

Tässä kurssissa tehtäviä varten on tehty erilliset konttikonfiguraatiot valmiiksi, 
eikä niitä tarvitse erikseen luoda.
Keskimäärin riittää siis, että osaa käynnistää kontin ja sulkea sen.

Käynnistus tapahtuu seuraavasti (projektin juuressa):

```sh
podman compose -f ./podman-compose.yml up
```

Sammutus tapahtuu:

```sh
podman compose -f ./podman-compose.yml down
```

Jos kontin luoma image pitää luoda uudelleen, vanhan voi poistaa komennolla:

```sh
podman rmi <kontin imagen nimi>
```

Esimerkiksi svelte-harjoitusten tapauksessa kontin nimi on `nodejs`, joten komento näyttää seuraavalta:

```sh
podman rmi nodejs
```

`compose up` luo tuon poistetun tiedoston automaattisesti uudelleen.

Voit tarkistaa imagen nimen komennolla:

```sh
podman images
```

Seuraavissa osissa esitellään tarkemmin konttien toimintaa ja konfiguraatiota

## Miten kontit toimivat

Kontit määritellään kahdella keskeisellä eri tiedostomuodolla:

* `Containerfile` (vanhalta nimeltään `Dockerfile`) - määrittelee yhden kontin sisällön
* `podman-compose.yml` - määrittää miten yksi tai useampi kontti käynnistetään

### `Containerfile`-tiedosto

`Containerfile`, tai vanhalta nimeltään `Dockerfile` on yaml-muotoinen tiedosto,
joka määrittää sen miten kontin käyttämä image rakennetaan.

Se sisältää yhden tai useamman komennon.
Jokainen tällainen komento alkaa isoilla kirjaimilla rivin alussa kirjoitetulla varatulla sanalla, 
ja sisältää komennolle annetut parametrin sen rivin muuna tekstinä.

Tälläinen komento saattaa olla esimerkiksi:

```Dockerfile
FROM node:22.12-alpine
```

Se kertoo, että kontin imagea ei luoda tyhjästä, 
vaan sen pohjana käytetään aiempaa imagea.
Tässä tapauksessa dockerhub:ista löytyvää node-imagea versiolla "22.12-alpine".
Tämä tarkoittaa, että imagelle on esiasennettu noden versio 22.12 
ja sen käyttöjärjestelmänä on minimiaalinen linux-distribuutio nimeltään alpine.

Oikea `Dockerfile` saattaa näyttää seuraavalta:

```Dockerfile
FROM node:22.12-alpine

RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app

WORKDIR /home/node/app

COPY package*.json ./

USER node

RUN npm install

COPY --chown=node:node . .

EXPOSE 6006

CMD [ "npm", "run", "storybook" ]
```

Tässä luodaan:

1. valmiista node-imagesta pohja, jolle
2. luodaan kansioita,
3. määritetään työskentelykansio,
4. kopioidaan konfiguraatio tiedostoja (`package.json` ja `package-lock.json`),
5. asetetaan käyttäjä,
6. asennetaan npm-paketit
7. kopioidaan lisää tiedostoja
8. avataan portti 6006 (jota storybook käyttää)
9. ajetaan komento `npm run storybook`, käynnistäen storybookin.

Konttien hienous piilee siinä, että nimensä mukaisesti ne ovat vakiomallisia.
Tarkoittaen tässä sitä, että jokainen edellä olevista komennoista oikeastaan luo uuden kontin,
joka asettuu edellisten konttitasojen päälle.

Mitä tämä sitten käytännössä tarkoittaa: 
koska kontit rakentuvat tasoista, ne pystyvät uudelleenkäyttämään olemassa olevia tasoja.

Toisaalta, kontit voivat rakentua toistensa päälle.
Samaan aikaan, konttiohjelman ei tarvitse luoda niitä aina uudestaan alusta, jos jotain osaa päivitetään.
Esimerkiksi jos `package.json`-tiedostoa päivitetään, ja konttiohjelma huomaa tämän muutoksen, 
seuraavan ajon aikana, konttiohjelma voi uudelleenkäyttää kaikki ennen `package.json`-tiedoston käyttöä määritetyt 
konttitasot, ja sen tarvitsee luoda uudelleen vain ne konttitasot, jotka ovat tuon tason yläpuolella.

Konttienhallintaohjelmat pystyvät siis uusiokäyttämään alempiakonttitasoja. 
Toisaalta, jos konttitaso vaatii uudelleenajon, myös kaikki sitä käyttävät tasot vaativat uudelleensuorituksen.

Käytännössä tämä nopeuttaa huomattavasti konttien ajoa.

### `podman-compose.yml`-tiedosto

Siinä missä `Containerfile` määritteli kontin luomiseen tarvittavat vaiheet, 
compose-tiedosto määrittää miten yhtä tai useampaa konttia käytetään.

Tyypillisessä tilanteessa palvelin tarjoilee yhdestä kontista frontend-koodin, 
toisesta käynnistää palvelimen rest-rajapinnan, 
ja kolmannesta huolehtii sql-tietokannan suorituksesta.

Tämä vaatii kaikissa tapauksissa kolmen `Containerfile`-tiedoston luontia - siitä ei pääse yli.
Ilman compose-tiedostoa, tämä vaatisi jokaisen kontin käynnistämistä ja hallintaa erikseen komentoriviltä,
ja verrattain monimutkaisten komentorivikomentojen käyttöä.

Compose-tiedostoa apuna käyttäen näiden konttien hallinta ja yhteistyön määrittäminen onnistuu yhden yaml-tiedoston avulla.

Compose-tiedoston avulla jokaiselle kontille määritellään mm.:

* mitä `Containerfile`-tiedostoa ne käyttävät,
* millä nimellä niitä kutsutaan
* mitä portteja ne käyttävät,
* mihin verkkoihin ne näkyvät, ja
* mitä tiedostojärjestelmiä ne tarvitsevat.

Tässä yhteydessä meidän ei tarvitse välittää, miltä compose-tiedosto näyttää. 
Riittää, että se toimii.
Käynnistykseen ohjeet löytyvät yltä.

Voit kuitenkin halutessasi kurkata käytettyä [compose-tiedostoa](/podman-compose.yml).

## Podman vikatilanteita

### Podman ilmoittaa podman engine:ä luodessa wsl:ään liittyvästä virheestä

Kokeile powershellissä pääkäyttäjänä (administrator):

1. päivittää wsl:n versio - `wsl --update`, tai jos se ei onnistu,
2. asentaa wsl - `wsl --install`

### .ssh-kansio puuttuu

Joissain tilanteissa podman ei välttämättä käynnisty komentoriviltä.

Jos tällöin virheviesti valittaa jotain `.ssh`-kansion puuttumisesta, tarkoittaa se, 
että käyttäjäkansiosi sisällä oleva `.ssh`-kansio puuttuu.

#### Selitys

`.ssh`-kansio pitää sisällään salausavaimet, ja podman käyttää ilmeisesti näitä avaimia jutellessaan wsl-virtuaaliympäristön kanssa.
Podmanin lähdekoodista johtuvan bugin takia podman ei tätä kirjoittaessa ilmeisesti itse osaa luoda puuttuvaa `.ssh`-kansiota,
jolloin se pitää luoda manuaalisesti

#### Korjaus

Mene käyttäjätunnuksesi kansioon joka, löytyy:

* suomenkielisessä windowsissa `C:\käyttäjät\<käyttäjätunnuksesi>`-kansiosta, 
* englanninkielisessä windowsissa `C:\Users\<käyttäjätunnuksesi>`-kansiosta.

Luo kansioon uusi kansio nimellä `.ssh`.

Tämä onnistuu käyttäjäsi kotihakemistosssa, powershellissä, komennolla:

```
mkdir .ssh
```

### Podman ei saa yhteyttä olemassa olevaan podman machineen

Joissain tapauksissa podman ei saa yhteyttä olemassa olevaan podman machine:en.

Tällöin voit poistaa vanhan ja luoda luoda uuden podman machinen seuraavien komentojen avulla:

```sh
podman machine stop
podman machine list
podman machine rm podman-machine-default
podman machine init
podman machine start
podman machine stop
podman machine set --rootful
podman machine start
```

Edellä oletus on, että `podman machine list`-komento on sanonut, 
että olemassa olevan podman machinen nimi on `podman-machine-default`.

Komennot poistavat vanhan podman machinen, luovat uuden ja asettavat sen toimimaan root-tilassa.
Lopuksi kone käynnistetään.

Tämän jälkeen podman-komennon pitäisi toimia oikein. 
Voit kuitenkin mahdollisesti joutua välissä käynnistämään koneen uudelleen.
