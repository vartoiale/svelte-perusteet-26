# Harjoitukset 3: css ja flexbox

Edellisten tehtävien loppupuolella päästiin kokeilemaan css:n ja flexboxin käyttöä valmiin tyylitiedoston muodossa.
Seuraavissa tehtävissä jatketaan tästä, kirjoittamalla omia tyylitiedostoja.

Tyylitiedostojen lisääminen sivulle tapahtui, kuten edellisistä tehtävistä muistamme, 
käyttämällä `link`-metaelementtiä `head`-elementin sisällä.

```html
<head>
  <link href="style5.css" rel="stylesheet" />
</head>
```

## Tehtävät

### Tehtävä 0A - flexbox froggy

**palautettavan tiedoston nimi:** `teht0.jpg` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht0.jpg`) (myös muut kuvaformaatit ja tiedostopäätteet käyvät)

Kokeile flexboxin käyttöä [Flexbox Froggy](https://flexboxfroggy.com/) -sammakkopelissä.

Peli ohjeistaa, miten flexbox toimii. Jos et heti saa juonesta kiinni, ei kannata hätääntyä, ehdit palata peliin myöhemminkin.
Esimerkiksi tämän sivun tehtävät tehtyäsi.

Kun olet päässyt pelin viimeisen kentän läpi, ota pelistä kuvakaappaus, ja lisää se tämän harjoituksen palautuskansioon.

### Tehtävä 0B

**palautettavien tiedostojen nimet:** 

* `teht0.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht0.html`)**
* `teht0.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht0.css`)**

Kopioi aiempien tehtävien html- ja css-tiedostosi uuteen kansioon.

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

Näin sinulla on tallessa aiempi versio, josta lähdet muokkaamaan työtä eteenpäin.

Käytännössä edellinen versio löytyy jo kahdesta paikasta, edellisten tehtävien tiedostoista, sekä versionhallinnasta,
joista molemmista vanhaa versiota olisi helppo halutessa tarkastella.
Tallennamme kuitenkin tässä tiedostoista vielä yhdet kopiot, 
koska ne toimivat pohjana, kalliona, jolle lähdemme rakentamaan uutta sisältöä.
Välillä on ihan mukavaa nähdä nopeasti, mitkä olivat ne lähtökohdat, joista uutta lähdettiin rakentamaan.

### Tehtävä 1 - luokkien nimiä BEM-syntaksilla

**palautettavien tiedostojen nimet:** 

* `teht1.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht1.html`)**
* `teht1.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht1.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

tehtävänanto (alla tarkemmin):

* Poista vanhasta html-dokumentista kaikki `rivi`- ja "`sarake`-luokkien käytöt. (käytä vscoden haku- ja korvaustyökalua. Lue lisää alta.)
  Jätä vielä `class`-attribuutit elementteihin.
* Poista `rivi` ja `sarake` luokat (ja niihin liittyvät säännöt) myös css-tiedostosta.
* lisää html-tiedostoon jokaiselle elementille uusi luokka. Käytä tähän BEM-syntaksia. (Lue lisää [BEM-syntaksista](../../01-01-bem.md) materiaalista.)

#### Ohjeita

##### vscoden haku ja korvaustyökalu

Voit tehdä sanojen haun ja korvauksen nopeasti vscoden hakutyökalun avulla (`ctrl + f`).
Saat korvauskentän näkyviin klikkaamalla nuolta hakukentän vasemmalla puolella.
Etsi sanoilla `rivi` ja `sarake`, ja korvaa nämä tyhjällä ` ` tekstillä tässä uudessa html-tiedostossa.

##### Nimeämisestä

Käytämme luokkien nimeämiseen BEM-sääntöjä.

Tarkoituksena on käyttää luokkien niminä kuvaavia nimiä, joita joku muukin kuin alkuperäinen kehittäjä itse, siis sinä, saattaa ymmärtää.

Jos kaksi elementtiä ovat samanlaisia, esimerkiksi samankaltaisia otsikoita, tai keskenään samankaltaisia listan kohtia,
ei näille tarvitse luoda omaa luokan nimeä, vaan samaa luokan nimeä voi käyttää kaikissa niissä.
Tämä vaatimus täyttyykin melkein itsestään BEM-nimeämistapaa käytettäessä.

#### Alitehtävät

Tehtävään kuuluu seuraavat alitehtävät:

1. nimeä yläpalkki ja alapalkki
2. nimeä alapalkin musta ja harmaa alue
3. nimeä alapalkin harmaan alueen otsikolliset osat
4. nimeä alapalkin mustan alueen osat
5. nimeä yläpalkin alempi rivi
6. nimeä yläpalkin ylempi rivi
7. nimeä loputkin elementit

##### Alitehtävä 3: nimeä alapalkin harmaan alueen otsikolliset osat

Lähdetään helposti nimettävistä sivun osista.

Aloitetaan ylä- ja alapalkista.

Osioiden nimeäminen tapahtui BEM-nimeämistavassa määrittämällä niille pelkkä `block`-muotoinen nimi.

Yläpalkki voidaan yksiselitteisesti nimetä nimellä "sivun-yläpalkki" tai vaikka englannista vakiintuneella nimellä `header`.

Vastaavasti alapalkki voidaan yksiselitteisesti nimetä nimellä "sivun-alapalkki", tai sen englannista vakiintuneettä termillä `footer`.

Sivu siis näyttäisi seuraavan kaltaiselta:

```html
<html>
  <head>
  <body>
    <header class="sivun-yläpalkki">...</header>
    <!-- sivun varsinainen sisältö, josta emme ole kiinnostuneet -->
    <footer class="sivun-alapalkki">...</footer>
  </body>
</html>
```

##### Alitehtävä 3: nimeä alapalkin harmaan alueen otsikolliset osat

Kun alapalkki on nyt nimetty, voimme nimetä alapalkin harmaan ja mustan alueen.

Käytämme tähän BEM-syntaksia `block__element`.

Koska niillä ei oikein ole selvää nimeä, voimme käyttää kuvaavia nimiä:

* harmaa alue - `sivun-alapalkki__harmaa-alue`
* musta alue - `sivun-alapalkki__musta-alue`

Sivu näyttää siis vähän seuraavalta:

```html
<html>
  <head>
  <body>
    <header class="sivun-yläpalkki">...</header>
    <!-- sivun varsinainen sisältö, josta emme ole kiinnostuneet -->
    <footer class="sivun-alapalkki">
      <div class="sivun-alapalkki__harmaa-alue">...</div>
      <div class="sivun-alapalkki__musta-alue">...</div>
    </footer>
  </body>
</html>
```


##### Alitehtävä 3: nimeä alapalkin harmaan alueen otsikolliset osat

Jatketaan edelleen helposti nimettävistä sivun osista, mutta mennään vähän isompiin osioihin.

Nimetään kaikkien sivun alapalkin harmaan-osan otsikoiden osiot.

Vaikka edellä annoimmekin alapalkille BEM-nimeämiskäytännön mukaisen nimen, unohdamme sen nyt.
Teemme näin, koska oikeastaan osiot eivät tässä tapauksessa oikeastaan suoraan kiinnity alapalkkiin.
Siksi niiden nimessä ei tarvitse suoraan mainita tätä kytköstä niiden vanhempien rakenteeseen.

Voit katsoa esimerkkiä alta, siitä miten "asiakaspalvelu"-osion nimeäminen tapahtuu.

###### Ohjeita alitehtävään 3

Kun sivulla on otsikko, voimme helposti päätellä,
että kyseinen osio selvästi muodostaa sivulle itsenäisen osan.

Näin ollen otsikon sisältävän ylemmän tason elementin nimeäminen on helppoa BEM-nimeämiskäytännön ansiosta.

BEM-käytännön mukaan, itsenäisen block-osan luokannimeksi tulee pelkkä `block`-muotoa oleva nimi.

Voimmekin käyttää tuon otsikon sisältävän laajemman elementin nimeämiseen otsikon nimeä. 
Otsikosta itsestään tulee siis block-elementin block-osan nimi.

Esimerkiksi, kun meillä on asiakaspalvelu-osio:

```html
<div>
  <h2>Asiakaspalvelu</h2>
  <ul>
    <li>
      <div>Ma-Su</div>
      <div>24/7</div>
    </li>
  </ul>
</div>
```

Voimme nimetä tämän ylimmän `div`-elementin luokannimen otsikon nimestä muodostetulla nimellä.
Koska otsikko on lyhyt, voimme käyttää otsikkoa sellaisenaan: "asiakaspalvelu".

Kerrataan vielä: 

* edellisen esimerkin ylin `div`-elementti muodostaisi siis oman block-osan,
* block-osan nimi tulisi helposti otsikosta, joka todennäköisesti esiintyy sivulla vain kerran

Tällöin `div`-elementti nimettäisiin siis nimellä `asiakaspalvelu`.

Edellisen esimerkin html näyttäisi nyt siis seuraavalta:

```html
<div class="asiakaspalvelu">
  <h2>Asiakaspalvelu</h2>
  <ul>
    <li>
      <div>Ma-Su</div>
      <div>24/7</div>
    </li>
  </ul>
</div>
```

Nyt block-osiollamme olisi siis nimi.
Tämän jälkeen voisimme nimetä block-osion välittömiä lapsielementtejä käyttäen muotoa `block__element`.

Voisimme nimetä kaksi välitöntä lasta:

* otsikko - `asiakaspalvelu__otsikko`
* lista - `asiakaspalvelu__aukioloajat`

Molemmat ovat kuvaavia nimiä, jotka selvästi kertovat, mistä elementeissä on kyse.

Nyt esimerkki-html näyttäisi seuraavalta:

```html
<div class="asiakaspalvelu">
  <h2 class="asiakaspalvelu__otsikko">Asiakaspalvelu</h2>
  <ul class="asiakaspalvelu__aukioloajat">
    <li>
      <div>Ma-Su</div>
      <div>24/7</div>
    </li>
  </ul>
</div>
```

Tästä jatkaisimme nimeämällä `li`-elementin kuvaavalla nimellä, jatkaen sen vanhemman nimestä:

```
asiakaspalvelu__aukioloajat__aukioloaika
```

Vastaavasti li-elementin lapset pitäisi nimetä kuvaavasti:

* päivät - `asiakaspalvelu__aukioloajat__aukioloaika__päivät`
* aika avoinna - `asiakaspalvelu__aukioloajat__aukioloaika__avoinna`

Lopulta esimerkki-html näyttäisi seuraavalta:

```html
<div class="asiakaspalvelu">
  <h2 class="asiakaspalvelu__otsikko">Asiakaspalvelu</h2>
  <ul class="asiakaspalvelu__aukioloajat">
    <li class="asiakaspalvelu__aukioloajat__aukioloaika">
      <div class="asiakaspalvelu__aukioloajat__aukioloaika__päivät">Ma-Su</div>
      <div class="asiakaspalvelu__aukioloajat__aukioloaika__avoinna">24/7</div>
    </li>
  </ul>
</div>
```

Nyt tehtävänäsi olisi siis samaa metodia käyttäen nimetä muut alapalkin harmaan osan otsikolliset osiot.

##### alitehtävä 4: nimeä alapalkin mustan alueen osat

Nimeä alapalkin mustan alueen osat.

Tämä onkin helpompi tehtävä, koska alapalkin mustalla osalla on vain muutama kenttä.

Otsikkoa ei kuitenkaan ole, joten joudut itse miettimään hyvän block-osan

##### alitehtävä 5: nimeä yläpalkin alempi rivi

Nimeä yläpalkin alempi rivi, ja sen osat.

Huomaa, että kyse näyttäisi olevan listauksesta.

##### alitehtävä 6: nimeä yläpalkin ylempi rivi

Nimeä yläpalkin ylempi rivi, ja sen osat.

Tässä osilla ei oikeastaan ole suurempaa yhtenäistä tekijää.

Nimet pitäisi olla kuitenkin helppo johtaa elementtien tehtävistä sivulla.

##### alitehtävä 7. nimeä loputkin elementit

Nimeä lopuksi kaikki loputkin elementit.

Koska kyse on lopulta suomen, tai englannin, kielen käytöstä, 
oikeita vaihtoehtoja ei ole.

Tärkeätä kuitenkin on, että nimet ovat mahdollisimman selviä ja kuvaavia.

### Välihuomio

