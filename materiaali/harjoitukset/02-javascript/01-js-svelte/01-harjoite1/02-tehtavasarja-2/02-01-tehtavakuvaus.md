# Tehtäväsarja 2: tehtäväkuvaus

Alussa kaikkien svelte-kauppa -harjoituskokonaisuuden komponenttien tiedostot ovat tyhjiä.
Tiedostot on kuitenkin luotu etukäteen, 
joten niitä ei tarvitse luoda itse.

Tässä tehtäväsarjassa lisäämme kaikkiin komponentteihin tilanvaraaja (engl. placeholder) sisältöä,
jonka avulla pystymme tarinassa tarkastamaan,
että katselemme oikeaa komponenttia.

Lisäämme siis tässä tehtäväsarjassa jokaiselle komponentille tilapäiseksi sisällöksi kyseisen komponentin nimen.

## Tiedostojen sisältö

Tiedostot löytyvät kansiosta `/harjoitukset/02-javascript/01-svelte`.

## Tehtävä

Lisää kaikkiin komponentteihin kansioissa `teht07` - `teht27`,
kunkin komponentin sisällöksi komponentin nimi `div`-elementin sisälle.

Esimerkiksi `teht07/alarivi.svelte`-tiedoston sisältö näyttäisi tämän jälkeen seuraavalta:

```svelte
<div>
    alarivi
</div>
```

Kun olet saanut komponenteille luotua tällaista tilapäistä tilanvaraajasisältöä, tarkista, että komponenttien sisällöt näkyvät jokaisen komponentin tarinan kohdalla oikein storybookissa.

Nyt jokaisen komponentin tarinassa pitäisi näkyä valkoinen ruutu, jossa lukee komponentin nimi tekstinä.

## Miltä komponentin pitäisi näyttää tehtäväsarjan lopussa?

Kun avaat komponentit storybook:in avulla, niissä pitäisi näkyä vain komponentin nimi.
Mahdollisesti joissain komponenteissa voi näkyä myös teksti "globaalit-tyylit".

Alla on kuvat `alarivi.svelte`-komponentista, mutta myös muiden komponenttien pitäisi näyttää tässä vaiheessa samalta.

Tilanne ennen tehtäväsarjaa ja komponentin nimen lisäystä:

![Tilanne ennen tehtäväsarjaa ja komponentin nimen lisäystä.](/materiaali/kuvat/02-01-svelte/ts00_7_alarivi.png)

Tilanne komponentin nimen lisäyksen jälkeen:

![Tilanne komponentin nimen lisäyksen jälkeen.](/materiaali/kuvat/02-01-svelte/ts02_7_alarivi.png)

### Huomioita ja virhetilanteita

#### `globaalit-tyylit`-teksti ei näy

Jos "globaalit-tyylit"-teksti ei näy, tästä ei kannata huolestua.

Tähän on kaksi vaihtoehtoista syytä:

1. Et ole lisännyt `globaalit-tyylit.svelte`-komponenttiin tekstiä.
2. Osassa tarinoista tarina on konfiguroitu näyttämään komponentin lisäksi myös `globaalit-tyylit.svelte` -komponentti. Mutta näin ei välttämättä ole kaikissa. Erityisesti vanhemmissa versioissa tämä saattaa puuttua osista komponentteja.

#### Sivupalkista puuttuvat kuvassa näkyvät `ts0X`-kansiot

Näyttökuvat on otettu opettajan näkymästä, jossa on normaalista poiketen sivupalkissa ylimääräisiä `ts0X`-kansioita. Näitä ei kuulu näkyä normaalisti.

## Seuraavaksi

Seuraavaksi: [Tehtäväsarja 3](../03-tehtavasarja-3/README.md)
