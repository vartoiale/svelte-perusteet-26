# Harjoitukset 2: Lisää html-rakenteita

## Ohjeita tehtävien palautukseen

Tällä kertaa tehtävät palautetaan uuteen kansioon `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/`.

## Tehtävät

### Tehtävä 0A

**palautettavan tiedoston nimi:** `referenssikuva.jpg` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/referenssikuva.jpg`) (tiedostonpääte saa olla myös muu kuvatiedosto: jpeg, png, yms)

Ota kuvakaappaus jimms-kaupan verkkokaupasta, oheisen kuvan mukaisesti.

Skrollaa sivu sivun loppuun niin, 
että yläpalkki (engl. header) ja alapalkki (engl. footer) ovat molemmat näkyvissä samassa kuvassa. 
Itse sivun muun sisällön ei tarvitse näkyä kuvassa, 
muutoin kuin valkoisena raitana joka erottaa ylä- ja alapalkin toisistaan.

Tallenna kuvakaappaus ylläolevalla nimellä tähän repositorioon, yllä mainittuun kansioon.

![referenssikuva jimms-kaupan verkkosivun ylä- ja alapalkista](/materiaali/kuvat/referenssikuva-header-footer-jimms.jpeg)

### Tehtävä 0B1

**palautettavien tiedostojen nimet:** 

* `referenssikuva-yle-osioittain.jpg` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/referenssikuva-yle-osioittain.jpg`) (tiedostonpääte saa olla myös muu kuvatiedosto: jpeg, png, yms) - jimms (tehtiin yhdessä)
* `referenssikuva-jimms-osioittain.jpg` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/referenssikuva-jimms-osioittain.jpg`) (tiedostonpääte saa olla myös muu kuvatiedosto: jpeg, png, yms) - yle.fi (tehdään yksin)

Tätä tehtävää varten piirretään referenssikuvaan suorakulmioiden avulla erilaisia osioita, joita kuvassa näkyvästä sivusta löytyy.

#### Referenssikuvat

Kopioi alla olevista linkeistä kuvat koneellesi, ja nimeä ne uudelleen (yllä ohjeet nimeämiseen).

* [yle.fi](/materiaali/kuvat/referenssikuva-etusivu-ylaosa-yle.jpeg) 
* [jimms](/materiaali/kuvat/referenssikuva-header-footer-jimms.jpeg)

#### Ohje

Ohjeet (samat molemmille kuville):

* Tee referenssikuvasta kopio, ja muokkaa sitä kuvankäsittelyohjelmalla, esimerkiksi paintilla. 
* Käytä suorakulmionpiirtotyökalua apunasi, ja piirrä näkyviin, 
missä kaikkialla referenssikuvassa saattaisi olla yhtenäisiä kokonaisuuksia, jotka muodostaisivat omia osiaan.

Käytetyt värit:

* keltainen - elementti jolla on lapsia
* oranssi - elementti, jolla on vain yksi lapsi (esim, kuva, teksti)

Jokainen kuvassa näkyvä asia pitäisi siis olla lopulta oman oranssin laatikon sisällä.
Lisäksi oranssien laatikoiden pitäisi olla yhden tai useamman keltaisen laatikon sisällä.

*Voit myös käyttää jotain muita värejä kuvaamaan näitä erilaisia elementtejä. 
Jos käytät toisia värejä, merkitse kuvaan, mitä värejä käytit.*

*Tätä harjoiteltiin yhdessä luokassa 5.11.2024.*

Lopputuloksena pitäisi olla seuraavan kaltainen kuva.
Siitä näkyy visuaalisessa muodossa, alustavasti, minne kaikkialle html-elementtejä sivulla pitää todennäköisesti luoda. 

![referenssikuva jimms-kaupan verkkosivun ylä- ja alapalkista](/materiaali/kuvat/refererenssikuva-header-footer-jimms-osioittain.jpg)

### Tehtävä 1

**palautettavan tiedoston nimi:** `teht1.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht1.html`)

Luo yksinkertainen html-dokumentti, joka:

* sisältää kaiken referenssikuvassasi näkyvän tekstin,
  * jokaisen tekstin pitää olla omalla rivillään
  * järjestä rivit kuvan perusteella:
    * yhtenäisinä osina, jotka ovat tyhjän tilan ympäröimiä
    * vasemmalta oikealle,
    * ylhäältä alas
  * jos sivulla on kuvia tai ikoneita, lisää myös nämä omille riveilleen käyttäen selvää nimeä
    * esim. `ostoskori-ikoni`
* ei sisällä yhtään html-elementtiä.

#### Esim. toteutus

Tiedoston pitäisi muistuttaa seuraavaa esimerkkiä. 
Merkintä `...` tarkoittaa, että tähän kohtaan tulee esimerkistä pois jätettyjä kohtia. 

```html
jimms
hae tuotteista
kirjaudu/luo tili
ostoskori-ikoni
tietokone
komponentit
...
kampanjat
asiakaspalvelu
ma-su 24/7
+358 ...
...
Yritysmyynti
ma-su 24/7
...
Myymälä turku
ma-pe ...
...
Yhteisöt
...
Jimm's PC-Store Oy
```

Tehtävässä ei tule lisätä yhtään html-elementtiä. Ne lisätään seuraavissa tehtävissä.


### Tehtävä 2

**palautettavan tiedoston nimi:** `teht2.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht2.html`)

Luo yksinkertainen html-dokumentti seuraavien määrittelyjen puitteissa:

* se sisältää kaiken mitä teht1.html sisälsi (eli leikkaa ja liimaa edellisestä tehtävästä),
* se sisältää html-elementit: `html`, `head` ja `body`,
* jokainen teht1.html:n rivillä oleva teksti on ympäröity `div`-elementillä.

#### Esim. toteutus

Tiedoston pitäisi muistuttaa seuraavaa esimerkkiä. 

```html
...
<div>jimms</div>
<div>hae tuotteista</div>
<div>kirjaudu/luo tili</div>
...
```


### Tehtävä 3

**palautettavan tiedoston nimi:** `teht3.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht3.html`)

Luo yksinkertainen html-dokumentti seuraavien määrittelyjen puitteissa:

* se sisältää kaiken mitä teht2.html sisälsi (eli leikkaa ja liimaa edellisestä tehtävästä),
* se sisältää html-elementit: `html`, `head` ja `body`,
* yläpalkin rivit on ympäröity `header`-elementillä
* alapalkin rivit on ympäröity `footer`-elementillä

#### Esim. toteutus

Tiedoston pitäisi muistuttaa seuraavaa esimerkkiä. 

```html
<header>
...
<div>jimms</div>
<div>hae tuotteista</div>
<div>kirjaudu/luo tili</div>
...
</header>
<footer>
...
</footer>
```

### tehtävä 4.1 | jae (uusi tehtävä)

**palautettavan tiedoston nimi:** `teht4-1.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht4-1.html`)

Tässä tehtävässä lähdetään luomaan rakennetta sivulle. 
Käytämme edelleen `div`-elementtejä, koska ne sopivat vähän joka paikkaan, ja niitä voi myöhemmin vaihtaa toisiin html-elementteihin.

Yläpalkki ja alapalkki on melko selvästi nähtävissä erilaisista vertikaalisesti toisistaan eroavista osuuksista.

Yläpalkissa on nähtävissä, että siinä olisi selvästi kaksi erilaista riviä.
Alempi rivi, jossa listataan tuotealueita, tai kategorioita, on selvästi oma ylemmästä rivistä irrallinen kokonaisuus.
Ylemmällä rivillä on useampaa erilaista kenttää, mutta ne voidaan mieltää omaksi yhteiseksi rivikseen.
Yläpalkki koostuisi siis kahdesta eri rivistä, joita voidaan kuvata uusilla `div`-elementeillä, 
jotka ympäröisivät näiden rivien nykyisiä sisältöjä.
Lisätään siis nämä kaksi uutta `div`-elementtiä yläpalkkiin.

Alapalkissa on selvästi enemmän sisältöä, mutta senkin voisi ajatella koostuvan useammasta vertikaalisesta osiosta.
Helpoin erottaa, on lopusta löytyvä, tummemmalla taustavärillä osoitettu takuuehdoista kertova osio.
Tämä osio voidaan nostaa omaksi osiokseen, ympäröimällä sen sisältö uudella `div`-elementillä.


Tämän tehtävän jälkeen sivulla pitäisi olla neljä uutta `div`-elementtiä.

yläpalkki:

* ensimmäinen rivi
* toinen rivi

alapalkki:

* harmaa, ylempi osa
* tummempi, alempi osa

### tehtävä 4.2 | pilkotaan alapalkki vielä isoihin osiin

**palautettavan tiedoston nimi:** `teht4-2.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht4-2.html`)

Kun tarkastelemme alapalkkia, ja sen ylempää, harmaata osaa, näyttäisi se vielä koostuvan kahdesta eri osasta.
Alapalkin vaaleamman harmaan yläosion näyttäisi halkaisevan kahtia horisontaalinen viiva. 
Alapalkin yläosio näyttäisi siis koostuvan vielä kahdesta eri osasta, harmaasta yläosasta ja harmaasta alaosasta.

Tehdään näillekin vielä omat `div`-elementit.

Tämän tehtävän jälkeen pitäisi olla kaksi uutta `div`-elementtiä:

alapalkki:

* harmaan osan ylempi osa
* harmaan osan alempi osa

### tehtävä 4.3 | itsenäisiä osioita (vanha tehtävä 4)

**palautettavan tiedoston nimi:** `teht4-3.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht4-3.html`)

Jatketaan rakenteen luomista.

Lisää `div`-elementti jokaisen itsenäisen sivun kokonaisuuden ympärille.

* jos näet sivulla viivan, jakaa se luultavasti edellisen ja seuraavan osan omiin `div`-elementteihin.
* jos näet tyhjää tilaa osion ympärillä, on kyseessä luultavasti myös eri `div`-elementit.
* jos osan tekstuaalinen sisältö on samanlainen viereisen osan kanssa, on niillä luultavasti jossain kohtaa vanhempana sama `div`-elementti.

Tarkoituksena olisi siis tässä tehtävässä jo saada sivulle vähän oikeanlaista rakennetta. 
Tämä tapahtuu ympäröimällä isompia yhtenäisiä kokonaisuuksia `div`-elementeillä.

Sivulle pitäisi tässä tehtävässä lisätä seuraavat uudet `div`-elementit, 
jotka ympäröivät näiden listattujen kohtien viereisiä elementtejä:

yläpalkin ensimmäinen rivi:

* jimms (vain kaupan logo)
* hakupalkki (vain hakupalkki ja sen sisältö)
* kirjaudu ja ostoskori (nämä kaksi)

alapalkki:

* asiakaspalvelu (ja siihen liittyvät muut kentät)
* yritysmyynti (...)
* myymälä turku
* yhteisöt
* tilaa uutiskirje
* info
* shop in shops
* artikkelit ja blogit
* sertifikaatit ja palkinnot
* takuu ja copyright

#### Esimerkiksi

Kun edellisen osan jälkeen näytti tältä:

```html
...
<div>yritysmyynti@jimms</div>
<div>myymälä turku</div>
<div>ma-pe 11:00-19:00</div>
<div>la 10:00-16:00</div>
<div>maksuvälineenä ...</div>
<div>lukkosepänkatu ...</div>
<div>yhteisöt</div>
...
```

Niin tämän tehtävän jälkeen pitäisi näyttää seuraavalta:

```html
  ...
  <div>yritysmyynti@jimms</div>
