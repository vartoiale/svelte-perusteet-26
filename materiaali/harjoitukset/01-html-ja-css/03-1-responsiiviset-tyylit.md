# 03.1 responsiiviset tyylit

## Tehtävät

### Tehtävien palautus

Tee uusi kansio: `03-1-responsiiviset-tyylit` (`/harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit`).

Luo taas jokaista tehtävää varten uudet html- ja css-tiedostot.

Nimeä tiedostot muotoon:

* `tehtXX.html`,
* `tehtXX.css`,

missä `XX` on tehtävän numero.

### Tehtävä 0 - `viewport`-metatunniste

**palautettavan tiedostojen nimet:** 

* `teht0.html` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht0.html`) 
* `teht0.css` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht0.css`)

Jotta responsiiviset tyylit toimivat mm. mobiililaitteilla,
html-dokumentin `head`-elementtiin pitää lisätä seuraava rivi:

```html
<meta name="viewport" content="width=device-width,initial-scale=1" />
```

`head`-elementin pitäisi näyttää jotakuinkin seuraavalta:

```html
<head>
  <!-- 
   Tässä välissä olisivat muut elementit head-elementin sisällä, kuten esimerkiksi tyylitiedoston linkittävä link-elementti. 
   -->
  <meta name="viewport" content="width=device-width,initial-scale=1" />
</head>
```

Lisää aiheesta: [MDN:n dokumentaatio](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Responsive_Design#the_viewport_meta_tag)

### Tehtävä 1 - css-muuttujat

* `teht01.html` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht01.html`) 
* `teht01.css` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht01.css`)

Tässä tehtävässä vaihdetaan aiemmin tehtyjä css-sääntöjä käyttämään [css-muuttujia](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) (englanniksi "css custom properties") osana niiden määrittelyä.

Katsomme ensin miten css-muuttujat toimivat, ja sen jälkeen lähdemme käyttämään niitä.

#### teoriaa: css-muuttujat yleisesti

Css-sääntöjen käyttämiä arvoja, siis säännön oikeaa puolta, on mahdollista tallettaa muuttujiin,
ja näitä muuttujia on mahdollista käyttää elementtien tyylittämiseen.

Syntaktiltaan muuttujan määrittäminen tapahtuu seuraavasti:

```css
valitsin {
  <muuttujan nimi>: <muuttujan arvo>
}
```

Muuttujan nimi alkaa aina kahdella viivalla `--`, ja on muotoa `--muuttujan-nimi`.

Käytännössä se voisi siis tapahtua vaikka seuraavasti:

```css
body {
  --väri-teksti: #fff; 
}
```

Tämän jälkeen sitä käytetään normaalisti css-säännön sisällä. 
Tällöin viittaus muuttujaan tapahtuu funktion kutsua viittaavalla syntaksilla `var(--muuttujan-nimi)`.

Edellisen `--väri-teksti`-muuttujan käyttö tapahtuisi siis seuraavasti, 
kun halutaan määrittää luokalle ".joku-luokka" tekstin väri:

```css
.joku-luokka {
  color: var(--väri-teksti);
}
```

Huomattavaa: css-muuttuja näkyy aina siinä elementissä, 
jossa se on määritelty, sekä sen lapsi-elementeissä.
Edellisissä esimerkeissä määritimme css-muuttujan `body`-elementissä,
jolloin se on näkyvissä kaikkialla sivulla.

