# Sovelluksen ajo kehityspalvelimella

Teemme svelte-kauppa -projektin osalta pääasiallisen sovelluskehityksen storybookissa.

Kuitenkin, lopulta, kun haluamme laittaa sivun esille,
teemme tämän julkaisun ilman storybookia.

Jotta voimme tarkastella sivua ensin kehitysympäristössä,
kehityspalvelimella,
meidän pitää käynnistää palvelin kehitysympäristön asetuksilla.

Se onnistuu komennolla:

```sh
yarn run dev-svelte-harjoitukset
```

repositorion juuressa ajettuna.

Tällöin `yarn` käynnistää kehityspalvelimen komennon tulosteen ilmoittamaan porttiin.
Voit tällöin avata kehityspalvelimen selaimessa tuossa portissa.

Esim. jos komennon tuloste ilmoittaa kehityspalvelimen löytyvän portista `5173`, voit avata selaimeen tuon lokaalin portin: [localhost:5173](http:localhost:5173).
Jos tämä sivu ei sinulla näytä mitään, komento saattaa käyttää koneellasi toista porttia.
Tarkista tällöin komennon tuloste.

## Seuraavaksi

Seuraavaksi: [sovelluksen julkaisu](./00-2-4-sovelluksen-julkaisu.md)

