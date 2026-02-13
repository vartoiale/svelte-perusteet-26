# Huomioita ja korjauksia harjoituksessa 3 (css ja flexbox) käsiteltyihin asioihin

Alla on huomioita ja korjauksia harjoituksessa 3 käsiteltyihin asioihin.

Nämä kannattaa lukaista läpi, ja jos muutokset sopivat omaan koodiin, kannattaa ne korjata itselläkin.

## BEM ja aukioloajat

Harjoituksen 3 tehtävässä 1 lisätään BEM-nimeämistavan avulla luokkia elementeille.

Yksi mielenkiintoinen tilanne liittyy aukioloajat-kenttään, joka löytyy useammasta paikasta.

BEM:iä käytettäessä, on tärkeää elementtiä nimetessä miettiä, onko elementti itsenäinen kokonaisuus, 
vai onko se alisteinen sen vanhempana olevalle elementille.

Joissain tilanteissa, kuten aukioloajat-osan yhteydessä, molemmat näistä voivat päteä:

* aukioloajat on keskeisesti sen vanhempaan liittyvä asia,
  esimerkiksi asiakaspalvelun aukioloajat liittyvät keskeisesti asiakaspalveluun.
* aukioloajat on kuitenkin itsenäinen osio sivulla, joka vieläpä toistuu useiden eri osioiden alla.

Miten tämä tilanne sitten tulisi ratkaista? Lisäämällä elementille kaksi eri nimeä: 

* vanhemman mukaan määrittyvän nimen muotoa `block__element`, esimerkiksi `asiakaspalvelu__aukioloajat`
* itsenäisen osion nimen muotoa `block`, siis `aukioloajat`

Tämän jälkeen, lähdemme lisäämään `.aukioloajat`-elementin lapsille nimiä käyttäen tätä lyhyempää `block`-muodosta lähtevää nimeä.
Teemme näin, koska pystymme silloin käyttämään samoja nimiä kaikissa `aukioloajat`-elementin ilmentymissä, 
käytettiin sitä asiakaspalvelussa tai yritysmyynnissä.

### Esimerkkitoteutus: aukioloajat

BEM-nimeämiskäytäntöä käyttäen nimeämme asiakaspalvelun aukioloajat seuraavasti:

```html
<div class="asiakaspalvelu">
  <h2 class="asiakaspalvelu__otsikko">Asiakaspalvelu</h2>
  <ul class="asiakaspalvelu__aukioloajat aukioloajat">
    <li class="aukioloajat__aukioloaika">
      <div class="aukioloajat__aukioloaika__päivä">Ma-Pe</div>
      <div class="aukioloajat__aukioloaika__auki">24/7</div>
    </li>
  </ul>
</div>
```

ja vastaavasti myymälän osiossa käytetään samaa mallia:

```html
<div class="myymälä-turku">
  <h2 class="myymälä-turku__otsikko">Myymälä Turku</h2>
  <ul class="myymälä-turku__aukioloajat aukioloajat">
    <li class="aukioloajat__aukioloaika">
      <div class="aukioloajat__aukioloaika__päivä">Ma-Pe</div>
      <div class="aukioloajat__aukioloaika__auki">11:00-19:00</div>
    </li>
    <li class="aukioloajat__aukioloaika">
      <div class="aukioloajat__aukioloaika__päivä">La</div>
      <div class="aukioloajat__aukioloaika__auki">10:00-16:00</div>
    </li>
  </ul>
</div>
```

### Myymälän aukioloaikojen toteutus tekee asiakaspalvelun aukioloaikojen toteutuksesta monimutkaisemman - ja se on hyvä asia

On huomattavaa, että jouduimme avaamaan aukioloajat listaksi, 
jotta pystyimme käyttämään samaa rakennetta myös myymälöiden yhteydessä.

Emme oikeastaan tarvitsisi listana määritettyä aukioloaikaa asiakaspalvelun yhteydessä.
Toisaalta koska tarvitsemme listaa myymälän yhteydessä, joudumme käyttämään sitä kuitenkin tuossa yhteydessä.

Tällöin on mielekästä toteuttaa monimutkaisin vaihtoehto ensin,
ja käyttää samaa määrittelyä myös yksinkertaisimmissa tapauksissa.

Tästä etuna on, että meidän tarvitsee näin ylläpitää vain yhtä tyyliratkaisua.
Jos olisimme luoneet eri tyyliratkaisut listaa ja yksittäistä aukioloaikaa varten,
saattaisivat ne ajan kuluessa muuttaa muotoaan, ja luisua toisista erilleen, koska ne olisi määritetty eri paikoissa.
