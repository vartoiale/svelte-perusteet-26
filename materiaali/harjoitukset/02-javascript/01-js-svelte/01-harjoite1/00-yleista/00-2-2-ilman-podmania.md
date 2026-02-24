# Käyttö: ilman podman-konttia

## Ohjeet tarvittaviin sovelluksiin

(Tässä oletetaan, että teet kehitystä windows-virtuaalikoneella)

Asenna seuraavat kolme ohjelmaa:

1. Github Desktop
2. VS Code
3. node.js

### Asennus: Github Desktop

Lataussivu: [desktop.github.com](https://desktop.github.com)

Asenna github desktop oheisesta linkistä.

Kirjaudu github desktop:iin, ja kloonaa itsellesi paikallinen versio aiemmin käsitellystä harjoitusrepositoriosta.

### Asennus: VS Code

Lataussivu: [code.visualstudio.com](https://code.visualstudio.com)

Asenna vs code oheisesta linkistä.

Pystyt käynnistämään vscoden oikeassa kansiossa klikkaamalla github desktop:issa repositorion yhteydessä yläriviltä `repository` -> `open in visual studio code`.
Tällöin vscode käynnistyy repositorion juurikansioon.

### Asennus: Node.js

1. Lataa node.js sen sivuilta: [nodejs.org/download](https://nodejs.org/download).
2. Asenna node.js

#### Node.js:n lataus

Asennukseen kannattanee valita node.js:n lataussivuilta löytyvä `.msi`-jakelu.

#### Node.js:n asennus

Asennus pitäisi olla `msi`-jakelun osalta melko ongelmaton.

## Ohjeet sovelluksen asennukseen ja käynnistykseen

Jos et halua tai voi käyttää podmania (tai muuta konttityökalua, kuten docker:ia),
voit myös käynnistää palvelimen komentoriviltä.

Tällöin edellytyksenä on, että olet asentanut sopivan [nodejs](https://nodejs.org)-version.

Käynnistys koostuu neljästä vaiheesta:

1. yarn:in käyttöön otto
2. pakettien asennus / päivitys
3. storybookin käynnistys

### `yarn`-komennon käyttöönotto

Projektinhallintaan käytetään `yarn`-komentorivityökalua.

Se tulee node.js:n asennuksen mukana, mutta se pitää vielä erikseen ottaa komentoriviltä käyttöön.

Käyttöönotto tapahtuu komennolla:

```sh
corepack enable
```

Voit suorittaa komennon missä tahansa kansiossa.

### Pakettien asennus ja päivitys

Pakettien asennus ja päivitys onnistuu komennolla (repositorion juuressa):

```cmd
yarn
```

Tämä komento pitää ajaa ennen ensimmäistä käynnistystä.

Toisinaan, kun tehtäviä päivitetään, pitää se ajaa uudelleen.
Esimerkiksi, jos uudessa tehtävässä on otettu uusi javascript-kirjasto käyttöön,
kyseinen kirjasto ei asennu projektiisi ennen kuin ajat install-komennon uudelleen.

Virhetapauksissa, jos svelte-palvelin ei käynnisty, tai tehtävät eivät toimi oikein -
sen jälkeen kun olet ladannut päivitetyt tehtävänannot -
voit kokeilla ajaa uudelleen `yarn`-komennon.

### Harjoitusten käynnistys

Harjoitukset käynnistetään ajamalla komentorivillä, repositorion juurikansiossa, komento:

```cmd
yarn run storybook
```

Tämä käynnistää palvelimen, ja avaa sivun selaimeen. 

Sivun pitäisi tällöin löytyä url-osoitteesta: `localhost:6006`.
