### Harjoitusten alkutyöt

Javascript projektit vaativat, että niiden käyttämät javascript-kirjastot asennetaan, 
ennen kuin niitä voidaan käyttää.

Tähän käytämme konttiteknologiaa, ja podman-konttityökalua.

#### Podmanilla kontin ajo

Palvelimen ajamiseen käytämme podman-konttityökalua.

Huomaa, että joudut windowsilla käynnistämään ensin aina podman-desktop-ohjelman, 
ennenkuin pystyt ajamaan podmania komentoriviltä.

##### Podmanin asennus

###### Alkuvalmistelut

Aja powershellissä, mahdollisesti pääkäyttäjän oikeuksilla komento:

```cmd
wsl --update
```

Jos koneellasi ei ole viimeisintä versiota WSL:stä (windows subsystem for linux), 
komento lataa ja päivittää koneellesi uusimman version WSL:stä.

###### Asennus

Podman löytyy osoitteesta [podman.io](https://podman.io).
Lataa ja asenna sekä podman-desktop, että podman-komentorivityökalu.

Valitse podman-desktop:in asennuksen aikana käyttöön wsl, ja valitse, 
että asennusohjelma konfiguroi wsl:n toimimaan podmanin kanssa.

###### Podman-desktop-työkalun konfigurointi

Podman vaatii ensimmäisen käynnistyksen yhteydessä konfiguroinnin. 
Tämä onnistuu klikkaamalla etusivulta nappia jossa mainitaan jotain podmanin konfiguroinnista.
Avautuvasta wizardista valitse aina next-nappi, kun edellinen vaihe valmistuu.
Lopulta kun kaikki on konfiguroitu, olet valmis siirtymään komentoriville.

##### Kontin käynnistys

Käynnistä kontti komennolla:

```cmd
podman compose -f compose.yml up
```

Tällöin storybook avautuu selaimessa osoitteeseen [`localhost:6006`](http://localhost:6006).

Komento ajaa podmanin compose-aliohjelman, 
ja antaa sille konfiguraatiotiedostoksi tämän repositorion juuresta löytyvän `compose.yml`-tiedoston.
Lopussa oleva `up` kertoo komposelle, että haluat nostaa kontit pystyyn.

Composen sammuttaminen tapahtuu terminaalissa näppäinkomennolla `ctrl + C`.

HUOM: Joudut toistaiseksi jokaisen koodiin tapahtuvan muutoksen jälkeen käynnistämään composen uudelleen,
jotta muutokset näkyvät palvelimella.

Kontin voi sammuttamisen jälkeen ajaa alas komennolla:

```cmd
podman compose -f compose.yml down
```

Tarvittaessa, jos käynnistys ei onnistu, voit alasajon jälkeen poistaa kontin komennolla:

```cmd
podman rmi localhost/nodejs
```

Tämä poistaa "localhost/nodejs"-nimisen kontin. 
Olemme antaneet `Containerfile`-tiedostossa kontillemme nimeksi juuri kyseisen "localhost/nodejs"-nimen,
käyttäen `index`-attribuuttia.
