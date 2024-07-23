# Random

Joskus haluamme saada ohjelmiimme satunnaisuutta. Tällöin tarvitsemme kirjastoa `random`.

Kirjaston hyödyllisin komento on `randint()`, jolla voi arpoa satunnaisen kokonaisluvun annetulta väliltä. Se toimii siis kuin noppa.

Kaikki kirjaston komennot löytyvät dokumentaatiosta: [https://docs.python.org/3/library/random.html](https://docs.python.org/3/library/random.html)

## Esimerkkejä

|komento|mitä tekee|
|---|---|
|from random import randint| ottaa käyttöön kirjastosta _random_, komennon _randint_|
|randint(0, 2)| arpoo satunnaisen luvun väliltä 0, 1, 2|


## Tehtävät

Tässä harjoituksessa pääset koodaamaan kivi, paperi, sakset-pelin, missä pelaaja pelaa tekoälyä vastaan. Aloita kopioimalla alla oleva koodi: 

```Python3
while True:

    pelaaja = input("kivi, paperi, sakset?")
    tekoäly = "kivi"
    print("Tekoäly valitsi: " + tekoäly)

    if pelaaja == tekoäly:
        print("Tasapeli!")

    elif pelaaja == "kivi":
        if ta == "paperi":
            print("Hävisit!")
        else:
            print("Voitit!")

    elif pelaaja == "paperi":
        if ta == "sakset":
        print("Hävisit!")
        else:
            print("Voitit!")

    else:
        print("Vastaa kivi, paperi tai sakset!")
```

2. Koodista puuttuu kokonaan vaihtoehto, että pelaaja vastaa sakset! Korjaa tämä koodiin.

3. Nyt tekoäly pelaa aina kiven. Tee tekoälystä satunnainen.

**Bonustehtäviä**

Peli toimii nyt melko hyvin, mutta parannetaan sitä vielä lisää!

4. Lisää peliin pisteiden lasku.

5. Muuta koodia niin, että peliä pelataan esimerkiksi 5 kierrosta, minkä jälkeen pelaajalle kerrotaan pistemäärät ja voittaja. 

While-loop voisi näyttää nyt esimerkiksi tältä:

```Python3
kierrokset = 0

while kierrokset < 5:
    ....
    koodia....
    .....
    kierrokset += 1 
```

Lopputulostus voisi olla esimerkiksi seuraavanlainen:

```
Peli loppui! Sait 3 pistettä ja tekoäly 2 pistettä.
Sinä voitit!
```