</div>
<div>
  <div>myymälä turku</div>
  <div>ma-pe 11:00-19:00</div>
  <div>la 10:00-16:00</div>
  <div>maksuvälineenä ...</div>
  <div>lukkosepänkatu ...</div>
</div>
<div>
  <div>yhteisöt</div>
  ...
```

Eli turun myymälään liittyvien tietojen olisi nyt pitänyt saada ympärilleen yhteinen `div`-elementti.
Samoin tämän tehtävän jälkeen pitäisi olla käynyt muille saman tason kokonaisuuksille.

### tehtävä 4.4 | yhdistetään alapalkkin asiakaspalvelu ja yritysmyynti yhteiseksi sarakkeeksi

**palautettavan tiedoston nimi:** `teht4-4.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht4-4.html`)

Alapalkin harmaan osan yläosio näyttäisi koostuvan sarakkeista.
Edellisessä tehtävässä lisäsimme melkein kaikkien näiden sarakkeiden ympärille `div`-elementit.
Poikkeuksen muodostavat ensimmäisen sarakkeen "asiakaspalvelu"- ja "yritysmyynti"-osiot.

Erotellaan vielä nämä kaksi omaan yhteiseen `div`-elementtiinsä, 
luomalla niiden ympärille uusi `div`-elementti.

Tämän tehtävän jälkeen pitäisi olla jälleen yksi uusi `div`-elementti, joka sisältää:

* asiakaspalvelu-osion
* yritysmyynti-osion

---

Tässä kohtaa sivun rakenteen pitäisi olla pitkälti valmista. 
Ainakin yksinkertaisessa muodossaan.
On siis aika lähteä tyylittämään sivua.
Emme vielä tee sivusta lopullisen näköistä, 
vaan tyydymme vain katsomaan, 
että sivu muotoutuu valunnaltaan, tai virtaukseltaan (engl. flow), oikean kaltaiseksi.

### tehtävä: 5 | rivit ja sarakkeet

*tehtävän kuvaus tarkentuu myöhemmin.*

**palautettavan tiedoston nimi:** 

* `teht5.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht5.html`)
* `style5.css` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/style5.css`)