Nyt kun olet lisännyt jokaiselle elementille oman kuvaavan luokan nimen, alamme vähitellen lisäämään näihin luokkiin flexbox-sääntöjä, jotka muistuttavat aiemmin käytettyjä, valmiiksi luotuja sääntöjä.
Teemme tämän kuitenkin askel kerrallaan.

### Tehtävä 2 - `body`-elementin margin nollataan

Tässä tehtävässä poistetaan oletusarvona oleva css-sääntö `body`-elementiltä.

**palautettavien tiedostojen nimet:** 

* `teht2.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht2.html`)**
* `teht2.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht2.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### tehtävänanto:

Lisää css-tiedostoon seuraava uusi valitsin bodylle:

```css
body {
  margin: 0
}
```

Oletuksena, historiallisista syistä johtuen, `body`-elementillä on pieni `margin`, siis elementtiä ympäröivä tyhjä tila.
`body`-elementtiä ympäröivän tyhjän tilan idea on oletettavasti ollut, että dokumentin teksti ei kulje reunasta reunaan, 
vaan reunan ja tekstin välillä pieni rako

Tänä päivänä haluamme kuitenkin yleensä tapauskohtaisesti itse kehittäjinä valita, mihin elementtiin sijoitamme tuon raon,
sekä kuinka suuri tuo ero reunan ja muun sivun sisällön välillä on.

### Tehtävä 3 - `box-sizing`

**palautettavien tiedostojen nimet:** 

* `teht3.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht3.html`)**
* `teht3.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht3.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### tehtävänanto:

Lisätään css-tiedostoon [box-sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)-sääntö:

```css
* {
  box-sizing: border-box;
}
```

Tässä opimme kaksi uutta asiaa:

* `*` valitsimen, jolla voidaan kohdistaa säännöt kaikkiin elementteihin
* `box-sizing`-säännön, jolla voidaan vaikuttaa siihen miten elementin koko lasketaan

Sääntö siis tarkoittaa, että kaikille elementeille dokumentissa, kohdistetaan sääntö `box-sizing: border-box;`

Tämä sääntö ei ole pakollinen, mutta tykkään itse käyttää sitä.

#### Mitä `box-sizing`-sääntö tarkoittaa?

Asettamalla `box-sizing`-säännölle arvoksi `border-box`, voidaan määrittää, että elementin täysi levyys lasketaan huomioiden elementin reunat (engl. border).
Siis kun elementin leveydeksi määritetään `100%` (`width: 100%;`), tämä tarkoittaa, että myös sen reunat, jotka saattavat olla kovin paksut, tulee mahtua elementin vanhemman sisälle.

Elementin leveytenä arvo `100%` tarkoittaa elementin vanhemman leveyttä. Kun sanomme `width: 100%;`, tarkoitamme että elementin pitäisi täyttää sen vanhemman leveys.

Vastaavasti `box-sizing: content-box` tarkoittaisi, että elementin täysi leveys ei ota huomioon reunoja, vaan vain sen sisäosan leveyden. Tällöin `width: 100%;`-säännöllä elementti on reunojen (2x reunan leveys) verran vanhempaansa leveämpi.

Voit kokeilla kliksutella yllä olevasta linkistä löytyvää mdn:n esimerkkiä `border-box` ja `content-box`-arvoista, kunnes hahmotat eron. 

### Tehtävä 4 - lisätään valitsimia

**palautettavien tiedostojen nimet:** 

* `teht4.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht4.html`)**
* `teht4.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht4.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### tehtävänanto:

Lisää css-tiedostoon kaikkien aiemmin merkittyjen luokkien nimet omiksi valitsimikseen.

Kertauksena, css-syntaksi näytti seuraavalta:

```css
valitsin {
  sääntö: arvo;
  sääntö: arvo;
}
```

Lisää siis aiemmin luomasi bem-nimeämiskäytännön mukaiset luokat css-tiedostoon.
Vielä näille valitsimille ei tarvitse lisätä ensimmäistäkään sääntöä.
Sen teemme seuraavissa tehtävissä.

Lisää valitsin myös `body`-valitsimelle, jos et ole sitä vielä tehnyt.

Nyt siis vain valmistelemme css-tiedostoa seuraavia tehtäviä varten.

### Tehtävä 5 - `display: flex`

Tässä tehtävässä käytetään `display: flex;`-sääntöä.

**palautettavien tiedostojen nimet:** 

* `teht5.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht5.html`)**
* `teht5.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht5.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Lyhyesti `display: flex`-säännöstä

Kuten aiemmin olemme käsitelleet, moderni css-tyylittely pohjautuu pitkälti juurikin flexbox-asemoinnin käyttöön.

Elementin määrittäminen käyttämään flexboxia tapahtuu juurikin käyttäen `display: flex;`-sääntöä.
Kun määritämme elementille `display`-säännön arvoksi `flex`-arvon, se asemoituu flexboxin avulla riveiksi tai sarakkeiksi.

`flex` ei ole kuitenkaan ainoa arvo, jonka `display`-sääntö voi saada.
[`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display)-sääntö voi saada myös muita arvoja, mm.:

* `block` - oletusarvo mm. `div`-elementillä
* `inline-block` - tekstielementin ja display-elementin välimuoto,
* `none` - elementtiä ei näytetä. Tämä voi olla hyödyllistä mm. bem:in modifier-muuntajaa käyttäessä,
* `flex` - asemoituu käyttäen flexboxia, riveihin ja sarakkeisiin, päätyihin ja keskelle, tilaa jättäen,
* `grid` - toinen moderni näyttötapa, jossa elementit järjestetään ruudukkoon,

Voit kokeilla mitä nämä tekevät.

Aiemmin kun käytimme valmiiksi luotuja `rivi`- ja `sarake`-luokkia, teimme juurikin tämän saman asian, jonka teemme tässä tehtävässä - asetimme elementin asemoitumaan flexboxin avulla.

Määritimme tuolloin myös flex-elementin järjestymissuunnan, käyttäen `flex-direction`-sääntöä. 
Tästä lisää seuraavassa tehtävässä.

Miksi sitten haluamme asemoida elementit flexboxin avulla?
Voimme tällöin helposti asemoida elementit sisäkkäiksi riveiksi ja sarakkeiksi,
mutta tämän lisäksi pystymme myös asemoimaan elementtejä niiden pääsuuntaan nähden vastakkaisessa suunnassa.
Yleensä haluamme asemoida elementit esimerkiksi riveiksi, ja keskittää ne vertikaalisesti.
Tämä onnistuu helposti juuri flexboxin avulla.

Nyt alkuun kuitenkin riittää, että otamme flexboxin käyttöön kaikilla elementeillä.

Huomaat, että kaikki elementit, joilla flexbox on käytössä, asemoituvatkin riveiksi.
Tämä on oletusasetus flexboxille.
Korjaamme sen seuraavassa tehtävässä.

Nyt siis kuitenkin otetaan vain flexbox käyttöön.

#### tehtävänanto:

Lisää jokaiselle valitsimelle sääntö `display: flex;`

Esimerkiksi yläpalkin alempi rivi, kategoriat, määritettäisiin käyttämään flexboxia seuraavasti:

```css
.sivun-yläpalkki__kategoriat {
  display: flex;
}
```

### Tehtävä 6 - `flex-direction`-sääntö

Kun aiemmin otettiin flexbox käyttöön, seuraavaksi laitetaan elementit riveiksi ja sarakkeiksi.

**palautettavien tiedostojen nimet:**

* `teht6.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht6.html`)**
* `teht6.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht6.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Lyhyesti `flex-direction`-säännöstä

`flex-direction` määrittää, valuuko flexboxilla asemoidun elementin lapset rivinä vai sarakkeena.
Se on melkeinpä tärkein yksittäinen sääntö flexbox-asemointiin liittyen.

Käytimme aiemmin `flex-direction`-sääntöä, osana valmiiksi luotuja `rivi`- ja `sarake`-sääntöjä.
Voit tarkistaa tämän aiemmista tehtävistä!

Nyt kuitenkin otamme sen itse käyttöön, ja lisäämme sen jokaiselle elementille html-dokumentissamme.

Miten sitten `flex-direction`-sääntö toimii?

Se voi saada kaksi eri arvoa:

* `flex-direction: row;` - elementin välittömät lapset järjestyvät riviin, siis vierekkäin,
* `flex-direction: column;` - elementin välittömät lapset järjestyvät sarakkeeseen, siis allekkain.

On huomattavaa, että `flex-direction`-sääntö ei toimi itsenäisesti, 
vaan se vaatii, että elementin `display`-arvoksi on asetettu `flex`-arvo.

Oletuksena flexbox-elementti asemoi lapsensa riviin.
Meidän ei siis tarvitsisi käyttää `flex-direction: row;`-sääntöä.
On kuitenkin yleensä hyvä merkitä nämä säännöt näkyviin.

Kun otamme eksplisiittisesti jonkin säännön käyttöön, se tarkoittaa, että olemme tehneet tietoisen valinnan.
Jos taas implisiittisesti käytämme oletussääntöä, sitä on helpompi myöhemmin vaihtaa.
Kun taas jos olemme merkinneet eksplisiittisesti säännön käyttöön, sen vaihtaminen vaihtaa vanhan säännön poistoa tai muuttoa.

Nyt siis otamme käyttöön eksplisiittisesti `flex-direction`-säännön kaikissa elementeissä.

#### tehtävänanto:

Lisää jokaiselle valitsimelle `flex-direction`-sääntö. Se voi saada arvokseen joko `row` (suom. rivi) tai `column` (suom. sarake).

Tämän tehtävän jälkeen, jokaisella valitsimella pitäisi olla jompi kumpi seuraavista säännöistä:

* `flex-direction: row;` - jos sen välittömät lapset ovat rivissä,
* `flex-direction: column;` - jos sen välittömät lapset ovat allekkain.

**Tämän tehtävän osalta `flex-direction` tulee lisätä elementeille, vaikka kyseessä olisikin rivi.**

Lisää jokaiselle css-tiedostosta löytyvälle css-valitsimelle jompi kumpi arvoista, sen mukaan kumpi tarvitaan. 
Yritä välttää katsomasta mallia aiemmista tehtävistä.

Jos et keksi mistä aloittaa, voit aloittaa vaikka yläpalkin kategorioista, jotka asemoituvat riviin:

```css
.sivun-yläpalkki__kategoriat {
  display: flex;
  flex-direction: row;
}
```

### Tehtävä 7 - `justify-content`-sääntö

Kun olemme järjestäneet elementtien lapset riveiksi ja sarakkeiksi, 
voimme alkaa järjestämään näiden rivien ja sarakkeiden sisältämiä elementtejä rivien ja sarakkeiden sisällä.

Tähän käytämme `justify-content`-sääntöä.

**palautettavien tiedostojen nimet:** 

* `teht7.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht7.html`)**
* `teht7.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht7.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### `justify-content` asemoi elementit, ja määrittää minne tyhjä tila elementtien välillä menee

`justify-content`-sääntö määrittää sen, miten elementin lapset asemoituvat siinä suunnassa, joka on asetettu `flex-direction`-säännöllä.

Jos elementti on asetettu järjestämään lapsensa riviin:

* `flex-direction: row;`-säännöllä, `justify-content` määrittää sen, miten lapset asemoituvat vaakasuunnassa,
* `flex-direction: column;`-säännöllä, `justify-content` määrittää sen, miten lapset asemoituvat pystysuunnassa.

`justify-content` voi saada useamman arvon, näistä tärkeimmät ovat:

* `justify-content: start;` - lapsielementit järjestyvät rivin tai sarakkeen alkuun, jättäen tyhjää tilaa loppuun,
* `justify-content: center;` - lapsielementit järjestyvät rivin tai sarakkeen keskelle, jättäen tyhjää tilaa alkuun ja loppuun,
* `justify-content: end;` - lapsielementit järjestyvät rivin tai sarakkeen loppuun, jättäen tyhjää tilaa alkuun,
* `justify-content: space-between;` - lapsielementit järjestyvät rivin tai sarakkeen koko matkalle siten, että reunimmaiset lapset ovat kiinni reunoissa, ja lasten välissä on tasaisesti tilaa,
* `justify-content: space-around;` - lapsielementit järjestyvät riviin tai sarakkeelle tasaisesti, jättäen tasaisesti tilaa toistensa väliin, mutta myös reunoille

Näitä arvoja kannattaa kokeilla ajan kanssa itsekseen, mdn:n sivuilta, tai sitten flexbox froggy -pelissä.

`justify-content`-sääntö on flexbox-asemoinnin toiseksi tärkein sääntö heti `flex-direction`-säännön jälkeen, 
koska se määrittää, miten elementit asemoituvat rivin tai sarakkeen sisällä.

#### tehtävänanto:

Käytä [`justify-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content)-sääntöä.

