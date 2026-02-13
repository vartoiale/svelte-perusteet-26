# 3.3 Dynaaminen html

## Tehtävät

### Tehtävien palautus

Tee uusi kansio: `03-3-dynaaminen-html` (`/harjoitukset/01-html-ja-css/03-3-dynaaminen-html`).

Luo taas jokaista tehtävää varten uudet html- ja css-tiedostot.

Nimeä tiedostot muotoon:

* `tehtXX.html`,
* `tehtXX.css`,

missä `XX` on tehtävän numero.

### Tehtävä 1 - popover

Html tarjoaa useamman modernin rajapinnan elementtien näyttämiseen dynaamisesti, ilman javascriptia tai css:ää.

Yksi tällainen rajapinta on [`popover`](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/popover).

`popover` nostaa muiden elementtien yläpuolelle `popover`-attribuutilla varustetun elementin, kun käyttäjä painaa tähän `popover`-elementtiin kohdistettua nappia.

Yksinkertaisuudessaan `popover` näyttää seuraavalta:

```html
<button popovertarget="popover-kohteen-id">Avaa</button>

<div popover id="popover-kohteen-id">Elementti joka tulee näkyville nappia painamalla.</div>
```

`popover` ei näytä `popover`-attribuutin elementtiä sen omalla paikalla, vaan nostaa sen kaikkien muiden elementtien yläpuolelle, ja keskittää sen sivulle.

Se sopii siis hyvin erilaisten popover-ikkunoiden toteuttamiseen.

Jos popover-ikkunan ulkopuolelta painetaan, popover-ikkuna sulkeutuu itsestään.

Esimerkiksi jimm's:in sivuilla oleva hampurilaismenu, 
voidaan laittaa avautumaan ja sulkeutumaan käyttäen `popover`-toiminnallisuutta.

Popover sallii myös saman elementin avaamisen ja sulkemisen useammasta eri napista:

```html
<button popovertarget="popover-kohteen-id">Avaa</button>

<div popover id="popover-kohteen-id">
    <button popovertarget="popover-kohteen-id">X</button>

    <div>Elementti joka tulee näkyville nappia painamalla.</div>
</div>
```

#### `command` ja `commandfor`

`popover`:in lisäksi selaimiin on piakkoin tulossa sen laajennettu versio `command`- ja `commandfor`-attribuuttien muodossa.

Voit lukea lisää aiheesta [chromen kehittäjä-blogista](https://developer.chrome.com/blog/command-and-commandfor?hl=en).
