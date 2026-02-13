# Tehtäväsarja 4: div:in kaltaiset elementit sveltessä

Tässä lyhyessä tehtäväsarjassa teemme svelte-kauppa -sivuston `div`-elementin kaltaisista komponenteista toimivat,
jotta voimme lähteä muotoilemaan niitä.

Haluamme siis tehdä div-elementin kaltaisia elementtejä,
joiden alku- ja lopetustagin väliin määritetään sisältöä:

```svelte
<div>
    sisältö
</div>
```

Tällaisia div-elementin kaltaisia komponentteja on svelte-kauppa -sivustolla kaksi:

* teht21: `AlapalkinOsio.svelte` - vastaa alapalkin osiosta ja sen otsikosta - auttaa tyylittelemään osiot yhtälaisesti
* teht22: `AlapalkinSarake.svelte` - vastaa alapalkin sarakkeiden yhtenevästä leveydestä, käyttäen css-sääntöä `flex: 1;`
