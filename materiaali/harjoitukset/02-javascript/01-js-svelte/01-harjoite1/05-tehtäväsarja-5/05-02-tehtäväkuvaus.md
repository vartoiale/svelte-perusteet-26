# Tehtäväsarja 4: Tehtävä 1

**palautettavien tiedostojen ja kansioiden nimet:** 

* tiedosto: `teht28/globaalit-tyylit.svelte` (kansiossa: `harjoitukset/02-javascript/01-svelte/teht28/globaalit-tyylit.svelte`)

Huomaa, että tälle tehtävälle ei ole olemassa erillisiä tarinoita storybookin puolella,
vaan muutokset näkyvät muiden tehtävien osana tehdyissä komponenteissa.

Tässä tehtävässä määritämme komponentin, joka vastaa globaalien tyylien määrittämisestä.
Globaaleja tyylejä voi määrittää mistä tahansa komponentista käsin, 
mutta tässä teemme niitä varten yhden erillisen tiedoston,
jotta ne tulisi määritettyä yhdestä ja samasta paikasta.


#### Tehtävänanto

Asetetaan yleisimmät globaalit tyylit komponenteille:

1. nollataan css-säännöt
2. asetetaan yleisesti elementeille `border-box: box-sizing`

## Alitehtävä 1: css-sääntöjen nollaus

Lisää komponenttiin yleiset css-tyylit, joilla sivulta poistetaan selaimen tyypillisimmät muotoilut.

Tehdään siis niin sanotusti tehdasalustus css-säännöille (engl. css reset).

Poista muotoilut seuraavilta elementeiltä:

* `body`
* `h1`, `h2`, `h3`, `h4`, `h5`, `h6`
* `ul`, `ol`
* `a` (käytä pseudoluokkaa `:any-link`)

Voit myös poistaa säännöt muilta elementeiltä.

Nollattavia sääntöjä ovat ainakin `margin` ja `padding`.

Linkeiltä kannattaa poistaa ainakin alleviivaus.

## Alitehtävä 2: `box-sizing: border-box`

Asetetaan tälläkin kertaa kaikille elementeille `box-sizing: border-box` -sääntö:

```css
* {
  box-sizing: border-box;
}
```

## Alitehtävä 3: muut yhteiset tyylit

Voit itse lisäillä haluamasi globaalit tyylit `globaalit-tyylit.svelte`-komponenttiin.
Voit tehdä lisäykset saman tien,
tai sitä mukaan, 
kun ne tulevat sivua rakentaessasi ajankohtaisiksi.

Tällaisia tyylejä voivat olla esimerkiksi:

* kirjasimen lataus ja käyttö,
* css-muuttujien määrittäminen `:root`-elementissä,
* yhteiset responsiiviset tyylit

## Seuraavaksi

Seuraavaksi: [globaalit tyylit käyttöön sivulla](./04-03.md)
