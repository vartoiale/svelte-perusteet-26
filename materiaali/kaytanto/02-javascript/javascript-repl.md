# Käytäntö: javascriptia REPL:ssä

## REPL

REPL tulee englanninkielisestä termistä: Read, Evaluate, Print Loop.
Se tarkoittaa vapaasti kääntäen toistorakennetta, jossa järjestyksessä suoritetaan lukuvaihe, suoritusvaihe ja tulostusvaihe, uudestaan ja uudestaan.

Käytännössä se on komentorivin kaltainen työkalu.
Erona se, että REPL:ssä ei ajetakaan ohjelmia, vaan siinä suoritetaan aina jotain ohjelmointikieltä.

Tässä REPL:ssä, josta olemme kiinnostuneita, suoritetaan javascriptiä.
Se löytyy selaimessa jokaiselta sivulta, kehittäjän työkaluista, yleensä nimellä konsoli (engl. console).

Saat konsolin auki avaamalla selaimessa vaikka tämän sivun kehittäjätyökalut,
esimerkiksi klikkaamalla oikealla hiiren napilla sivun sisältöä, 
ja valitsemalla kontekstivalikosta kohdan "tarkista".
Kehittäjä työkaluissa löytyy melkein joka selaimessa välilehti nimellä "console" tai "konsoli".
Avaa nyt tämä konsoli.

Konsoli säilyttää kaikki sille syötetyt arvot siihen asti, 
kunnes sivu ladataan uudelleen.
Se siis toimii vähän samaan tapaan, 
kuin jos kirjoittaisit riveittäin koodia.
Tällöin sivun uudelleenlataaminen vain tyhjentää koko kooditiedoston.

Tämä konsolin muisti mahdollistaa sen käytön samalla tavalla kuin normaalin lähdekooditiedoston.

REPL on erityisesti hyödyllinen työkalu, 
kun tarvitsee nopeasti tarkistaa, mitä jokin koodinpätkä tai funktio tekee.

Käytämmekin sitä juuri näihin tarkoituksiin tässä käytännönharjoitteessa.

## Miten tätä dokumentaatiota luetaan

Tämä dokumentti koostuu lyhyistä komento-paluuarvo-selitys -osista.

Tässä dokumentissa siis kerrotaan kolmesta osasta koostuvina ryhminä:

1. javascript-konsolissa ajettava komento, (alun `>` merkkiä indikoi syötettä, eikä sitä kirjoiteta konsoliin),
2. komennon paluuarvo, (alun `<-` symboloi paluuarvoa, ja sekin on vain esitystekninen merkintä), 
3. lyhyt selitys siitä mitä komennossa tapahtuu.

Huomautettakoon, että tässä tekstissä ilmaus `<- !` tarkoittaa, että komennon suoritus epäonnistuu, ja tuottaa virheilmoituksen.
Se ei siis tarkoita, että paluuarvona saataisiin `!`-tunniste.

Tarkoituksenasi on tätä dokumenttia lukiessasi syöttää komennot selaimen konsoliin,
ja sanallisesta selityksestä pohtia, paluuarvon avulla, 
mitä tämä lyhyt javascript-koodinpätkä tarkoittaa.

Älä hyppää mitään kohtaa yli, vaan kirjoita kaikki komennot konsoliin.
Jos jäät pohtimaan jotain kohtaa, kokeile muokata annettua komentoa hieman toisenlaiseksi,
ja tarkista, toimiiko komento tällöin tavalla jolla olettaisit sen toimivan.

Tarkoituksena ei ole tehdä kohtia vain kerran, vaan tarvittaessa lukea uudelleen, useampaan kertaan,
kunnes kyseisen kohdan sisältö aukenee.
Tämä voi vaatia montakin lukukertaa.
Lisäksi joitain kohtia voi olla tarpeen lukea uudelleen enemmän kuin toisia.

Jos kohta ei avaudu ensimmäisellä kerralla, siirry seuraavaan kohtaan ja kokeile palata siihen myöhemmin.
Seuraavalla kerralla se saattaa avautua paremmin, kun sille on avautunut uutta kontekstia muun uuden syntaksin kautta.

Triviatietona mainittakoon, että tämä opetustyyli on lainattu Daniel P. Friedmanin mainiosta kirjasta The Little Schemer.

## Javascriptin perusteet

Lähdetään liikkeelle javascriptin perusteista. Aloitetaan arvoista, joilla määritetään muuttuvia osia sovelluksesta.

### Aloitetaan arvoista

Käsitellään aluksi javascriptin yleisimmät arvotyypit:

---

```js
>  undefined
```

```js
<- undefined
```

`undefined` on tyhjä arvo. Tarkemmin, se tarkoittaa arvon puuttumista. Tätä tarvitaan mm. funktioiden paluuarvona, silloin kun funktio ei palauta mitään. `undefined` on myös varattu sana, eikä sitä siksi voi käyttää esimerkiksi muuttujan nimenä.

