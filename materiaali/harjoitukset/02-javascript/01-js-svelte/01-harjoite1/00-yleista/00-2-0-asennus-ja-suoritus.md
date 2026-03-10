# Asennuksesta ja suorituksesta 

Koska haluamme ajaa koodia, siis suorittaa sitä, näitä tehtäviä varten,
pitää meidän ensin asentaa ajoympäristö koneelle.

Tähän meillä on kaksi vaihtoehtoa:

1. kontit
2. tarvittavien ohjelmien asennus suoraan koneelle

## Pohdintaa: kontti vai asennus suoraan koneelle

Yleensä kontin asentaminen on tuotantoympäristöjä varten se ammattimaisempi vaihtoehto.

Se kuitenkin vaatii hieman enemmän osaamista.

Koska tämän kurssin osalta vielä harjoitellaan web-kehityksen perusteita, on ehkä helpompi jättää vielä kontit sivuun.

Kurssin edellisestä versiosta on olemassa myös ohjeet konttien käyttöön.
Ne voivat kuitenkin olla vanhentuneita.

## Virtuaalikoneet ja tietoturva

Jos et käytä kontteja, on kuitenkin suositeltavaa asentaa ohjelmat virtuaalikoneeseen.

Virtuaalikone on yleensä turvallisempi vaihtoehto, myös jos käytät kontteja.

Kontit tarjoavat hieman ylimääräisiä mutkia ongelmalliselle koodille, jos sellaista npm:n syövereistä pääsisi koneellesi eksymään.

Konttiteknologia ei yleensä kuitenkaan muodosta tietoturvamuuria, ja yleinen ymmärrys on, 
että haittaohjelmien on verrattain helppoa murtautua ulos kontista.
Virtualisointi lisää kerroksia ajettavan koodin, ja isäntäympäristön välille, toimien vakuuttavampana tietoturvamuurina.
Aukoton sekään ei kuitenkaan ole.

Yleensä hyvä nyrkkisääntö kehitysympäristön asentamiseen koneelle on, että samalla koneella, 
jolla sovelluskehitystä tehdään, ei kannattaisi tehdä tietoturvan kannalta haasteellisia asioita, esim. pankkiasiointia.

## Ohjeet:

* [0.2.1 podmanilla](./00-2-1-podman.md) - kontit saattavat olla vanhentuneita
* [0.2.2 ilman podmania](./00-2-2-ilman-podmania.md) - suositeltava
