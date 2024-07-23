# Toistamisen alkeet

## while-silmukka

Jos haluaa toistaa saman tyylistä asiaa monta kertaa, käytetään toistorakennetta. Pythonissa on kaksi erilaista toistorakennetta ja niistä yksinkertaisempi on `while`. While on englantia ja tarkoittaa "niin kauan kuin".

`while`-komentoa käytetään niin, että sille annetaan ehto ja se toistaa sen sisäistä koodia niin kauan kuin ehto on totta. Koodin sisällä voidaan muun muassa muuttaa muuttujien sisältöä niin, että toisto loppuu, kun muuttujat saavat jonkin tietyn arvon.

Silmukasta voi myös poistua pakotetusti komennolla `break`. Tämä välittömästi lopettaa toiston ja siirtyy suorittamaan sen jälkeistä koodia.

Muista sisentää koodi, joka kuuluu toiston sisään!

Silmukan ehdoksi voi myös antaa suoraan totuusarvon `True`. Tällöin silmukka toistuu ikuisesti, kunnes siitä poistutaan `break`-komennolla.

## Esimerkkejä

**Esimerkki 1**
```Python3
luku = 0
while luku <10:
    print(luku)
    luku = luku + 1
```

**Mitä tekee:** Luodaan muuttuja _luku_, johon tallennetaan ensin nolla. Sen jälkeen niin kauan kuin luku on alle 10, tulostetaan luku ja sen jälkeen kasvatetaan lukua yhdellä.

**Esimerkki 2**
```Python3
while True:
    print("sammutat minut komennolla: pois")
    syöte = input()
    if syöte == "pois":
        break
    else:
        print("en tunne tuota komentoa")
```

**Mitä tekee:** `While` toistaa sisältööä niin kauan kuin sen saama ehto on totta. Ehdon paikalle voi myös asettaa vain totuusarvon `True`. Tämä "ehto" on aina totta, koska se on kirjaimellisesti totuusarvo "totta".

Toisto siis toistaa ikuisesti sisäistä koodiaan, jossa se tulostaa terminaaliin "sammutat minut komennolla: pois". Jos sen saama syöte on "pois", toisto lopetetaan `break`-komennolla. Jos taas syöte on jotain muuta, tulostetaan "en tunne tuota komentoa".

**Esimerkki 3**
```Python3
vastaus = ""
while vastaus != "moi":
    print("sano mulle moi")
    vastaus = input()
print("jee!")
```

**Mitä tekee:** Luodaan muuttuja _vastaus_, johon tallennetaan ensin tyhjä merkkijono. Sen jälkeen ohjelma tulostaa terminaaliin "sano mulle moi" ja tallentaa käyttäjän syötteen _vastaukseen_, niin kauan kuin _vastauksen_ arvo ei ole "moi". Kun _vastaus_ on "moi", poistutaan toiston sisältä ja tulostuu terminaaliin "jee!"

## Tehtävät

1. Tee ohjelma, joka tulostaa luvut yhdestä kahteenkymmeneen.

1. Tee ohjelma, joka tulostaa kaikki parilliset luvut väliltä 0–20.

1. Tee ohjelma, joka ikuisesti kysyy käyttäjän nimeä ja vastaa aina "niin varmaan".

1. Muokkaa edellistä ohjelmaa niin, että vastaus on "niin varmaan, _nimi_", jossa _nimi_ on käyttäjän antama syöte.

1. Fibonaccin lukujono on 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, jne. Lukujonon alussa on luvut 0 ja 1, ja sen jälkeen jokainen luku on kahden edellisen luvun summa. Tee ohjelma, joka tulostaa Fibonaccin lukujonon 100 ensimmäistä lukua. 