```js
>  "undefined"
```

```js
<- "undefined"
```

`"undefined"` on merkkijono (engl. string). Se eroaa edellisestä lainausmerkkien ansiosta. Lainausmerkkien ympäröimänä asiat muuttuvat merkkijonoiksi, tuttavallisemmin tekstiksi. Merkkijono on yksi arvojen sisäänrakennetuista tyypeistä. Se palauttaa arvona itsensä.

```js
>  true
```

```js
<- true
```

`true`, suomeksi "tosi", on ensimmäinen kahdesta totuusarvosta. Se ilmaisee, että jokin pitää paikkansa. 
Totuusarvoja käytetään ehtolauseiden haarauman valintaan.

```js
>  false
```

```js
<- false
```

`false`, suomeksi "epätosi", on toinen kahdesta totuusarvosta. Se ilmaisee, että jokin ei pidä paikkaansa.

```js
>  1
```

```js
<- 1
```

`1` on kokonaisluku (engl. integer). Javascriptissa on kolme erilaista numeroarvoa, 
ja kokonaisluvut ovat näistä arvoista yksi.

```js
>  1.24234
```

```js
<- 1.24234
```

`1.24234` on liukuluku (engl. decimal). Liukuluvut ovat javascriptin toinen kolmesta numerotyypistä.

```js
>  NaN
```

```js
<- NaN
```

`NaN` tulee englanninkielisistä sanoista "not a number". Se tarkoittaa, että arvo ei ole numero. Tästä huolimatta se itsessään on kuitenkin paradoksaalisesti numerotyyppi. `NaN` on javascriptin kolmas numerotyyppi.
`NaN` on `undefined` arvon tavoin varattu sana.

```js
>  nan
```

```js
<- !
```

`nan` antaa virheilmoituksen. Se ei ole varattu sana, eikä sitä ole vielä määritetty muuttujan nimeksi,
joten konsoli ei tunnista sitä. Kirjainten koolla on merkitystä. 
Konsoli ei kuitenkaan tästä huolimatta kaadu, vaan vain yksi REPL-kierros epäonnistuu.
Konsoli onkin heti valmis seuraavaan REPL-kierrokseen, pyytäen jo lukemaan seuraavan lauseen.

### Merkkijonoista

Katsellaan vähän tarkemmin erilaisia merkkijonoja:

---

```js
>  'undefined'
```

```js
<- "undefined"
```

`'undefined'` on myös merkkijono. Huomaa lainausmerkkien vaihtuminen kaksinkertaisista yksinkertaisiin lainausmerkkeihin. Voit käyttää kumpia tahansa lainausmerkkejä, kunhan aloitus- ja lopetusmerkit ovat samaa lainausmerkkiä. Huomaa, että selain mahdollisesti palauttaa arvon kuitenkin kaksinkertaisilla lainausmerkeillä ilmaistuna.

```js
>  'yksinkertaisten lainausmerkkien sisällä voi käyttää "-merkkiä'
```

```js
<- 'yksinkertaisten lainausmerkkien sisällä voi käyttää "-merkkiä'
```

Jos tarvitset tekstiä, joka sisältää kaksinkertaisen lainausmerkin, voit määrittää merkkijonon yksinkertaisten lainausmerkkien avulla. Huomaa, että paluuarvo on tällä kertaa yksinkertaisilla lainausmerkeillä määritetty.


```js
>  "kaksinkertaisten lainausmerkkien sisällä voi käyttää '-merkkiä"
```

```js
<- "yksinkertaisten lainausmerkkien sisällä voi käyttää '-merkkiä"
```

Jos tarvitset tekstiä, joka sisältää yksinkertaisen lainausmerkin, voit määrittää merkkijonon kaksinkertaisten lainausmerkkien avulla. Huomaa, että paluuarvo on tällä kertaa kaksinkertaisilla lainausmerkeillä määritetty.

```js
>  "kaksinkertaisten lainausmerkkien sisällä ei voi käyttää "-merkkiä"
```

```js
<- !
```

Tämä ei toimikaan vaan antaa virheilmoituksen. 
`"kaksinkertaisten lainausmerkkien sisällä ei voi käyttää "-merkkiä"` ei olekaan merkkijono, koska siinä on kolme kertaa sama lainausmerkki. 
Sen sijaan `"kaksinkertaisten lainausmerkkien sisällä ei voi käyttää "` on merkkijono, ja sen jälkeen tuleva `-merkkiä"` on vain rikkinäistä javascriptiä, jota konsoli ei osaa suorittaa.

### Muuttujista ja vakioista