Otetaan css käyttöön.

Tässä tehtävässä on tarkoitus käyttää valmiiksi laadittuja css-sääntöjä html-tiedostosta käsin.

Tarkemmin sanottuna, harjoittelemme `flexbox`-css-sääntöjen käyttöä ilman, että kirjoitamme itse css-sääntöjä.

`flexbox`:in yksi keskeinen ominaisuus on, että se antaa määrittää elementin lasten järjestykseksi joko rivi-suuntaisen järjestyksen, tai sarake-suuntaisen järjestyksen.

Tehtävänäsi on annettuja sääntöjä käyttämällä määrittää järjestyvätkö elementit riveittäin vain sarakkeittain. 

Alla olevassa ohjeita-osiossa on määritelty yksinkertainen css-sisältö, jonka tulet kopioimaan omaan tiedostoonsa.

#### Tehtävänanto

* kopioi edellisen html-tiedoston sisältö uuteen html-tiedostoon,
* lisää `body`-elementtiin ja jokaiseen sen alla olevaan html-elementtiin (siis `div`-elementteihin) `class`-attribuutti
  * `class`-attribuutin arvo, eli siis luokka, tulisi olla joko `rivi` tai `sarake` 

#### Ohjeita

Css:n käyttöönotto tapahtuu lisäämällä html-tiedoston `head`-elementin sisälle seuraavanlainen `link`-elementti.

