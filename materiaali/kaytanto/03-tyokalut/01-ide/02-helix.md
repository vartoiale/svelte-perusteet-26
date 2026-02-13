# Helix

Helix on moderni versio `vim`-komentorivitekstieditorista.

Sen osaaminen on hyödyllistä,
koska Vim on suosittu,
mutta komennoilta erikoinen komentorivieditori.

Linuxin puolella monet sovellukset tykkäävät käyttää Vim:iä oletustekstieditorinaan.
Näin tekee mm. git.

Lopulta kun Vim:in näppäinkomennoista saa kiinni,
se osoittautuu monipuoliseksi ja tehokkaaksi työkaluksi.

Sitä ennen sen käyttö saattaa kuitenkin osoittautua vaikeaksi.

Helix on moderni Vim:in inkarnaatio,
jota on ilo käyttää.

## Ohjeet

Helix tukee samoja näppäinkomentoja, 
joita `vi` ja `vim` tukevat.

### Pikaohjeet

Jos löydät itsesi Vim:istä, tai helix:stä,
saat sen sammutettua seuraavilla näppäinkomennoilla:

1. paina `esc`-näppäintä siirtyäksesi meta-tilaan,
2. kirjoita teksti `:wq` tallentaaksesi bufferin ja poistuaksesi,
3. suorita komento painamalla `enter`-näppäintä.

### Pidemmät ohjeet

Toisin kuin muissa tekstieditoreissa, 
Vim-pohjaisissa työkaluissa on useampi tila,
joissa pystyy tekemään eri asioita.

Jotta asiat eivät olisi liian helppoja,
Vim, ja siihen pohjautuvat työkalut,
koska ovat ammattilaisille tarkoitettuja työkaluja,
eivät ole pahemmin kiinnostuneita turhasta kädestä pitelystä.
Vim:in kulloistakin tilaa, 
ei siis välttämättä ole kovin helppo kokemattomamman käyttäjän tunnistaa.

#### Tilat

Vim-pohjaisten työkalujen tilat:

1. komentotila (engl. command mode)
2. suoritustila (engl. execute mode)
3. lisäystila (engl. insert mode)

Siirtymät tilojen välillä, tapahtuvat painamalla tilan näppäintä:

* komentotilaan - painamalla `esc`-näppäintä
* suoritustilaan - painamalla `:`-näppäintä komentotilassa
* lisäystilaan - painamalla `i`-näppäintä komentotilassa

Näiden lisäksi tilojen välillä pääsee siirtymään myös muilla näppäinyhdistelmillä.

##### Lisäystila

Lisäystila on tila, 
jossa käyttäjä pystyy lisäämään sisältöä tekstitiedostoon.

Se on siis se tyypillisin tekstieditorin tila, 
jossa muokataan tekstitiedostoa.

Jos et tiedä missä tilassa olet, 
voit aina painaa `esc`-näppäintä päästäksesi komentotilaan.

Komentotilasta pääset lisäystilaan painamalla `i`-näppäintä.

Lisäystilan tunnistaa kirkkaan vaaleasta kursorista.

##### Komentotila

Komentotila on välitila suoritus- ja lisäystilan välillä.

Siellä voi myös suorittaa erilaisia komentoja, 
kuten valita tekstialueita, 
sekä poistaa rivejä.

Ennen kuin kuvittelee muokkaavansa lisäystilassa tekstitiedostoa,
kannattaa tarkistaa, missä tilassa on,
tai painaa varmuudeksi `i`-näppäintä,
siirtyäkseen lisäystilaan,
sillä väärien kirjainten painaminen komentotilassa saattaa johtaa yllättäviin bufferiin vaikuttaviin muutoksiin.

Komentotilan tunnistaa haaleammasta kursorista.

##### Suoritustila

Suoritustila on tila, 
jossa käyttäjä voi suorittaa erilaisia tekstieditorin toimintoja.
Esimerkiksi bufferin, siis tiedoston, tallentaminne tapahtuu suoritustilassa.
Samoin myös editorin sulkeminen tapahtuu juuri suoritustilan kautta.

Suoritustilan komennot alkavat `:`-merkillä, ja ne suoritetaan painamalla `enter`-näppäintä.

#### Lisää aiheesta

Voit lukea lisää esim. helix:in ohjeista.

## Linkit

Linkit:

* [sivu](https://helix-editor.com)

Dokumentaatio:

* [dokumentaatio](https://docs.helix-editor.com)
* [asennus](https://docs.helix-editor.com/install.html)
