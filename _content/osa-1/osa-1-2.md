## Tulostus ja tietotyypit

### Oma tiedosto

Jos haluamme kirjoittaa ohjelman, jossa on useampia rivejä ja jonka voimme tallentaa, meidän pitää käyttää tiedostoa. 

### Tulostus

Kun ohjelma kirjoitetaan tiedostoon, mutta haluamme saada jotain näkyviin terminaaliin, voimme tulostaa sinne tekstiä komennolla ```print()```.

### Tietotyypit

Kun tietokone käsittelee tietoa, sille on tärkeää minkä tyyppinen tieto on kyseessä. Tietotyyppejä ovat muun muassa erilaiset luvut, kuten kokonaisluvut, ja teksti, jota kutsutaan usein merkkijonoksi. Pythonissa kun muuttujaan tallettaa tietoa, tietokone päättelee annetusta tiedosta automaattisesti tietotyypin. Esimerkiksi koodista ```x = 1```, tietokone osaa päätellä, että ```x``` on kokonaisluku, koska ```1``` on kokonaisluku. Tekstin eli merkkijonot se tunnistaa tekstin ympärillä olevista lainausmerkeistä, esim. ```y = "sana"```.


### Esimerkkejä

| koodi | mitä tekee |
| ----- | ---------- |
| print("moikka") |tulostaa terminaaliin viestin _moikka_ |
|print(2)| tulostaa terminaaliin _2_ |
| print(2+2) | tulostaa terminaaliin _4_ |
| print("2+2") | tulostaa terminaaliin _2+2_ |
| print(muuttuja) | tulostaan terminaaliin muuttujan arvon |
| print("muuttuja") | tulostaa terminaaliin _muuttuja_ |
| print("moi" + "ka") | tulostaa terminaaliin _moikka_ |

### Tehtävät

1. Luo Idlessä uusi tiedosto ja nimeä se testi.py. Seuraavat tehtävät tehdään tähän tiedostoon.

1. Kirjoita ohjelma joka tulostaa tekstin: Hei! Olen robotti.

1. Kirjoita ohjelma joka tulostaa tekstin: Hei! Olen ihminen.

1. Kirjoita ohjelma, joka tulostaa ikäsi.

1. Kirjoita ohjelma, joka tulostaa ikäsi kymmenen vuoden päästä käyttäen yhteenlaskua.

1. Kirjoita ohjelma, joka tulostaa laskutoimituksen 4+2 (EI sen tulosta 6!)

1. Ohjelmoi tervehtijä

   - Luo muuttuja nimi ja tallenna siihen nimesi.

   - Tulosta muuttujan avulla Hei nimi, jossa nimi on oma nimesi.

8. Kirjoita tarina muuttujilla

    - Luo muuttujat x ja y ja anna niille haluamasi arvot. Esim. Tiittu ja robotti. 

    - Kirjoita tarina käyttäen muuttujia x ja y ja seuraavaa tekstiä:

```Python3
Olipa kerran x. x oli hieno y. 
Mutta se, että x oli y aiheutti ongelmia, sillä kaikki eivät pitäneet siitä, että x oli y.
Jonkin ajan kuluttua muut kuitenkin hyväksyivät että x oli y, koska x oli niin ystävällinen y. Ja kaikki elivät onnellisina elämänsä loppuun asti.
```