Arvojen keskeinen hyöty on, että niille voidaan antaa nimi. 
Näin tehdään muuttujien, vakioiden ja parametrien yhteydessä. 
Tässä vaiheessa perehdymme vasta muuttujiin ja vakioihin.

---

```js
>  let muuttujan_nimi = "arvo"
```

```js
<- "arvo"
```

`let` on varattu sana, jonka yhteydessä määritetään tunnisteen avulla muuttujan nimi. Tässä `muuttujan_nimi` on muuttujan nimi. Muuttujan arvoksi tulee merkkijono `"arvo"`. Tämä tallettaa muistiin, että `muuttujan_nimi`-muuttujaan on talletettu arvo "arvo". Se myös palauttaa muuttujaan sijoitetun arvon.

```js
>  muuttujan_nimi
```

```js
<- "arvo"
```

Konsoli muistaa, että `muuttujan_nimi`-muuttujasta löytyy arvona `"arvo"`-merkkijono.

```js
>  muuttujan_nimi2
```

```js
<- !
```

Tämä antaa virheilmoituksen. `muuttujan_nimi2` ei ole vielä muuttujan nimi, koska emme sitä ole sellaiseksi `let`:llä tai muulla komennolla määrittäneet. Se ei myöskään ole varattu sana tai funktion nimi, joten konsoli ei tunnista sitä.

```js
>  muuttujan_nimi
```

```js
<- "arvo"
```

`muuttujan_nimi`-muuttuja pitää yhä sisällään saman merkkijonon. 
Tilanne ei ole muuttunut, vaikka saimme välissä aikaan virheilmoituksen.


```js
>  muuttujan_nimi = 2
```

```js
<- 2
```

Muuttujan arvon voi vaihtaa uudella sijoitusoperaatiolla. Koska olemme jo määrittäneet aiemmin `let`-termin avulla, että `muuttujan_nimi` on muuttuja, voi sen arvon jälkikäteen vaihtaa.

```js
>  muuttujan_nimi
```

```js
<- 2
```

Viimeisin vaihdettu arvo säilyy muuttujan arvona. Vanhat arvot vain katoavat pois.

```js
>  muuttujan_nimi = 2.2
```

```js
<- 2.2
```

Muuttujan arvon voi vaihtaa niin monta kertaa kuin halutaan.

```js
>  alustamaton_muuttujan_nimi = "ei taida onnistua."
```

```js
<- !
```

Konsoli antaa virheilmoituksen.
Tämä ei onnistukaan, koska emme ole määrittäneet, että `alustamaton_muuttujan_nimi` olisi muuttuja. Emme ole käyttäneet `let`-termiä, tai muuta varattua sanaa, jolla tämä onnistuisi. 
Näin ollen myös sijoitus epäonnistuu, koska javascript ei tiedä mitä tekisi `alustamaton_muuttujan_nimi`-tunnisteen avulla - se ei edes tunnista sitä tunnisteeksi.

```js
>  let alustamaton_muuttujan_nimi = "onnistuu."
```

```js
<- "onnistuu."
```

Nyt onnistuu, koska käytämme `let`-termiä alussa tallentamaan `alustamaton_muuttujan_nimi`-nimen muuttujan nimeksi.

```js
>  let kolmas_muuttujan_nimi
```

```js
<- undefined
```

`let` ei vaadi, että sille annetaan arvo `=`-sijoitusoperaattorin avulla. 
Tällöin se palauttaa tyhjän arvon paluuarvonaan, koska sillä ei ole arvoa.

```js
>  kolmas_muuttujan_nimi
```

```js
<- undefined
```

Koska `kolmas_muuttujan_nimi`-muuttuja ei saanut määrittelyn yhteydessä arvoa, sen arvoksi jäi toistaiseksi tyhjä arvo `undefined`.

```js
>  kolmas_muuttujan_nimi = true
```

```js
<- true
```

Koska se on muuttuja, sille voidaan koska tahansa määrittää uusi arvo sijoitusoperaattorin avulla.


```js
>  var toinen_muuttujan_nimi = 111
```

```js
<- 111
```

Myös `var`-termi mahdollistaa muuttujien määrittämisen. 
Se toimii pitkälti samalla tavalla kuin `let`.
Se on kuitenkin vanhempi termi, eikä sitä enää suositella käytettäväksi, paitsi erikoistilanteissa.

```js
>  const vakion_nimi = 2.2
```

```js
<- 2.2
```

`const`-termiä käytetään vakioiden määrittämiseen. Vakiolle annetaan arvo määrityksen yhteydessä.
Vakion arvo sitoo nimeen kyseisen arvon, suorituksen loppuun asti.
Se on tavallaan tapa, jolla voidaan antaa jollekin erityiselle arvolle helpommin käytettävä nimi.

```js
>  vakion_nimi
```

```js
<- 2.2
```

