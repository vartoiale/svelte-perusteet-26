# css-sääntöjen määräytyvyydestä

Css-sääntöjen määräytyvyyden määrittävät mm. seuraavat asiat:

1. valitsimen tarkkuus (engl. specificity),
2. sääntöjen kirjoitusjärjestys (viimeinen jää voimaan),
3. periytymisjärjestys.

Sekä erikoistapaukset:

1. säännön määrityspaikka,
2. Käsin merkitty tarkkuuden ylikirjoitus-merkintä.

## Mistä on kyse css-sääntöjen määräytyvyydessä?

Kun määritämme samalle elementille samoja sääntöjä useammassa paikassa,
se mikä sääntö jää voimaan,
ei ole vain sattumaa,
vaan määräytyy tarkan prosessin avulla.

Tässä tekstissä kuvataan tuota mallia yleisimmissä käyttötapauksissa, mutta yksinkertaistetaan hieman asioiden helpottamiseksi. MDN:stä löytyy aiheesta kuitenkin tarkempi kuvaus [Introduction to CSS Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_cascade/Cascade)-dokumentista.

## Eli mikä määräytyvyys

Aloitetaan yksinkertaisella esimerkillä, 
jossa meillä on yksinkertainen html-dokumentti:

```html
<div>teksti</div>
```

Määritämme sille seuraavat tyylit:

```css
div {
    color: blue;
}

div {
    color: red;
}
```

Minkä värinen on teksti lopulta?

Oikea vastaus: punainen.

Minkä takia kahdesta vaihtoehdosta voimaan jää juuri sitten punainen tekstin väri?

### Viimeinen samalla tarkkuudella tehty määritys jää voimaan

Jos säännön valitsimet on määritetty samalla tarkkuudella,
viimeinen säännöistä jää voimaan.

Näin käy myös edellisessä esimerkissä:
ensin määritelty sininen väri ylikirjoitetaan 
sen jälkeen määritetyllä punaisella tekstin värillä.

Mutta miten sitten käy, 
jos sääntöjen valitsimet ovat erilaisia?

### Valitsimet määrittävät säännön määräytymisen tarkkuuden

Kun sääntöjen valitsimet ovat erilaiset,
sen mikä säännöistä jää voimaan,
määrittää yleensä säännön valitsin.

Valitsin ja sääntöhän näyttivät seuraavilta:

```css
<valitsin> {
    <sääntö>: <arvo>;
}
```

Eli esimerkiksi voisimme `div`-valitsimelle asettaa `color`-säännön arvoksi värin `#fff` seuraavasti:

```css
div {
    color: #fff;
}
```

Vastaavasti `teksti`-luokalle, voisimme määrittää värin,
asettamalla `color`-säännön arvoksi värin `red`:

```css
.teksti {
    color: red;
}
```

Jos nämä kaksi sääntöä kilpailisivat seuraavan html-dokumentin muodossa:

```css
<div class="teksti">tekstiä</div>
```

Olisi teksti tälläkin kertaa punainen. Mutta miksi?

Koska valitsinten tarkkuus on erilainen.

Tutkitaan siis seuraavaksi valitsimien tarkkuutta.

#### Valitsimien tarkkuudesta

Valitsinten tarkkuus määrittyy laskemalla niiden eri tarkkuuksisten osien tulokset yhteen valitsimen kokonaistarkkuudeksi.

Mennään kohta tarkemmin tähän yhteenlaskuun, mutta katsotaan ensin, mitkä nuo kolme erilaista tarkkuuden tasoa valitsimilla ovat.

Meillä on käytännössä kolmea tarkkuuden tasoa valitsimissa:

1. elementit (esim. `div`)
2. luokat (esim. `.luokka`)
3. tunnisteet (esim. `#tunniste`)

Nämä kaikki tarkkuudet voisivat löytyä esimerkiksi seuraavasta html-dokumentista:

```html
<div id="tunniste" class="luokka">teksti</div>
```

Tarkkuus määritetään kolmena lukuna:

```
specificity(0,0,0)
```

Tämän luvun voi lukea vasemmalta oikealle,
vähän kuin se olisi kolminumeroinen luku.
Mitä enemmän isoja numeroita on vasemmalla, 
sitä tarkemmasta valitsimesta on kyse.

Tarkkuudet menevät seuraavasti:

1. elementti - `specificity(0,0,1)`
2. luokka - `specificity(0,1,0)`
3. tunniste - `specificity(1,0,0)`

Tällöin isoin tarkkuus menee edelle.

Tunnisteella määritelty valitsin on siis lähtökohtaisesti isompi kuin luokalla määritetty valitsin, 
ja vastaavasti molemmat ovat isompia kuin pelkällä elementillä määritetyt valitsimet.

Mutta miten sitten käy, jos kahdella säännöllä onkin monimutkaisemmat valitsimet?

### Monimutkaisemmat valitsimet

Jos säännöllä onkin monimutkaisempi valitsin,
tämän valitsimen osien tarkkuudet lasketaan yhteen.