Toinen yleinen tapa määrittää globaaleja css-muuttujia 
on käyttää [`:root`](https://developer.mozilla.org/en-US/docs/Web/CSS/:root)-pseudoluokkavalitsinta määrittelyssä:

```css
:root {
  --väri-teksti: #0f0;
}
```

#### Tehtävänanto

Käytä css-muuttujia komponenttien tyylien määrittämisessä.

Yleinen tapa on määrittää seuraavia arvoja ylätasolla (`:root`):

* värit (teksti, tausta, korostus, apu, yms)
* fontit (leipäteksti, otsikko) ja niiden eri arvot (koko, paksuus, yms)
* tyhjä tila (1x, 2x, 3x, 4x)
* reunus (koko, väri)

Tyypillisesti näiden nimeämisessä käytetään muotoa `--<kategoria>-<sääntö>`, 
esimerkiksi `--fontti-leipäteksti`.

Voit määrittää esimerkiksi seuraavat css-muuttujat ylätasolla:

* `--fontti-perhe-leipäteksti`
* `--fontti-perhe-otsikko`
* `--fontti-koko-leipäteksti`
* `--fontti-koko-otsikko`
* `--väri-musta`
* `--väri-valkoinen`
* `--väri-ensisijainen`
* `--väri-toissijainen`
* `--väri-tausta`
* `--väri-teksti-yläpalkki`
* `--väri-teksti-alapalkki`
* `--väri-teksti-sisältö`
* `--väri-reunus
* `--väli-x1`
* `--väli-x2`
* `--väli-x3`
* `--väli-x4`

Huomaa, että voit käyttää css-muuttujien määrittelyssä arvona toisen css-muuttujan arvoa.
Näin tehdään yleensä värien osalta. 
Ensin nimetään väri, 
jonka jälkeen tietylle käytettävälle värille (esim. `---väri-teksti-yläpalkki`) annetaan aiempi väri arvoksi.

Esimerkiksi:

```css
:root {
  --väri-ensisijainen: #00f;
  --väri-teksti-yläpalkki: var(--väri-ensisijainen);
}
```

Tämän jälkeen, käytä näitä css-muuttujia eri sääntöjen sisällä.

### Tehtävä 2 - `margin: 0 auto;`

* `teht02.html` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht02.html`) 
* `teht02.css` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht02.css`)

Tässä tehtävässä muokataan sivua siten, 
että sivun reunoilla olevat tyhjät tilat määräytyvät automaattisesti sivun leveyden mukaan.

Tämä onnistuu käyttäen `margin`-säännön `auto`-arvoa, sekä määrittämällä sivun sisällölle kiinteä leveys.

#### Teoriaa: `auto`-arvo

`margin`-säännölle on mahdollista asettaa arvoksi `auto`.
Tällöin selain valitsee margin:in arvoksi sopivan todellisen arvon.
Apuna se käyttää muita tietoja siitä, kuinka paljon muut elementit vievät tilaa.

Tyypillinen käyttötapaus on keskittää elementti tämän säännön avulla.

Se onnistuu kahden vaiheen avulla:

* määritetään elementille itselleen kiinteä leveys
* asetetaan elementin molemmille horisontaalisille reunoille marginin arvoksi `auto`.

Tällöin, jos tässä tilassa on kaikkien muiden elementtien leveys selvillä, 
jakaa selain molemmille sivuille yhtä paljon tyhjää tilaa.

Yleensä tätä sääntöä käytetään uloimmalla mahdollisella elementillä, 
joka ei varaa käyttöönsä koko elementin leveyttä.

Esimerkiksi, jos meillä on sininen keskitetty neliö:

```html
<html>
<body>
  <div class="sininen-keskitetty-elementti"></div>
</body>
</html>
```

Tällöin määritämme tyylit:

```css
.sininen-keskitetty-elementti {
  margin: 0 auto;
  width: 200px;

  /* tehdään lisäksi elementistä neliö, ja sininen */
  height: 200px;
  background-color: blue;
}
```

Vähän vaikeammaksi tilanne menee, jos, kuten referenssisivun tilanteessa, 
haluammekin määrittää taustavärillä määritetylle elementille keskityksen taustavärin sisällä.

Ongelmana on, että `auto`-arvo ei ole käytössä `padding`-säännölle. 
Emme siis voikaan käyttää sääntöä sille elementille, jolle asetamme taustavärin,
vaan joudummekin mahdollisesti luomaan elementin sisällölle uuden keskitetyn elementin.

Tällöin html voisi olla seuraava:

```html
<html>
<body>
  <header class="taustavärillinen-yläpalkki">
    <div class="uusi-yläpalkin-keskitetty-sisältö-elementti">
	  sisältö
	</div>
  </header>
</body>
</html>
```

Tällöin määritämme tyylit:

```css
.taustavärillinen-yläpalkki {
  background-color: black;
  color: white;
}

