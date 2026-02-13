# Käytäntö: html:n perusrakenne

Seuraavaksi tutustumme html:n perusrakenteeseen.

## Hyvin yksinkertainen html-sivu

Yksinkertaisimmillaan html-dokumentin ei tarvitse sisältää ensimmäistäkään html-elementtiä. 
Se voi koostua vain pelkästä tekstistä.

Seuraavassa on yksinkertainen html-sivu.

index.html:

```html
Heippa maailma.
```

Kun selain tuottaa siitä näkyvän sisällön, näyttää se vain nämä samat sanat ruudulla: "Heippa maailma.".

## Selaimet osaavat näyttää myös virheellisiä html-sivuja

Selaimet ovatkin hyvin mukautuvaisia.
Aikojen saatossa html-sivuja kirjoittaneet tahot, siis kuten sinä ja minä, ovat säännöstään tehneet hyvin paljon erilaisia virheitä.
Tästä johtuen, selainten on ollut pakko hyväksyä, että html-sivuilla voi olla paljonkin virheitä.
Käytännössä selaimet pyrkivät näyttämään html-sivun, jollain tavalla, olipa siinä kuinka paljon virheitä tahansa.

Tältä osin, aiemmin mainittu, html:n deklaratiivinen luonne, on erittäin hyödyllinen ominaisuus.
Deklaratiivinen tarkoittaa siis "määrittelevää".

Html on monia muita suppeampi ohjelmointikieli. 
Tämän takia sen määrittelemät sivun osat, eivät ole suoraan toisistaan riippuvaisia.
Koska html-sivun osat ovat itsenäisiä, ei sivun muiden osien näyttämiseen vaikuta, 
vaikka yksi tai useampi osa sivusta olisi väärin kirjoitettu, niin kauan kuin sivu on syntaktisesti oikein kirjoitettu.

Lisäksi, html-sivu sisältää vain sen, mitä siinä näkyy.
Html-sivu sisältää vain ne html-elementit, jotka se on kirjoitettu sisältämään.
Se ei siis sisällä samanlaisia näkymättömiä elementtejä, kuin esimerkiksi javascript.
Javascriptissa tällaisia näkymättömiä elementtejä ovat mm. funktiot ja vaikka `for`-toistolauseet.

Myöhemmin opimme, että html-sivulle on mahdollista lisätä html-elementtejä javascript-kielellä.
Teoriassa tämä kuitenkin aina luo uuden version sivusta.

Html-sivulla ei myöskään pysty viittamaan mihinkään muualle sivulle siten, että viittaus vaikuttaisi viittajaan toimintaan.
Ainakaan kielen perusominaisuuksien puitteissa.

Koska html ei pysty luomaan näkymättömiä osuuksia, kuten `for`-toistolauseella, 
eikä sivun osilla voi olla niiden näyttämiseen vaikuttavia keskinäisiä riippuvuuksia,
selaimen ei tarvitse keskeyttää virheen kohdatessaan sivun piirtämistä,
vaan se voi vain piirtää virheellisen osuuden niin hyvin kuin se pystyy, 
ja sitten jatkaa muun sivun piirtämistä.

Yhteen sivun osaan kohdistuva virhe ei siis kaada koko muuta sivua, toisin kuin monissa voimakkaammissa ohjelmointikielissä käy.

Html-sivut voivat siis pitää sisällään paljonkin virheitä, ja silti selain pystyy näyttämään ne jollain tavalla.

Tästä selaimen ominaisuudesta on kyse myös edellä olevassa html-esimerkissä, 
joka ei sisällä ensimmäistäkään html-elementtiä, mutta toimii silti.

Miltä html-sivun sitten pitäisi näyttää?

## Pienin oikeaoppinen html-sivu

Pienimmillään html-sivu sisältää kolme html-elementtiä: `html`-, `head`- ja `body`-elementit.

Lyhykäisyydessään pienin oikeaoppinen sivu näyttää seuraavalta:

```html
<html>
  <head></head>
  <body></body>
</html>
```

Edellä olevassa esimerkissä ei tosin piirtyisi mitään näytölle, 
koska siinä ei ole mitään näkyvää sisältöä.

Perinteisempi "heippa, maailma"-sivu näyttäisi seuraavalta:

```html
<html>
  <head></head>
  <body>
    Heippa, maailma!
  </body>
</html>
```

Tämä oikeaoppinen html-sivu piirtäisi selaimen ruudulle tekstin "Heippa, maailma!".

Tarkastelemme seuraavaksi lyhyesti näitä kolmea elementtiä yksitellen.

### `html`-elementti

`html`-elementti pitää sisällään kaikki muut sivun html-elementit. 

Kaikki sivun html-elementit ovat siis `html`-elementin lapsia.
Tai sen lapsenlapsia, tai lapsenlapsenlapsia, ja niin edelleen, niin monena sukupolvena, kuin joku vain html-puuhun jaksaa elementtejä auki kirjoittaa.