Vakio on kuin muuttuja siinä, että se säilyttää sille annetun arvon.

```js
>  vakion_nimi = 3
```

```js
<- !
```

Vakioon kohdistettu sijoitusoperaatio määrityksen jälkeen ei onnistukaan, vaan antaa virheilmoituksen. 
Muuttujasta poiketen, vakiolle ei siis voi vaihtaa toista arvoa sen määrittelyn jälkeen. 
Se on sidottu määrittelyssä annettuun arvoonsa ohjelman suorituksen loppuun asti.
Tai ainakin kyseisessä suoritusympäristössä.

```js
>  const vakion_nimi = 2.2
```

```js
<- !
```

Tämäkin antaa virheilmoituksen.
Vakiota ei myöskään voi määritellä uudelleen `const`-termin avulla, ei edes samalla arvolla.

```js
>  { const abc = 1 } { const abc = 2 }
```

```js
<- undefined
```

Tämä onnistuu. Aaltosulkeiden (`{...}`) sisälle määritetään suoritusympäristö, käytettäessä `const`- ja `let`-termejä.
Vakio on käytettävissä vain suoritusympäristön sisällä, 
joten voimme määritellä sen uudelleen myös jälkimmäisessä uudessa suoritusympäristössä.
Koska suoritusympäristöt ovat uusia, vakion määrittely onnistuu.
Tätä `{}`-merkintää ei kannata sekoittaa svelten html-koodin sisällä käyttämään samankaltaiseen syntaksiin.

```js
>  abc
```

```js
<- !
```

Tämä antaa virheilmoituksen, koska `abc` ei ole määritetty.
Vaikka edellä määritimme `{}`-suoritusympäristön avulla, siinä suoritusympäristössä `abc`-vakiolle arvon,
tuo vakio ei tallennukaan suoritusympäristön ulkopuolelle. 
Se katoaa siinä kohtaa kun sulkeva aaltosulje tulee vastaan.
Suoritusympäristöistä on myöhemmin hyötyä, mutta nyt ne on vasta hyvä tunnistaa.

```js
>  let numero_merkkijonona = "12";
```

```js
<- "12"
```

Merkkijonot voivat sisältää myös tekstimuotoisia numeroita.

### Sisäänrakennetut operaatiot ja lauseet ja lausekkeet

Javascript tarjoaa ohjelmoijan käyttöön joukon yksinkertaisia operaattoreita, ja näillä suoritettavia operaatioita.

Peruspalikoihin kuuluvat myös lauseet ja lausekkeet

---

```js
>  let numero = 12;
```

```js
<- 12
```

Tässä on lause. Lause päättyy puolipisteeseen (`;`).
Lause on tärkeä työkalu perinteisessä proseduraalisessa ohjelmoinnissa, kuten monissa olio-ohjelmointikielissä.

```js
>  numero = 13
```

```js
<- 13
```

Lauseke on lausetta kevyempi muoto. Se ei pääty puolipisteeseen. Jokainen lause sisältää yhden tai useamman lausekkeen.
Lausekkeet ovat funktionaalisen ohjelmoinnin tärkeimpiä työkaluja.

```js
>  numero = 14, numero = 15;
```

```js
<- 15
```

Tässä on lause, joka sisältää kaksi lauseketta. Siitä tulee lause vasta puolipisteen avulla. 
Palaamme lausekkeisiin myöhemmin uudelleen.

```js
>  10 + 2
```

```js
<- 12
```

Voimme tehdä `+`-yhteenlaskuoperaattorilla numeroiden kanssa yhteenlaskuja.

```js
>  "heippa " + "maailma"
```

```js
<- "heippa maailma"
```

Mutta merkkijonojen yhteydessä sama `+`-operaattorisymboli muuttuukin konkatenaatio-operaattoriksi, jolla voi yhdistää kaksi merkkijonoa yhdeksi merkkijonoksi. 
Huomaa, että ensimmäinen merkkijono sisältää lopussa välilyönnin, joka estää sanojen menemästä yhteen.

```js
>  "heippa" + "maailma"
```

```js
<- "heippamaailma"
```

Tässä välilyönti puuttui. Konkatenaatio ei siis lisää välilyöntejä merkkijonojen väliin.

```js
>  10 - 2
```

```js
<- 8
```

Numeroille löytyy vähennysoperaatio `-`-operaattorin avulla.


```js
>  "heippa" - "maailma"
```

```js
<- NaN
```

Mutta merkkijonot eivät tunnekaan `-`-operaatiota. 
Yllä oleva esimerkki siis yrittää vähentää merkkijonosta toisen, ja saa paluuarvona `NaN`-numeron,
koska lasku ei pysty tuottamaan todellista numeraalista arvoa.
Se kuitenkin on numero-operaatio, joten se palauttaa numeron, siis `NaN`-arvon.