.uusi-yläpalkin-keskitetty-sisältö-elementti {
  margin: 0 auto;
  width: 1024px; /* kiinteä leveys, joka keskitetään */
}
```

Periaatteessa saman keskityksen saa aikaiseksi myös käyttäen flexboxin `justify-content: center`-sääntöä
ja kiinteätä leveyttä.
Voit käytännössä valita näistä tekniikoista kumman tahansa. 
Myöhemmin katsomme, miten voimme vaihtaa tätä kiinteää leveyttä tarjoiltaessa sivua eri kokoisille näytöille.

Lopuksi mainittakoon vielä mielenkiintoisena [teknisenä yksityiskohtana](https://stackoverflow.com/questions/44244549/whats-the-difference-between-marginauto-and-justify-content-align-items-cent/44244743#44244743), 
että `margin: auto` varaa tilan ennen flexboxin laskemaa tilan varausta.

### Tehtävä 3 - `@media`-sääntö

* `teht03.html` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht03.html`) 
* `teht03.css` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht03.css`)

Responsiivisten sivujen teossa tärkeimpiä css:n tarjoamia työkaluja on [`@media`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)-sääntö.

Tässä tehtävässä lähdemme tekemään sivusta responsiivista.
Muokkaamme aiemmin luotuja komponentteja, 
ja asetamme `@media`-säännön avulla erilaisia kohtia,
joissa sivun tyylit vaihtuvat toisenlaisiksi.

Tätä varten käytämme apuna selaimien kehittäjätyökaluista löytyvää responsiivista tilaa,
joka antaa kehittäjän kokeilla työpöydän koosta riippumattomasti erilaisia sivun resoluutioita.

#### Selaimen responsiivinen kehitystila

Responsiivisesta kehitystilasta voit lukea esimerkiksi firefoxin [responsiivisen tilan dokumentaatiosta](https://firefox-source-docs.mozilla.org/devtools-user/responsive_design_mode/).
Ominaisuus toimii suurin piirtein samoin kaikissa selaimissa,
ja löytyy enemmän tai vähemmän samasta paikasta.

Responsiivinen tila käynnistyy yleensä kehittäjätyökalujen vasemmasta yläreunasta löytyvästä pienestä napista jossa on yhden tai useamman laitteen kuva.

#### Teoriaa: `@media`-sääntö

`@media`-sääntö lisätään css-tiedostoon normaalin css:n ympärille.

Yleensä haluamme määrittää tietylle elementille normaalit tyylit, 
sekä yhtä tai useampaa resoluutiota varten erityiset tyylit.

Oletetaan, että haluamme näyttää linkin sosiaalisen median sivustolle.
Työpöydällä, kun tilaa on paljon, haluamme käyttää sivustosta sen kuvaketta, ja kuvakkeen vieressä koko nimeä,
mutta mobiilissa haluamme näyttää vain sivuston kuvakkeen.

Emme tätä varten tarvitse javascriptiä, vaikka dynaamisesti sivulla näkyvää sisältöä muokkaammekin.
Riittää, että vain piilotamme `@media`-sääntöjen avulla kapeammilla resoluutioilla sivuston nimen.

Tässä tilanteessa haluamme ensin määrittää sivun tyylit työpöytäkoossa, 
ja sen jälkeen mobiililaitteille. 
Monesti tänä päivänä tyylit kuitenkin määritetään päinvastaisesti ensin mobiililaitteille,
ja vasta sen jälkeen mobiililaitteista poikkeaville resoluutioille.

Html voisi tällöin olla seuraava:

```html
<div class="some">
  <img class="some__kuvake" src="twitter.png" />
  <div class="some__nimi">Twitter</div>
</div>
```

Css olisi vastaavasti:

```css
/* elementin normaalit tyylit: perustyylit ja tyylit isolla näytöllä */
.some {
  display: flex;
  flex-direction: row;
}

.some__kuvake {
  width: 20px;
  height: 20px;
}

.some__nimi {
  font-size: 20px;
}

/* elementin responsiiviset tyylit keskikokoisille näytöille */
@media (max-width: 800px) {
  .some__nimi {
    font-size: 18px; /* vähän pienempi fontti */
  }
}

