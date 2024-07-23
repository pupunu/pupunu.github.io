# Ehtolauseet 

Kun haluamme, että ohjelma tekee jotain vain tietyssä tilanteessa, tarvitsemme ehtolauseita. Ehtolauseet aloittaa Pythonissa aina ```if```. Se on englantia ja tarkoittaa _jos_. Käytämme sitä, kun haluamme, että ohjelmamme tekee jotain vain _jos_ tietty ehto toteutuu. Muita ehtolauseita ovat ```else```, eli _muussa tapauksessa_, ja ```elif```, eli _tai jos_.

## if (jos)

Tehdään ohjelma, joka kysyy käyttäjältä vihannesta ja **jos vihannes on sipuli**, tulostaa terminaaliin _silmiä kirvelee_. Tämä tehdään seuraavasti:

```Python3
vihannes = input("sano vihannes")
if vihannes == "sipuli":
    print("silmiä kirvelee")
```

if-rakenteessa on ensin komento if ja sitä seuraa vertailu. Vertailun jälkeen on kaksoispiste.

Jos annettu vihannes oli sipuli, siirrytään if-rakenteen sisään ja toteutetaan ```print("silmiä kirvelee")```. Jos vihannes ei ollut sipuli, hypätään sisennetyn koodin yli ja terminaaliin ei tulostu mitään.

Sisennys on tärkeä, koska se kertoo tietokoneelle, että ```print("silmiä kirvelee")``` on if-rakenteen sisällä.

## else (muussa tapauksessa)

Entäs jos haluamme, että jotain tapahtuu silloinkin, kun vihannes ei ollut sipuli? Silloin käytämme komentoa ```else```. Se on englantia ja tarkoittaa _muussa tapauksessa_. Else seuraa aina if:iä ja sen sisällä oleva koodi toteutuu, jos if:n koodi ei toteudu. Muutetaan hiukan aikaisempaa ohjelmaa.



```Python3
vihannes = input("sano vihannes")
if vihannes == "sipuli":
    print("silmiä kirvelee")
else:
    print("tuntematon vihannes")
```

Nyt jos vihannes on _sipuli_, terminaaliin tulostuu _silmiä kirvelee_, mutta jos vihannes ei ollut _sipuli_, tulostuu terminaaliin _tuntematon vihannes_.

## elif (tai jos)

Viimeinen ehtolause on ```elif```. Se tulee englannin sanoista _else if_, joka tarkoittaa _tai jos_. Se seuraa aina if:ä. Se toimii muuten kuin if, mutta jos sitä edeltävän ehtolauseen sisälle on siirrytty, se hypätään yli. Ehtolause alkaa siis aina if:llä ja sitä seuraa haluttu määrä elif:ejä. Viimeisenä on else, jos sellaisen haluaa.

Listään vihannesohjelmaamme muutama lisäehto.

```Python3
vihannes = input("sano vihannes")
if vihannes == "sipuli":
    print("silmiä kirvelee")
elif vihannes == "porkkana":
    print("se on oranssi")
elif vihannes == "kurkku":
    print("namskis")
else:
    print("tuntematon vihannes")
```

Nyt jos vihannes on sipuli, tulostuu terminaaliin _silmiä kirvelee_. Tai jos vihannes on porkkana, tulostuu _se on oranssi_. Tai jos vihannes on kurkku, tulostuu _namskis_. Muussa tapauksessa tulostuu _tuntematon vihannes_.

## Tehtävät

1. Kirjoita ohjelma, joka kysyy salasanaa, ja jos se saa syötteen "salasana", vastaa "oikea salasana".

1. Kirjoita ohjelma, jossa pitää arvata suosikki jäätelömakusi. Jos arvaa oikein, tulostuu "oikein". Jos arvaa väärin, tulostuu "väärin".

1. Alla on kivi-sakset-paperipelin koodi. Kopioi alla oleva koodi ja täydennä puuttuvat kohdat.

```Python3


```