Huomaa, että `href`-attribuutin arvo vastaa css-tiedostonimeä, jonka seuraavaksi luomme. 

```html
<head>
  <link href="style5.css" rel="stylesheet" />
</head>
```

Seuraavaksi luodaan css-tiedosto, nimellä `style5.css`.

Emme vielä aloita kirjoittamaan omia css-sääntöjä. 
Voit vain kopioida alla olevan css-tiedoston sisällön omaan `style5.css`-tiedostoosi.

```css
.rivi {
    display: flex;
    flex-direction: row;
    background-color: violet;
    border: solid 1px black;
    padding: 7px;
}

.sarake {
    display: flex;
    flex-direction: column;
    background-color: green;
    border: solid 1px black; 
    padding: 7px;
}
```

### Välihuomautus: rakenne alkaa muotoutumaan

Edellisen tehtävän jälkeen sivun pitäisi alkaa jo vähän näyttämään oikeanlaista rakenteidensa asettelun puolesta.

Kuitenkin tähän mennessä sivulla on käytetty vain `div`-elementtejä.

Moderniin html-sivujen luontiin kuuluu ajatus, että sivujen rakenteen pitäisi olla semanttinen.
Semanttinen tarkoittaa merkityksen sisältävää.
Siis elementtiä, joka itsessään kertoo kyseisen elementin käyttötarkoituksesta jotain.
Tämä tarkoittaa, että sivujen elementtien pitäisi itsessään kertoa lukijalleen mahdollisimman paljon.

Eli siis, ei käytetäkään pelkkiä `div`-elementtejä, vaan mitä moninaisimpia,
ja parhaiten tilanteeseen sopivia html-elementtejä.
Html tarjoaa runsaasti erilaisia semanttisia elementtejä, jotka kertovat jotain sisällöstään.
Näitä ovat mm. otsikot, linkit, napit, kappaleet, listat, otsakkeet ja alaotsakkeet, osiot ja koodiblokit.
Ne kaikki kertovat jotain siitä, minkälaista sisältöä ne pitävät sisällään.

Tämän huomioiden, `div`-elementti on loistava apuväline sivua luotaessa - kun ei vielä tarkkaan tiedetä, mitä elementtiä tulisi käyttää, 
voidaan aina käyttää aluksi `div`-elementtiä, ja myöhemmin vaihtaa se kuvaavammaksi.