Lisää tämäkin sääntö taas jokaiseen elementtiin sivulla käyttäen css-valitsimia.

Ota mallia referenssikuvasta, nähdäksesi, miten elementit ovat asemoituneet rivien ja sarakkeiden sisällä.

Tämä tehtävä on vähän edellistä vaikeampi tehtävä, mutta kuitenkin vielä suhteellisen helppo.
Joudut kuitenkin jo vähän miettimään, miten elementtien pitäisi rivien ja sarakkeiden sisällä järjestyä.

Aloita siis sellaisista elementeistä, joiden asemoituminen on helppoa kuvasta havaita.

Jos säännön käyttö tuntuu vaikealta, kokeile sitä johonkin elementtiin eri arvoilla, nähdäksesi miten se toimii.

Voit aloittaa taas vaikka yläpalkin kategorioista, jotka asemoituvat `space-between`-arvon avulla:

```css
.sivun-yläpalkki__kategoriat {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
```

### Tehtävä 8 - `align-items`- ja `align-content`-säännöt

Kun edellisessä tehtävässä määritimme miten elementin lapset asemoituvat rivin tai sarakkeen suuntaisesti,
nyt määritämme miten ne asemoituvat vastakkaisessa suunnassa.

Tähän käytämme `align-items`-sääntöä.

Tarkastelemme myös sille läheistä `align-content`-sääntöä, vaikkemme sitä käytäkään.

**palautettavien tiedostojen nimet:** 

* `teht8.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht8.html`)**
* `teht8.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht8.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### `align-items`

Siinä missä `justify-content` määrittää elementin lasten asemointia elementille asetetun `flex-direction`-säännön arvon puitteissa (`row` tai `column),
`align-items`-sääntö määrittää sitä vastakkaisessa suunnassa.

Jos elementti on asetettu järjestämään lapsensa riviin:

* `flex-direction: row;` säännöllä, `align-items` määrittää sen, miten lapset asemoituvat pystysuunnassa,
* `flex-direction: column;` säännöllä, `align-items` määrittää sen, miten lapset asemoituvat vaakasuunnassa.

Siinä missä `justify-content`-sääntö voi saada paljonkin eri arvoja, `align-items`-sääntö voi saada vain neljä arvoa:

* `align-items: start;` järjestää arvot alkuun (vasemmalle tai ylös)
* `align-items: center;` järjestää arvot keskelle
* `align-items: end;` järjestää arvot loppuun (oikealle tai alas)
* `align-items: stretch;` venyttää lapset käyttämään koko tilan

Näistä ehkä yleisin käyttötarkoitus on keskitys, `align-items: center;`-säännöllä.
Kun elementit ovat keskellä sivua, rivissä, ne yleensä halutaan keskittää vertikaalisesti, jotta eri kokoiset elementit näyttäisivät kulkevan samalla suoralla janalla.

Usein on myös tarpeen järjestää joko alkuun tai loppuun. 
Näin on, jos elementtien halutaan seuravaan jotain kiinteää tasoa, jota vasten ne ikäänkuin järjestyvät - vähän kuin selkä seinää vasten.
Esimerkiksi jos elementit ovat sivun oikealla puolella, ne voidaan haluta asemoida kulkemaan oikean reunan suoraa rajaa mukaillen.
Toisaalta asemointi vasempaan reunaan voi sarakkeessa tulla kyseeseen, 
jos halutaan järjestää pidempi teksti alkamaan joka rivillä, perinteisen kappaleen muotoilun mukaisesti, länsimaisittain, vasemmasta reunasta - vähän niin kuin tämä kappale.

`align-items` on monesti tärkeä sääntö, sillä se mahdollistaa elementtien keskittämisen, tai reunaan asemoinnin flexboxin toissijaisessa suunnassa.

#### `align-content`

`align-content`-sääntö tekee samaa, mitä `align-items`, mutta siinä missä `align-items` asetetaan vanhemmalle ja vaikuttaa lasten asemointiin, `align-content` annetaankin suoraan lapsielementille, ja se vaikuttaa sen asemointiin. 
Eli `align-content` on vähän kuin varatyökalu, jota voidaan käyttää lapsella, jos ei syystä tai toisesta haluta käyttää `align-items`-sääntöä vanhemmalla.

Yleensä helpointa on kuitenkin käyttää `align-items`-sääntöä vanhemmalla, koska se silloin vaikuttaa kaikkiin (välittömiin) lapsielementteihin, eikä näin ollen tarvitse asettaa `align-content` arvoa erikseen jokaiselle lapselle. 
Välillä myös `align-content`-sääntö saattaa olla hyödyllinen.

Molemmissa tapauksissa vanhemman `flex-direction` vaikuttaa samalla tavalla siihen, miten.

#### tehtävänanto:

Käytä [`align-items`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)- ja [`align-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content)-sääntöjä.

Haluat todennäköisesti asettaa tämänkin säännön melkein kaikille elementeille.

Esimerkiksi tarkastellaan taas yläpalkin kategorioita.
Ne järjestyvät riviin flexboxilla.
Haluat kuitenkin luultavasti asemoida ne myös pystysuunnassa, siten että ne ovat pystysuunnassa keskellä:

```css
.sivun-yläpalkki__kategoriat {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
```

Tee sama myös muille elementeille, joiden lasten pitää asemoitua myös toissijaisessa suuunnassa.

Huomaa, ettet todennäköisesti tarvitse tässä tehtävässä `align-content`-sääntöä, vaan pärjäät pelkällä `align-items`-säännöllä.
Voit kuitenkin kokeilla molempia.

### Lyhyt teoriaosuus: Tyhjästä tilasta

Käytännössä flex-boxin käytön jälkeen kyse onkin lopulta vain tyhjän tilan lisäämisestä, tai varaamisesta, elementtien ympärille.

Seuraavaksi katsommekin tyhjän tilan määrittämistä css:n avulla.

1. aloitamme `border`-säännöstä, ja määritämme sillä reunaviivoja
2. jatkamme `margin`- ja `padding`-säännöillä, ja määritämme tyhjää tilaa vähän suuremmin

#### `border`

[`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border)-säännöllä määritetään elementille reunaviiva. Säännön avulla on mahdollista määrittää reunaviivan tyyli, paksuus ja väri.
Tämän lisäksi on mahdollista määrittää, onko elementillä reuna joka puolella, vai vain yhdellä neljästä sivusta.

Käytännössä `border`-elementille voi antaa arvoja monella tavalla. 
Tämä johtuu pitkälti historiallisista syistä - ennen kuin `border`-säännön muoto lopulta vakiintui, sille oli mahdollista antaa arvoja eri tavoilla eri selaimissa.
Ilmeisesti taaksepäin yhteensopivuuden takia, näitä sääntöjä ei ole lähdetty poistamaan, vaan ne on säilytetty sallittuina.
Erilaisia tapoja määrittää arvoja `border`-säännön avulla voi lukea mm. mdn:n puolelta.

Tässä keskitymme kuitenkin yhteen kattavaan säännön arvon määrittämismuotoon.

##### `border`-säännön arvot

Näissä tehtävissä käytämme `border`-säännöstä versiota, jossa se saa kerralla kaikki kolme arvoa. 

Nämä arvot ovat järjestyksessä, väleillä eroteltuina:

* tyyli - yleisin on `solid`, joka tekee normaalin jatkuvan viivan, mutta myös täplitetyt viivat ovat mahdollisia, voit katsoa lisää mm. mdn:n sivuilta, 
* paksuus - esim. pikseleinä,
* väri - värin voi määrittää varatulla sanalla, joita löytyy englanninkielisenä monia, tai `rgb(r,g,b)` arvona.

Ehdottomasti yleisin muoto `border`-säännnöstä näyttää jotakuinkin seuraavalta:

```css
border: solid 1px black;
```

Se asettaa elementille yhden pikselin levyisen tasaisen reunuksen, joka kulkee elementin ympäri, sen jokaisella sivulla.

Yleensä yksi pikseli riittää leveydeksi, lähes pelkästään reunana käytetään jatkuvaa viivaa, ja valkoisella taustalla viiva on useimmiten kirjainten oletusarvon tavoin musta.

##### `border`-säännön asettaminen vain yhdelle reunalle

Reuna on mahdollista asettaa myös vain yhdelle sivulle. 

Tällöin arvot ovat samat kuin päätapauksessa, mutta säännön nimi muuttukin:

* `border-top: <arvo>` - asettaa elementille yläreunan, arvon mukaisesti,
* `border-right: <arvo>` - asettaa elementille oikean reunan, arvon mukaisesti,
* `border-bottom: <arvo>` - asettaa elementille alareunan, arvon mukaisesti,
* `border-left: <arvo>` - asettaa elementille vasemman reunan, arvon mukaisesti.

Esimerkiksi, jos haluamme asettaa elementille harmaan ohuen alareunan, voimme kirjoittaa:

```css
border-bottom: solid 1px gray;
```

Vastaavasti paksu valkoinen oikea reuna saadaan säännöllä:

```css
border-right: solid 3px white;
```

### Tehtävä 9 - `border`

Aiemmin olemme käyttäneet sivulta löytyviä reunaviivoja elementtien ryhmittelyyn, ja sivun eri osien rajojen päättelyyn.

Nyt lähdemmekin piirtämään näitä rajoja itse sivulle.

Tehtävien alta löytyy tietoa `border`-säännön käytöstä.

**palautettavien tiedostojen nimet:** 

* `teht9.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht9.html`)**
* `teht9.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht9.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### tehtävänanto:

Tässä tehtävässä teemme seuraavat alitehtävät. Jokaisesta löytyy tarkemmat ohjeet oman alaotsikon alta alempaa.

1. lisää ostoskori -kuvakkeelle reunus
2. lisää asiakaspalvelu-osiolle alareuna
3. lisää alapalkin harmaan alueen keskelle horisontaalinen raja

##### alitehtävä 1 - ostoskori

Ostoskorin ympärillä on nähtävissä paksu, valkoinen reunaviiva.

Sen saa aikaan seuraavalla css-säännöllä:

```css
border: solid 2px white;
```

Anna tämä sääntö ostoskorin valitsimelle. Seuraavassa oletetaan, että ostoskorin luokan nimi, bem-nimeämistapaa käyttäen, on `header__ensimmäinen-rivi__oikea-osio__ostoskori`:

```css
.header__ensimmäinen-rivi__oikea-osio__ostoskori {
  border: solid 2px white;
}
```

Voit vielä lopuksi korvata ostoskorin tekstin tilapäisesti "u"-kirjaimella, jotta siitä tulee vähän neliötä muistuttava.
Teemme myöhemmin ostoskorista neliön käyttäen `width`- ja `height`-sääntöjä.

##### alitehtävä 2 - asiakaspalvelu-osion alareuna

Alapalkin alussa, asiakaspalvelu-osion ja yritysmyynti-osion välissä on nähtävissä lyhyt poikkiviiva.

Yleensä tällaisia viivoja ei tehdä erillisinä elementteinä, vaan ne vain määritellään jonkin elementin yhtenä reunaviivana.

On tärkeä huomata, että css ei salli reunojen määrittämistä elementtien välille, vaan reuna täytyy aina asettaa yhdelle elementille.

Tällöin kehittäjän tehtäväksi jää päättää, mille elementille reuna kannattaa asettaa.

* Välillä reuna on selvästi jonkin elementin reuna, koska se vaikka on lähempänä toista elementeistä. Tällöin on yleensä helppo määrittää reuna tietylle elementille.
* Välillä reuna on yhtä kaukana molempia erotettavia elementtejä, jolloin pitää vain valita toinen elementeistä, ja antaa sille näkyvä reuna.
* Välillä reuna täytyy teknisistä syistä asettaa tietylle elementille, vaikka se ehkä visuaalisesti näyttäisi enemmän toisen elementin reunalta.

Tällä kertaa lisätään reuna juurikin asiakaspalvelu-osion alareunaksi, koska se vähän näyttäisi olevan referenssikuvassa lähempänä asiakaspalvelu-osiota.

Tämä onnistuu seuraavalla säännöllä:

```css
  border-bottom: solid 1px grey;