```js
>  10 / 2
```

```js
<- 5
```

Jakolaskut onnistuvat.

```js
>  10 * 2
```

```js
<- 20
```

Kuten myös kertolaskut.

```js
>  10 + "hei"
```

```js
<- "10hei"
```

Numeron ja merkkijonon yhteenlasku tuottaakin konkatenaation, eli liiton merkkijonoksi.


```js
>  "hei" + 10
```

```js
<- "hei10"
```

Järjestyksellä ei ole väliä.

### Funktioista

Lyhyesti funktioista.

---

```js
>  console.log("tämä tulostuu konsoliin")
```

```js
<- undefined
```

`console.log` on funktio.
`console.log("merkkijono")` on funktion kutsu, jolle annetaan yksi merkkijono-muotoinen parametri.
Oheinen esimerkki tulostaa konsoliin sille annetun arvon.
Huomaa, että tämä funktion kutsu ei palauta mitään arvoa - vain tyhjän arvon.

```js
>  function neliö(a) { return a * a; }
```

```js
<- undefined
```

Tämä määrittelee funktion `neliö`, joka saa yhden parametrin.
Funktio laskee luvun neliön, eli kertoo sen itsellään.
Tämän jälkeen funktio palauttaa `return` termille annetun arvon, eli laskutoimituksen summan. 
Se varaa `neliö`-nimen käyttöönsä, samalla tavalla kuin `let` varaa sille annetun muuttujan nimen.

```js
>  neliö(1)
```

```js
<- 1
```

Funktiota `neliö` voidaan nyt kutsua eri arvoilla. 1 * 1 = 1.


```js
>  neliö(4)
```

```js
<- 16
```

Funktio näyttäisi toimivan.

```js
>  const tupla = (a) => a + a
```

```js
<- undefined
```

Funktion voi määritellä useammalla tavalla. 
Tässä käytämme `const`-vakiota yhdistettynä nuoli-syntaksilla määritettyyn funktioon.
Nuoli-syntaksilla määritetty funktio palauttaa automaattisesti viimeisen lausekkeensa arvon.

```js
>  tupla(12)
```

```js
<- 24
```

Nuolisyntaksilla määritetyn funktion käyttö ei eroa mitenkään muilla tavoilla määritettyjen funktioiden käytöstä.

```js
>  const summa = (a, b) => { return a + b }
```

```js
<- undefined
```

Funktion määrittelyssä voi määrittää useamman parametrin, pilkuilla eroteltuna, joita voidaan käyttää funktion sisällä.
Jos haluamme tehdä funktion sisällöstä useamman rivin pituisen, 
meidän täytyy käyttää aaltosulkeita (`{...}`) rungon määrittelyyn.

```js
>  const summa_ilman_paluuarvoa = (a, b) => { a + b }
```

```js
<- undefined
```

Kun funktion runko määritellään aaltosulkeilla, funktio ei palauta mitään ilman `return`-termiä.

```js
>  summa_ilman_paluuarvoa(1,2)
```

```js
<- undefined
```

Ei paluuarvoa, koska määrittelyssä ei ollut käytetty return termiä.

### Funktiot arvoina

Javascript on funktionaalinen kieli, jossa funktiot ovat ensimmäisen luokan arvoja. 
Niitä voidaan siis sijoittaa muuttujiin, ja antaa edelleen parametreinä toisille funktioille.

---

```js
>  tupla
```

```js
<- function tupla(a)
```

Funktion nimi on vain vakio, joka pitää sisällään funktion määrittelyn.
Toisin sanoen, funktio on itsessään vain arvo.

```js
>  let uusi_tupla = tupla
```

```js
<- undefined
```

Koska funktio on vain arvo, se voidaan tallettaa muuttujaan.

```js
>  uusi_tupla(4)
```

```js
<- 8
```

Sitä voidaan suoraan käyttää uuden muuttujan nimen kautta, johon se oli talletettu.

```js
>  tupla(4)
```

```js
<- 8
```

Myös vanha nimi on edelleen käytettävissä.

```js
>  (a) => { return a + a }
```

```js
<- function
```

Funktion määrittely nuolisyntaksilla on lauseke.
Lausekkeena sitä voi siis käyttää arvon tapaan.
Tällöin se palauttaa funktion itsensä.
Jos funktiota ei tallenneta minnekäään, se ei tallennu minnekään ja sitä ei voi myöhemmin käyttää.

```js
>  ((a) => { return a + a })(2)
```

```js
<- 4
```

Aina funktioita ei tarvitse tallentaa minnekään.
Kuitenkin koska nuolisyntaksilla määritellyt funktiot ovat vain arvoja, niitä voidaan kutsua saman tien.
Yllä oleva funktion kutsu vastaa aiempaa kutsua `neliö(2)` paitsi, 
että tällä kertaa emme tallenna funktiota minnekään.