Tämä tarkoittaa, toisin sanoen, että `html`-elementin ulkopuolella ei voi olla mitään muita elementtejä.

Kuten edellä näimmekin, sekä `head`- ja `body`-elementit olivat `html`-elementin lapsia.

#### Oikea html-elementin käyttö

Oikea `html`-elementin käyttö, jossa kaikki muut elementit ovat `html`-elementin lapsia:

```html
<html>
  <head></head>
  <body></body>
</html>
```

#### Väärin

Molemmat seuraavista `html`-elementin käytöistä ovat vääriä, 
koska niissä yksi tai useampi html-elementti eivät ole `html`-elementin lapsia.

Seuraavassa esimerkissä `body`-elementti on väärässä paikassa.

```html
<html>
  <head></head>
</html>

<body></body>
```

Seuraavassa esimerkissä taas molemmat `head`- ja `body`-elementit ovat väärässä paikassa.

```html
<html>
</html>

<head></head>
<body></body>
```

Kaikkien sivun html-elementtien kuuluu olla `html`-elementin sisällä. Aina.

### `head`-elementti

`head`-elementti pitää sisällään sivun metatiedon.

Siellä ei pitäisi olla mitään sellaista, minkä selain näyttäisi käyttäjälle sivulla.

Siellä ei siis pitäisi olla mitään sivun näkyvää sisältöä.

Sen sijaan se pitää sisällään sivun konfiguraatiotietoja.

Yleisesti sinne laitetaan linkkejä tyylitiedostoihin, javascript-koodia, tai linkkejä javascript-kooditiedostoihin.
Siellä voi myös olla tietoa, joka on tarkoitettu koneiden luettavaksi.

Näitä katsellaan paremmin myöhemmin.

### `body`-elementti

`body`-elementti on se sivun elementti, jonka lapseksi kaikki sivun näkyvä sisältö pitäisi sijoittaa.

```html
<body>
  {Kaikki sivun näkyvä sisältö tulee tänne}
</body>
```

Tai vähän kokonaisemmin esitettynä, `html`- ja `head`-elementtien kanssa esitettynä.

```html
<html>
  <head></head>
  <body>
    {Kaikki sivun näkyvä sisältö tulee tänne}
  </body>
<html>
```

Se on yksinkertaisuudessaan `body`-elementin ainoa tehtävä: 
pitää sisällään html-sivun näkyvä sisältö.

Tästä päästäänkin sisällön määrittämiseen.

## Sisällön määrittäminen

Kuten edellä esitettiin, html-sivun sisällön ei tarvitse koostua yhdestäkään elementistä.
On kuitenkin helpompaa erotella sivun eri osia toisistaan, jos sivun eri osat on eroteltu jotenkin toisistaan.

On myös helpompaa kohdistaa css-sääntöjä tarkasti sivun yksittäisiin osuuksiin,
jos sivun eri osat on eroteltu toisistaan.

Tähän käytetään taas html-elementtejä. 

Html-elementtejä on tarjolla paljon, mutta niistä kenties eniten käytetty on `div`-elementti.

### `div`-elementti

`div`-elementti on jonkinlainen html-sivun jokapaikan höylä. 
Sitä voi käyttää otsikkona, kappaleena, listana ja listan osiona, sivun osiona ja vaikka minä - jopa kuvana.

Se ei välttämättä näissä tapauksissa toimi ihan yhtä hyvin kuin tarkempi, 
kyseiseen käyttötarkoitukseen suunniteltu html-elementti, mutta se toimii paremman puutteessa.

Jos kehittäjä ei tiedä mitä html-elementtiä käyttäisi, voi aina turvautua `div`-elementtiin.
Jos myöhemmin keksii, tai löytää, tilanteeseen paremmin sopivan elementin, 
voi vanhan `div`-elementin jälkeenpäin korvata toisella, paremmin tilanteeseen sopivalla html-elementillä.

Käytämme alkuun siis vain `div`-elementtiä.

Sillä pääsee hyvin alkuun.
Myöhemmin otamme käyttöön muita elementtejä, tilanteen mahdollistaessa sen.

`div`-elementti näyttää syntaksinsa puolesta samalta kuin muutkin elementit:

```html
<div>tekstisisältö</div>
```

Sillä voi olla lapsenaan muita `div`-elementtejä:

```html
<div>
  <div>
    <div>
      <div>tekstisisältö</div>
    </div>
  </div>
</div>
```

Sillä voi olla attribuutteja:

```html
<div id="paras-elementti-ikinä" class="ihan-normaali-divi">
  tekstisisältö
</div>
```

Se toimii siis kuin mikä tahansa muukin html-elementti, syntaksin puolesta, ja melkein muutenkin.
