# harjoitustöiden julkaisu github-pages -palvelun avulla

Osana tutkinnon osan suoritusta, tutkinnon osan aikana tehdyt isommat projektit julkaistaan github pages -palvelun avulla.
Halutessasi voit kuitenkin käyttää jotain muuta palvelua julkaisuun.

* Repositorio: `ohjelmointi-harjoitukset`
* julkaistu sivusto: `<github käyttäjätunnuksesi>.github.io/ohjelmointi-harjoitukset`

## Repositorion luonti

Luo uusi repositorio: `ohjelmointi-harjoitukset`

Aseta sille julkisuudeksi `public`.

Jos sinulla on github pro -tunnukset, 
voit tehdä repositoriosta myös privaatin. 
Github sallii pro-tunnuksilla github pages -sivujen tekemisen myös privaateista repoista.

Jos sinulla ei ole githubiin pro-tunnuksia, 
joudut tekemään reposta julkisen, 
jotta github antaa tehdä repolle github pages -sivut.

## Github pages -sivujen luonti.

Luo repositoriolle sivut käyttäen github-pages -palvelua.

Ohjeet löytyvät [github-pages -dokumentaation](https://pages.github.com) kohdasta projektit (sivun puolivälistä löytyy valikosta kohta: "projekti").

Kun olet valmis, 
sivusi löytyy osoitteesta `<github käyttäjätunnuksesi>.github.io/ohjelmointi-harjoitukset`.

Asetusten sivu, jossa luot github-sivut näyttää myös tämän sivun, 
kun sivut on luotu. 
Tähän saattaa mennä minuutti.

## Kansiorakenne

Luo kansio `projektit`, ja sille `index.html`-sivu juureen. 

Lisäksi jokaiselle harjoitustyölle oma luodaan kansio. 

Kansiorakenne tulee olemaan seuraava:

```
<komponenttiohjelmointi-harjoitukset>
|
|__ projektit
   |
   |__ html-jimms
      |
   |
   |__ html-yle
      |
   |
   |__ index.html
``` 

## Sivut

Julkaistavat itsenäiset sivut:

1. index.html -sivu juuressa, jossa linkit muihin sivuihin  - sijainti: `/projektit/index.html`

Julkaistavat projektit:

1. jimms (html + css) - kansio: `/projektit/html-jimms`
2. yle (html + css) - kansio: `/projektit/html-yle`

### `index.html`

Sisältää linkit kaikkiin harjoitustöihin, listana.

Sivun ei tarvitse käyttää erillisiä tyylejä. Pelkkä `ul > li > a` -html-rakenne riittää tyylittelyyn.

### Harjoituskohtaiset sivut

Tee muutokset sivuihin classroom repositorion puolella, ja vain kopioi ne tänne.

Tee jokainen projekti omaan kansioonsa yhteisen kansion alle (joko "harjoitukset" tai "projektit").

Nimeä tiedostot:

* `index.html` - html-sivu (html + css -tehtävissä)
* css-tiedoston nimen voit valita itse (html + css -tehtävissä) - ei kuitenkaan kannattane käyttää `teht<numero>.css` -muotoisia tiedostonimiä.

### `.nojekyll`

Github pages käyttää taustalla Jekyll-nimistä staattisten sivujen generoinnin työkalua. 
Ongelmallisesti jekyll sivuuttaa alaviivalla (`_`) varustellut kansiot, koska se olettaa, että ne eivät kuuluu julkaistavaan materiaaliin.

Esimerkiksi sveltekit:llä luotu `build`-kansio sisältää juurikin `_app`-nimisen kansion osana sveltekitin luomaa polkua, 
jota jekyll ei halua näyttää perusasetuksillaan. Tarkoittaen, että kuvat ja css-tiedostot eivät svelte-projekteissa näy,
jos jekyll on käytössä.

Tämän takia repositorion juureen pitää luoda tyhjä tiedosto nimellä `.nojekyll`.
Tiedoston olemassaolo kertoo github-pagesille, 
että sen ei tule käyttää jekylliä, vaan sivut määritellään html-tiedostoina.

**Luo siis juureen tyhjä tiedosto nimellä `.nojekyll`.**