```js
>  let funktion_paluuarvo = ((a) => { return a + a })(2)
```

```js
<- 4
```

Koska funktion kutsuminen palauttaa arvon, voidaan tuo arvo tallettaa muuttujaan.
Tässä lisäämme funktion määrittelyn ympärille sulut, jotta kääntäjä ymmärtää, että kyse on funktiosta, jota käytetään saman tien.
Tallennamme muuttujaan siis vain funktion arvon, emme itse funktiota.
Tämä menee jo vähän vaikeammaksi.
Jos se vaikuttaa vaikealta, voit palata siihen myöhemmin.

---

Filosofisesti voi ajatella, että oikeastaan javascriptissä kaikki arvot ovat vähän kuin funktioita, 
koska ne palauttavat oman arvonsa.
Niillä ei vain tavallaan syntaksisesti tarvitse käyttää kutsumiseen parametrillista `()`-syntaksia,
toisin kuin tavallisilla funktioilla.

### Ehtolauseet, totuusarvot ja ehdot, ja ehtolausekkeet

Jotta sovellus voi reagoida eri arvoihin, 
täytyy sovelluksen toimintaa pystyä muokkaamaan toimimaan eri tavoilla eri tilanteissa.
Tähän käytämme ehtolauseita.

Aloitamme kuitenkin tutustumisen totuusarvoista ja ehdoista (engl. condition), 
jotka tuottavat totuusarvoja.

Jatkamme tästä ehtolauseisiin, ja lopuksi katsomme funktionaalisen ohjelmoinnin puitteissa ehtolausekkeita.

---

#### Totuusarvot

```js
>  true
```

```js
<- true
```

Tämän kävimmekin jo aiemmin läpi: `true` on tosi totuusarvo.

```js
>  false
```

```js
<- false
```

Myös tämän kävimme aiemmin läpi: `false` on epätosi totuusarvo.

```js
>  !true
```

```js
<- false
```

Voimme kääntää totuusarvon päinvastaiseksi, käyttämällä `!`-predikaattioperaattoria,
eli negaatiota.
Negaatio todesta on epätosi.

```js
>  !false
```

```js
<- true
```

Sama käy myös toisin päin. 
Negaatio epätodesta on tosi.

```js
>  !!false
```

```js
<- false
```

Voimme myös tehdä negaation negaatiosta, jolloin saamme alkuperäisen totuusarvon.

```js
>  !!1
```

```js
<- true
```

Voimme tehdä myös negaation muistakin arvoista. 
Kaikilla arvoilla javascriptissa on totuudellinen arvo.
Numerot ovat tosi:hkoja (engl. truthy), poislukien nolla.

```js
>  !!0
```

```js
<- false
```

Nolla on epätosi:hko (engl. falsy) arvo. 
Muista numeroista poiketen se onkin epätosi.

```js
>  !!NaN
```

```js
<- false
```

Myös `NaN` on epätosi:hko arvo.

```js
>  !!"merkkijono"
```

```js
<- true
```

Merkkijonot ovat lähtökohtaisesti tosi:hkoja arvoja.

```js
>  !!""
```

```js
<- false
```

Paitsi tyhjä merkkijono, joka onkin taas epätosi:hko.

```js
>  !![]
```

```js
<- true
```

Tässä on kyse tyhjästä taulukosta (engl. array), joka onkin tosi:hko.
Taulukoihin palaamme myöhemmin. 

#### Ehdot

Totuusarvoja voi käyttää sellaisenaan ehtolauseissa, 
ja voisimme näin ollen jo siirtyä ehtolauseisiin.

Yleensä kuitenkin haluamme tehdä jonkinlaisen vertailun ehdon muodossa.
Katsotaan siis vielä niitä, ennen ehtolauseisiin siirtymistä. 

---

```js
>  1 < 2
```

```js
<- true
```

`<` on vertailuoperaattori, jonka nimi on __"pienempi kuin"__.
Sillä voidaan nähdä onko sen vasemman puoleinen arvo pienempi kuin sen oikean puoleinen arvo.
Se palauttaa totuusarvon sen mukaan, onko väittämä totta.
Tässä tapauksessa 1 on pienempi kuin 2.

```js
>  2 < 1
```

```js
<- false
```

Jos vertailu ei pidä paikkaansa, se palauttaa epätoden totuusarvon.
2 ei ole pienempi kuin 1.

```js
>  2 > 1
```

```js
<- true
```

`>` on vertailuoperaattori, joka tietää kertoa, onko ensimmäinen luku __suurempi__ kuin toinen.
Se toimii siis päin vastoin kuin `<`-vertailuoperaattori.

```js
>  1 > 2
```

```js
<- false
```

