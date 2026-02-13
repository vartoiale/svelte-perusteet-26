# Osa 1. Html ja css

Aloitamme ohjelmoinnin perusteet kertaamalla aiemmin käsiteltyä.

Orientoivalla jaksolla ehdittiin lyhyesti käsitellä html:n ja css:n perusteita. Kertaamme näitä alusta asti tämän jakson yhteydessä.

## Html:n perusteet

### Lyhyesti html:stä ohjelmointikielenä

Html on niin sanottu deklaratiivinen ohjelmointikieli. 
Se tarkoittaa, että html:llä määritellään miltä selaimessa avattavan sivun tulisi näyttää, 
ja selaimen tehtäväksi jää piirtää näytölle tätä kuvausta vastaava näkymä.

Eli selaimelle siis kerrotaan, että ensin olisi vaikka otsikko, sitten kuva, ja sitten tekstiä, ja sen jälkeen vielä vähän lisää tekstiä.
Tämän jälkeen selain huolehtii, html:ssä määriteltyjen ohjeiden perusteella, miten teknisesti nämä annetut tekstit ja kuvat piirretään ruudulle.

Vaikka html:stä voi puhua ohjelmointikielenä, se ei ole kuitenkaan aivan niin voimakas ohjelmointikieli, kuin vaikka javascript.
Sillä ei voi suoraan tehdä ehtolauseita, eikä sillä voi määrittää toistorakenteita.
Tästä huolimatta, sillä voi määrittää monia asioita, ja on ihan paikallaan kutsua sitä ohjelmointikieleksi.

### Html-kielen syntaksista

Html on syntaksiltaan yksinkertainen. 
Syntaksi tarkoittaa niitä sääntöjä, joiden puitteissa määritellään, millaisia asioita voi laittaa html:ssä toistensa perään. 
Syntaksi on vähän niinkuin html-kielen kielioppi.

#### Yksinkertainen html-kielen esimerkki

Yksinkertainen html-kielen esimerkki voisi olla vaikka seuraavanlainen otsikko-elementin ja tekstin määrittävä koodinpätkä:

```html
<h1 id="sivun-otsikko">Tässä on kuvitteellisen sivun otsikko</h1>
```

Edellä oleva html-kielen esimerkki, sisältää yhden `h1`-elementin, jolle on määritetty `id`-attribuutti, ja teksti "Tässä on sivun otsikko". 
Se voisi olla jonkin html-sivun pääotsikko.

Käytännössä edellisessä esimerkissä näkyy html-kielen koko syntaksi:

* elementti - `<h1 id="sivun-otsikko">Tässä on kuvitteellisen sivun otsikko</h1>`,
* elementin nimi - `h1`,
* aloitustagi - `<h1 id="sivun-otsikko">`,
* lopetustagi - `</h1>`,
* elementin attribuutti - `id="sivun-otsikko"`,
* elementin attribuutin nimi - `id`,
* elementin attribuutin arvo - `sivun-otsikko`,
* elementin sisältö, eli elementin lapsi (tässä tekstiä) - `Tässä on kuvitteellisen sivun otsikko`

Siinäpä se sitten oikeastaan oli - koko html-kielen syntaksi. 
Vain elementtien nimet, attribuuttien nimet, arvot ja lukumäärät, sekä elementin lapset vaihtelevat.
Se mikä pysyy, on tämä edellä esitelty syntaksi.

#### Hieman monimutkaisempia html-kielen esimerkkejä

Otetaanpa toinen, vähän monimutkaisempi html-kielen esimerkki.
Se voisi esimerkiksi olla lista, jossa on kaksi kohtaa. Vaikka nimet ja arvot vaihtuvat, säilyy syntaksi samana:

```html
<ul class="lista">
  <li class="kohta">ensimmäinen kohta</li>
  <li class="kohta">toinen kohta</li>
</ul>
```

Samaan tapaan, tämäkin voidaan jaotella syntaksinsa puitteissa eri osiin:

* elementti - `<ul class="lista"><li class="kohta">ensimmäinen kohta</li><li class="kohta">toinen kohta</li></ul>`,
* elementin nimi - `ul`,
* aloitustagi - `<ul class="lista">`,
* lopetustagi - `</ul>`,
* elementin attribuutti - `class="lista"`,
* elementin attribuutin nimi - `class`,
* elementin attribuutin arvo - `lista`,
* elementin sisältö, eli elementin lapset (tässä toisia elementtejä) - `<li class="kohta">ensimmäinen kohta</li><li class="kohta">toinen kohta</li>`

Tästä esimerkistä voi nopeasti huomata kaksi isompaa eroavaisuutta edelliseen esimerkkiin nähden:

1. nimet ja arvot ovat eri,
2. elementin lapsena on tekstin sijaan muita elementtejä.

Näistä jälkimmäinen on ehkä suurempi muutos. 
Eli elementti voikin saada lapsikseen muita elementtejä. 
Tämän lisäksi lapsielementtejä voi olla yksi tai useampi.
Lisäksi näillä lapsi elementeillä voi itsellään olla omia lapsielementtejä.
Elementillä voikin olla lapsisukupolvia melkein loputtomiin. 
Tai ainakin niin paljon, kuin joku niitä jaksaa elementille kirjoittaa.

Käytännössä elementeillä onkin yleensä paljon lapsia.
Juuri tälle piirteelle rakentuukin html-kielen hyödyllisyys.
Sillä voidaan kuvata melko selvästi, verrattain monimutkaisia rakenteita.

Puhutaankin, että html-elementit muodostavat puun.
Siis samassa sanan merkityksessä kuin vaikka sukupuusta puhutaan puuna.
Sukupuussa tarvitaan aina kaksi vanhempaa, mutta lapsia voi olla nolla, yksi tai useampi.
Html-puu eroaa tästä hieman - elementillä voi aina olla vain yksi suora, oma vanhempi. 
Lapsia html-elementillä voi olla nolla, yksi tai useampi.

Alla on tyypillinen yksinkertainen esimerkki html-rakenteesta, 
jossa on elementti (`ul`), jolla on lapsielementti (`li`), jolla on lapsielementti (`p`), jolla on lapsena tekstiä.

```html
<ul>
  <li>
    <p>listan kohdan kappaleen teksti</p>
  </li>
</ul>
```

Eli siis yhden kohdan lista, jolla on sisällään lyhyen kappaleen verran tekstiä.

Lisättäköön vielä, että toisinaan kun puhutaan "html-puusta", saatetaan käyttää termiä "html-dokumentti". 
Nämä ovat käytännössä sama asia.

#### Yleinen html-kielen syntaksi

Html:n syntaksi on siis aikasen helppo.

Kirjoitetaan se vielä kuitenkin uudelleen:

```html
<elementin-nimi ensimmäisen-attribuutin-nimi="attribuutin arvo" toisen-attribuutin-nimi="attribuutin arvo">
  {elementin sisältö}
</elementin-nimi>
```

Huomataan, että aloitus- ja lopetustagit muistuttavat toisiaan. 
Molemmissa on kulmasulkeet auki (`<`) ja kiinni (`>`), sekä elementin nimi.

Ne kuitenkin eroavat kahdella tavalla:

1. aloitustagissa voi olla yksi tai useampi attribuutti (mutta voi olla myös nolla kappaletta attribuutteja),
2. lopetustagissa on ennen elementin nimeä kauttaviiva (`/`)

Attribuutit ovat aina aloitustagissa. Niitä ei siis koskaan laiteta lopetustagiin.
Jos ne laitettaisiin lopetustagiin, selain ei osaisi lukea niitä sieltä.

Vastaavasti lopetustagi on aina muotoa (`</>`).
Tähän sääntöön on kuitenkin pieni poikkeus.

Jos elementillä ei ole lainkaan lapsia:

```html
<script><script>
```

voidaan se kirjoittaa niin kutsutun itsensäsulkevan tagin avulla:

```html
<script />
```

Nämä kaksi esimerkkiä tarkoittavat samaa asiaa. 
`script`-elementillä voidaan lisätä suoritettavaa koodia html-sivulle.
Sillä voidaan lisätä vaikka lyhyt javascript-koodinpätkä, joko tiedostosta, tai suoraan elementin lapseksi auki kirjoitettuna.