```

Anna tämä sääntö asiakaspalvelun uloimman elementin valitsimelle. Seuraavassa oletetaan, että asiakaspalvelun luokan nimi, bem-nimeämistapaa käyttäen, on `asiakaspalvelu`:

```css
.asiakaspalvelu {
  border-bottom: solid 1px grey;
}
```

Voit halutessasi hienosäätää väriä paremmin sopivaksi, tai vaikka katsoa mitä väriä referenssisivu tässä tilanteessa oikeasti käyttää.

##### alitehtävä 3 - alapalkin harmaan alueen keskellä oleva poikkiviiva

Vastaavasti alapalkin harmaan alueen erottaa lähes koko leveyden kattava poikkiviiva.

Asetetaan se tällä kertaa harmaan alueen alemmalle osalle yläreunaksi.
Se kenties voisi sellainen olla, jos ajatellaan, että jälkimmäinen osa haluaa erottua ensimmäisestä osasta. 

Tätä valintaa voidaan järkeillä sillä oletuksella, että ensimmäinen osa ei tavallaan tiedä, onko sillä jäljessä toista osaa, joten sille ei aseteta alareunaa, siltä varalta, 
että sen jälkeen ei tulisikaan enää mitään. 
Yleinen tapa onkin, että jos listataan asioita, ensimmäiselle elementille ei aseteta reunaa tai tyhjää väliä, vaan nämä asetetaan kaikille sen jälkeen tuleville.
Tämäkin kuitenkin on vain yksi tapa tehdä asioita, ja muitakin valintoja voi tehdä, jos ne osaa perustella.

On kuitenkin hyvä huomata, että ohjelmoinnissa on monellakin tavalla ja tasolla kyse kielestä ja kielenkäytöstä.
Yleistä kielille on, että niiden tulee yleensä soljua tai virrata vapaahkosti.
Kielen käyttö on tapa, jonka voi oppia.

Yläreuna voidaan asettaa seuraavalla säännöllä:

```css
border-top: solid 1px grey;
```

Tässä oletetaan, että alapalkin alemman harmaan osion nimi, käyttäen bem-nimeämiskäytäntöä, olisi `.footer__alempi-harmaa-osio`:

```css
.footer__alempi-harmaa-osio {
  border-top: solid 1px grey;
}
```

Tässä yhteydessä on hyvä huomata, että minkä värin viivalle valitsetkaan, tulisi sen olla sama harmaan sävy, kuin asiakaspalvelun ja yritysmyynnin välistä löytyvän viivan yhteydessä.

Edelleen, sivulla valitsee muotokieli, siis säännöstö, jonka puitteissa tavallisissa tapauksissa pitäisi noudattaa samoja muodollisia sääntöjä - siis käyttää samoihin asioihin eri kohdissa samoja kokoja, värejä ja muita arvoja. Värejä ja kokoja voi olla toki sivuilla useita, moninkertoja ja sävytyksiä, mutta niiden pitäisi olla kaikkien samoista pohja-arvoista johdettuja.
Jos kuitenkin halutaan erottautua jossain tilaanteessa tavanomaisesta, voidaan tätä korostaa rikkomalla näitä sääntöjä, ja käyttämällä eri kokoja tai värejä, tai muita arvoja.

### Lyhyt teoriaosio: tyhjästä tilasta - jatkuu

#### `margin`, `border` ja `padding`

`margin` ja `badding` ovat hyvin samankaltaisia sääntöjä.
Ne molemmat lisäävät, tai varaavat, tyhjää tilaa elementin sisällön ympärille.
Elementin sisältöhän tarkoitti siis sen lapsia, olivat ne sitten toisia elementtejä, tekstiä, tai vaikka kuva `img`-elementin tapauksessa.

Näiden lisäksi myös `border` on oikeastaan hyvin samanlainen sääntö. 
Opimme edellä että `border`:in tyypillisin tehtävä on toimia värillisenä reunuksena elementin ympärillä. 
Käytännössä kuitenkin myös border varaa tyhjää tilaa elementin ympärille, näiden kahden säännön tavoin.

Ero onkin lähinnä siinä, miten näille elementeille annetaan arvoja. 
Opimme aiemmin miten `border`-sääntö saa arvoja.
Seuraavaksi katsomme, miten `margin` ja `padding` saavat arvoja.

`padding` ja `margin` voivat saada arvoja useammalla tavalla. 
`border`-säännön tavoin, kaikille sivuille voidaan antaa arvot kerralla, tai jokaiselle sivulle arvot voidaan antaa erikseen.
Kuitenkin, `padding` ja `margin` saavat aina arvokseen vain yhden asian: tyhjän tilan koon annettuina yksikköinä. 
Yksiköt voivat olla pikseleitä, mutta ne voivat olla myös jotain muita arvoja, esimerkiksi prosentteja.

#### `padding`- ja `margin`-säännöt yksinkertaisimmassa muodossaan 

Yksinkertaisimmillaan säännöt näyttävät siis seuraavilta.

Margin saa arvon:

```css
margin: 7px;
```

Vastaavasti `padding`-sääntöä käytetään lyhykäisyydessään seuraavasti:

```css
padding: 7px;
```

Jos halutaan poistaa arvo, voidaan säännölle asettaa arvoksi nolla:

```css
margin: 0;
```

Tällöin, kun asetetaan arvoksi nolla, ei yleensä lisätä yksikköä. 

Sama toimii myös padding:in kanssa:

```css
padding: 0;
```

Kaikissa edellä esitetyissä tapauksissa, näille säännöille annettiin kaikille sivuille samat arvot.

##### `padding`- ja `margin`-sääntöjen osalta tyhjän tilan voi asettaa sivu kerrallaan

Kuitenkin, kuten `border`-säännön yhteydessä, myös `padding`- ja `margin`-säännöistä on olemassa säännöt, 
jotka asettavat vain yhden sivun arvon (tässä näytämme vain `padding`-säännön osalta nämä sääntöjen nimet, mutta samat löytyvät myös `margin`-säännölle):

* `padding-top: 14px;` - asettaa elementin yläpuolelle 14px:n paddingin,
* `padding-right: 7px;` - asettaa elementin oikealle puolelle 7px:n paddingin,
* `padding-bottom: 21px;` - asettaa elementin alapuolelle 21px:n paddingin,
* `padding-left: 28px;` - asettaa elementin vasemmalle puolelle 28px:n paddingin,

Toisin sanoen:

```css
padding-top: 7px;
padding-right: 7px;
padding-bottom: 7px;
padding-left: 7px;
```

tarkoittaa siis samaa kuin yksittäinen sääntö:

```css
padding: 7px;
```

##### `padding` ja `margin`-sääntöjen yhdistetyt arvot

Kun edellä sanottiin, että `padding`- ja `margin`-säännöt saavat aina vain yhden arvon, se ei ollut aivan totta.

Taas, historiallisista syistä, molemmat säännöt voivat saada arvokseen muutaman erilaisen yhdistetyn arvon:

* `padding: <yksi arvo>` - kaikki neljä sivua saavat saman arvon,
* `padding: <ensimmäinen arvo> <toinen arvo>` - ylä- ja alasivu saavat arvokseen ensimmäisen arvon, oikea ja vasen sivu saavat arvokseen toisen arvon,
* `padding: <ensimmäinen arvo> <toinen arvo> <kolmas arvo>` - yläsivu saa arvokseen ensimmäisen arvon, oikea ja vasen sivu saavat arvokseen toisen arvon, alasivu saa arvokseen kolmannen arvon,
* `padding: <ensimmäinen arvo> <toinen arvo> <kolmas arvo> <neljäs arvo>` - sivut saavat arvot seuraavassa järjestyksessä: ylä, oikea, ala, vasen.

Kannattaa huomata, että jos tilan arvoja on useampi, ne erotellaan tässä tapauksessa, säännön arvon sisällä, toisistaan välilyönneillä.

##### `padding`, `border` ja `margin` varaavat elementin ympärille tyhjää tilaa järjestyksessä

Nämä kolme sääntöä varaavat tilaa elementin ympärille tietyssä järjestyksessä:

* `padding` on sisin kerros välittömästi elementin sisällön ympärillä,
* `border` on seuraava kerros, joka jää `padding`- ja `margin`-tilojen väliin
* `margin` on ulommainen kerros

On lisäksi huomattavaa, että kun elementille määritetään taustaväri, se värjää sekä elementin sisällön, ja lapset, mutta myös `padding`-säännön varaaman tyhjän tilan.
Sen sijaan `border` saa värin omista määrityksistään, ja `margin` värjäytyy elementin vanhemman värillä (joka voi olla valkoinen, jos väriä ei erikseen ole määritetty sivulle).
Tätä ominaisuutta käytettiin hyväksi värjätessä aiemmassa tehtävässä rivejä violeteiksi ja sarakkeita vihreiksi.

Tavallaan, kun asiaa pohtii, lapsielementin `margin`-tila on siis se osa, joka on kiinni vanhemman `padding`-tilassa.
Tämä on hyvä ymmärtää, koska se auttaa hahmottamaan muutoin helposti sekavalta tuntuvia tyhjän tilan määrityksiä.
Vaikeata tämä ei kuitenkaan pohjimmiltaan ole, koska muuttujia jokaisella elementillä on aina vain nämä kolme: `padding`, `border` ja `margin`.
Pitää vain keksiä, mille elementille mikäkin osa tyhjästä tilasta kuuluu, ja mistä näistä osista tyhjä tila muodostuu. 

Melkein kaikissa selaimissa, kehittäjän työkalut osaa näyttää yhdellä silmäyksellä elementin kaikki kolme arvoa: `margin`, `border` ja `padding`. 
Kehittäjien työkalut avautuvat yleensä selaimessa klikkaamalla oikealla hiirennäppäimellä sivua, ja valitsemalla tarkista.
Yleensä valitsemalla elementin, ja sen jälkeen tarkastelemalla sen css-tyylejä, pääsee näkemään nämä arvot. 
Koska nämä välit ovat niin keskeisiä tyylittelyn työkaluja, monet selaimet osaavat tässä yhteydessä näyttää nämä sisäkkäiset välit visuaalisena kuvana, 
jossa välit on merkitty numeroina.

#### Arvoista

Yleensä sivustolla valitaan alkuun jokin pikseliarvo, joka toimii sivun perusmittana.
Tämän jälkeen, kaikki sivulla käytetyt arvot esitetään tämän arvon moninkertoina.

Monesti käytettyjä perusmittoja ovat luvut `7px` ja `10px`.

Jos perusmitta olisi `10px`:

* sen kaksinkertainen arvo (2x) olisi `20px`
* sen kolminkertainen arvo (3x) olisi `30px`
* sen nelinkertainen arvo (4x) olisi `40px`

Jos perusmitta olisi `7px`:

* sen kaksinkertainen arvo (2x) olisi `14px`
* sen kolminkertainen arvo (3x) olisi `21px`
* sen nelinkertainen arvo (4x) olisi `28px`

Tyypillisesti `padding` tai `margin` saattaa elementillä olla normaalisti 2xperusmitta, mutta toisinaan ohuempi (1x) ja toisinaan vähän leveämpi (3x). 
Välillä voidaan tarvita isompaakin mittaa (4x).

Välillä halutaan käyttää vielä näitäkin suurempia kokoja. 
Välillä asioiden koot määräytyvät laskutoimitusten pohjalta: 
esim. lisätään normaalisti 4x tyhjä tila, mutta lisätään siihen yläpuolella olevan elementin vasemman reunan paksuus ja padding, 
jotta saadaan asemoitua kaksi allekkaista elementtiä horisontaalisesti samaan kohtaan.
Nämä laskut ovat kuitenkin tapauskohtaisia, ja niistä suoriutuu yleensä kokeilemalla eri arvoja, kunnes sivu näyttää visuaalisesti oikealta.

Tätä perusmittaa käytetään mahdollisesti myös muiden asioiden, kuten esimerkiksi fonttien koon ilmaisemiseen.

Tällöin käytetään yleensä pikselien sijaan `rem`-yksikköä. Tästä kuitenkin myöhemmin lisää.

### Tehtävä 10 - `margin` ja `padding`

Käytännössä flex-boxin käytön jälkeen kyse onkin lopulta vain tyhjän tilan lisäämisestä, tai varaamisesta, elementtien ympärille.

Tässä tehtävässä tarkastelemme lähemmin [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)- ja [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)-sääntöjen käyttöä.

**palautettavien tiedostojen nimet:** 

* `teht10.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht10.html`)**
* `teht10.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht10.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### tehtävänanto:

Lisää eri elementtien ympärille tyhjää tilaa käyttäen `margin`- ja `padding`-sääntöjä.

1. lisää ylä- ja alapalkin oikealle ja vasemmalle sivulle saman verran tyhjää tilaa
2. lisää alapalkin harmaan osion ylä- ja alaosalle saman verran tyhjää tilaa ylä ja alapuolelle
3. lisää alapalkin otsikoiden alle saman verran tyhjää tilaa
4. lisää aukioloaika-osioiden ympärille, kaikissa paikoissa, saman verran tyhjää tilaa
5. lisää tyhjää tilaa muihin paikkoihin


##### alitehtävä 1. tyhjä tila ylä- ja alapalkin oikealla ja vasemmalla sivulla

Huomaamme nopeasti, että referenssikuvassa molempien sivun ylä- ja alapalkin sisällöt, ovat selvästi irrallaan sivun reunoista.
Huomaamme myös, että näissä molemmissa sisällön etäisyys sivun reunoihin on sama, molemmilla puolilla.

Miten tämä sitten toteutetaan?
Lisäämme yläpalkille ja alapalkin harmaalle osiolle sopivan tyhjän tilan.
Valitsemme tässä tapauksessa käytettäväksi `padding`-tilan..

```css
header,
footer__harmaa-osio {
  padding: 60px 0;
}
```

*Tässä oletimme, että elementeille olisi annettu edellä olevat nimet, käyttäen bem-nimeämiskäytäntöä.
On mahdollista, että olet antanut näille elementeille eri luokkien nimet.
Käytä siis antamiasi luokkien nimiä.*

Edellä arvo `60px` on vain jokin satunnainen iso luku. Valitse sen tilalle luku, joka silmämääräisesti näyttäisi vastaavan referenssikuvan tyhjää tilaa. Voit joutua kokeilemaan useampaa lukua.

Huomaa myös, ettemme voi yllä viitata koko `.footer`-elementtiin, koska mustassa osiossa tällaista tilannetta ei ole, vaan päinvastoin, sen sisältö, ja siis väri, alkaa sivun reunasta.

Kertauksena vielä, miksi käytämme tässä `padding`-sääntöä, emmekä `margin`-sääntöä? 
Koska kyse elementeistä, jotka määrittävät taustavärin, saamme taustavärin ulottumaan myös tyhjän tilan päälle, kun käytämme `padding`-sääntöä.
Jos käyttäisimme `margin`-sääntöä, taustaväri supistuisi, ja musta alue ei ulottuisikaan sivun reunasta toiseen.

Kokeile käyttää tässä myös `padding`-säännön sijaan `margin`-sääntöä, nähdäksesi eron itse.

##### alitehtävä 2. alapalkin harmaan osion tyhjät tilat

Sivun alapalkin harmaa osio jakautuu viivalla kahtia.
Jos katsot näitä kahta osiota, viivan molemmin puolin, näet,
että niillä on ylä- ja alapuolellaan suurin piirtein saman verran tyhjää tilaa.

Harmaassa osiossa on saman verran tyhjää tilaa neljässä kohdassa:

* harmaan osion yläosassa
* harmaan osion halkaisevan viivan yläpuolella
* harmaan osion halkaisevan viivan alapuolella
* harmaan osion alaosassa

Näihin voidaan lisätä tyhjää tilaa kahdella css-valitsimella ja yhdellä css-säännöllä:

```css
footer__harmaa-osio__yläosa,
footer__harmaa-osio__alaosa {
  padding: 10px 0;
}
```

*Tässä oletimme, että elementeille olisi annettu edellä olevat nimet, käyttäen bem-nimeämiskäytäntöä.
On mahdollista, että olet antanut näille elementeille eri luokkien nimet.
Käytä siis antamiasi luokkien nimiä.*

Määritämme siis, että edellä olleet kaksi valitsinta, saavat molemmat saman `padding`-tilan.
Niille molemmille määritetään tyhjät padding:it sivuille, ja 10px ylä- ja alapuolelle.

Miksi käytämme tässä `padding`-sääntöä, emmekä `margin`-sääntöä? Luultavasti tässä tapauksessa eroa ei ole,
koska elementillä ei ole taustaväriä. Joudumme kuitenkin valitsemaan jomman kumman.

##### alitehtävä 3. lisää alapalkin otsikoiden alle saman verran tyhjää tilaa

Huomaamme, referenssikuvaa katselemalla, että alapalkin harmaalla osiolla, otsikoiden alla näyttäisi olevan saman verran tilaa joka paikassa.

Tarvitsemme siis yhteisen säännön tätä varten.

Lisää tätä varten html-tiedostoon, jokaiselle harmaan palkin otsikolle uusi luokka (vanhojen rinnalle): `harmaa-osio__otsikko`.
Käytämme tätä luokkaa seuraavaksi valitsimena css-tiedostossa.

Luomme siis seuraavaksi uuden valitsimen ja sille säännön:

```css
.harmaa-osio__otsikko {
  margin-bottom: 20px;
}
```

Valitse silmämääräisesti tyhjälle tilalle sopiva arvo. Se voi olla esim. jokin sivun monikerta.

##### alitehtävä 4. lisää aukioloaika-osioiden ympärille, kaikissa paikoissa, saman verran tyhjää tilaa

Huomaamme, referenssikuvaa katselemalla, että alapalkin harmaalla osiolla, aikatauluja listattaessa, 
niiden ympärillä näyttäisi olevan aina saman verran tyhjää tilaa, niitä edeltäviin ja seuraaviin elementteihin.

Aikataulujen välillä ei siis ole poikkeavaa tyhjää väliä, vaan niiden välillä.

Tämä viittaisi siihen, että referenssikuvan sivustolla, peräkkäiset aikataulurivit olisi ympäröity elementillä, joka vastaisi tämän tyhjän tilan varaamisesta.
Näin tapahtuisi myös silloin, kun aikataulurivejä olisi vain yksi.

Lisätään siis aikataulurivien ympärille uusi elementti, jos sellaista ei vielä ole. Käytämme tässä tapauksessa `ul`-elementtiä.

Alla näytämme miltä "myymälä: turku"-osion aikataululistauksen pitäisi näyttää. Tee sama muutos myös muualle missä aikataululistauksia löydät.

```html
<ul class="aikataululista">
  <li class="aikataululista__aikataululistaus">
    <div class="aikataululista__aikataululistaus__päivämäärä">
      Ma-Pe
    </div>
    <div class="aikataululista__aikataululistaus__aika">
      11:00-19:00
    </div>
  </li>
  <li class="aikataululista__aikataululistaus">
    <div class="aikataululista__aikataululistaus__päivämäärä">
      La
    </div>
    <div class="aikataululista__aikataululistaus__aika">
      10:00-16:00
    </div>
  </li>
</ul>
```

Huomaa, että jos nämä elementit olivat jo olemassa, ja niillä oli entuudestaan jo joku antamasi luokka, älä poista tuota vanhaa nimeä, vaan lisää vain uusi lisäksi.

Nyt voimme helposti tyylittää nämä rivit:

```css
.aikataululistaus {
  margin: 20px 0;
}
```

Asetamme siis taas tyhjää tilaa ylä- ja alapuolelle, mutta jätämme sivut tyhjiksi. 
Voimme havaita, että sivut menevät referenssikuvassa aina samassa linjassa yläpuolella ja alapuolella olevien rivien kanssa, linjautuen vasempaan laitaan.
Eli sivuille ei siis tarvita tyhjää tilaa, vaan sivuilla oleva tyhjä tila tulee jostain vanhempana olevasta elementistä, ja koskee kaikkia osion elementtejä.

##### alitehtävä 5. tyhjää tilaa muihin paikkoihin

Olisiko näiden lisäksi muita paikkoja, joissa tyhjää tilaa pitäisi lisätä?

Mieti tätä. Jos keksit sellaisia paikkoja, lisää näihin tyhjää tilaa. Vihje: näitä on paljon.

### Tehtävä 11 - lisätään tyhjä `section`-osio sivun sisällölle

Lisämme pikaisesti html-dokumenttiin oman paikan sivun sisällölle.

Tähän käytämme [`section`](https://developer.mozilla.org/en-US/docs/Web/HTML/section)-elementtiä.

Tällä saamme erotettua visuaalisesti ylä- ja alapalkin toisistaan myöhemmin, kun lähdemme värjäämään sivua.

**palautettavien tiedostojen nimet:** 

* `teht11.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht11.html`)**
* `teht11.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht11.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### tehtävänanto

1. Lisätään html-dokumenttiin tyhjä `section`-elementti.
2. Lisätään tälle elementille css-tyylit

##### Alitehtävä 1. Lisätään html-dokumenttiin tyhjä `section`-elementti.

Lisätään html-dokumenttiin tyhjä `section`-elementti.
Annetaan elementin luokaksi `sivun-sisältö`.
Jätämme elementin nyt tyhjäksi, koska meillä ei oikeastaan ole tällä hetkellä sivulle sisältöä.

```html
<section class="sivun-sisältö"></section>
```

Kutsumme elementtiä sivun sisällöksi, koska oikealle sivulla se vastaisi kaikesta todellisesta sivun sisällöstä.
Nythän olemme rajoittaneet sivun osalta kiinnostuksemme vain ylä- ja alapalkkiin,
mutta todellisuudessahan sivun todellinen kiinnostava sisältö olisi juuri tässä uudessa `sivun-sisältö`-elementin sisässä.
On kuitenkin hyvä vihdoin lisätä elementti myös tälle sivun todelliselle sisällölle, vaikkakin vain näin tyhjänä.

Lisätään tämä uusi elementti `header`- ja `footer`-elementtien väliin.

Sivun pitäisi korkealla tasolla näyttää tämän jälkeen seuraavalta:

```html
<html>
<head>...</head>
<body>
  <header>...</header>
  <section class="sivun-sisältö"></section>
  <footer>...</footer>
</body>
</html>
```

Huomaa, että lisäsimme siis vain yhden rivin html-dokumenttiin.

##### Alitehtävä 2. Lisätään tälle elementille css-tyylit

Lisätään vielä muutama tyyli tälle elementille css-tiedoston puolelle:

```css
.sivun-sisältö {
  display: flex;
  min-height: 14px;
  max-height: 14px;
  min-width: 100%;
  max-width: 100%;
}
```

Käsittelemme `height`- ja `width`-sääntöjä vähän myöhemmin lisää. 
Nyt riittää, että kopioit nämä säännöt elementille.

---

Nyt kun meillä on uusi sivun sisällölle yksilöity elementti `header`- ja `footer`-elementtien välissä,
voimme seuraavaksi lähteä paremmin värittämään sivua.
Pystymme muun muassa erottamaan tumman yläpalkin tummasta alapalkista, jättämällä näiden väliin tyhjän railon.

### Tehtävä 12 - `background-color`- ja  `color`-sääntö

Tässä välissä tarkastelemme [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)- ja [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color)-sääntöjä.

Näillä on mahdollista värjätä elementin tausta ja fontti tietyllä värillä.

Tarvitsemme värjättyjä elementtejä seuraavaa tehtävää varten.

**palautettavien tiedostojen nimet:** 

* `teht12.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht12.html`)**
* `teht12.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht12.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### lyhyesti `background-color`-säännöstä

`background-color`-sääntö on yksinkertainen:
Se annetaan elementille, ja sille annetaan väri, jolloin kyseinen elementti värjäytyy annetulla värillä.

```css
valitsin {
  background-color: <väri>;
}
```

Väri voi olla:

* varattu sana, esimerkiksi "black". Voit kokeilla erilaisia englanninkielisiä värin nimiä. Monet niistä varmasti toimivat.
* rgb-väri, muotoa `rgb(255,255,255)`

#### lyhyesti `color`-säännöstä

