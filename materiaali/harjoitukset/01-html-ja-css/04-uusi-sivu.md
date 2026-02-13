# Harjoitus 4: uusi sivu

Nyt kun olemme ottaneet haltuumme suuren joukon yleisimpiä css-sääntöjä,
voimme kokeilla taitojamme toisella sivulla.

Aiemmassa tehtävässä piirsimme elementttejä myös toisesta sivusta otettuun kuvaan.
Nyt nuo piirrokset tulevat käyttöön, kun lähdemme toteuttamaan tuota toista sivua.

Tehdään siis toinen sivu ylen etusivun (yläosan) pohjalta.

![ylen etusivun referenssikuva](/materiaali/kuvat/referenssikuva-etusivu-ylaosa-yle.jpeg)

Tässä tehtävässä pääset itsenäisemmin toteuttamaan sivua.

Alla esitetään kuitenkin joitain uusia sääntöjä, jotka auttavat tiettyjen erikoistilanteiden toteuttamisessa.

## Uusi sääntö: `position: absolute;`

Kun referenssikuvasas näytetään kahdessa eri kohdassa uutisotsikoita listana, 
niissä molemmissa otsikoiden vieressä on apuelementteinä muuta tietoa.

Ylärivissä apuelementtien avulla ilmaistaan kellonaikaa, jolloin uutinen on ilmestynyt.
Oikean reunan listauksessa näytetään apuelementtinä uutisen sijoitusta.

On huomattavaa, että molemmissa apuelementti on sijoitettu uutisen reunaviivan päälle.
Toisena huomiona on, että molemmisssa apuelementille on asetettu taustaväri,
joka peittää viivan apuelementin sisällön kohdalla.

Näin on myös aikatietojen kohdalla, vaikka siltä ei ehkä näytäkään.
Niiden taustaväriksi kun on asetettu sama valkoisen sävy, 
joka löytyy viivan takaa sivun taustalta.

Mutta miten nämä elementit sitten on siirretty viivan päälle?

Se onnistuu käyttäen [`position: absolute;`](https://developer.mozilla.org/en-US/docs/Web/CSS/position)-sääntöä.

`position: absolute;`-sääntö määrittää, että elementti piirretään siihen kohtaan, 
mihin se pitäisikin sivulla, sille html-dokumentissa määritetyn sijainnin mukaan, piirtää.
Tämän lisäksi sääntö kuitenkin kertoo, että elementille ei normaalista poiketen pidä varata tilaa.

Mitä tämä tilan varaaminen sitten tarkoittaa?

Kun html-elementti piirretään ruudulle, se varaa itselleen tarvittavan tilan,
jotta mikään muu elementti ei mene sen kanssa päällekkäin.

Kun siis merkitsemme elementin `position: absolute;`-säännöllä,
sen kohdalle piirretäänkin seuraavana vuorossa oleva elementti, 
ja merkitty elementti siirtyy leijailemaan sen vanhemman alkuun.

Tarkemmin, siihen, mihin elementin sijainti määräytyy, kun käytetään `position: absolute`-sääntöä, vaikuttaa useampi asia.
Emme tässä lähde niitä katselemaan tarkemmin.

Sen sijaan olemme kiinnostuneita, miten voimme siirtää elementtiä toiseen kohtaan,
nyt kun olemme irrottaneet sen vakinaiselta paikaltaan.

Tämä onnistuu käyttäen neljää apusääntöä:

* `top` - määrittää arvon, jolla elementtiä siirretään alkuperäisestä paikastaan, sen yläkohdasta käsin
* `left` - määrittää arvon, jolla elementtiä siirretään alkuperäisestä paikastaan, sen vasemmasta reunasta käsin
* `right` - määrittää arvon, jolla elementtiä siirretään alkuperäisestä paikastaan, sen oikeasta reunasta käsin
* `bottom` - määrittää arvon, jolla elementtiä siirretään alkuperäisestä paikastaan, sen alakohdasta käsin

Näistä yleensä käytetään kerrallaan vain yhtä tai kahta. 
Riittää, että valitaan toinen horisontaalisista säännöistä, ja toinen vertikaalisista säännöistä, ne kun ovat kilpailevia keskenään.

Säännöt saavat yhden arvon, joka perinteiseen tapaan koostuu numerosta ja yksiköstä.

Esimerkiksi:

```css
top: 10px;
```

Kokonaisuudessaan säännöt näyttäisivät seuraavalta:

```css
.jokin-elementti {
  position: absolute;
  top: 10px;
  left: -200px;
}
```

Jolloin elementille, jonka luokka olisi "jokin-elementti", määritettäisiin siirto pystysuunnasśa 10 pikseliä yläosasta, ja -200 pikseliä sivusuunnassa vasemmalta.

Negatiivisilla arvoilla siirretään elementtiä päinvastaiseen suuntaan, kuin positiivisella arvolla.

Kokeile taas erilaisia arvoja, kunnes löydät sopivan siirtomäärän.

Kannattaa kokeilla arvojen löytämistä selaimen kehittäjän työkaluissa, jossa pääsee nopeasti kokeilemaan eri arvoja, 
ja näkee välittömästi miten elementti niihin reagoi.

Voit myös haluta käyttää saman kaltaista `position: relative;`-sääntöä sivulla.
