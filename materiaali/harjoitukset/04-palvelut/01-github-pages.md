# Github pages -sivut, käyttäjäprofiilit ja github CV:nä

Tänä päivänä yksi tärkeimmistä ohjelmoijan taitojen esittelyyn käytetyistä työkaluista on github.

Github tarjoaa useamman eri tavan jaella sisältöä:

* repositoriot
* github pages -sivut
* käyttäjäprofiilit

Olemmekin jo pienimuotoisesti, tämän repositorion puitteissa,
tutustuneet githubin repositorioiden toimintaan.

Seuraavissa tehtävissä tutustumme paremmin 
kahteen jälkimmäiseen kohtaan edellisellä listalla:
github pages -sivuihin ja githubin tarjoamaan käyttäjäprofiiliin.

Aloitamme käyttäjäprofiilin luonnista.

## Tehtävä 1 - github käyttäjäprofiilin README-tiedoston luonti

### Tehtävänanto

Tässä tehtävässä lisäämme githubin käyttäjäprofiiliisi lyhyen kuvauksen.

1. luo githubissa uusi repositorio: repositorion nimen tulee olla sama kuin githubin käyttäjätunnuksesi.
2. Määritä repositorio julkiseksi (engl. public)
3. lisää tähän uuteen repositorioon `README.md`-tiedosto
4. Tyhjennä `README.md`-tiedostosta kaikki teksti, joka siinä mahdollisesti valmiiksi on (jos loit `README.md`-tiedoston osana repositorion luontia)

Seuraavassa tehtävässä lähdemme tutustumaan markdown-syntaksiin, 
jota käytetään README.md -tiedoston muotoiluun.

### Lisää tietoa githubin käyttäjäprofiilista

Linkkejä:

* [yleistä githubin profiilisivusta](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/about-your-profile)
* [ohjeet profiilisivun readme:n luomiseen](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
* [ohjeet profiilin täyttämiseksi](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/quickstart-for-writing-on-github)

## Tehtävä 2 - markdown-syntaksi

Github käyttää sivuillaan tekstitiedostojen määrittelyyn markdown-formaattia.

Markdown on yksinkertainen tyylittelymuoto, joka näyttää raakatekstimuodossaan lähestulkoon samalta,
miltä se näyttää myös hahmonnettuna (engl. render).

Esimerkiksi tämä `01-github-pages.md`-tiedosto on kirjoitettu käyttäen markdown-syntaksia.

Myös edellisessä tehtävässä luotu `README.md`-tiedosto käyttää markdown-syntaksia.

Markdown-tiedostojen tiedostopääte onkin juuri edellisissä tiedostonimissä näkynyt `.md`.

Tässä tehtävässä harjoittelemme pikaisesti markdown-syntaksia.

Voit hypätä tämän tehtävän yli, jos koet jo osaavasi käyttää markdown-syntaksia.

### Tehtävänanto

#### Alustavat toimenpiteet

Olet tähän mennessä luultavasti jo ehtinyt luoda, 
TÄHÄN classroom-repositorioon, 
`projektit`-kansion alle vähintään yhden projektikansion
tekemääsi projektia varten.

Jos et vielä ole ehtinyt näin tehdä, luo uusi kansio `projektit`-kansion alle tätä tehtävää varten.

Luomme kohta kyseisen kansion alle harjoittelua varten README.md-tiedoston.

Tarkoituksena on siis harjoitella tässä repositoriossa markdown:in käyttöä,
ennen julkisen profiilin kirjoittamista markdownia käyttäen.

#### Markdown-tiedostojen esikatselu

##### Markdown-tiedostojen muokkaus github.com-sivustolla selaimessa

Tämä tehtävä kannattaa tehdä githubin nettisivujen puolella, 
jossa pystyy luomaan uusia tiedostoja painamalla etusivulla `+`-nappia.
Tiedoston sijainnin vaihtaminen githubin sivujen tekstieditorissa
onnistuu lisäämällä `/`-viivalla eroteltuna kansioiden nimiä tiedoston polkuun, ennen tiedoston nimeä.
Uusia sivuja voi myös luoda suoraan githubin sivujen kansiosivuilta löytyvän ``-napin avulla kyseiseen kansioon.

##### Markdown-tiedostojen muokkaus vscodessa

Vaihtoehtoisesti voit käyttää README.md-sivun hahmonnetun version näyttämiseen myös vscoden "preview"-näkymää.
Sen saa yleisimmin auki klikkaamalla oikealla hiirennäppäimellä markdown-tiedoston nimeä vscoden-tiedostopuunäkymässä,
ja valitsemalla `preview file`-valinnan (voi olla myös jollain muulla kirjoitusasulla).

##### Markdown-tiedostojen muokkaus muissa tekstieditoreissa

Myös monille muille IDE:ille yleensä löytyy jonkinlainen markdown-esikatselutila.

Jos omasta tekstieditoristasi ei markdown-esikatselutilaa löydy, 
kannattaa tämä tehtävä tehdä github.com:in puolella selaimessa.

#### Tehtävät

1. Lue githubin lyhyet [markdown-ohjeet](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
1. Lisää johonkin `projektit`-kansion alla olevaan kansioon `README.md`-tiedosto,
ja kirjoita siihen kuvaus kansion sisältämästä projektista.
2. Käytä `README.md`-tiedostossa kaikkia 

### Lisää tietoa

Linkkejä:

* [githubin markdown-ohjeet](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## Tehtävä 3 - githubin käyttäjäprofiilin README-tiedoston täyttäminen

Nyt kun olet luonut käyttäjäprofiilin README-tiedoston 
ja sille repositorion (repositorion nimenä piti olla github-käyttäjänimesi),
sekä tutustunut markdown-syntaksiin,
lähdemme täyttämään README-tiedostoa.

### Missä sijaitsee githubin käyttäjäprofiili ja sen README

Githubin käyttäjäprofiili löytyy osoitteesta `github.com/<github-käyttäjätunnus>`.

Esimerkiksi oma käyttäjäprofiilini, käyttäjätunnuksella "gratoiale", 
löytyy osoitteesta [github.com/gratoiale](https://github.com/gratoiale). 
Vastaavasti sen julkinen repositorio löytyy osoitteesta https://github.com/gratoiale/gratoiale

Löydät profiilisi myös klikkaamalla githubissa oikean yläkulman käyttäjäkuvaasi,
ja valitsemalla pudotusvalikosta "your profile"-valinnan.

Avaa siis käyttäjäprofiilisi. 

Jos olet jo tallentanut tehtävässä 1 luomaasi `README.md`-tiedoston,
sen pitäisi näkyä profiilisi yläosassa `<github-käyttäjätunnus>/README.md`-otsikon alla.

Jos jätit tiedoston tyhjäksi, voi olla, että github ei näytäkään sitä vielä profiilissasi.

Tässä tehtävässä tarkoituksesi olisi lisätä sisältöä github käyttäjäprofiilisi `README.md`-osioon.

### luotujen repositorioiden julkisuudesta

Huomaa, että koska kaikki näissä tehtävissä luotavat sisällöt ovat julkisia, 
myös näiden sisältöjen määrittämiseen käytetyt repositoriot ovat pääsääntöisesti julkisia.
Maksaville käyttäjille github kuitenkin tarjoaa mahdollisuuden luoda github pages -sivuja myös yksityisistä repositorioista käsin.

### Mitä profiiliin kannattaa laittaa

Github-profiilisi kannattaa pitää lyhyenä ja ytimekkäänä, 
ja sisällöissä kannattaa pitäytyä ohjelmointiin liittyvässä informaatiossa.

Profiiliin ei lähtökohtaisesti kannata laittaa itsestään mitään henkilökohtaista tietoa.

Kannattaa kertoa lyhyesti ohjelmointiosaamisestaan, ohjelmoinnin osalta kiinnostuksen kohteistaan,
sekä lisätä tärkeitä täkyjä omista github-sisällöistään.

### Tehtävänanto

Käytä uusia, tai vanhoja, markdown-taitojasi ja täytä profiilisi README.md osio informaatiolla.

Jos tuntuu, että et halua vielä lisätä tällaista osiota profiilisi, 
voit tässä vaiheessa jättää sen tyhjäksi.

Suosituksena kuitenkin olisi kertoa ammatillisesta itsestäsi hieman jotain:
esimerkiksi, että opiskelet sovelluskehittäjäksi, 
ja kenties hieman jotain pääasiallisista ohjelmointitaidoistasi, tai näyttävistä työnäytteistäsi.

Voit esimerkiksi linkata profiilistasi johonkin tässä tutkinnon osassa tekemääsi projektiin, 
jonka olet viimeistellyt julkaisukuntoiseksi (muista mm. responsiiviset tyylit).

Profiili kannattaa pitää lyhyenä ja ytimekkäänä, ja ennen kaikkea [asiallisena](https://www.youtube.com/watch?v=ZRzxJZrm3iU), 
mutta tekstiä ryydittämään voi käyttää pieniä kuvia (esim. ohjelmointikielten logoja) ja emojia :sparkles:.

#### Linkitä tekemiisi sivuihin

Voit esimerkiksi linkittää tekemiisi sivuihin.

Tällöin profiilisi readme.md -osio voi sisältää esimerkiksi seuraavankaltaisen osion:

```markdown
# Tekemiäni sivuja:

* jimms (footer, header) - [demo](<demo-url>) - [repositorio](<repositorio-url>) - [referenssi](jimms.fi) :page_facing_up:
* yle.fi (etusivun yläosa) - [demo](<demo-url>) - [repositorio](<repositorio-url>) - [referenssi](yle.fi) :page_facing_up:
* abstract - [demo](<demo-url>) - [repositorio](<repositorio-url>) - [referenssi](https://www.frontendpractice.com/projects/abstract) :postbox:
```

Tämän jälkeen voit lisätä lyhyen osion jossa selität käytettyjä emojeja (emojit kannattaa valita paremmin):

```markdown
Edellisessä emojit merkitsevät seuraavaa:

* :page_facing_up: - referenssisivuna toimi normaali verkkosivu
* :postbox: - referenssinä toimi frontendpractice.com:in projektisivu
```

Tai muuten ilmaista, mitä olet käyttänyt projekteissa referenssinä.
 
Kannattaa huomioida, että jokainen edellä olevista esimerkeistä sisälsi neljä tärkeää tietoa:

* nimi (toimii samalla myös erittäin lyhyenä projektin kuvauksena)
* demo-sivu, jossa käyttäjä voi itse tarkastaa tuotoksen (eli siis itse verkkosivu, selaimessa käytettävässä muodossa)
* repositorio (paikka, josta lähdekoodi löytyy)
* referenssi (tieto siitä, mitä oli tarkoitus saada valmiiksi - siis vertailukelpoinen näyttö siitä, että olet saanut aikaiseksi sen mitä lähdit tekemäänkin.)

Viimeisin, eli referenssi on erityisen tärkeä muistaa lisätä mukaan, 
sillä se asettaa riman, jota vastaan pystyt osoittamaan osaamistasi.

## Tehtävä 4 - github pages -sivu github käyttäjätunnuksellesi

Github tarjoaa kahta erilaista github pages -sivua:

* käyttäjätunnuksille - osoite muotoa: `<github-käyttäjätunnus>.github.io`,
* repositorioille - osoite muotoa: `<github-käyttäjätunnus>.github.io/<repositorion nimi>`.

Huomaa, että käyttäjien sivujen url on muusta github.com-sivustosta poiketen domainin `github.io` alla.

Eli kun käyttäjäprofiili löytyy osoitteesta `github.com/<github-käyttäjätunnus>`, 
löytyy käyttäjän sivu osoitteesta `<github-käyttäjätunnus>.github.io`.

Vastaavasti repositorio löytyy osoitteesta `github.com/<github-käyttäjätunnus>/<repositorion nimi>`, 
löytyy repositorion sivu osoitteesta `<github-käyttäjätunnus>.github.io/<repositorion nimi>`.

Käytännössä nämä github pages -sivutyypit (käyttäjäsivut, reposivut) 
ovat ominaisuuksiltaan suurin piirtein samanlaiset. 
Niiden suurin ero on niiden url-osoitteessa, sekä vähän siinä missäpäin repoa sivut sijaitsevat.

Tässä tehtävässä teemme käyttäjätunnuksellesi sivut.

### Tehtävänanto

Tee omille github käyttäjätunnuksellesi sivut:

1. Lue github pages -sivujen ohjeet osoitteesta [pages.github.com](https://pages.github.com/),
2. luo uusi repositorio muotoa `<github-käyttäjätunnus>.github.io`, esim. omalla käyttäjätunnuksellani "gratoiale" tämä nimi olisi `gratoiale.github.io`,
3. Seuraa ohjeita pages.github.com -sivuilta

pages.github.com -sivulla käyttäjäsivujen ohjeet löytyvät "user or organization site"-otsikon alta.

Voit tältä osin lisätä sivuille haluamaasi sisältöä, tai voit jättää sen halutessasi vielä tyhjäksi.

Kokeile kuitenkin lisätä sivulle sekä html:ää, että tyylejä css:llä, jotta tiedät miten se tapahtuu.

Huomaa, että sivujen päivittymisessä kestää hetken, yleensä vajaan minuutin verran, 
siitä kun commitoit muutokset, ja pushaat ne githubin palvelimille.

Voit kurkata miten sivujen sisältö yksinkertaisimmillaan onnistuu sivuiltani (gratoiale.github.io):

* repo: [github.com/gratoiale/gratoiale.github.io](https://github.com/gratoiale/gratoiale.github.io)
* sivut: [gratoiale.github.io/](https://gratoiale.github.io/)

Jos laitoit sivulle järkevää sisältöä, ja sait sen viimeisteltyä, 
voit lisätä linkin siihen käyttäjäprofiilisi `README.md`-osioon.

## Tehtävä 5 - sivu repolle

Tässä tehtävässä teemme uuden repositorion, ja sille github pages -sivut.

### Tehtävänanto

1. Tee uusi julkinen repositorio (aihe vapaa, mutta pitäydy asiallisissa sisällöissä),
2. Tee sivulle github pages -sivut github.pages.com -ohjeiden mukaan.

pages.github.com -sivulla ohjeet repositoriosivun luontiin löytyvät "project site"-otsikon alta.

Voit valita sisällön vapaasti.

Tärkeää kuitenkin on, että lisäät sivulle vähintään yhden html-sivun ja yhden css-sivun.

yksinkertainen esimerkkisivu:

* projektisivut: https://gratoiale.github.io/joulukortti/
* repositorio https://github.com/gratoiale/joulukortti/

## Github CV:n täyttäminen

Olet nyt tehnyt itsellesi:

* käyttäjäprofiiliisi `README.md`-osion,
* käyttäjätunnuksellesi github pages -sivut,
* repollesi github pages -sivut.

Jatkossa, kun saat jonkin isomman tehtävän tai projektin tehtyä, 
oli kyse sitten koulutyöstä tai harrasteprojektista,
jos tekemäsi työ on tarpeeksi viimeistelty, 
kannattaa se lisätä osaksi github CV:täsi.

Ja vaikka työ ei olisikaan ollut vielä viimeistelty palautusvaiheessa,
sen voi aina omalla ajalla viimeistellä CV:tä varten.

### Web-sivujen viimeistelystä

Jos laitat osaksi CV:täsi web-sivun tai -sivuston, 
esimerkiksi jonkun monista tässä tutkinnon osassa tehdyistä sivuista,
muista viimeistellä se myös responsiivisuuden osalta.

Responsiivisten sivujen tekemiseen 
löytyy ohjeet [svelte-tehtävien](/materiaali/harjoitukset/02-javascript/01-js-svelte.md) 
lopusta (tehtävät 29-32).

### Mitä kannattaa lisätä Github CV:hen

#### Muista call-to-action -ohjaus

Markkinoinnissa käytetään englanninkielistä termiä "call-to-action"-kuvaamaan toiminnallisuutta, 
joka ohjaa käyttäjän tekemään halutun toiminnon.
Tällainen toiminto saattaa olla vaikka toiselle sivulle siirtyminen, tai puhelimella soittaminen tiettyyn numeroon.

Keskeinen call-to-action -ohjauksen piirre on, että se tarjoaa välittömän ja helpon tavan käyttäjälle toteuttaa haluttu tehtävä.

Esimerkiksi, jos halutaan, 
että käyttäjä mainoksen nähtyään soittaa tiettyyn puhelinnumeroon 
(esim. tilatakseen tuotteen, kuten kuulemma 1950-luvulla yleisesti tehtiin),
on tärkeää, että mainoksessa näytetään puhelinnumero, 
ja vieläpä ilmaistaan toivottu puhelinnumeron käyttötapa, siis kehotetaan lukijaa soittamaan siihen.

Tänä päivänä yleisin verkkosivujen call-to-action -ohjeistus on linkin muodossa.
Välillä linkkien yhteyteen on tärkeää lisätä kehotus, 
mutta tehokkaampaa yleensä on sijoittaa linkki keskeiselle paikalle, selvällä viestillä.

Github-CV:si osalta call-to-action -ohjaus tarkoittaa pääasiallisesti sitä, 
että on tärkeää, että laitat työnäytteesi yhteyteen, näkyvälle paikalle, 
linkin käyttäjäprofiiliisi, ja linkin yhteydessä ilmaiset selvästi, 
että tekijästä löytyy lisää tietoa käyttäjäprofiilista.

##### Esimerkki:Call-to-action -yläpalkki tehtyjen sivujen yläosaan

Jos esimerkiksi, flexbox-tehtävät tehtyäsi, olet saanut kaupan etusivun valmiiksi,
ja olet lisäämässä responsiivista toteutustasi osaksi github CV:täsi, 
muista lisätä sivulle yläosaan, korkeimmalle paikalle, ylimääräinen header-osio, 
jossa lyhyesti kerrot, että kyse on frontend practice -projektista, 
linkität koodin repositorioon, ja omaan käyttäjäprofiiliisi.

Tällöin tämä lisäotsake toimii call-to-action:ina, 
jolla pystyt ohjaamaan työnäytteeseesi eksyneet selailijat
profiiliisii, sekä varsinaisen koodisi pariin.

Valitse tälle lisäotsakeosiolle vielä nätti:

* fontti - esimerkiksi google fonts:ista (muista kuitenkin jaella fontti samasta paikasta html:n kanssa, älä käytä googlen cdn:ää),
* väri väripalettisivustolta - colourlovers.com (vanha mutta nykyään kyseenalaisesti mahdollisesti täynnä haittaohjelmia), coolors.co, yms.
* tyylien osalta siisti keskitys elementeille flexboxilla, ja vähän tyhjää tilaa sopivassa suhteessa yleensä riittää.

Tämä yläpalkki voi näyttää html:n osalta esimerkiksi seuraavalta:

```html
<header>
	<div>työn nimi</div>
	<div>
		<div>repo:</div>
		<a href="linkki repoon">käyttäjänimesi/reposi-nimi</a>
	</div>
	<div>
		<div>
			<div>Referenssi:</div>
			<a href="linkki sivuun, jota käytit oman työsi referenssinä">sivu</a>
		</div>
		<div>
			Mahdollisesti muu referenssi, esim. linkki tehtävänmäärittelyyn.
		</div>
	</div>
</header>
<main>
	<!-- sivun todellinen sisältö -->
</main>
```

Varmista kuitenkin, ettet ole käyttänyt sivulla yksittäisiä elementtejä css-valitsimina, 
joka saattaisi häiriintyä tästä muutoksesta sivun rakenteeseen, sekä ylimääräisistä elementeistä.
Jos näin on käynyt, voit helposti korjata sivusi toimimaan ilman elementti-css-valitsimia, 
käyttäen pelkkiä luokkia valitsimina.