Kannattaa huomata, että edellä esitetyn kahden kauttaviivan sisältävän tagin, lopetustagi ja itsensäsulkeva tagi, osalta kauttaviivan sijainti eroaa toisistaan:

* `</script>` - lopetustagissä kauttaviiva on ennen elementin nimeä,
* `<script />` - itsensä sulkevassa tagissa kauttaviiva on elementin nimen (ja välilyönnin) jälkeen

Tyypillisenä esimerkkinä, kuvan määrittämiseen käytetty `img`-elementti ei sisällä laisinkaan lapsia, koska sen sisältö määritellään `src`-attribuutilla. 
Sen takia se yleensä kirjoitetaankin yleensä itsensäsulkevan tagin avulla:

```html
<img src="kuvan-sijainti.png" />
```

## Css:n perusteet

### Lyhyesti css:stä ohjelmointikielenä

Css on vähän html:ää voimakkaampi kieli. Se ei ole aivan yhtä voimakas kieli kuin tavalliset ohjelmointikielet, ainakaan perussääntöjensä puitteissa. 
Nykyisillä laajennoksillaan css tosin taitaa olla jo yhtä voimakas kuin mikä tahansa perinteisempi ohjelmointikieli, siis kuten esimerkiksi javascript.
Mutta tästä ohjelmointikielen voimakkuudesta meidän ei oikeastaan tarvitse välittää tämän opintojakson puitteissa.

Css:n pääasiallinen tarkoitus on määrittää, miltä html-dokumentin pohjalta luodun sivun pitäisi ulkoisesti näyttää.

Siis jos html-dokumentilla määritetään sivun rakenne, ja sisältö, niin css:llä määritellään sen visuaalinen ilme.
Sanotaan, että css:ää käytetään html-sivujen tyylittämiseen.

### Css:n syntaksista

Css on myös hyvin yksinkertainen syntaksiltaan.

#### Css:n syntaksista valitsimien ja sääntöjen tasolla

Lyhykäisyydessään css-kielen syntaksi koostuu valitsimista ja säännöistä. 

```css
valitsin {
  sääntö
}
```

Tämä tarkoittaa, että `valitsimeen` kohdistuu aaltosulkeiden sisälle merkitty `sääntö`.

On perin tyypillistä, että yhdellä valitsimella on useita sääntöjä.

```css
valitsin-1 {
  sääntö-1
  sääntö-2
}
```

Kuitenkin, myös valitsimia, voi olla yhdessä merkinnässä useita:

```css
valitsin-1, valitsin-2 {
  sääntö-1
  sääntö-2
}
```

Tämä tarkoittaa samaa kuin jos kirjoitettaisiin kaksi erillistä valitsinta, joilla olisi samat säännöt.

```css
valitsin-1 {
  sääntö-1
  sääntö-2
}

valitsin-2 {
  sääntö-1
  sääntö-2
}
```

#### Css:n syntaksista sääntöjen tasolla tarkemmin

Tarkemmin sanottuna, css-sääntö on hieman edellistä esimerkkiä monimutkaisempi.
Se koosstuu useammasta osasta: säännön nimestä ja säännön arvo(i)sta:

```css
  säännön-nimi: säännön arvo(t);
```

On huomioitavaa, että:

* säännön nimen ja arvon välissä erottimena toimii kaksoispiste (`:`)
* säännön päättää puolipiste (`;`)
* säännön nimen osat yhdistetään viivalla (`-`)
* säännön arvoja voi olla yksi tai useampi. Jos niitä on useampi, ne erotellaan toisistaan välilyönneilllä.

#### Css:n syntaksista valitsimen tasolla tarkemmin

Valitsimia siis voi olla useampi, jolloin niitä erotellaan toisistaan pilkuilla.

Kuitenkin, valitsin voi myös koostua useammasta osasta.
Tällöin käytetään muita merkkejä.

Näistä kohta lisää.

Tästä kuitenkin pääsemmekin siihen:

* mitä valitsimilla tehdään,
* mitä ne saavat arvoikseen, ja
* miten niitä käytetään.

Valitsimilla viitataan aina html-dokumentin elementteihin. 

