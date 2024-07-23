# Tulostus ja tietotyypit

## Oma tiedosto

Terminaalissa voi testailla yksittäisiä komentoja, mutta ohjelman kirjoittamiseen se ei sovellu. Jos haluamme kirjoittaa ohjelman, jossa on useita rivejä ja jonka voimme tallentaa, meidän pitää kirjoittaa se tiedostoon. Tiedostoon tallennetun ohjelman voi suorittaa, jolloin tietokone suorittaa sen komennot lähtökohtaisesti rivi kerralla ylhäältä alas.

## Tulostus

Kun haluamme ohjelman kirjoittavan jotain terminaalii, käytetään komentoa ```print()```. Sulkujen sisään laitetaan tulostettava asia.

## Luvut ja merkkijonot

Kun tietokone käsittelee tietoa, sille on tärkeää millainen tieto on kyseessä. Erilaisia tietoja ovat muun muassa luvut, kuten kokonaisluvut, ja teksti, jota kutsutaan merkkijonoksi. Pythonissa kun muuttujaan tallettaa tietoa, tietokone päättelee annetusta tiedosta automaattisesti tietotyypin. Esimerkiksi koodista ```x = 1```, tietokone osaa päätellä, että ```x``` on kokonaisluku, koska ```1``` on kokonaisluku. Tekstin eli merkkijonot se tunnistaa tekstin ympärillä olevista lainausmerkeistä, esim. ```y = "sana"```. Jos tekstin kirjoittaa ilman lainausmerkkejä, tietokone ei ymmärrä kyseessä olevan tekstiä, vaan ajattelee sen olevan komento tai muuttuja. Tällöin ohjelma ei suoritu oikein.

Myös merkkijonoja voi laskea yhteen, mutta niitä ei voi vähentää, kertoa tai jakaa. Merkkijonojen yhteenlasku yhdistää kaksi merkkijonoa. Myös muuttujia, joiden arvo on merkkijono, voidaan laskea yhteen merkkijonojen kanssa. Esim. jos meillä on muuttuja ```nimi = "Kaneli"```, voimme yhdistää ```"Moikka " + nimi```, jolloin saamme merkkijonon ```"Moikka Kaneli"```.


## Esimerkkejä

| koodi | mitä tekee |
| ----- | ---------- |
| print("moikka") |tulostaa terminaaliin viestin _moikka_ |
|print(2)| tulostaa terminaaliin _2_ |
| print(2+2) | tulostaa terminaaliin _4_ |
| print("2+2") | tulostaa terminaaliin _2+2_ |
| print(muuttuja) | tulostaan terminaaliin muuttujan arvon |
| print("muuttuja") | tulostaa terminaaliin _muuttuja_ |
| print("moi" + "kka") | tulostaa terminaaliin _moikka_ |

## Tehtävät

1. Luo Idlessä uusi tiedosto ja nimeä se testi.py. Seuraavat tehtävät tehdään tähän tiedostoon.

1. Kirjoita ohjelma joka tulostaa tekstin: Hei! Olen robotti.

1. Kirjoita ohjelma joka tulostaa tekstin: Hei! Olen ihminen.

1. Kirjoita ohjelma, joka tulostaa ikäsi.

1. Kirjoita ohjelma, joka tulostaa ikäsi kymmenen vuoden päästä käyttäen yhteenlaskua.

1. Kirjoita ohjelma, joka tulostaa laskutoimituksen 4+2 (EI sen tulosta 6!)

1. Kirjoita ohjelma, joka tulostaa

    ```Python3 
    0000
    0  0
    0  0
    0000
    ```

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