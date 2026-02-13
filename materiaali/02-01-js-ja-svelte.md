# Teoria 2.1: javascript ja Svelte-sovelluskehys

Seuraavaksi lähdemme tutustumaan javascriptiin komponenttikirjasto Svelte:n avulla.

## Svelte

Svelte on melko helposti lähestyttävä sovelluskehys (engl. framework).

Se muistuttaa läheisesti jo tuntemaamme html-dokumenttia, 
jonka tiedosto pääte vain on muutettu muotoon `.svelte`, 
ja html-syntaksin päälle on lisätty hieman Svelten omaa syntaksia.

Lyhykäisyydessään yksinkertainen Svelte-tiedosto näyttää seuraavalta:

`Heippa.svelte`:

```svelte
<h1>Tervehdys, hyvä maailma!</h1>
```

Se näyttää selaimessa otsikon tekstillä "Tervehdys, hyvä maailma!",
juuri niin kuin html-dokumentiltakin saattaisi odottaa.

Vähän monimutkaisempi svelte-komponentti saattaisi näyttää seuraavalta,
sisältäen nyt javascriptiä ja css-tyylejä.

`Heippa-js-css.svelte`:

```svelte
<script>
  // tässä on javascriptiä
  console.log("Heippa, maailma!")
</script>

<style>
  h1 {
    color: red;
  }
</style>


<h1>Tervehdys, hyvä maailma!</h1>
```

Sekin on edelleen pitkälti saman näköistä kuin vastaava html-dokumentti olisi:

* `script`-elementti mahdollistaa javascriptin liittämisen myös html-dokumenttiin - emme tosin ole vielä käyttäneet tätä, mutta se toimisi silti html-dokumentissakin,
* `style`-elementti mahdollistaa css-tyylien määrittämisen osana html-dokumenttia - tätäkään emme ole käyttäneet, mutta sekin toimii html-dokumentin sisällä.

Tämä svelte-komponentti näyttää selaimessa tekstin "Tervehdys, hyvä maailma!", punaisella kirjasimella.
Sen lisäksi se javascriptin avulla kirjoittaa selaimessa sivun kehittäjätyökaluista löytyvään konsoliin tekstin "Heippa, maailma!".

Tulemme myöhemmin käyttämään paljonkin tätä javascript komentoa `console.log()`, ja sen kykyä tulostaa kehityksessä apuna käytettäviä viestejä konsoliin.

Huomaamme komponentin syntaksista nopeasti myös, että svelte-komponentti ei sisällä ollenkaan `html`-, `head`- tai `body`-elementtejä.
Toisaalta, eipä näitä oikeastaan tarvitse käyttää html-dokumenteissakaan, kuten jo tiedämmekin.

Svelte olisi siis hyvin tutun oloinen.

Sen takia se sopiikin hyvin ensimmäiseksi kosketukseksi javascript-maailmaan.

Erojakin kuitenkin löytyy. 
Esimerkiksi se, miten svelte-komponentti käynnistetään kehitysympäristössä.

## Svelteä ajetaan noden avulla

Suuri ero html-dokumentin ja svelte-komponentin välillä on siinä miten svelte-komponenttina määritelty sivu käynnistetään selaimeen katseltavaksi.

Loppukäyttäjälle eroa ei näy, koska molempia jaellaan lopulta verkossa sijaitsevilta palvelimilta.
Web-kehittäjälle ero kuitenkin jo näkyy, 
sillä svelteä varten pitää pystyttää palvelin jo kehitysvaiheessa.

Siinä missä html-dokumentti oli mahdollista avata helposti vain avaamalla `.html`-tiedosto tiedostoselaimesta internet-selaimeen,
joudummekin svelteä varten käynnistämään palvelimen, 
joka kääntää svelte-koodimme selaimen ymmärtämäksi oikeaksi html:ksi, css:ksi ja javascriptiksi.

Näin alkuvaiheessa harjoitusten kansioon on jo valmiiksi lisätty vaadittavat tiedostot, 
jotta svelten käynnistäminen onnistuu helposti.

Hieman myöhemmin opettelemme itse konfiguroimaan svelte-projektin, 
jotta saamme sen käynnistettyä haluamillamme asetuksilla.

Näin alkuun menemme kuitenkin valmiilla asetuksilla.

### Node.js:n asennus

Node.js:n voi asentaa osoitteesta: [nodejs.org](https://nodejs.org).

## Svelte helpottaa javascriptin käyttöä html-dokumentin sisällön muokkaamisessa

Kuitenkin kehityksessä tapahtuvaa käynnistystavan muutosta suurempi ero on svelten kyky muokata html-dokumentin sisältöä javascriptin avulla.

Tämä onkin se oikea syy, miksi svelteä lähdemme opettelemaan.

Aiemmassa svelte-komponentissa javascriptiä käytettiin konsoliin viestin tulostamiseen.
Sillä voi kuitenkin tehdä muutakin.

Sveltellä voidaan määrittää javascriptissä arvoja, ja sen jälkeen näitä arvoja voidaan käyttää html-osion sisällä.
Tältä osin syntaksi poikkeaa html:n syntaksista.

```svelte
<script>
    let tervehdittävä = "muailma"
</script>

<h1>Tervehdys, {tervehdittävä}!</h1>
```

Tässä määritämme javascriptin puolella `tervehdittävä` nimisen muuttujan ja annamme sille arvoksi merkkijonon.

Sen jälkeen käytämme `tervehdittävä`-muuttujaa html-osion puolella.

Tässä vaiheessa ei tarvitse vielä ymmärtää, mitä javascript-osio tarkoittaa.

Tärkeää on vain havaita, että `tervehdittävä`-nimi löytyy javascript-osiosta (`script`-elementin sisältä), sekä aaltosulkeiden sisältä `h1`-elementin sisältä.

Tässä esimerkissä `h1`-elementin sisältä löytyvä aaltosulje-syntaksi (`{...}`) onkin osa svelten lisäämää omaa syntaksia, joka ei suoraan kuulu html:n syntaksiin.
Tarkennuksena vielä, että se ei myöskään ole javascript-syntaksia, vaan tosiaan ihan svelte:n omaa syntaksia.

(Voit kurkata javascript-syntaksia osiosta: [`/materiaali/kaytanto/javascript-repl.md`](/materiaali/kaytanto/javascript-repl.md).)

## Svelte ja vscode

Sveltelle löytyy vscode:en lisäosa, joka osaa värjätä svelte-tiedostojen syntaksin:

https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode

Se kannattaa asentaa vscode:en, kehityksen helpottamiseksi.

Asentaessasi lisäosaa, varmista, että olet asentamassa juuri oheisen lisäosan, 
etkä vain jotain toista vähän samannimistä lisäosaa.
Vertaa lisäosan nimeä, ja sen kehittäjän nimeä, sivulla ja vscode:ssa.
