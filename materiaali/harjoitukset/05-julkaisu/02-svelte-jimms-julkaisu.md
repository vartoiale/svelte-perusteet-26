# svelte-jimms

Sveltellä tehtyjen jimms-sivujen rakentamista varten on tehty valmiiksi tarvittavat konfiguraatiot,
ja niiden rakentaminen pitäisi onnistua ilman konfigurointia.

Huomaa, että svelte-jimms on konfiguroitu sillä oletuksella, että sivut löytyvät polusta `/komponenttiohjelmointi-harjoitukset/projektit/svelte-jimms`.
Tarkoittaen, että repon nimi on `komponenttiohjelmointi-harjoitukset` ja projekti löytyy siinä kansiosta `/projektit/svelte-jimms`.
Jos näin ei ole, joudut konfiguroimaan tiedostoa `/harjoitukset-apu/svelte.config.js` 
ja asettamaan sen `config.kit.paths.base`-kentän vastaamaan oikeaa polkua.

Sveltekit luo `yarn run build`-komennolla `build`-nimisen kansion `harjoitukset-apu`-kansion alle (löytyy siis polusta `/harjoitukset-apu/build`).

Voit myös ajaa repositorion juuressa:

```
yarn run build-svelte-harjoitukset
```

joka tekee saman asian.

## svelte-jimms ja kuvat

Jotta kuvat ja fontit näkyvät oikein,
niiden pitää löytyä kansiosta [`/harjoitukset-apu/static`](/harjoitukset-apu/static).

Voit lukea tämän kansion käytöstä lisää sen [README.md](/harjoitukset-apu/static/README.md)-tiedostosta.

## Build-kansion luonti

1. mene komentorivillä `/harjoitukset-apu`-kansioon,
2. aja `yarn run build`.

Jos kaikki menee hyvin, tämä luo `build`-kansion (`/harjoitukset-apu/build`). 

Jos komento ilmoittaa virheitä, yritä korjata nämä virheet, ja aja `yarn run build`-komento uudelleen.

Voit vielä tarkistaa, että luotu build-kansio toimii, ajamalla `yarn run preview`-komennon samassa kansiossa (`/harjoitukset-apu`).

## Seuraavaksi

Seuraavaksi [svelte julkaisu yleisesti](/materiaali/harjoitukset/05-julkaisu/03-svelte-julkaisu-yleisesti.md).