Hyötynä tästä kuvaavampien elementtien käytöstä on myös, että selaimet osaavat paremmin hyödyntää tätä semanttista tietoa sivun rakenteesta,
tarjoten käyttäjälle paremmin sopeutettua toiminnallisuutta.

### tehtävä 6 | otsikot

**palautettavan tiedoston nimi:** `teht6.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht6.html`)

Tee sivun otsikko-teksteistä, jotka nyt ovat `div`-elementtejä, otsikoita.
Tämä onnistuu muuttamalla `div`-elementti otsikkoelementiksi.

Otsikkoelementit olivat:

* `h1`
* `h2`
* `h3`
* `h4`
* `h5`
* `h6`

Huomaa otsikoihin liittyvät säännöt: 

* sivulla tulisi olla vain yksi `h1`-elementti. 
* otsikkotasojen välillä ei tulisi tapahtua hyppyjä, eli
  * `h1` jälkeen tulisi tulla `h2`-elementtejä, ja `h2`-elementtien jälkeen `h3`,
  * `h5`-elementtiä ei siis voi olla sivulla, jollei sen vanhemmassa (esim. `div`-elementissä) ole aiemmin ollut `h4`-elementtiä. 

Yleensä `h1`-elementti löytyy aivan sivun alusta.

### tehtävä 7 | listat

**palautettavan tiedoston nimi:** `teht7.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht7.html`)

Sivulla on useita listoja. Nyt tarkoituksenasi olisi muuttaa sivulta löytämäsi listaukset html-listoiksi.

Tämä tapahtuu:

* vaihtamalla listattujen elementtien välittömänä vanhempanana toimiva elementti `div`-elementistä `ul`-elementiksi.
* vaihtamalla listattujen elementtien omat elementit `div`-elementistä `li`-elementiksi.

Tunnistat listan siitä, että toisiaan sijainniltaan lähekkäiset, peräkkäiset elementit tai tekstit, sisältävät samankaltaisia asioita.
Niitä siis listataan toistensa perään.

Huomaa, että listan ei tarvitse olla sivulla rivissä.
Rivitys on esitystekninen asia, joka voidaan toteuttaa css:n puolella.
Lista taas on sivun rakenteen ominaisuus, joka määritetään html:n puolella.

Sivulta löytyy listoja sekä ylä- että alapalkista.
Mm. seuraavien otsikkojen alta löytyy listoja: "info", "shop-in-shops", "artikkelit ja blogi" ja "sertifikaatit ja palkinnot".

Huomaa, että listoja saattaa olla sivulla myös muualla, lyhyempinä ja pidempinä listoina. 
Jos jotain listataan, kyse on todennäköisesti listasta.

### tehtävä 8 | linkit

Tässä tehtävässä lisätään sivulle linkkejä [`a`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)-elementin avulla.

**palautettavan tiedoston nimi:** `teht8.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht8.html`)

Monessa niistä paikoista, joihin haluamme linkin lisätä, käyttäen `a`-elementtiä, 
meillä on jo entuudestaan olemassa `div`-elementti.

```html
<div>Tietosuojaseloste</div>
```

Tällaisissa tapauksissa voimme helposti vaihtaa `div`-elementin nimen tilalle `a`-elementin nimen.
Lisäksi meidän tulee lisätä elementille `href`-attribuutti.
Arvoksi `href`-attribuutille voimme antaa `#`-tekstin.

```html
<a href="#">Tietosuojaseloste</a>
```

Huomaa, että jos olet vaihtanut `div`-elementin jo listan kohteeksi, eli `li`-elementiksi,
et voikaan enää vaihtaa `li`-elementtiä linkiksi, vaan sinun tulee luoda `li`-elementin lapseksi uusi `a`-elementti,
joka pitää sisällään tekstin.

Eli, seuraava:

```html
<ul>
  <li>jimm's oppaat</li>
  ...
</ul>
```

muuttuu muotoon

```html
<ul>
  <li>
    <a href="#">jimm's oppaat</a>
  </li>
  ...
</ul>
```

Voit laittaa linkin osoitteeksi nykyisen sivun osoitteen `#`. 
`#` on relatiivinen osoite, joka osoittaa nykyisen sivun alkuun.
Klikkaamalla tällaista linkkiä, käyttäjä siirtyy sivun alkuun - monissa selaimissa vieläpä ilman sivunlatausta.