Esimerkiksi seuraavan:

```css
.teksti:hover {}
```

tarkkuus on: `specificity(0,2,0)`, koska `.teksti` ja `:hover` ovat molemmat luokka-tason valitsimia.

Yhdellä kaksoispisteellä merkityt css-valitsimet, kuten `:hover` ovat nimeltään pseudoluokkia, näin ollen ne tarkkuudeltaan vastaavat luokkia.

Vastaavasti kahdella kaksoispisteellä merkityt pseudoelementit, 
kuten `::after` ja `::before`, lasketaan elementeiksi.

Esimerkiksi valitsin:

```css
.linkki::after {}
```

on tarkkuudeltaan `specificity(0,1,1)`, koska `.linkki` on luokkatason valitsin, ja `::after` elementtitason valitsin.

Edelleen, jos määritämme valitsimen, 
joka kohdistuu `.lista`-luokan lapsena oleviin `.alkio`-luokkiin:

```css
.lista .alkio {}
```

on tämän valitsimen tarkkuus `specificity(0,2,0)`, 
koska molemmat sen osavalitsimet, 
`.lista` ja `.alkio`, 
ovat luokkatason valitsimia.

Se, että nämä osavalitsimet kohdistuvat eri elementteihin,
ei vaikuta valitsimen tarkkuuteen,
vaan niiden tarkkuudet vain lasketaan yhteen.

Voit tarkastaa yllä olevat esimerkit helposti käyttäen automaattisia työkaluja.

Tästä seuraavaksi.

#### Miten valitsimen tarkkuutta voi tarkastella?

Css-valitsimen tarkkuuden voi laskea käsin,
mutta sen laskemiseen voi käyttää myös valmiita työkaluja:

Valitsimen tarkkuutta voi tarkastella automaattisesti:

1. VSCodessa, viemällä hiiren kursori, css-tiedostossa, valitsimen päälle.
2. Selaimen kehitystyökalujen tyylivälilehdellä, viemällä hiiren kursori css-valitsimen päälle.

Voit tarkastella näillä työkaluilla tästä kansiosta löytyviä tiedostoja:

* [`index.html`](index.html),
* [`css-määräytyvyys-esimerkki.css`](css-määräytyvyys-esimerkki.css).

Katsotaan vielä lopuksi erikoistapauksia sääntöjen määräytymiseen:

## Määräytyvyyden erikoistapaukset

Lisänsä sääntöjen määräytyvyyteen tuovat erikoistapaukset:

1. elementin `style`-attribuuttiin asetetut säännöt
2. `!important`-merkintä
3. transitiot

### elementin `style`-attribuutin säännöt

Elementille on mahdollista asettaa tyylejä suoraan html:ssä,
`style`-attribuutin avulla:

```html
<div style="color:red;">teksti</div>
```

Vastaavasti, jos taas asetamme dokumentille css-tyylit:

```css
div {
    color: blue;
}
```

jää taas elementti punaiseksi.

Vähän yksinkertaistaen,
html-dokumentissa määritellyillä elementtien omilla tyyleillä (engl. inline styles) on aina korkeampi määräytyvyys,
kuin muilla tyylimäärityksillä.

### `!important`-merkintä

Jos säännön lopussa on merkintä `!important`,
sen voi, hieman yleistäen, ylikirjoittaa vain toisella `!important`-määreellä varustetulla säännöllä.

Esimerkiksi:

```css
div {
    color: blue !important;
}

div {
    color: red !important;
}

div {
    color: green;
}
```

värjäisi taas elementin punaiseksi, 
koska viimeinen `!important`-merkinnällä varustettu sääntö jäisi voimaan.

`!important` onkin hyödyllinen, 
kun pitää ylikirjoittaa elementin `style`-attribuutissa määritettyjä sääntöjä.

Oletetaan seuraava html-dokumentti:

```html
<ul>
    <li class="li1" style="color: blue;">teksti1</li>
    <li class="li2" style="color: red !important;">teksti2</li>
</ul>
```

ja sille vastaavat css-tyylit:

```css
.li1 {
    color: red !important;
}

.li2 {
    color: blue !important;
}
```

Olisivat taas molempien `li`-elementtien tyylit punaisia.

Tällöin, `li2`-elementin osalta huomataan vähän yllättäen,
että jos molemmissa säännöistä, 
`style`-attribuutissa ja css-valitsimessa,
käytetään `!important`-määrettä,
elementin `style`-attribuutissa tehty määrittely vie taas voiton.

### transitiot menevät kuitenkin aina kaiken muun edelle

Tähän kaikkeen ovat kuitenkin poikkeuksena transitiot,
jotka menevät lähes kaikissa tapauksissa kaikkien muiden valitsimien ohi.

## Lisää luettavaa

Tarkemman kuvauksen css-sääntöjen määräytyvyydestä löytää mm. MDN:n [Introducing the CSS cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_cascade/Cascade)-dokumentista.
