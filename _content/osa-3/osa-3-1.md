# Listat

Tähän mennessä olemme voineet tallettaa tietoa muuttujiin ainoastaan yksittäisinä lukuina, tekstipätkinä tai totuusarvioina, mutta usein olisi kätevää säilöä paljon tietoa yhteen paikkaan. Tätä varten on Pythonissa listoja.

## Listan luominen

Pythonissa listat kirjoitetaan hakasulkeisiin, ja jokaista listan asiaan eli _alkiota_ erottaa pilkku, esim. `[1, 2, 3, 4]` on lista, jossa on luvut 1, 2, 3, ja 4. Kuten minkä tahansa muunkin asian, listan voi tallentaa muuttujaan antamalla muuttujan nimen, jota seuraa yhtäsuuruusmerkki ja sen jälkeen lista. Tämän jälkeen muuttuja nimellä pääsee käsiksi listan tietoihin. Esimerkiksi `lista = ["a", "b", "c"]` luo muuttujaan _lista_ listan, jossa on merkkijonot "a", "b" ja "c".

Tyhjän listän voi luoda niin, ettei listaan laita mitään alkioita eli `tyhjäLista = []`.

### Esimerkkejä

| koodi | mitä tekee |
| ----- | ---------- |
|lista = []| tallettaa muuttujaan _lista_, tyhjän listan.|
|a = [1, 2, 3]| tallentaa muuttujaan _a_ listan [1, 2, 3]|


## Listan arvojen käyttö

Kun luomme listan `lista = [1, 2, 3, 4]`, miten voimme päästä käsiksi jälkikäteen listan tiettyyn alkioon? Se onnistuu komennolla `lista[]`, jossa hakasulkeisiin kirjoitetaan monennenko alkion haluamme. Listan alkion jäjestysnumero eli _indeksi_ on ensimmäisellä alkiolla 0, toisella alkiolla 1 ja niin edespäin. Viimeisen alkion indeksi on siis yhtä pienempi kuin listan pituus.

Esimerkiksi voisimme tallentaa listan kolmannen alkion muuttujaan _kolmasAlkio_ komennolla `kolmasAlkio = lista[2]`.

Jos listasta yritetään etsiä indeksillä jota listassa ei ole, tulee virheilmoitus ja ohjelma kaatuu. Listan isoin indeksi on aina listan pituutta yhtä pienempi ja listan pituuden saa komennossa len(). Komentoa käytetään laittamalla lista sulkuihin, esim. `len([1, 2, 3])` antaa arvon 3, koska listan pituus on 3.

### Esimerkkejä

| koodi | mitä tekee |
| ----- | ---------- |
|lista[0]| antaa listan ensimmäisen alkion|
|lista[2]| antaa listan kolmannen alkion|
|eka = lista[0]| tallentaa muuttujaan _eka_ listan ensimmäisen alkion|
|len(lista)| antaa listan pituuden|
| lista[len(lista)-1] | antaa listan viimeisen alkion|

## Listan metodeja

Listoille on olemassa omia komentojaan, jotka toimivat vain listoille. Tällaisia komentoja kutsutaan metodeiksi. Tärkeimmät listojen metodit ovat `append()`, `remove()`ja `sort()`. Niitä käytetään kirjoittamalla listan nimi, sitten piste ja sitten metodin nimi, esim. `lista.sort()`, järjestää listan.

Append-komento lisää alkion listan perään. Lisättävä alkio kirjoitetaan komennon sulkujen sisään.

Remove-komento poistaa alkio listasta. Poistettava alkio kirjoitetaan komennon sulkuihin.

Sort-komento järjestelee lista. jos listassa on lukuja, ne menevät suuruusjärjestykseen. Jos listassa on tekstiä, ne menevät aakkosjärjestykseen.

### Esimerkkejä

| koodi | mitä tekee |
| ----- | ---------- |
|lista.append(1)| lisää listaan loppuun luvun 1|
|lista.remove("a")| poista listasta merkkijonon "a"|
|["b", "d", "a", "c"].sort() | järjestää listan, eli palauttaa lista ["a", "b", "c", "d"]|

## Listojen pikaluomisen komentoja

Tietynlaisten listojen luomisesta on haluttu tehdä helppoa. Listan jossa tietyt arvot toistuvat, voi luoda kertomalla listan. Esimerkiksi `lista = [1]*4` luo listan `[1, 1, 1, 1]`.

Toinen tapa luoda listoja nopeasti, on käyttää `range()`-komentoa. Sillä voi luoda listoja, joissa on tietyn kaavan mukaisesti lukuja. Rangelle voi antaa yhden luvun, jolloin syntyy lista, jossa on luvut nollasta yhtä annettua lukua pienempään lukuun. Jos listalle antaa sulkuihin kaksi lukua, saa listan jossa on luvut ensimmäisestä luvusta oista annettua lukua yhtä pienempään lukuun. Jos antaa kolme lukua, kolmas luku määrittää minkä kokoisia "askeleita" lukujen välillä on.

### Esimerkkejä

| koodi | mitä tekee |
| ----- | ---------- |
|[2]*3| luo listan [2, 2, 2]|
|["a", "b"]*2 | luo listan ["a", "b", "a", "b"]|
| range(5) | luo lista [0, 1, 2, 3, 4]|
| range(2, 6)| luo listan [2, 3, 4, 5]
|range(0, 10, 2) | luo listan [0, 2, 4, 6, 8] |

## Tehtävät

**Tee seuraavat tehtävät terminaaliin**

1. Tallenna muuttujaan tyhjä lista.

1. Lisää listaan kolme hedelmää. Tulosta lista.

1. Järjestä lista aakkosjärjestykseen. Tulosta se uudestaan.

1. Tulosta terminaaliin vain listan toinen alkio.

1. Poista listasta toinen alkio.

1. Luo lista _triplahedelmä_, jossa toistuu hedelmälistasi kolmesti.

1. Luo lista komennolla range, jossa on luvut 0...19

1. Luo lista komennolla range, jossa on luvut 4...10

1. Luo lista komennolla range, jossa on luvut 0, 3, 6, 9, 12

**Tee seuraavat tehtävät omana ohjelmanaan tiedostoon**

1. Tee ohjelma, jossa luodaan lista, jossa on kolmen hahmon nimi. Ohjelman tulee tulostaa lista.

1. Tee ohjelma, joka kysyy listaan lisättäviä asioita ja lisää käyttäjän syötteen listaan. Jokaisen lisäyksen jälkeen lista tulostetaan. (Vinkki: käytä while-silmukkaa)

