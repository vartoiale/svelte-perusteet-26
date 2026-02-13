# Tehtävä 1: ristinolla

Pelataan ristinollaa.

## Pelin alkuvalmistelu

1. Luokaa toisen pelaajan koneella uusi kansio `merge-conflict-pariharjoitus`-repositorioon, 
nimellä `ristinolla`.
   Kansion polku on siis tällöin `/ristinolla`.
2. Luokaa tiedosto, nimellä `pelit-kierros-1.md`, jossa pelaatte ristinollaa.
   Huomatkaa, että tiedosto on markdown-tiedosto, 
   ja voitte halutessanne lisätä sinne muutakin tekstisältöä.

_Voitte katsoa mallia markdown-syntaksin käytöstä [githubin markdown-ohjeesta](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)_

## `pelit-kierros-1.md`-tiedoston rakenne

Tiedosto saa näyttää miltä tahansa, sisältäen pelin lisäksi markdown-tekstiä, 
mutta sen peliruudukon pitää näyttää seuraavalta:

~~~markdown
# Peli 1

```
   |   |   
--- --- ---
   |   |   
--- --- ---
   |   |   
```
~~~

Peliä pelataan lisäämällä ristiä ja nollaa ruutuihin, 
yksi merkki vuorollaan.

~~~markdown
```
   |   |   
--- --- ---
   | o |   
--- --- ---
   |   |   
```
~~~

~~~markdown
```
   |   |   
--- --- ---
   | o |   
--- --- ---
   | x |   
```
~~~

## Pelin kulku: peli 1

Peliin liittyykin kuitenkin käänne:

1. Pelaatte yhdessä peliä, samaan aikaan, kahdella koneella. 
   Lisähuomiona, molemmat pelaavat yhdessä.

Kun olette tehneet siirron,
siis muokanneet tiedostoa,
tallentaneet sen,
ja kommitoineet muutoksen,
siirtäkää muutos palvelimelle.

Seuraavan siirron teette toisella koneella.

Ladatkaa muutokset palvelimelta kuitenkin vasta aina siirron tehtyänne.

Tällöin on mahdollista, että siirto tuottaa merge-konfliktin.

Pyrkikää tarkoituksella aiheuttamaan merge-konflikteja.

Yleensä merge-konflikti syntyy, 
kun laitatte peräkkäiset siirrot samalle riville.

# Seuraava peli

Kun olette saaneet ensimmäisen pelin pelattua, lisätkää tiedostoon uusi otsikko, ja uusi peli otsikon alle:

~~~markdown
## Peli 2

```
   |   |   
--- --- ---
   |   |   
--- --- ---
   |   |   
```
~~~

### Pelin kulku: peli 2

Uusi käänne:

1. molemmat pelaavat peliä omalla koneellaan, samanaikaisesti. 
Siirtäkää (engl. push) muutokset kuitenkin palvelimelle, vasta kun molemmat ovat tehneet siirtonsa,
ja ladatkaa ne palvelimelta samaan aikaan.

Tällöin merge-konfliktin mahdollisuus kasvaa.

# Pelit 3 ->

Pelatkaa peliä useampaan kertaan, kunnes saatte tarpeeksi merge-konflikteja aikaiseksi.

Laittakaa jokainen peli oman otsikkonsa alle, samaan tiedostoon.
