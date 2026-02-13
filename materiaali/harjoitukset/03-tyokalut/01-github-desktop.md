# Työkalut: 1. Github Desktop

Kaikki kurssin tehtävät palautetaan tähän samaan classroom-repositorioon, joten versionhallinnan osaaminen on tärkeää.

Versionhallintaa ei kuitenkaan alussa tarvitse osata käyttää komentoriviltä, 
vaan riittää, kun pystyy tekemään tallennuksia versionhallintaan graafisen käyttöliittymän kautta.

Myöhemmin, keväällä lähdemme käyttämään enemmän versionhallintaa, osana ryhmätyöskentelyä, 
jolloin myös versionhallinnan osaaminen korostuu.

## Github Desktop - githubin graafinen versionhallinnan työpöytäsovellus

linkki: [desktop.github.com](https://desktop.github.com)

Asenna itsellesi Github Desktop.

Tarvittaessa Github Desktop on saatavilla myös linux-ympäristöön.

Github Desktopin keskeisiä etuja on sen kyvykkyys helppoon talletettavien koodin osien valintaan.
Tarvittaessa Github Desktop mahdollistaa rivikohtaisen muutosten poiminnan valinnan.

## Lyhyt ohjeistus Github Desktop:in käyttöön

### Sovelluksen käyttö

#### Kirjautuminen

Ladattuasi sovelluksen, se pyytää kirjautumaan ja sallimaan github-tunnuksen käytön sovelluksesta.
Tällä hetkellä tämä onnistuu näppärästi, sovelluksen ohjatessa selaimeen, 
jossa pystyt yhdistämään sovelluksen käyttämään github-tunnustasi.

#### Repositorion lisääminen

Repositorion voi avata github desktopiin kolmella tavalla ylävalikosta:

* `File > New repository` - luo uusi tyhjä versionhallinnan alainen projekti.
* `File > Add local repository` - lisää sovellukseen paikallinen repositorio, jonka olet aiemmin luonut tai kloonannut.
* `File > Clone repository` - kloonaa githubista tiliisi yhdistetty repositorio.

Valitessasi tallennuskansiota on mahdollista tehtä virheitä. 
Tähän liittyen voit lukea alhaalta ohjeita hyvästä kansion sijainnista, osiosta [Repositorion polku](#repositorion-polku).

#### Repositorion avaaminen tekstieditoriin

Github Desktop osaa avata valittuna olevan projektin juurikansion tekstieditoriisi.

Se tuntuu suosivan vscoden käyttöä tekstieditorina, mahdollisesti koska molemmat ovat microsoftin omistamia tuotteita.

Repositorion juurikansion avaaminen tekstieditoriin tapahtuu ylävalikosta `Repository > Open in ...`.

#### Commit-tallennukset

Kun olet muokannut tiedostoja, tallennus (engl. commit) tapahtuu seuraavasti:

1. tarkista oikeasta listauksesta mitkä tiedostoista haluat tallentaa "changed files"-otsakkeen alta.
2. valitse tiedostot, jotka haluat tallentaa
3. valitse listasta rivit, jotka haluat tallentaa
4. anna tallennukselle nimi "summary (required)"-kenttään - tämä on pakollinen tieto
5. voit halutessasi antaa pidemmän selostuken tallennuksen sisällöistä "description"-kenttään
6. tallenna commit painamalla sinistä "Commit to"-nappia

Kun olet tehnyt yhden tai useamman tallennuksen, 
muista siirtää tallennuksesi myös versionhallinnan palvelimelle, 
eli yleensä juurikin githubiin.

7. klikkaa oikeasta yläkulmasta löytyvää "push changes"-nappia

Näin olet saanut talletettua muutoksesi, ja muutokset on - toivottavasti onnistuneesti - lähetetty palvelimelle talteen.

Kurssin kannalta on huomioitavaa, että tämä on myös se tilanne, jossa talletetut tehtäväsi on määritelty palautetuiksi. 
Kun olet tallettanut tehtäväsi palvelimelle, ne ovat myös opettajan tarkasteltavina.

### Repositorion polku

Voit tallentaa git-versionhallintaa käyttävät projektit minne tahansa paikallisen koneesi kovalevyllä.

Huomioi kuitenkin, että git-repositorioita **ei kannata** tallentaa microsoftin OneDrive:n hallinnoimiin kansioihin.
Git ja OneDrive ovat molemmat versionhallinnan työkaluja, 
eikä niiden käyttäminen päällekkäin ei tuo mitään käytännön hyötyä.
Päin vastoin, ne saattavat kilpailla keskenään siitä, 
kumpi niistä päättää tallentuvien muutosten hyväksynnästä virhetilanteissa.
OneDrive ei välttämättä myöskään ole hyvä paikka koodiprojektien tallentamiseen, 
koska OneDrive pyrkii synkronoimaan hallinnoimiensa kansioiden sisältöä jatkuvasti pilveen,
ja tämä saattaa dynaamisten sovelluskehitysprojektien kanssa johtaa turhaan työhön.
Esim. web-ohjelmoinnin maailmassa, 
javascript-projektien riippuvuuksia sisältävät `node_modules`-kansiot saattavat kasvaa hyvin suuriksi, 
useita gigatavuja kattaviksi kokonaisuuksiksi. 
Jos OneDrive synkronoi tällaista kansiota jatkuvasti, samalla kun sitä suuresti muokataan,
saattaa tämä viedä mehuja tehokkaammaltakin koneelta.

#### Suositeltu repositorion sijainti

Tämän opetuksen puitteissa suositeltu polku ohjelmointiprojekteille on seuraava:

```sh
<sopiva juurikansio>/workspace/gradia/<repositorio>
```

Tällöin windowsissa kansio voisi sijaita käyttäjän omissa tiedostoissa:

```sh
c:\Käyttäjät\<windowsin käyttäjätunnus>\workspace\gradia\<repositorio>
```

tai englanninkielisessä windows-ympäristössä:

```sh
c:\Users\<windowsin käyttäjätunnus>\workspace\gradia\<repositorio>
```

Tässä polussa:

* `workspace` on valittu varattu sana, joka toivottavasti ilmaisee, 
että sen sisältö koostuu jonkinlaisista projekteista.
* `gradia` ilmaisee, että kansiossa sijaitsevat projektit liittyvät gradia-kouluun.

Jos teet samalla tietokoneella omia projektejasi, 
voit luoda `workspace`-kansion alle muita projektejasi varten toisia kansioita:

* toisessa oppilaitoksessa suoritettavia opintoja varten tarvittavat repositoriot voisivat olla yhdessä kansiossa.
  Esim. jamk:in repositoriot voisivat olla `workspace\jamk`-kansiossa.
* omalla github-tunnuksellasi tekemäsi projektit, jotka eivät ole kouluprojekteja, 
  voisivat olla github-tunnuksen mukaan nimetyssä `workspace\<github-käyttäjätunnus>`-kansiossa.
  
Näin pystyt pitämään omat ja koulun projektit helposti erillään toisistaan.