/* elementin responsiiviset tyylit pienille ruuduille */
@media (max-width: 600px) {
  .some__nimi {
    display: none; /* poistetaan teksti kokonaan näkyvistä */
  }
}
```

Tyypillisesti säännöstä käytetään muotoja:

* `@media (max-width: <leveys>) {}` - voimassa kun ruudun leveys on enintään `<leveys>`-mitan verran.
* `@media (min-width: <leveys>) {}` - voimassa kun ruudun leveys on vähintään `<leveys>`-mitan verran.

Kuten edellisessä elementissä, jos useampi `@media`-sääntö pätee elementtiin,
silloin kaikkia niitä sovellettaan elementtiin.

Voit lukea tarkemmin `@media`-säännölle annettavista arvoista mdn:n sivuilta.

#### Tehtävänanto

Lisää responsiiviset tyylit käyttäen `@media`-sääntöä. 
Käytä apuna referenssisivua, ja tarkkaile miten sen eri osat käyttäytyvät,
kun sivun leveys kasvaa tai pienenee.

Todennäköistä on, että joudut kohdistamaan sääntöjä useisiin eri elementteihin.

### Tehtävä 4 - `rem`-yksikkö

* `teht04.html` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht04.html`) 
* `teht04.css` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht04.css`)

Tässä tehtävässä siirrymme käyttämään pikselien sijaan `rem`-leveysyksikköä.

`rem`-yksiköstä voit lukea lisää mdn:n [leveysyksikköjen](https://developer.mozilla.org/en-US/docs/Web/CSS/length) dokumentaatiosta.

#### Teoriaa: `rem`-yksikkö

`rem`-yksikkönä on responsiivisen tyylittelyn kannalta oivallisempi yksikkö.

Siinä missä yksi pikseli vastaa yhtä ruudulla näkyvää pikseliä,
yksi `rem`-yksikkö vastaa juurielementissä määritetyn `font-size`-säännön arvoa.

Jos esimerkiksi haluamme asettaa rem-yksikön kooksi 20 pikseliä, asetamme juurielementin fontin kooksi 20 pikseliä:

```css
:root {
  font-size: 20px;
}
```

Responsiivisessa tyylittelyssä tästä tulee hyödyllistä, 
jos haluammekin pienentää kaikkea kokoa pienemmille laitteille.

Tällöin voimme vain asettaa `@media`-säännön avulla toisen arvon juurielementille:

```css
@media (max-width: 500px) {
  :root {
    font-size: 10px;
  }
}
```

Tällöin kaikki `rem`-yksiköitä käyttävät tyylit vaihtuvat automaattisesti pienemmiksi,
suhteessa leipätekstin fontin kokoon. 
Mahdollisesti olemme tällöin voineet johtaa myös muiden fonttien koot käyttäen `rem`-yksiköitä,
ja nekin vaihtuvat samalla.

#### Tehtävänanto

Määritä sivun body-elementille tietty fontinkoko. 

Tämän jälkeen, vaihda kaikki aiemmin käyttämäsi pikseliä yksikkönään käyttävät arvot käyttämään `rem`-arvoja.

Huomioi, että et luultavasti suoraan voi vaihtaa `px`-yksikköä `rem`-yksikköön, 
vaan joudut myös vaihtamaan itse arvoa, jotta ruudulla näkyvät koot eivät muutu.

Tämä on helpompaa, jos olet vaihtanut suurimman osan numeroarvoista käyttämään css-muuttujia.
Tällöin pystyt helposti vaihtamaan yksiköt vain muuttujissa, 
ja laskemaan niille helposti tarvittavat muutetut arvot.

### Tehtävä 5 - `calc`-css-funktio

* `teht05.html` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht05.html`) 
* `teht05.css` (kansiossa: `harjoitukset/01-html-ja-css/03-1-responsiiviset-tyylit/teht05.css`)

Tässä tehtävässä käytetään [calc](https://developer.mozilla.org/en-US/docs/Web/CSS/calc) -css-funktiota.

Tämä tehtävä on jatkoa css-muuttuja -tehtävälle (teht 29).

Toisinaan, pelkkä yhden muuttujan käyttö ei riitäkään, 
vaan muuttujien arvoja pitää laskea yhteen toisten muuttujien arvojen kanssa, tai muiden arvojen kanssa.

Yksinkertaisiin matemaattisiin laskuihin voi css:n puolella käyttää `calc`-css-funktiota.

Yksinkertaisuudessaan sen sulkujen sisään laitetaan matemaattinen operaatio arvoineen. 

Esimerkiksi yhteenlasku tapahtuu seuraavasti:

```css
.elementti {
  margin-left: calc(1px + 1px); /* vastaa sääntöä: `margin-left: 2px;` */
}
```

Tyypillinen tapaus `calc`-funktion käytölle on kun muuttujan pituudesta pitääkin lisätä tai poistaa toisen elementin padding:in leveys.

Tällainen saattaisi näyttää seuraavalta:

```css
:root {
  --leveys-sivu: 100%;
  --väli-1x: 7px;
}
.elementti {
  width: calc(var(--leveys-sivu) - var(--väli-1x));
}
```

Huomaa, että edellistä sääntöä ei voi luoda ilman `calc`-css-funktiota, 
koska siinä vähennetään kahden eri yksikön (prosentit ja pikselit) arvoja toisistaan.

#### Tehtävänanto

Kokeile käyttää `calc`-css-funktiota jossain sivulla.
