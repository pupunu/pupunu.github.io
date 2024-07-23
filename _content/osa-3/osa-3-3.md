# For-silmukka

Tutustuimme edellisessä osassa while-silmukalla toteutettuun toistoon. For on toinen Pythonin toistorakenteista. Sille annetaan lista, jonka se käy läpi niin, että jokaisella toistokerralla käsitellään listan seuraava alkio.

For-komentoa käytetään seuraavasti:

```Python3
for asia in lista:
    print(asia)
```

Toistorakenne aloitetaan komennolla `for`, jota seuraa _väliaikainen muuttuja_. Tällä muuttujalla voidaan toiston sisällä käyttää tämän toistokerran listan alkiota. Väliaikaismuuttujaa seuraa komento `in`, jota seuraa läpikäytävän listan nimi ja kaksoispiste. Tätä seuraa sisennettynä toistorakenteen sisältö, eli mitä toistetaan.

Yllä näytetyssä esimerkissä tulostetaan yksitellen kaikki listan alkiot.

Voimme myös tehdä silmukan sisällä eri asioita riippuen alkiosta ehtorakenteen avulla:

```Python3
for hedelmä in hedelmät:
    if hedelmä == "omena":
        print("jee, omena!")
```

Tämä koodi tulostaa "jee, omena!", jokaisella toistolla, jossa alkio listassa _hedelmät_ on "omena".

Listan alkioita ei ole myöskään pakko käyttää toiston sisällä. Siksi jos haluamme yksinkertaisesti toistaa jotain tietty määrä, se käy helposti luomalla haluttujen toistojen pituinen lista ja käymällä se läpi. Esimerkiksi jos haluamme tulostaa kymmenne kertaa "moi", se käy helpoiten näin:

```Python3
for asia in range(10):
    print("moi")
```

Komennolla `range(10)` luodaan lista [0, ..., 9], jossa on 10 alkiota. Siispä sen läpikäynti tuottaa 10 toistoa. Jokaisella toistolla tulostetaan "moi".

## Tehtävät

1. Tee ohjelma, joka tulostaa luvut 1, 2, 3, ..., 100. 

1. Tee ohjelma, joka tulostaa parilliset luvut 2, 4, 6, ..., 100. 

1. Tee ohjelma, joka tulostaa 100 kertaa "hei!"

1. Tee ohjelma, joka tulostaa 20 riviä, joissa lukee vuorotellen apina ja banaani.