`color`-sääntö on yksinkertainen:
Se annetaan elementille, ja sille annetaan väri, jolloin kyseisen elementin teksti värjäytyy annetulla värillä.

```css
valitsin {
  color: <väri>;
}
```

Väri voi olla:

* varattu sana, esimerkiksi "black". Voit kokeilla erilaisia englanninkielisiä värin nimiä. Monet niistä varmasti toimivat.
* rgb-väri, muotoa `rgb(255,255,255)`


#### tehtävänanto:

1. lisää musta taustaväri, ja valkoinen fontinväri yläpalkille
2. lisää harmaa taustaväri, ja valkoinen fontinväri alapalkille
3. lisää musta taustaväri, ja valkoinen fontinväri alapalkin alaosalle
4. lisää valkoinen taustaväri, ja musta fontinväri yläpalkin hakukentälle
5. lisää valkoinen taustaväri, ja musta fontinväri sivun sisällöstä vastaavalle elementille
6. lisää oranssi taustaväri, ja valkoinen fontinväri uutiskirje-napille

##### alitehtävä 1. lisää musta taustaväri, ja valkoinen fontinväri yläpalkille

```css
.sivun-yläpalkki {
  background-color: black;
  color: white;
}
```

##### alitehtävä 2. lisää harmaa taustaväri, ja valkoinen fontinväri alapalkille

```css
.sivun-alapalkki {
  background-color: darkgray;
  color: white;
}
```

##### alitehtävä 3. lisää musta taustaväri, ja valkoinen fontinväri alapalkin alaosalle

```css
.sivun-alapalkki__musta-osio {
  background-color: black;
  color: white;
}
```

##### alitehtävä 4. lisää valkoinen taustaväri, ja musta fontinväri yläpalkin hakukentälle

```css
.sivun-yläpalkki__haku {
  background-color: white;
  color: black;
}
```

##### alitehtävä 5. lisää valkoinen taustaväri, ja musta fontinväri sivun sisällöstä vastaavalle elementille

```css
.sivun-sisältö {
  background-color: white;
  color: black;
}
```

##### alitehtävä 6. lisää oranssi taustaväri, ja valkoinen fontinväri uutiskirje-napille


```css
.tilaa-uutiskirje__sisältö__nappi {
  background-color: orange;
  color: white;
}
```

---

Tarkista, että käyttämäsi valitsimet todella toimivat. Jos ne eivät toimi, niin vaihda valitsimet sellaiseksi, jotka vastaavat elementtien nimiä omassa html-dokumentissasi.

### Tehtävä 13 - `flex`-sääntö

Tässä tehtävässä tarkastelemme [`flex`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)-sääntöä.

Sillä on mahdollista varata flexboxilla asemoidun elementin lapselle enemmän tilaa kuin sen viereisille elementeille annetaan.

**palautettavien tiedostojen nimet:** 

* `teht13.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht13.html`)**
* `teht13.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht13.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Lyhyesti `flex`-säännöstä

`flex`-sääntö on vähän harvinaisempi sääntö flexboxin työkalupaketissa, mutta se on silti hyvin hyödyllinen.

Sillä on mahdollista määrittää, että jokin elementti vie enemmän tilaa rivillä tai sarakkeessa kuin sen viereiset elementit.

Käytännössä tämä tapahtuu antamalla `flex`-sääntö lapsielementille, josta haluat tehdä sisaruksiaan isomman.
Tällöin annat kyseiselle elementille `flex`-säännön arvoksi numeron.
Oletuksena elementin `flex`-säännön arvo on 1, tarkoittaen, että se vie yhden sisaruksen verran tilaa.
Jos annat jonkin muun arvon `flex`-säännölle, se tarkoittaa, että kyseinen lapsi vie näin monta kertaa tilaa suhteessa muihin sen sisaruksiin.

Taas, tämä sääntö toimii vain, jos sen vanhemmalle on asetettu `display: flex;`-sääntö.

#### tehtävänanto:

1. sivun yläpalkin hakukenttä
2. sivun alapalkin sarakkeet

##### alitehtävä 1. sivun yläpalkin hakukenttä

Lisää `flex`-sääntö sivun yläpalkin hakukentälle.

Voit katsastaa referenssikuvasta, miltä hakukentän pitäisi näyttää.

Asetetaan hakukentälle siis `flex`-sääntö:

```css
.sivun-yläpalkki__haku {
  flex: 4;
}
```

Tässä flex:ille annettu arvo on vain esimerkkiarvo. 
Kokeile antaa sille isompi tai pienempi arvo, kunnes palkin koko vaikuttaa vastaavan referenssikuvan hakukentän kokoa.

##### alitehtävä 2. sivun alapalkin sarakkeet

Sivun alapalkin harmaalla alueella on sarakkeita. 
Näitä sarakkeita on neljä poikkiviivan ylä- ja alapuolella.

Näyttäisi siltä, että kaikki sarakkeista ovat saman levyisiä.

Tämäkin leveys on mahdollista määrittää `flex`-säännön avulla.

Pystyt tekememään sisarus-elementeistä saman levyiset antamalla niille kaikille saman `flex`-arvon.

Oletetaan, että olet antanut kaikille sarakkeille saman luokannimen.
Tällöin voit helposti tehdä elementeistä yhtä leveät:

```css
.sivun-alapalkki__harmaa-alue__sarake {
  flex: 1;
}
```

---

Voisiko `flex`-sääntöä käyttää muualla?

### Tehtävä 14 - `width`- ja `height`-säännöt

Tässä tehtävässä tarkastelemme [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width)- ja [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height)-sääntöjä.

Niillä on mahdollista asettaa elementille kiinteä leveys tai korkeus.

**palautettavien tiedostojen nimet:**

* `teht14.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht14.html`)**
* `teht14.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht14.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Lyhyesti `width`- ja `height`-säännöistä

`width`-säännöllä on mahdollista määrittää elementille kiinteä leveys.
Se saa arvokseen numeron ja yksikön. Esimerkiksi `10px`.

Se toimii seuraavasti:

```css
width: 10px;
```

Tämä asettaa elementin leveydeksi 10 pikseliä.

`height`-säännöllä on mahdollista määrittää elementille kiinteä korkeus.
Se saa arvokseen numeron ja yksikön. Esimerkiksi `10px`.

Se toimii seuraavasti:

```css
height: 10px;
```

Tämä asettaa elementin korkeudeksi 10 pikseliä.

##### huomio liittyen `width`- ja `height`-sääntöjen käyttöön flexboxin kanssa

On huomioitava, että `width`- ja `height`-säännöt eivät kuitenkaan toimi elementeillä, joille on asetettu `display: flex;`.

Tällöin pitää käyttää niiden sisarsääntöjä: 

* `width`-säännön sijaan käytetään sekä `min-width`- ja `max-width`-sääntöjä,
* `height`-säännön sijaan käytetään sekä `min-height`- ja `max-height`-sääntöjä,

Esimerkiksi normaalilla div-elementillä: 

```css
valitsin {
  display: block;
  width: 10px;
  height: 10px;
}
```

kun taas flexboxia käyttäessä:

```css
valitsin {
  display: flex;
  min-width: 10px;
  max-width: 10px;
  min-height: 10px;
  max-height: 10px;
}
```

Mitä `min-width`-sääntö oikeasti tekee?
Se asettaa minimileveyden, joka elementin täytyy vähintään täyttää.

Vastaavasti `max-width`-sääntö määrittää maksimileveyden, jota elementin leveys ei saa ylittää.

Kun asetamme molemmat arvot samoiksi, määritämme, että elementin minimileveys ja maksimileveys ovat samat, jolloin ne eivät voi olla tätä isompia tai pienempiä.

Sama toimii myös `height`-elementin osalta, käyttäen `min-height`- ja `max-height`-sääntöjä.

#### tehtävänanto:

Lisää leveys ja korkeus ostoskori-elementille.

```css
.sivun-yläpalkki__ostoskori {
  min-width: 28px;
  max-width: 28px;
  min-height: 28px;
  max-height: 28px;
}
```

Kokeile mikä on hyvä leveys ja korkeus ostoskori-kuvakkeelle. Vertaa versiotasi referenssikuvaan.

### Tehtävä 15 - `font-family`- ja `font-size`-säännöt

Tässä tehtävässä tarkastelemme [`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)- ja [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family)-sääntöjä.

Näillä säännöillä on mahdollista määrittää fontti, ja fontille koko.

**palautettavien tiedostojen nimet:** 

* `teht15.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht15.html`)**
* `teht15.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht15.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### `font-family`-sääntö

`font-family`-säännöllä on mahdollista määrittää elementin fontti.

Se määrittää elementin fontin, mutta myös kaikkien sen lapsielementtien fontin, kunnes jollekin lapsielementille asetetaan fontti uudelleen.

Se saa arvokseen pilkulla erotellun listan fontteja.
Selain käyttää ensimmäistä listalta löytyvää fonttia, jonka se löytää käyttäjän koneelta.

Yleensä viimeiseksi arvoksi annetaan vara-arvoksi joko `serif` (päätteellä) tai `sans-serif` (ilman päätettä), sen mukaan onko fontissa päätettä. 
Päätteellä tarkoitetaan fontista löytyvää väkästä.
Tyypillisesti paperilla kirjasimissa käytetään väkäsiä, mutta näytöllä taas välttämättä ei.

```css
font-family: serif;
```

#### `font-size`-sääntö

`font-size`-säännöllä asetetaan elementin fontin koko.
Se saa arvokseen numeron ja yksikön, esimerkiksi `10px`.

```css
font-size: 16px;
```

Taas, kun elementille asetetaan fonttikoko, tämä fonttikoko valuu myös kaikille elementin lapsille, ellei toisin määritetä.

#### tehtävänanto:

Määritä elementeille fontin koko. 
Voit myös määrittää elementeille jonkin tietyn fontin käytettäväksi.

Erityisesti haluat luultavasti vaihtaa otsikoiden fontin kokoa vastaamaan referenssikuvan otsikoiden fonttien kokoa.

Luultavasti kaikki fonttikoot vaativat pientä säätämistä.

### Tehtävä 16 - `text-transform`-sääntö

Tässä tehtävässä tarkastelemme [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform)-sääntöä.

Tällä säännölllä on mahdollista vaihtaa css-tyylien avulla teksti isoilla kirjaimilla kirjoitetuksi. Tarvitsemme sitä otsikoissa.

**palautettavien tiedostojen nimet:** 

* `teht16.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht16.html`)**
* `teht16.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht16.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### tehtävänanto

1. Vaihda otsikot isolla kirjoitetuksi
2. Vaihda Tilaa uutiskirje -napin teksti isolla kirjoitetuksi

##### alitehtävä 1. Vaihda otsikot isolla kirjoitetuksi

Vaihda jokainen otsikko isolla kirjoitetuksi.

Asiakaspalvelun otsikon vaihtaminen onnistuu seuraavasti:

```css
.asiakaspalvelu__otsikko {
  text-transform: uppercase;
}
```

##### alitehtävä 2. Vaihda Tilaa uutiskirje -napin teksti isolla kirjoitetuksi

```css
.tilaa-uutiskirje__sisältö__nappi {
  text-transform: uppercase;
}
```

---

Katso mitä muita arvoja `text-transform`-säännölle voi antaa.
Voisiko jotain muuta niistä käyttää sivulla?

### Tehtävä 17 - pseudo-elementit

Tässä tehtävässä tarkastelemme [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)-pseudo-elementtiä.

Kerromme myös nopeasti [`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)-pseudo-elementistä.

Lisäämme nyt siis lopultakin "shop-in-shops"-osion listoihin pystyviivat.

**palautettavien tiedostojen nimet:** 

