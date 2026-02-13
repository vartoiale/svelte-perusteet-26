# Merge-konflikteista

Merge-konflikti versionhallinnassa syntyy, 
kun saman tiedoston samaa riviä muokataan samaan aikaan kahdessa eri commitissa, 
jotka eivät ole versionhallinnan historiassa peräkkäisiä.

## Merge-konfliktin synty

Merge-konflikti syntyy, kun käyttäjä vetää palvelimelta versionhallinnan muutokset omalle koneelleen,
ja versionhallinta huomaa, 
että samaan tiedostoon, samoille riveille,
on tehty muutoksia palvelimella ja paikallisesti.

Tämän jälkeen version hallinta keskeyttää merge-toiminnon,
ja pyytää kehittäjää korjaamaan konfliktin.

Github-desktop kiltisti listaa tiedostot, joissa konflikteja löytyy.

## Merge-konfliktin tunnistaminen tiedostossa

Tiedoston sisällä merge-konfliktin tunnistaa ylimääräisistä riveistä: `<<<<<<<<<<`, `=========` ja `>>>>>>>>>`.

```
Koodia ennen merge-konfliktia.
<<<<<<<<<<<
Ensimmäisen haaran muutos.
===========
Toisen haaran muutos.
>>>>>>>>>>>
Koodia merge-konfliktin jälkeen.
```

Nämä ylimääräiset rivit pitää poistaa, jotta merge voi jatkua.

## Merge-konfliktin ratkaisu

Merge-konflikti on ratkaistu, kun edellä mainitut kolme riviä on poistettu.

On kuitenkin tärkeää pohtia, mitkä osat molempien haarojen muutoksista haluaa poimia.

Edellisen esimerkin jälkeen ratkaistu koodi voi näyttää esimerkiksi seuraavilta:

Molemmat muutokset otettu mukaan:

```
Koodia ennen merge-konfliktia.
Ensimmäisen haaran muutos.
Toisen haaran muutos.
Koodia merge-konfliktin jälkeen.
```

tai vain ensimmäiset muutokset:

```
Koodia ennen merge-konfliktia.
Ensimmäisen haaran muutos.
Koodia merge-konfliktin jälkeen.
```

tai vain toiset muutokset:

```
Koodia ennen merge-konfliktia.
Toisen haaran muutos.
Koodia merge-konfliktin jälkeen.
```

Tai muu yhdiste:

```
Koodia ennen merge-konfliktia.
Ensimmäisen ja toisen haaran muutos.
Koodia merge-konfliktin jälkeen.
```

Tämän jälkeen merge pitää vielä viedä loppuun.

Github desktop tunnistaa tiedostojen tallennuksen jälkeen ratkaistut konfliktit, 
ja merkitsee ne ikkunassaan korjatuiksi. 
Lopuksi, kun kaikki on kunnossa, se kertoo, että merge voidaan viedä loppuun.

## Linkit:

*  https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github