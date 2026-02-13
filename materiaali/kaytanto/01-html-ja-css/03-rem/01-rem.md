# yksiköistä CSS:ssä ja erityisesti `rem`-yksiköistä

CSS tukee lukuisia erilaisia mittayksiköitä.

Yleinen suositus sivuilla on käyttää pikseleitä (`px`) tai dokumentin juurielementin fonttikoon määräytyviä `rem`-yksiköitä.

## Miten `rem` toimii?

`rem` on kuin `px`, mutta sen koko on suhteellinen dokumentin juurielementin (`:root` tai html-dokumentissa `html`) fonttikokoon nähden.

Esimerkiksi, jos olemme määrittäneet dokumentin juureen fonttikoon:

```css
:root {
    font-size: 10px;
}
```

on tällöin yhden `rem`-yksikön (`1rem`) pituus `10px`.

Vastaavasti:

* jos juuren fonttikoko on `10px`, `2rem` on `20px`,
* jos juuren fonttikoko on `16px`, `1rem` on `16px`,
* jos juuren fonttikoko on `16px`, `2rem` on `32px`,
* jos juuren fonttikoko on `100px`, `1rem` on `200px`.

Tämä pätee kaikkialla sivulla.

## `rem` vai `px`

`rem` on käytännöllisempi yksikkönä kuin `px`,
koska sitä pystyy muokkaamaan `@media`-määrittelyiden avulla.

Voimme määrittää juuren fonttikoon muuttumaan tietyillä näytön leveyksillä,
jolloin kaikki `rem`-yksiköllä määritetyt mitat muuttuvat samassa suhteessa.

Näin pystymme helposti vaikuttamaan sivun elementtien kokojen suhteisiin hallitusti yhdestä paikasta,
säilyttäen samalla sivun sopusuhtaisena.

Toisaalta pystymme myös helposti kokeilemaan erilaisia kokoja,
ilman että joutuisimme tyylejä muuttaessamme vaihtamaan monia eri pikseliarvoja, useammassa eri paikassa.

## `em`-yksikköä ei kannata yleensä käyttää

`rem`-yksikön kaltaista `em`-yksikköä ei kuitenkaan yleisesti suositella käyttämään erikoistapauksia lukuunottamatta.

`em`-yksikön ominaisuus, ja ongelma, on, 
että se on suhteellinen, sen elementin fontin kokoon, 
jossa sitä käytetään.

Se siis mahdollistaa elementin koon vaihtamisen irrallaan sen viereisistä elementeistä,
aina kun sen fontin koko vaihtuu.

Tämän takia se saattaa muuttaa sivun ulkoasua yllättävillä tavoilla, 
jos sen käytössä ei ole tarkkana.
Liiallinen käyttö saattaa tehdä sivun ulkoasusta sattumanvaraisen näköisen.

Toisaalta `em` on erittäin toimiva yksikkö erikoistilanteissa:

* Jos esimerkiksi haluamme lisätä elementin ympärille tyhjää tilaa suhteessa sen fonttikokoon,
tämä onnistuu helposti juuri `em`-elementin avulla.

## Muut CSS:n mittayksiköt

Voit lukea muista yksiköistä esimerkiksi
mdn:n [Values and units](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Values_and_units) -dokumentaatiosta.

## esimerkit

Voit katsella eri yksiköiden (`px`, `em` ja `rem`) eroja tästä samasta kansiosta löytyvästä `index.html`-esimerkkisivusta.

Esimerkeistä voit nähdä eroja siitä,
miksi esimerkiksi `em`-yksiköitä ei kannata käyttää.

## lisää

`rem`-yksiköistä löytyy lisää harjoituksen 1.3.1 tehtävästä 4.