* `teht17.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht17.html`)**
* `teht17.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht17.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### lyhyesti pseudo-elementeistä

Pääasiallisesti rakenteet määritetään html-dokumentin puolella.
Voimme kuitenkin jossain tilanteissa tarvita avustavia rakenteita myös sivun tyylitykseen.

Tällainen tilanne on mm. sivulla, kun haluamme "shop-in-shops"-osiossa erotella tuotemerkit toisistaan pystyviivalla.
Pystyviiva ei tällöin ole merkityksellinen sivun rakenteen osalta, eli emme merkitse sitä html-dokumenttiin.

Pystyviiva on kuitenkin visuaalisesti tärkeä, ja helpottaa luettavuutta, joten lisäämme sen css-tyylien puolella.

Tämä onnistuu pseudo-elementtien avulla.

CSS:n kaksi tärkeintä pseudo-elementtiä ovat `::before` ja `::after`.

* `before` lisää sivulle uuden pseudo-elementin ennen elementtiä
* `after` lisää sivulle uuden pseudo-elementin elementin jälkeen

Ne vaativat kaksi asiaa toimiakseen:

1. ne pitää liittää css-valitsimessa toisen elementin valitsimeen
2. niille pitää asettaa sisältö `content`-säännön avulla

Kun molemmat näistä on tehty, pseudo-elementti näkyy sivulla.
Kun pseudo-elementti on luotu, sen voi tyylittää melkein kun normaalin elementin.

##### 1. pseudo-elementit pitää liittää css-valitsimessa toisen elementin valitsimeen

Pseudo-elementille ei siis luoda omaa elementtiä html-dokumentin puolella, vaan ne lisätään css-tiedoston valitsin kohdassa olemassa olevaan elementtiin.

Se tapahtuu liittämällä kahdella kaksoispisteella (`::`) olemassa olevan elementin valitsimen perään pseudo-elementin varattu sana (`before` tai `after`).

```css
valitsin::before {
  /* sääntöjä */
}
```

tai

```css
valitsin::after {
  /* sääntöjä */
}
```

##### 2. niille pitää asettaa sisältö `content`-säännön avulla

Pelkkä valitsimen käyttö ei riitä, vaan pseudo-elementillä täytyy aina olla sisältö, vaikka sitten tyhjä sellainen.

Tämä sisältö määritetään `content`-säännön avulla.
Se saa arvokseen merkkijonon, jota merkitään lainausmerkkien sisään kirjoitetulla tekstillä.

```css
valitsin::after {
  content: "Pseudo-elementin näkyvä teksti tulee tähän."
}
```

Tämä merkkijono voi olla tyhjä, jos pseudo-elementin ei haluta sisältävän tekstiä.

```css
valitsin::after {
  content: ""
}
```

#### tehtävänanto

Lisätään "shop-in-shops" -osion listauksiin pystyviivat.

```css
.shop-in-shops ul li::after {
  content: "|";
}
```

Tässä `.shop-in-shops ul li` tarkoittaa, että `.shop-in-shops`-luokalla on `ul`-lapsielementti, jolla on vuorostaan yksi tai useampi `li`-lapsielementti.

Vastaavasti `.shop-in-shops ul li::after` tarkoittaa, että pseudo-elementti kiinnittyy kaikkiin `li`-lapsielementteihin.

---

Kokeile mitä tapahtuu, jos käyttäisitkin `before`-pseudo-elementtiä.

### Tehtävä 18 - `border-radius`-sääntö

Tässä tehtävässä tarkastelemme [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)-sääntöä.

`border-radius`-säännön avulla pystymme pyöristämään elementtien kulmia, tai tekemään elementeistä kokonaan pyöreitä.

**palautettavien tiedostojen nimet:** 

* `teht18.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht18.html`)**
* `teht18.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht18.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### lyhyesti `border-radius`-säännöstä

Nimensä mukaisesti `border-radius`-sääntö vaikuttaa elementin reunoihin. 
Se ei kuitenkaan vaadi, että elementille olisi asetettu reunoja `border`-säännön avulla.

Samalla kun se pyöristää elementin reunoja, se pyöristää myös elementin padding-alueen sisältöä,
siis elementin taustaväriä ja sitä aluetta, johon taustaväri vaikuttaa.

Yleisin muoto `border-radius`-säännöstä on muoto, jossa se saa yhden arvon.
Tämä arvo koostuu numerosta ja yksiköstä.

```css
border-radius: 10px;
```

Tällöin sen saama arvo vaikuttaa kaikkien kulmien pyöristämiseen samassa suhteessa.

Yleinen yksikkö pikselien lisäksi on prosentit:

```css
border-radius: 10%;
```

Sille on myös mahdollista antaa useampia arvoja, jolloin on mahdollista pyöristää eri kulmia eri suhteessa:

```css
border-radius: 10% 50%;
```

Näitä harvemmin kuitenkin näkee käytetyn. 
Yleisintä on, että elementin kaikkia kulmia halutaan pyöristettävän samassa suhteessa.

Sen lisäksi, että `border-radius`-sääntö mahdollistaa elementin kulmien pyöristämisen,
sillä voi myös tuottaa pyöreän muodon, antamalla riittävän suuren arvon.

```css
border-radius: 50%;
```

Arvon määrittäminen 50-prosenttiin tuottaa ympyrän, tai ellipsin, riippuen elementin sivujen pituuksista.

Jos tarvitaan ympyrää, tulee varmistaa, että elementti on neliön mallinen,
siis että sen kaikki sivut ovat yhtä pitkät.

```css
border-radius: 50%;
width: 10px;
height: 10px;
```

Tai flexboxia käytettäessä, jolloin `width` ja `height` eivät toimi:

```css
border-radius: 50%;
min-width: 10px;
max-width: 10px;
min-height: 10px;
max-height: 10px;
```

#### tehtävänanto

Lisätään sivulle pyöreitä muotoja:

1. Pyöristetään hakupalkin kulmia
2. Pyöristetään nappien kulmia
3. Tehdään pyöreät tilanvaraaja-elementit toimimaan tilanvaraajina ympyränmuotoisille kuville


##### alitehtävä 1. Pyöristetään hakupalkin kulmia

Tehdään hakupalkin kulmista pyöreät.

Kun hakupalkki nyt näyttää suurin piirtein seuraavalta:

```html
<div class="haku-palkki">
  <div class="haku-palkki__ikoni">Q</div>
  <div class="haku-palkki__teksti">Hae tuotteista</div>
</div>
```

Kohdistetaan sen uloimpaan osaan uusi sääntö:

```css
.haku_palkki {
  border-radius: 7px;
}
```

Älä käytä suoraan esimerkissä käytettyjä luokannimiä, 
vaan korjaa css-valitsin kohdistumaan omassa html-dokumentissasi käyttämiisi luokannimiin.

Vastaavasti, kokeile erilaisia arvoja `border-radius`-säännölle, 
kunnes kulman pyöristys mielestäsi muistuttaa referenssikuvasta löytyviä pyöristyksiä.

Vinkkinä, referenssikuvassa pyöristys on hyvin pieni, mutta se kuitenkin näyttäisi olevan olemassa.

Tarkoituksena ei kuitenkaan ole ottaa valmiita arvoja oikealta sivulta, 
vaan opettaa silmä havaitsemaan eroja referenssikuvan ja oman toteutuksen väliltä.
Teemme siis sivua referenssikuvan pohjalta - emme kopioi alkuperäistä sivua.

##### alitehtävä 2. Pyöristetään nappien kulmia

Tehdään samoin muiden referenssikuvassa pyöreitä kulmia sisältävien nappien elementeille.

Voit ottaa mallia edellisestä alitehtävästä.

##### alitehtävä 3. Tehdään pyöreät tilanvaraaja-elementit toimimaan tilanvaraajina ympyränmuotoisille kuville

Kun edellisissä alitehtävissä pyöristettiin vain vähän kulmia, tässä luodaan pyöreitä muotoja.

Palkinnot-osiossa on referenssikuvassa kaksi pyöreää kuvaa.
Teemme näitä varten tilanvaraajat (engl. placeholder).
Emme siis lähde lisäämään oikeita kuvia, 
vaan teemme nopeasti css-säännöillä nykyisistä elementeistä kuvia päällisin puolin muistuttavat versiot.
Tällöin elementit tarjoavat näkymää siitä, millaisia kuvien lopulta tulisi olla.

Kun html näyttää taas suurin piirtein seuraavalta:

```html
<div class="palkinto">
  palkinto
</div>
```

Css on taas yksinkertainen:

```css
.palkinto {
  border-radius: 50%
}
```

Määrittämällä `border-radius`-säännön arvoksi 50-prosenttia, tai suurempi arvo, teemme elementistä pyöreän.

Tee sama myös toiselle palkinnolle.
Se ei kuvana ole täysin pyöreä, mutta tekemällä siitä nyt pyöreän, saamme tuotettua tarpeeksi alkuperäistä lähellä olevan tilanvaraajan.

Lisää molempiin vielä sopiva taustaväri, jotta ne näyttäisivät oikealta, ja jotta pyöristys siis alkujaankaan erottuisi.

### Tehtävä 19 - fontit

Referenssikuvassa käytetty fontti on Open Sans. Se on [ladattavissa](https://fonts.google.com/specimen/Open+Sans) Googlen fonttijakelusta.

**palautettavien tiedostojen nimet:** 

* `teht19.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht19.html`)**
* `teht19.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht19.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Fonttien käyttö

##### Lataa Open Sans -fontti

Lataa [Open Sans](https://fonts.google.com/specimen/Open+Sans) -fontti.

Pura ladattu zip-tiedosto, ja kopioi sieltä ttf-tiedosto samaan kansioon html-tiedostosi kanssa.
Huomioi, että et halua kursivoitua *italic*-versiota fontista,
vaan version tavallisen.
Eli kopioi normaali "variable font" -versio fontista.

##### Ota fontti käyttöön css:ssä

lisää css-tiedoston alkuun seuraavanlainen pätkä:

```css
@font-face {
  font-family: 'Open Sans';
  src: url(XX);
}
```

jossa `XX` on lataamasi Open Sans -tiedoston nimi.
Pelkkä tiedoston nimi riittää.
Nimeen ei tarvitse liittää polkua, koska se on samassa kansiossa sitä käyttävän css-tiedoston kanssa.

##### Käytä fonttia elementeillä

Voit ottaa fontin käyttöön kaikilla elementeillä lisäämällä sen `body`-elementille:

```css
body {
  font-family: "Open Sans";
}
```

Tällöin `body`-elementti, ja kaikki sen lapsielementit käyttävät fonttia, 
ellei niille ole puussa erikseen muuta fonttia määritetty.

Tunnistat, että Open Sans on oikein käytössä, 
kun sivulla olevassa "tilaa uutiskirje"-otsikossa J-kirjaimen alaosa menee muiden kirjaimien alapuolelle.

#### Tehtävänanto

1. Lataa Open Sans -fontti googlen sivuilta. 
2. Lisää lataamasi fontti samaan kansioon html-tiedostojen kanssa.
3. Valitse zip-tiedostosta variable font -muotoinen fontti.
4. Ota fontti ohjeiden mukaan sivulla käyttöön css-tiedostossa.

Huomaa, että **et voi käyttää googlen välityspalvelinta fontin jakeluun,** 
vaan sinun pitää ladata fontti itsellesi, ja jaella se html-tiedoston kanssa omasta lähteestäsi. 
EU:n GDPR-asetuksen puitteissa tiedostojen jakelu ulkopuolisten palvelujen puitteissa on mahdollisesti laitonta, 
jos jakelijan kanssa ei ole tehty erillistä sopimusta tietojen käsittelystä. 
Google mahdollisesti jäljittää kaikki sen palveluihin tulevat sivun lataukset, 
ja jos et ole saanut käyttäjiltä suostumusta tietojen jakoon googlen kanssa, 
et lähtökohtaisesti voi ohjata näitä googlen palveluihin ilman tällaista erillistä ja tietoista suostumusta. 
Helpompaa on siis vain tarjoilla fontit itse samasta paikasta html-tiedostojen kanssa.

### Tehtävä 20 - ikonit fontteina

Referenssikuva käyttää ikoneita useissa paikoissa.
Voit käyttää valitsemaasi ikonikirjastoa sivun ikonien toteuttamiseen.

Tässä tehtävässä voit käyttää:

* normaaleina ikoneina googlen apache-lisenssillä lisensoitua [Material Icons](https://fonts.google.com/icons) -ikonikirjastoa,
* sosiaalisten medioiden ikoneina esim. [font awesome:n](https://fontawesome.com/) -ikoneita.

**palautettavien tiedostojen nimet:** 

* `teht20.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht20.html`)**
* `teht20.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht20.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Tehtävänanto

Lisää sivulle referenssikuvan mukaisiin paikkoihin ikoneita.

Voit toteuttaa ikonit esim. yhdellä seuraavista neljästä tavasta:

* käytä kirjaimia tai merkkejä ikonien tilanvaraajina (yleinen tapa kehitysvaiheessa)
* käytä unicodeen kuuluvia emojeja ikonien tilalla
* käytä esim. googlen material icons -kirjaston ikoneja (oletusvaihtoehto, johon alla ohjeet)
* käytä jotain muuta ikonikirjastoa

Huomioi taas, että et voi käyttää ikoneitakaan varten ulkopuolisia cdn-palveluita, 
vaan kaikki ikonien käyttöön vaaditut tiedostot pitää jaella hallitsemastasi paikasta. 
Näissä tehtävissä tuo paikka oletetaan omaksi tietokoneeksesi, 
mutta käytännössä se olisi jokin hallitsemasi palvelin.

#### kuvien lisääminen `img`-elementin avulla

Jos haluat käyttää kuva-muotoisia ikoneita, onnistuu tämä `img`-elementin avulla.

`img`-elementtiä käytetään itsestään sulkeutuvan tagin muodossa. 
Se saa yhden `src`-attribuutin, jolle annetaan polku näytettävään kuvatiedostoon.

Esim.

```html
<img src="kuva.jpg" />
```

Huomaa, että jos kuvatiedostosi on samassa kansiossa html-tiedoston kanssa, 
riittää, että annat `src`-attribuutille pelkän tiedoston nimen polkuna (esim. "kuva.jpg").
Tässäkin tapauksessa kyse ei kuitenkaan oikeasti ole tiedostonnimen antamisesta,
vaan relatiivisesta polusta, joka sattuu vain koostumaan pelkästä tiedoston nimestä.
Tämä lyhyt relatiivinen polku on mahdollinen, 
jos tiedosto löytyy samasta kansiosta html-tiedoston kanssa, josta sitä käytetään.

#### Material icons

Voit lukea material icons:in käytöstä lisää seuraavista linkeistä:

* [dokumentaatio](https://developers.google.com/fonts/docs/material_icons) - ohjeet ja tietoa käytöstä
* [jakelu](https://github.com/google/material-design-icons) - lataa ikonit ja tarkista lisenssi
* [galleria](https://fonts.google.com/icons) - katso mitä ikoneja on tarjolla

Voit käyttää materia icons -ikoneita useammassa eri muodossa:

* fonttina
* svg-kuvina
* png-kuvina

Voit lukea näistä käyttötavoista lisää yllä olevasta dokumentaatio-linkistä.

Mikä näistä sitten kannattaisi valita?

* Jos käytät paljon ikoneita sivulla, voi kyseeseen tulla fontin käyttö. Se on kuitenkin mahdollisesti raskain vaihtoehto. Näiden värjääminen on kuitenkin mahdollisesti helpointa.
* svg-kuvat ovat kuin html-tiedostoja, ja vaativat, että ne renderöidään selaimessa - modernit selaimet yleensä osaavat tehdä tämän hyvin.
* png-kuvat saattavat olla verrattain kevyitä. Toisaalta niitä ei pysty värjäämään itse.

Tässä tehtävässä kannattaa luultavasti käyttää ikoneita fonttina, koska niiden värjääminen css:llä pitäisi tällöin olla suhteellisen helppoa.

### Tehtävä 21 - `:hover`-pseudoluokka-valitsin

Tässä tehtävässä lisäämme sivulle dynaamista toimintaa, päivittämällä yläpalkin kategoriat vaihtamaan väriä, 
kun käyttäjä siirtää hiirensä niiden päälle.

Tämä onnistuu [`:hover`](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover)-valitsimen avulla.

**palautettavien tiedostojen nimet:** 

* `teht21.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht21.html`)**
* `teht21.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht21.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Tehtävänanto

Lisää css-tiedostoon yläpalkin kategoria-elementeille uusi valitsin, käyttäen `:hover`-valitsinta, ja lisää sille säännöt, jotka vaihtavat fontin ja taustan väriä. Alta löytyy esimerkki `:hover`-valitsimen käytöstä. 

Kun käyttäjä siirtää hiirensä yläpalkin kategorian päälle, sen tulisi vaihtaa väriä seuraavasti:

* taustaväri muuttuu valkoiseksi,
* fontin väri muuttuu oranssiksi. voit katsoa sävyn "tilaa uutiskirje"-napista.

Voit katsoa esimerkkiä toteutuksesta mallina käytetyltä sivulta.

##### `:hover`-valitsimen käyttö

Css:llä on mahdollista valita elementtien, tunnisteiden ja luokkien, sekä pseudoelementtien (`::before`, `::after`) lisäksi myös useita erilaisia pseudoluokkia. Tässä tehtävässä `:hover`-pseudoluokkaa. Voit lukea muista pseudoluokista mm. mdn:n sivuilta.

Pseudoluokan tunnistaa muista valitsimista sen edestä löytyvästä kaksoispisteestä, erotuksena esimerkiksi pseudoelementteihin, jotka sisältävät kaksi kaksoispistettä edessään.

Pseudoluokka ei ole oikea luokka, vaan se vaatii, että sitä käytetään ketjutettuna toiseen oikeaan valitsimeen:

```css
a:hover {
  background-color: red;
}
```

Tässä tehtävässä haluamme erityisesti värjätä yläpalkin kategoriat.
Tämä onnistuu seuraavasti:

```css
.kategoriat__kategoria:hover {
  color: orange;
  background-color: white;
}
```

Oletuksena on, että kategorioiden luokan nimenä on `.kategoriat__kategoria`. 
Jos olet käyttänyt muuta luokan nimeä, joudut vaihtamaan valitsimeksi käyttämäsi luokan nimen.

Käytä oranssina värinä jotain silmämääräisesti referenssikuvan oranssia väriä vastaavaa oranssin sävyä. 
Voit käyttää tähän halutessasi [rgb](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value/rgb)-arvoa.

---

Olisiko sivulla muita paikkoja, jossa voisi käyttää `:hover`-pseudoluokkaa? 
Jos on voit lisätä näihinkin samanlaisen dynaamisen toiminnallisuuden.
Tällaisia potentiaalisia paikkoja ovat erilaiset napit, jotka tyypillisesti hoveroituna vaihtavat taustansa väriä.

### Tehtävä 22 - linkkien värin asettaminen `:any-link`-pseudoluokka-valitsimen avulla

Tässä tehtävässä värjäämme sivulla olevia linkkejä. 

Perinteisesti html erottelee värien puolesta linkkejä sen perusteella, onko käyttäjä jo vieraillut niissä.

Koska sivumme ei ole perinteinen dokumentti vaan sovellus, 
emme hyödy vierailtujen sivujen näyttämisestä eri tavalla suhteessa vierailemattomiin sivuihin.
Sovelluksen kannalta kaikki sivut ovat tasa-arvoisia, oli käyttäjä jo käynyt niillä tai ei. 
Emme siis halua näyttää linkkejä erivärisinä, koska siitä ei ole meille toiminnallista hyötyä.

Värjäämme siis linkit kaikissa tilanteissa samalla värillä.

Tämä onnistuu [`:any-link`](https://developer.mozilla.org/en-US/docs/Web/CSS/:any-link)-valitsimen avulla,
joka valitsee molemmat linkkien muodot: vieraillut ja vierailemattomat.

**palautettavien tiedostojen nimet:** 

* `teht22.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht22.html`)**
* `teht22.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht22.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Tehtävänanto

Käytä `:any-link`-pseudoluokkaa valitsimena, ja värjää sivulla olevien linkkien tekstit referenssikuvan mukaisesti.

Voit kurkata yltä `:hover`-tehtävän kuvauksesta, miten pseudoluokkia käytetään.

### Tehtävä 23 - `flex-wrap`-sääntö ja elementtien wrappays, kun rivillä on liikaa elementtejä

Tässä tehtävässä korjaamme lopultakin shop-in-shops -osion brändilistauksen elementit virtaamaan nätisti riveittäin useammalle riville.

Tähän asti brändien `ul`-elemetin sisällä olevat `li`-elementit ovat olleet joko leveästi yhdellä rivillä,
tai pitkänä allekkaisena listana.

Jotta saamme ne referenssikuvan mukaisesti virtaamaan riveittäin, kuitenkin valuen aina seuraavalle riville,
kun sarakkeen leveys tulee vastaan, joudumme käyttämään [`flex-wrap`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap)-sääntöä.

**palautettavien tiedostojen nimet:** 

* `teht23.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht23.html`)**
* `teht23.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht23.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Tehtävänanto

Käytä `flex-wrap`-sääntöä rivittämään shop-in-shops -osion brändisivujen linkit nätisti riveittäin useammalle riville, referenssikuvan mukaisesti.

`flex-wrap`-sääntö asetetaan vanhempana toimivalle elementille seuraavasti:

```css
ul {
  flex-wrap: wrap;
}
```

Tällöin se näyttää lapsielementit `flex-direction`-arvon mukaisesti rivinä tai sarakkeena, mutta tilan loppuessa luo uuden rivin tai sarakkeen.

Voit lukea mdn:n linkistä lisää ohjeita säännön käyttöön muissa tilanteissa.

---

Jos et ole vielä vaihtanut sosiaalisen median logojen tilanvaraaja-tekstien tilalle pienempiä kuvakkeita, voit kenties haluta käyttää `flex-wrap`-sääntöä myös niihin.

### Tehtävä 24 - `input`-elementti

Lisätään hakupalkkiin input-elementti.

**palautettavien tiedostojen nimet:** 

* `teht23.html` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht23.html`)**
* `teht23.css` (kansiossa: `harjoitukset/01-html-ja-css/03-css-flexbox/teht23.css`)**

*Vaihda `html`-tiedoston `link`-elementin `href`-attribuutin arvo osoittamaan uudelleennimetyn `css`-tiedoston nimeen.*

#### Tehtävänanto

Jos et ole vielä ehtinyt vaihtaa yläpalkin hakukenttän elementiksi [`input`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)-elementtiä, 
nyt on viimeistään aika tehdä se.

##### itsensä sulkeva elementti

`input`-elementti on tyypillisesti itsensäsulkeva elementti muotoa `<input />`, sillä ei siis ole sisältöä, tai sulkevaa tagia.

##### Tyhjälle kentälle annetaan teksti `placeholder`-attribuutilla

`input`-elementille voidaan asettaa oletusteksti `placeholder`-attribuutilla, tilanvaraajaksi määritetty teksti näkyy silloin kun kentässä ei ole arvoa.

##### kenttä voi olla montaa eri tyyppiä

`input`-elementille on mahdollista määrittää tyyppi. Tällöin esim. puhelimet osaavat peittää `password`-tyyppiä olevan kentän tekstin käyttäjältä.

Kentän tyypin määrittäminen tapahtuu `type`-attribuutin avulla.
Tyypillinen arvo on "text", joka kertoo, että kenttä saa arvokseen tekstiä, eikä sitä tarvitse kohdella erityisesti.
Tätä tyyppiä käytämme tässäkin tapauksessa.

Voit tarkistaa ajantasaisen tiedon mahdollisista `type`-attribuutin arvoista mdn:n sivuilta.

##### Esimerkki: hakukenttä

`input`-elementin käytön jälkeen hakuelementin pitäisi näyttää enemmän tai vähemmän seuraavalta, toki omilla luokannimilläsi ja elementtirakenteillasi varustettuna:

```html
<input class="hakukenttä" type="text" placeholder="Hae tuotteista" />
```

### Lopputehtävä - viimeistele sivu

Lopuksi viimeistele tekemäsi sivu vastaamaan mahdollisimman tarkasti, ylä- ja alapalkin osalta, referenssikuvaa.

Tarkasta erityisesti, että:

* tekstin värit ja elementtien taustavärit vastaavat referenssikuvaa,
* tekstien koot ovat oikeat, silmämääräisesti,
* elementit ovat sivulla oikeissa kohdissa toisiinsa nähden,
* elementtien välissä olevaa tyhjää tilaa on joka puolella oikea määrä,
* sivu muutoin vastaa referenssikuvaa

Sivulla olevien elementtien välisten tyhjien etäisyyksien mittaamiseen voit käyttää jotain aputyökalua: 
esimerkiksi sormi tai hiiren kursori saattavat auttaa mittaamaan etäisyyksiä tarkemmin,
jos et silmämääräisesti eroja vielä pysty hahmottamaan.
Sama tekniikka toimii myös muiden kokojen ja mittojen kanssa, fonttien koosta nappien korkeuksiin.
