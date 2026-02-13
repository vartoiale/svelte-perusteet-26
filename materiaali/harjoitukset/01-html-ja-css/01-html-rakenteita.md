# Harjoitukset: Html-rakenteita

Tee tehtäviä varten repositorion juureen kansio `harjoitukset/01-html-ja-css`, jos sitä ei vielä ole olemassa.

Palauta yllä mainittuun kansioon kaikki tässä tiedostossa määritellyt tehtävät.

Näissä tehtävissä harjoitellaan vain html:n käyttöä.
Emme siis vielä käytä lainkaan css-tyylejä sivujen visuaalisen ilmeen muokkaamiseen.

## Ohjeita harjoitusten tekoon

### Tee tehtävät lokaalisti visual studio codessa

Tunnilla tästä repositoriosta tehtiin koneellesi paikallinen kopio.
Kaikki kurssin työt on tarkoitus tehdä tähän repositorioon.

Tee tehtävät omalla koneellasi käyttäen visual studio code -tekstieditoria (tai haluamaasi muuta tekstieditoria).
Tehtävät pitää tehdä lokaalisti, jotta voit testata tekemiäsi html-tiedostoja omassa selaimessasi.

Jos tekisit harjoitukset github.com-sivuston tekstieditorissa, et pystyisi testaamaan, miltä html-sivusi näyttävät selaimessa.

### Testaa tekemiäsi html-sivuja selaimessa

Voit kokeilla, että html-sivusi todella toimii, avaamalla html-tiedoston selaimessa.
Et tarvitse tähän palvelinta.
Selain osaa avata normaaleja html-sivuja suoraan windowsin tiedostojenhallinnan kautta, siis file explorer-työkalusta.

Tiedostoselaimessa klikkaa hiiren oikealla näppäimelllä html-tiedostoa, jonka haluat avata, 
ja valitse avautuvasta kontekstivalikosta "avaa sovelluksessa"-kohta. 
Valitse avaavaksi sovellukseksi haluamasi internet-selain, esimerkiksi Edge.
Sivun pitäisi näin avautua selaimeen.

### Muista commitoida muutokset github desktopilla

Kun olet tehnyt tehtävät, muistsa commitoida ne github desktopilla.

Ennen tehtävien tekemisen aloittamista on kuitenkin hyvä muistaa tehdä uusi branchi github desktopissa.
Voit nimetä branchin `feature-`-etuliitteellä, ja tekemiäsi muutoksia kuvaavalla lyhyellä loppuosalla.

## Tehtävät

### Tehtävä 1 - html-sivu tekstillä

**palautettavan tiedoston nimi:** `teht1.html` (kansiossa: `harjoitukset/01-html-ja-css/teht1.html`)

Luo yksinkertainen html-dokumentti, joka:

* sisältää tekstin "Tervehdys, hyvä maailma!",
* ei sisällä yhtään html-elementtiä.

### Tehtävä 2 - html-sivu `html`-elementillä

**palautettavan tiedoston nimi:** `teht2.html` (kansiossa: `harjoitukset/01-html-ja-css/teht2.html`)

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* sisältää tekstin "Tervehdys, hyvä maailma!",
* sisältää seuraavat html-elementit: `html`, `head`, `body`

### Tehtävä 3.1

**palautettavan tiedoston nimi:** `teht3.html` (kansiossa: `harjoitukset/01-html-ja-css/teht3.html`)

#### Ohjeistus

Otsikkoja pystyy tekemään `h1`-elementin avulla

`h1`-elementin sisällön, eli lapsen, tulee olla tekstiä.

#### Tehtävänanto

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* sisältää `h1`-otsikkoelementin
 * otsikko pitää sisällään tekstin "Tervehdys, hyvä maailma!"
* sisältää lisäksi seuraavat html-elementit: `html`, `head`, `body`

Otsikkoelementin kuuluu olla `body`-elementin sisällä.

### Tehtävä 3.1 - useita otsikoita

**palautettavan tiedoston nimi:** `teht3-1.html` (kansiossa: `harjoitukset/01-html-ja-css/teht3-1.html`)

#### Ohjeistus

Otsikkoja pystyy tekemään `h1`-elementin lisäksi myös seuraavilla elementeillä:

* `h2`
* `h3`
* `h4`
* `h5`
* `h6`

Myös näiden elementtien sisällön, eli lapsen, tulee olla tekstiä.

#### Tehtävänanto

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* sisältää 6 otsikkoa, jokainen toteutettu eri otsikkoelementin avulla (`h1`,`h2`,`h3`,`h4`,`h5`,`h6`):
 * jokainen otsikko sisältää tekstin "Tervehdys, hyvä maailma!"
* sisältää lisäksi seuraavat html-elementit: `html`, `head`, `body`

Otsikkoelementtien kuuluu taas olla `body`-elementin sisällä.

Huomaa, että otsikko elementit eivät saa olla toistensa lapsia, eli ne eivät saa olla toistensa sisällä. 
Niiden kuuluu kaikkien olla saman `body`-elementin lapsia, eli sisaruksia toisilleen.

Järjestä otsikot siten suurimmasta pienimpään.

### Tehtävä 4

**palautettavan tiedoston nimi:** `teht4.html` (kansiossa: `harjoitukset/01-html-ja-css/teht4.html`)