Vastaavasti se palauttaa epätoden totuusarvon, 
jos vasemman puoleinen arvo ei ole __suurempi__ kuin oikeanpuoleinen arvon.

```js
>  1 > 1
```

```js
<- false
```

Jos luvut ovat yhtä suuret, toinen niistä ei voi olla pienempi.

```js
>  1 <= 1
```

```js
<- true
```

`<=`-vertailuoperaattori osaa vastata, 
onko vasemman puoleinen luku __yhtä suuri, tai pienempi__, kuin oikean puoleinen luku.

```js
>  2 <= 1
```

```js
<- false
```

Se antaa epätoden arvon vasta kun vasemman puoleinen luku on aidosti isompi.

```js
>  1 >= 1
```

```js
<- true
```

Vastaavasti `>=`-vertailuoperaattori kertoo, 
onko vasemman puoleinen luku __yhtä suuri, tai suurempi__, kuin oikean puoleinen luku.

```js
>  0 >= 1
```

```js
<- false
```

Sekin on epätosi vasta, kun ensimmäinen arvo on aidosti pienempi.

```js
>  1 === 1
```

```js
<- true
```

Arvojen yhtä suuruuden vertailuun käytetään `===`-operaattoria.
Se palauttaa toden totuusarvon, kun luvut ovat yhtä suuria.

```js
>  1 === 2
```

```js
<- false
```

Jos arvot eivät ole samoja, se palauttaa epätoden totuusarvon.

```js
>  1 === "merkkijono"
```

```js
<- false
```

Jos arvot eivät ole samaa tyyppiä se palauttaa epätoden totuusarvon.

```js
>  "merkkijono" === "merkkijono"
```

```js
<- true
```

Myös merkkijonoja voi vertailla.

```js
>  "merkkijono1" === "merkkijono2"
```

```js
<- false
```

Tällöin vaaditaan, että merkkijonot ovat täysin samoja.
Vertailu ei kuitenkaan tapahdu viittausten tasolla, kuten joissain kielissä.

```js
>  true == 1
```

```js
<- true
```

Javascript tuntee myös `==`-operaattorin.
Sitä kannattaa kuitenkin välttää, koska se toimii vähän yllättävillä tavoilla.

```js
>  "merkkijono1" !== "merkkijono2"
```

```js
<- true
```

Myös epäsuuruutta on mahdollista tarkastella.
Se on päinvastainen operaatio `===`-yhtäsuuruusoperaattorin tulokseen verrattuna.

```js
>  "merkkijono" !== "merkkijono"
```

```js
<- false
```

Eli samat arvot antavat sillä epätoden totuusarvon.

#### Ehtolauseet

Ehtolauseet mahdollistavat ohjelman toteutuksen haarautumisen totuusarvojen ja ehtojen pohjalta.

---

```js
>  if (true) { true }
```

```js
<- true
```

Ehtolausetta merkitään `if`-termin avulla.
Se saa suluissa ehdon tai totuusarvon.
Jos ehto määrittyy todeksi totuusarvoksi, suoritetaan ehtolauseen lohko.
Tässä runko sisältää vain yhden arvon `true`.

```js
>  if (false) { true }
```

```js
<- undefined
```

Jos annettu ehto ei ole tosi, ei suoriteta ehtolauseen lohko.

```js
>  if (false) { true } else { false }
```

```js
<- false
```

On myös mahdollista määrittää, että ehtolauseella suoritetaan aina jotain, myös siinä tapauksessa, 
että ehto ei ole pitänyt paikkaansa.

Tämä onnistuu lisäämällä ehtolauseen loppuun `else`-termin avulla toinen lohko.
Tämä jälkimmäinen `else`-termin määrittämä lohko suoritetaan silloin kun ehtolauseen ehto on ollut epätosi.

```js
>  if (true) { true } else { false }
```

```js
<- true
```

Edelleen, jos ehto oli tosi, suoritetaan vain ehtolauseen ensimmäinen lohko, 
vaikka `else`-termillä olisi määritetty toinen lohko.
Tässä tapahtuu siis haarauma, jossa suoritetaan vain toinen ehtolauseen lohkoista.


```js
>  if (1) { true } else { false }
```

```js
<- true
```

Ehtolauseen ehtona ei tarvitse olla vain aitoja totuusarvoja, vaan myös tosihkot (engl. truthy) arvot käyvät.

```js
>  if (0) { true } else { false }
```

```js
<- false
```

Ja tietysti myös epätosi:hkot (engl. falsy) arvot käyvät ehdoiksi.

```js
>  if (!true) { true } else { false }
```

```js
<- false
```

Ehtoina ei tarvitse käyttää vain arvoja, joilla on totuusarvo, 
vaan kaikenlaiset totuusarvon tuottavat ehdot käyvät.

```js
>  if (1 < 2) { true } else { false }
```

```js
<- true
```

