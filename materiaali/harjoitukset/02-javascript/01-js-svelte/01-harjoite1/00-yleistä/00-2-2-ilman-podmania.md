#### Ilman podman-konttia

Jos et halua tai voi käyttää podmania (tai muuta konttityökalua, kuten docker:ia),
voit myös käynnistää palvelimen komentoriviltä.

Tällöin edellytyksenä on, että olet asentanut sopivan [nodejs](https://nodejs.org)-version.

Käynnistys koostuu kahdesta vaiheesta:

1. pakettien asennus / päivitys
2. storybookin käynnistys

##### Pakettien asennus ja päivitys

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

##### Harjoitusten käynnistys

Harjoitukset käynnistetään ajamalla komentorivillä, repositorion juurikansiossa, komento:

```cmd
yarn run storybook
```

Tämä käynnistää palvelimen, ja avaa sivun selaimeen. 

Sivun pitäisi tällöin löytyä url-osoitteesta: `localhost:6006`.
