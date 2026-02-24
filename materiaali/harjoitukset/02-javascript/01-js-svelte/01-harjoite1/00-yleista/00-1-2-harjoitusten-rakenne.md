# Harjoitusten rakenteesta ja harjoitusten tekemisestä

Svelteä-tehtävät jakaantuvat kahteen osioon:

1. tehtäväsarja 1 (kevyet svelten alkeet)
2. tehtäväsarja 2, ja siitä eteenpäin (komponenteista rakentuva verkkokauppa sveltellä)

## Tehtäväsarja 1 (kevyet svelten alkeet)

Tehtäväsarja 1 muodostaa kevyen alustuksen svelte:n perusteisiin.

Niissä opitaan tärkeimmät komponenttikirjastojen asiat:

* komponenttien luonti,
* komponenttien käyttö,
* alikomponenttien käyttö ja luonti,
* datan siirtäminen komponentilta sen lapsille.

Näitä ei ole tarkoitettu täydelliseksi alustukseksi sveltelle, vaan apuna on tarkoitus käyttää [svelte.dev](https://svelte.dev)-sivuston tutoriaalia.

### Svelte.dev -sivuston tutoriaali

Tämän repositorion tehtävien lisäksi oletuksena on,
että opiskelija käyttää svelten omaa kevyttä tutoriaalia [svelte.dev](https://svelte.dev)-sivustolta.

Se käsittelee laajuudessaan kattavammin svelten teknisiä ominaisuuksia, 
kuin tämä opetussisältö.

* [svelte.dev -tutoriaali](https://svelte.dev/tutorial)

Svelte:n omasta tutoriaalista olisi hyvä tehdä ainakin seuraavat osiot:

* introduction
* reactivity
* props
* logic

Hyödyllistä on kuitenkin lukea tutoriaalia pidemmällekin.

### Tiedostot harjoituskansiossa: tehtäväsarja 1

Tehtäväsarja 1 koostuu tiedostoista `teht1.svelte` - `teht6.svelte`.

Tämä tiedostojen numerointi johtuu historiallisista syistä. Se tullaan mahdollisesti myöhemmin korjaamaan vähän selvemmäksi.

## Tehtäväsarja 2+ (paloista rakentuva verkkokauppa sveltellä)

Tehtäväsarjasta 2 eteenpäin,
lähdemme rakentamaan uudelleen, tyhjästä, svelte-komponenteista, aiemmin html-tehtävissä luotua verkkokauppaa.

Teimme aiemmin html-sivuna verkkokaupan etusivusta yhden ruudullisen kokoisen version, 
joka suurinpiirtein sisälsi sivun `header`- ja `footer`-osiot, sekä näiden välissä pienen valkoisen viirun,
symboloimassa sivun varsinaista sisältöä.
Sivun varsinaisen pitkän sisällön siis jätimme pois harjoituksesta.

Nyt toteutamme tuon saman kokonaisuuden uudelleen.
Tällä kertaa vain pilkomme sivun paloiksi,
ja toteutammekin sen komponentteina, svelte:llä.

Lisäämme lopuksi sivulle myös hieman oikeaa sisältöä ylä- ja alapalkin välille,
sekä toteutamme yksinkertaisen hakusivun mvp:n (engl. minimum viable product).
Hakusivumme ei käytä oikeaa hakumoottoria taustalla,
mutta se osaa kertoa käyttäjälle, että käyttäjän hakemaa asiaa ei sivulta löytynyt.

Koska sivu on jo entuudestaan tuttu,
sen html ja css -osuuksiin ei kiinnitetä juuri huomiota, 
koska niiden oletetaan olevan tuttuja jo edellisestä harjoituksesta.

Koska sivu on jo kertaalleen toteutettu tavallisella html:llä ja css:llä,
sivun rakentamisen pitäisi mennäkin jo huomattavasti edellistä kertaa nopeammin.

### Tehtävien rakenne

Tehtäväsarjasta 2 eteenpäin,
jokainen tehtävä toteuttaa sivulle yhden tai useamman komponentin,
joita käytetään lopullisen sivun tekemisessä.

Tehtävien hakemistot on nimetty vähän hassusti numeroilla,
mutta niiden sisällä itse komponentit on nimetty kohdettaan kuvaavammin.

Esimerkiksi:

* kansio `teht07` (`/harjoitukset/02-javascript/01-svelte/teht07`) - luodaan komponentit sivun yläpalkin alempaa riviä varten,
* kansio `teht08` (`/harjoitukset/02-javascript/01-svelte/teht08`) - luodaan komponentit sivun yläpalkin ylempää riviä varten, ja
* kansio `teht09` (`/harjoitukset/02-javascript/01-svelte/teht09`) - kootaan `teht07`- ja `teht08`-kansioiden komponentit yhdeksi kokonaiseksi yläpalkiksi.

### Tiedostot harjoituskansiossa: tehtäväsarja 2

Tehtäväsarja 1 koostuu kansioista `teht7` - `teht40`, ja niiden sisältä löytyvistä komponenteista. 
Tämä kansioiden numerointi johtuu historiallisista syistä.
(Aiemmassa versiossa kansiot jatkuivat tehtävinä suoraan tehtäväsarja 1:n tehtävistä 1-6.)

Tehtäväsarjassa 2 lähtien, eri tehtäväsarjoissa tehdään aina yksi kierros näiden kansioiden läpi. 
Tällöin muokataan yleensä kaikkien kansioiden komponentteja, mutta joissain tehtäväsarjoissa muokkaukset kohdistuvat vain yksittäisiin komponentteihin.

## Seuraavaksi

Seuraavaksi: [harjoitusten tekemisestä](./00-1-3-harjoitusten-tekemisestä.md)
