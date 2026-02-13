# Yleisiä korjauksia väärinkäsityksiin harjoituksessa 2

Alla on joitain yleisiä väärinkäsityksiä, jotka toistuvat monella.
Kaikki näistä eivät ole väärinkäsityksiä, vaan osa näistä korjauksista on vain parempia tapoja tehdä asioita.

Lukaiskaapa nämä läpi, ja korjatkaa vastaavat kohdat omasta koodistanne, jos itseltänne näitä löytyy.

## muu kuin `li` elementti `ul`-elementin sisällä

### virhetilanne: `h2`-elementti `ul`-elementin sisällä

Hyvin usein toistuvana virheenä, tehtävän 7 jälkeen, 
monella oli `h2`-elementti päätynyt `ul`-elementin sisälle, yhdessä tai useammassa kohdassa sivua.

Kun ennen tehtävää, esimerkiksi info-osio näytti seuraavalta:

```html
<div class="sarake">
  <h2>Info</h2>
  <div>Yhteystiedot</div>
  <div>Toimitustavat</div>
  <div>Maksutavat</div>
  <div>Takuupalautus</div>
  <div>Palautus ja huolto</div>
  <div>Usein kysytyt kysymykset</div>
  <div>Yritysmyynti</div>
  <div>Maksutavat</div>
  <div>Ura</div>
  <div>Tuoteturva</div>
</div>
```

Oli se monella muuttunut virheelliseen muotoon:

```html
<!-- VÄÄRIN -->
<ul class="sarake">
  <h2 class="rivi">Info</h2>
  <li class="rivi">Yhteystiedot</li>
  <li class="rivi">Toimitustavat</li>
  <li class="rivi">Maksutavat</li>
  <li class="rivi">Takuupalautus</li>
  <li class="rivi">Palautus ja huolto</li>
  <li class="rivi">Usein kysytyt kysymykset</li>
  <li class="rivi">Yritysmyynti</li>
  <li class="rivi">Maksutavat</li>
  <li class="rivi">Ura</li>
  <li class="rivi">Tuoteturva</li>
</ul>
```

Tämä on kuitenkin väärin, koska nyt `h2`-elementin sisällään pitävä otsikko on listan sisällä. 

Tämä on virheellistä:

* semanttisesti: otsikko ei ole osa listaa, se ei ole sivun sisällä samanarvoinen muiden listattujen asioiden kanssa
* teknisesti: `ul`-elementin sisällä ei pitäisi olla `h2`-elementtejä

### taustaa

Pääasiallisesti `ul`-elementin sisällä ei kuitenkaan pitäisi olla muita elementtejä kuin `li`-elementtejä.

Tähän poikkeuksena ovat toiset `ul`- ja `ol`-elementit, sisäkkäisiä listoja luodessa.

### Korjaus: luodaan uusi `ul`-elementti ympäröimään vain listalle kuuluvia elementtejä

Sen sijaan, että vain vaihdettaisiin ylempi `div`-elementti `ul`-elementiksi, 
meidän pitääkin luoda uudelleen nimettyjen `li`-elementtien ympärille uusi `ul`-elementti.

```html
<!-- OIKEIN -->
<div class="sarake">
  <h2 class="rivi">Info</h2>
  <ul class="sarake">
    <li class="rivi">Yhteystiedot</li>
    <li class="rivi">Toimitustavat</li>
    <li class="rivi">Maksutavat</li>
    <li class="rivi">Takuupalautus</li>
    <li class="rivi">Palautus ja huolto</li>
    <li class="rivi">Usein kysytyt kysymykset</li>
    <li class="rivi">Yritysmyynti</li>
    <li class="rivi">Maksutavat</li>
    <li class="rivi">Ura</li>
    <li class="rivi">Tuoteturva</li>
  </ul>
</div>
```