Myös siis suuremmuuden tarkistukset.

#### Ehtolausekkeet

Koska javascript on lopulta pitkälti funktionaalinen ohjelmointikieli,
tarvitsee se myös tavan tuottaa lausekkeena haaraumia.

Lausekkeen ero lauseeseen on siinä, että lauseketta voi käyttää kaikkialla arvojen sijasta.

Ehtolausekkeena javascript käyttää niin sanottua kolmiosaista ehtolauseketta (engl. ternary operator).

---

```js
>  true ? true : false
```

```js
<- true
```

Se vastaa arvojensa puolesta siis `if`-lausetta: se saa kolme arvoa, joista:

* ensimmäinen on ehto, 
* toinen on lauseke, joka suoritetaan, jos ehto on tosi
* kolmas on lauseke, joka suoritetaan, jos ehto on epätosi

```js
>  let ehtolausekkeen_paluuarvo = true ? true : false
```

```js
<- undefined
```

Kolmiosainen ehtolauseke palauttaa suoritetun lausekkeen paluuarvon.
Tässä paluuarvo sijoitetaan muuttujaan.

```js
>  ehtolausekkeen_paluuarvo
```

```js
<- true
```

Tarkistettaessa edellisen paluuarvo on muuttujassa tallessa.

### Toistorakenteet

Javascript tarjoaa kaksi lausemuotoista toistorakennetta: `for`- ja `while`-rakenteen.

Lisäksi se tarjoaa funktionaaliseen ohjelmointiin funktioita, joilla voidaan muokata listoja ja muita tietorakenteita toistorakenteiden tavoin. Näistä kuitenkin myöhemmin.

#### `for`-toistorakenne

```js
>  for (let i=0; i<2; i++) { console.log(i) } 
```

```js
<- undefined
```

`for`-toistorakenne määritetään `for`-termillä, jolle annetaan kolme lauseketta, erotettuna puolipisteillä (`;`), sekä toistettava lohko.

Tässä: 

* ensimmäinen lauseke on toistossa käytettävän apumuuttujan alustus,
* toinen lauseke on ehto, siis vertailuoperaatio, joka tuottaa totuusarvon,
* kolmas lauseke on toiminto, joka suoritetaan jokaisen toistokierroksen lopussa.

Miten tämä siis käytännössä toimii:

1. ensin asetetaan `i`-muuttuja, ja sille alkuarvoksi 0.
2. verrataan, pitääkö ehto paikkaansa: 0 < 2
3. koska ehto pitää paikkaansa, siirrytään suorittamaan lohko: `console.log(i)`. Tämä tulostaa `i`-apumuuttujan arvon konsoliin: 0
4. lohkon päätyttyä tehdään toistoehtojen muokkaus: `i++` - tämä tarkoittaa samaa kuin `i = i + 1`. Kasvatetaan siis `i`-muuttujan arvoa yhdellä.
5. verrataan, pitääkö ehto vielä paikkaansa: 1 < 2
6. koska ehto pitää paikkaansa, siirrytään suorittamaan lohko: `console.log(i)`. Tämä tulostaa `i`-apumuuttujan arvon konsoliin: 1
7. lohkon päätyttyä tehdään toistoehtojen muokkaus: `i++` - Kasvatetaan taas `i`-muuttujan arvoa yhdellä.
8. verrataan, pitääkö ehto vielä paikkaansa: 2 < 2
9. Koska ehto ei enää pidä paikkaansa, lopetetaan toistorakenteen suoritus.

#### `while`-toistorakenne

```js
>  while (true) { true; break; } 
```

```js
<- true
```

`while`-toistorakenne määrittyy `while`-termillä, jolle annetaan suluissa ehto.
Niin kauan kuin ehto on tosi, `while`-rakenteen lohkoa toistetaan.
Toiston voi katkaista `break`-termin avulla. 

```js
>  let i = 0; while (i<1) { console.log(i); i++; } 
```

```js
<- undefined
```

`while`-toistorakenteella on mahdollista tehdä sama kuin `for`-toistorakenteella.

Tämä toimii käytännössä seuraavasti:

1. Asetetaan `i`-muuttujalle alkuarvo 0
2. aloitetaan `while`-toistorakenne
3. tarkistetaan ehto: 0 < 1
4. koska ehto on tosi, suoritetaan `while`-toistorakenteen lohko: `console.log(i); i++;`
5. tulostetaan siis `i`-muuttujan arvo konsoliin: 0
6. kasvatetaan `i`-muuttujan arvoa yhdellä
7. lohkon päätyttyä tarkistetaan uudestaan `while`-toistorakenteen ehto: 1<1
8. Koska ehto ei ole enää tosi, ei enää suoriteta uudelleen lohkoa, vaan lopetetaan toistorakenteen suoritus.


---

__jatkuu ...__