#### Ohjeistus

Listoja pystyy tekemään [`ul`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)-elementin avulla.
Listaelementin lapsielementtien tulee olla [`li`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/li)-elementtejä.

Vastaavasti `li`-elementillä voi olla lapsena tekstiä, tai mitä tahansa muita html-elementtejä.

#### Tehtävänanto

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* sisältää listan `<ul>`,
  * jossa on neljä listakohtaa (engl. list item) `<li>`
    * joissa lukee tekstinä yksi seuraavista: "ensimmäinen", "toinen", "kolmas", "neljäs"
* sisältää lisäksi seuraavat html-elementit: `html`, `head`, `body`

### Tehtävä 5 - kappale

**palautettavan tiedoston nimi:** `teht5.html` (kansiossa: `harjoitukset/01-html-ja-css/teht5.html`)

#### Ohjeistus

#### Tehtävänanto

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* sisältää listan `<ul>`,
  * jossa on neljä listakohtaa (engl. list item) `<li>`
    * joissa lukee tekstinä yksi seuraavista: "ensimmäinen", "toinen", "kolmas", "neljäs"
* sisältää lisäksi seuraavat html-elementit: `html`, `head`, `body`

### Tehtävä 6 - kappale

**palautettavan tiedoston nimi:** `teht6.html` (kansiossa: `harjoitukset/01-html-ja-css/teht6.html`)

#### Ohjeistus

Otsikoiden lisäksi html-sivuilla on yleensä tekstiä.
Kun haluamme lisätä tekstiä, käytämme yleensä [`p`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p)-elementtiä.
`p`-elementti saa nimensä englannin kielisestä sanasta "paragraph", joka tarkoittaa tekstin "kappaletta".

#### Tehtävänanto

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* sisältää kaksi peräkkäistä kappaletta `<p>`,
  * ensimmäisen kappaleen sisältö: "Tämä on ensimmäinen kappale." 
  * jälkimmäisen kappaleen sisältö: "Tämä on seuraava kappale." 
* sisältää lisäksi seuraavat html-elementit: `html`, `head`, `body`

### Tehtävä 7 - linkki

**palautettavan tiedoston nimi:** `teht7.html` (kansiossa: `harjoitukset/01-html-ja-css/teht7.html`)

#### Ohjeistus

Html-sivulta on mahdollista linkata toisille html-sivuille.
Tätä varten voidaan käyttää [`<a>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)-elementtiä.

Voit katsoa `a`-elementin syntaksin yllä olevasta mdn-sivun `a`-elementtiä käsittelevästä ohjeistuksesta.

#### Tehtävänanto

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* sisältää kappaleen `p`,
  * kappaleen sisältö: "Tässä kappaleessa on linkki, joka osoittaa github:in etusivulle."
  * tee kappaleen "linkki"-sanasta linkki `a`-elementin avulla, ja laita se osoittamaan github.com:in etusivulle: `https://github.com`.
* sisältää lisäksi seuraavat html-elementit: `html`, `head`, `body`

### Tehtävä 8 - koodielementti

**palautettavan tiedoston nimi:** `teht8.html` (kansiossa: `harjoitukset/01-html-ja-css/teht8.html`)

#### Ohjeistus

Jos halutaan merkitä html-sivulla esimerkkikoodia tekstin seassa,
kuten tällä sivulla on tehty erilaisten tiedoston- ja html-elementtien nimien osalta,
voidaan se tehdä [`code`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/code)-elementin avulla.

#### Tehtävänanto

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* sisältää kappaleen `p`-elementtiä käyttäen
  * kappaleen tekstinä on: "Tässä kappaleessa käytetty p-elementti on tehty käyttäen code-elementtiä."
  * tee tämän kappaleen `p`- ja `code`-sanoista koodielementin avulla koodielementin näköiset.
* sisältää lisäksi seuraavat html-elementit: `html`, `head`, `body`

### Tehtävä 9 - päivän lopputehtävä

**palautettavan tiedoston nimi:** `teht9.html` (kansiossa: `harjoitukset/01-html-ja-css/teht9.html`)

Tässä tehtävässä tarkoituksena on käyttää kaikkea tällä sivulla opittua.

Tehtävänäsi on tehdä tämän auki olevan `01-html-rakenteita.md`-sivun sisällöstä html-versio.

Tarvitset siis: 

* otsikoita,
* kappaleita,
* listoja,
* sisäkkäisiä listoja,
* linkkejä ja
* koodiesimerkkejä.

Sinun ei siis tarvitse toteuttaa github-sivun yleisiä piirteitä.
Tehtävänäsi on vain toteuttaa tämän tehtävänantosivun sisältö html-syntaksia käyttäen.

Sivulta tulee löytyä kaikki sama teksti mitä tältä sivulta löytyy tällä hetkellä.
Jos tätä tehtäväsivua päivitetään myöhemmin, muutoksia ei tarvitse lisätä tekemällesi sivulle. 

#### Tehtävänanto

Luo yksinkertainen, oikeaoppinen html-dokumentti, joka:

* näyttää tämän tiedoston html-versiolta
* sisältää lisäksi seuraavat html-elementit: `html`, `head`, `body`
