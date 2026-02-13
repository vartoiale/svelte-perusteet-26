# Sovelluksen julkaisu

Sovelluksen julkaisua varten joudumme käyttämään vielä yhtä uutta komentoa:

```sh
yarn run build-svelte-harjoitukset
```

Komento luo `build`-kansion

Voit kopioida tämän `build`-kansion sisällön palvelimellesi.

Huomioi kuitenkin,
että oletuksena sovellus odottaa, että se tarjoillaan sijainnista: `BASE_PATH_ASSETS="/ohjelmointi-harjoitukset/projektit/svelte-kauppa"`

Voit muokata tätä polkua muokkaamalla `.env.prod`-tiedostoa (sijainnissa: `/harjoitukset-apu/.env.prod`).

Tiedoston sisältö on oletuksena:

```env
BASE_PATH_ASSETS="/ohjelmointi-harjoitukset/projektit/svelte-kauppa
```

Tällöin se toimii automaattisesti `ohjelmointi-harjoitukset`-repositorion github-sivujen kanssa, jotka ovat muotoa: `<käyttäjänimi>.github.io/ohjelmointi-harjoitukset`.

Aseta siis `BASE_PATH_ASSETS`-ympäristömuuttujan arvo vastaamaan tarjoilusijaintia domainin juuresta lähtien, aina sovelluksen sijoituspaikkaan asti.

## Seuraavaksi

Seuraavaksi: [Tehtäväsarja 1: svelten lyhyet alkeet](../01-tehtavasarja-1/README.md)