Niillä siis valitaan html-puusta yksi tai useampi elementti.
Sen jälkeen tähän valitsimeen kohdistetaan sen yhteyteen liitetyt css-säännöt.

## Html:n ja css:n yhteistoiminta

Html ja css on tarkoitettu käytettäviksi yhdessä.

Ennen css:n luontia, html:n visuaalinen ilme määritettiin html:ssä. 
Lopputuloksena oli sekamelska, jossa html:stä monesti tuli kovin monimutkaista, koska sillä yritettiin saavuttaa kaksi asiaa samaan aikaan: määrittää sisältö ja ulkoasu.

Css:n hyöty onkin juuri siinä, että sen ansiosta html:ssä voi keskittyä pelkkään sisällön ja rakenteen määrittämiseen. 
Eikä siinä tarvitse, pääasiallisesti, miettiä sivun ulkoasua.
Aina tässä ei onnistuta, mutta suurelta osin silti onnistutaan.

Lisäksi, yhdellä html-dokumentilla voi periaatteessa olla useampi eri css-säännöstö.
Toisaalta, samaa css-säännöstöä voidaan käyttää useamman eri sivun tyylittämiseen.
Näin itse asiassa tapahtuu melkein joka sivustolla, kun saman sivuston eri sivuja, siis eri html-dokumentteja, tyylitellään saman css-tiedoston avulla.

### Miten html ja css toimivat yhteen?

Miten sitten html ja css toimivat yhteen?

Css-valitsimet voivat yksinkertaisimmallaan sanoa, että kaikkiin tietyn elementin ilmentymiin, käytetään tiettyjä sääntöjä:

```css
/* h1-otsikon kirjainten väri on musta (- ja tämä on siis kommentti) */
h1 {
  color: black;
}
```

Tällöin kaikkiin dokumentissa oleviin `h1`-elementteihin kohdistetaan edellä määritetty värjäyssääntö.

```html
<h1>Tämän otsikon teksti on mustaa</h1> 
```

Html-elementteihin on myös mahdollista lisätä erilaisia kiintopisteitä ja ankkureita css:ää varten.
Tyypillisimpiä näistä ovat `id`- ja `class`-attribuutit.

```css
/* tunniste merkitään css:n puolella `#`-etuliitteellä ennen tunnisteen nimeä */
#otsikko-tunniste {
  color: red;
}

/* luokka merkitään css:n puolella `.`-etuliitteellä ennen tunnisteen nimeä */
.kappale-luokka {
  color: blue;
}
```

Näiden avulla on mahdollista valita tunnisteella ja luokalla html:stä tiettyjä elementtejä. 
Siinä missä elementti-valitsimella valittiin tyylitettäväksi kaikki elementin ilmentymät,
voidaan tunnisteella ja luokalla valita vain tietyt, merkityt elementit.

```html
<h1 id="otsikko-tunniste">punainen otsikko</h1>
<h1>normaali, musta otsikko</h1>

<p class="kappale-luokka">sininen kappale</p>
<p>tavallinen, mustalla tekstillä oleva kappale</p>
<p class="kappale-luokka">toinenkin sininen kappale</p>
```

Huomattavaa on, että:

* yleensä sama `id`-tunniste annetaan yhdessä html-dokumentissa vain yhdelle elementille,
* sama `class`-luokka voidaan antaa useammallekin elementille

Tavallaan id-tunniste on siis tehokkaampi työkalu, 
koska sen pitäisi löytyä vain yhdeltä html-elementiltä koko html-dokumentista, 
ja sen pitäisi silloin varmuudella tyylittää vain yksi elementti.

Luokka taas on yleisempi käytetty css-valitsimena, koska monesti samoja tyylejä halutaan antaa useammallekin elementille.

Näitä on myös mahdollista yhdistellä:

* jos valitsimet kirjoitetaan yhteen (esimerkiksi `#tunniste.luokka`),
  tarkoitetaan molemmat valitsimet täyttävää elementttiä (siis elementtiä jolla on ""-id ja "luokka"-class),
* jos valitsimet erotetaan välilyönnillä (esimerkiksi `#tunniste .luokka`),
  tarkoitetaan lapsielementtiä, jolla on "luokka"-class, ja jonka vanhemmalla on "tunniste"-id.

