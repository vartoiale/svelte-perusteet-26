# Svelte-projektien julkaisu

Svelte- ja react-projektit pitää erikseen build:ata (siis rakentaa `yarn run build`-komennolla), että ne toimisivat staattisina sivuina.

Tätä varten pitää käyttää [adapter-static](https://svelte.dev/docs/kit/adapter-static) -adapteria, 
jonka avulla sveltekit osaa tehdä projektista ilman palvelinta toimivan.

Lue adapterin toiminnasta svelten dokumentaatiosta, ylläolevasta linkistä, ja ota `adapter-static`-käyttöön projektissasi.

#### sveltekit ja `yarn run build`

Kun adapteri on asetettu kuntoon, pitää sivut vielä rakentaa adapterin avulla.

Aja kyseisen svelte-projektin kansiossa:

```sh
yarn run build
```

## sveltekit ja kuvat

Jotta kuvat ja fontit näkyvät oikein,
niiden pitää löytyä projektin alta `static`-kansiosta.

Tällöin kyseisestä kansiosta löytyvien kuvien käyttö tapahtuu suoraan viittaamalla tiedostojen kansioon ja nimeen, `static`-kansion alla:

```svelte
<!-- kuvan sijaitessa polussa `<projekti>/static/kuva.png` -->
<img src="kuva.png" />

<!-- kuvan sijaitessa polussa `<projekti>/static/kuvat/kuva2.png` -->
<img src="kuvat/kuva2.png" />
```
