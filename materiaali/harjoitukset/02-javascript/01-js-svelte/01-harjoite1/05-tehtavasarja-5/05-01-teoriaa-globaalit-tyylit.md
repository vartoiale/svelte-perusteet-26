#### Teoria: globaalit tyylit sveltessä

##### Taustaa ja filosofisempaa pohdintaa komponenttien rajat rikkovista muokkausoperaatioista

Svelte mahdollistaa globaalien tyylien asettamisen mistä komponentista tahansa käsin.
Lähtökohtaisesti tämä on kuitenkin huono idea, 
ja elementtien pitäisi pääasiallisesti itse vastata omista tyyleistään.

Komponenttien keskeinen idea on, että ne ovat tavallaan mustia laatikoita,
joiden toiminnan ei pitäisi välittyä toisille komponenteille.
Tästä johtuen, muiden komponenttien ei pitäisi pystyä suoraan vaikuttamaan toisten komponenttien tyyleihin.

Tässä yhteydessä käytämme kuitenkin svelten työkaluja globaalien tyylien asettamiseen hienotunteisesti.

Seuraavissa tehtävissä tulemme pääasiallisesti lisäämään tässä tehtävässä määritetyn `globaalit-tyylit.svelte`-komponentin avulla juurielementille erilaisia avustavia tyylejä.

Tulemme mm. määrittämään css-muuttujia, joita komponentit voivat itse halutessaan käyttää.

Emme siis tule muokkaamaan muiden komponenttien tyylejä suoraan, 
vaan vain tarjoamaan niille mahdollisuuden tulla muokatuksi.

##### `:global`-määre sveltessä

Svelte tarjoaa globaalien tyylien muokkaukseen `:global`-määreen, 
jonka avulla voidaan määrittää komponentin sisällä määritetty css-valitsin kohdistumaan komponentin ulkopuolisiin elementteihin - siis toisten komponenttien omistamiin elementteihin.

Sen käyttö on yksinkertaisehkoa:

```svelte
<style>
  :global(:root) {
    color: black;
  }
</style>
```

Edellä asetamme juurielementille, ja kaikille sen lapsille tekstinväriksi mustan.

## Seuraavaksi

Seuraavaksi: [tehtäväsarja 5: tehtäväkuvaus](./05-02-tehtavakuvaus.md)