Linkkejä on css:stä tutun tunnisteiden valitsinsyntaksin avulla mahdollista määrittää kohdistumaan sivun sisältä löytyvien elementtien `id`-attribuutteihin.
Tällöin esimerkiksi linkki, jonka osoite olisi `#tunniste`, kertoisi selaimelle, 
että sitä painamalla tulisi näyttää nykyisen sivun elementti, jonka `id`-attribuutin arvo on "tunniste".
Linkin osoitteen arvona `#` tarkoittaa, että näytetään linkkiä painamalla nykyiseltä sivulta nimeämätön tunniste,
eli siis käytännössä sivun alku.

### tehtävä 9 | napit

**palautettavan tiedoston nimi:** `teht9.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht9.html`)

Lisätään sivulle nappeja, siis `button`-elementtejä.

Button näyttää seuraavalta:

```html
<button>napin teksti</button>
```

Näitä löytyy sivulta ainakin kaksi, mahdollisesti oman tulkintasi mukaan kenties enemmänkin:

* ostoskori
* tilaa uutiskirje

#### Huomioita napeista

##### Napin ja linkin ero

Linkkiä käytetään silloin, kun tarkoituksena on selvästi siirtyä toiselle sivulle.
Tällöin ideana on, että linkki tekee saman asian, minkä käyttäjä pystyisi tekemään vaihtamalla linkin osoitteen itse selaimen osoitekenttään.

Nappia taas käytetään, kun on tarkoitus tehdä nykyisellä sivulla jonkinlainen toiminto.
Voidaan esimerkiksi avata sivun päälle aukeava popup, kuten mahdollisesti ostoskorin yhteydessä tehdään.
Vaihtoehtoisesti napilla voidaan myös tehdä linkin kaltainen siirtymä, 
silloin kun siirtymän yhteydessä halutaan myös lähettää jonkinlaista tietoa seuraavalle sivulle.

Käytännössä linkin osoitteen olisi aina hyvä olla muodossa, jossa käyttäjä voi halutessaan tehdä osoitteesta suoraan kirjanmerkin.

##### Napin `type="button"`-attribuutti tekee siitä javascriptin ohjaaman

Kun käytetään nappeja, modernissa html:ssä, on tärkeää lisätä `button`-elementille attribuutti `type="button"`.
Alkujaan `button`-elementtejä on käytetty osana lomakkeiden lähettämistä.
Tästä johtuen, taaksepäin yhteensopivuuden säilyttämiseksi, `button`-napin painaminen tuottaa oletuksena `post`-kutsun,
johtaen sivun vaihtoon.
Kun lisäämme `button`-elementtiin `type="button"`-attribuutin, se ilmaisee, 
että nappi on tarkoitettu käytettäväksi osana sivun javascript-toiminnallisuutta, 
eikä sen siten tarvitse tuottaa sivun lähetystä.
Tämä toimii, vaikka emme vielä käytäkään sivulla javascriptiä.
Nappi ei siis näin ollen vain tee mitään.

Tällöin nappi `type`-attribuutilla näyttää seuraavalta:

```html
<button type="button">napin teksti</button>
```

### haastava tehtävä - ylen etusivu

**palautettavan tiedoston nimi:** `teht<x>-sivu-2.html` (kansiossa: `harjoitukset/01-html-ja-css/02-html-rakenne-jatko/teht<x>-sivu-2.html`)

Jos olet ennättänyt tehdä kaikki tehtävät, voit haastavampana tehtävänä tehdä tällä sivulla tehdyt tehtävät seuraavan sivun osalta.

Haastavampana tehtävänä toteutetaan itsenäisesti ylen etusivun toteutus.

Referenssikuvan toteutettavasta ylen etusivun osasta löydät tämän sivun alusta.

Toteuta siis jimmsin sivun rakentamisessa käytettyjä samoja vaiheita läpikäyden ylen etusivun raakaversio, soveltaen itsenäisesti ohjeita tähän uuteen sivuun.

Nimeä uudet tiedostot aiempien tehtävänantojen mukaisesti, mutta lisää tiedoston nimen loppuun "-sivu-2"-pääte.

Huomaa, että ylen etusivulla on joitain rakenteita, jotka eivät olekaan täysin samanlaisia jimmsin sivun kanssa. 
Voit joutua näiden osalta miettimään minkälaisia laatikoita määrität minkäkin sivun elementtien ympärille.
Erityisesti uutisotsikoiden ja niiden ilmestymisaikojen kanssa kannattaa kiinnittää huomiota tähän.
