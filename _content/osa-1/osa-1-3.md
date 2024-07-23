# Käyttäjän syöte ja tietotyyppien muuttaminen

## Käyttäjän syöte

Kun haluamme saada tietoa ohjelman käyttäjältä, voimme käyttää komentoa `input()`. Tämän komennon jälkeen, kun terminaaliin kirjoittaa jotain ja painaa rivinvaihtoa, kirjoitettu asia tulee ohjelman käyttöön. Tätä kirjoitettua asiaa kutsutaan syötteeksi. Syöte on ohjelman ulkopuolelta ohjelmalle annettua tietoa.

## Tietotyyppien muuttaminen

Käyttäjän syöte on aina merkkijono. Sitä ei siis voi suoraan vaikkapa laskea yhteen kokonaislukujen kanssa. Jos haluamme muuttaa annetun syötteen kokonaisluvuksi, käytämme komentoa `int()`. Komennon nimi tulee englannin sanasta _integer_, joka tarkoittaa kokonaislukua. Muutettava arvo laitetaan komennon perässä olevien sulkeiden sisään.

Kaikkia merkkijonoja ei voi muuttaa kokonaisluvuksi. Esimerkiksi `int("kissa")` antaa virheilmoituksen, koska tietokone ei ymmärrä miten kissasta saisi kokonaisluvun.

Vastaavasti kokonaisluvut voi muuttaa merkkijonoiksi komennolla `str()`, joka on lyhenne englannin sanasta _string_ ja tarkoittaa merkkijonoa.

## Esimerkkejä

| koodi | mitä tekee |
| ----- | ---------- |
| vastaus = input() | tallentaa käyttäjän syötteen muuttujaan _vastaus_ |
| nimi = input("Mikä on nimesi?") | kirjoittaa terminaaliin _Mikä on nimsesi?_ ja tallentaa muuttujaan käyttäjän syötteen muuttujaan _nimi_|
|int("42")| muuttaa merkkijonon "42" kokonaisluvuksi 42|
|int(vastaus) | muuttaa muuttujan _vastaus_ arvon kokonaisluvuksi (jos se on mahdollista)|
|int( input() )| muuttaa syötteen kokonaisluvuksi |
| str(1) | muuttaa kokonaisluvun 1 merkkijonoksi "1"|
| str(luku) | muuttaa muuttujassa _luku_ olevan arvon merkkijonoksi |

## Tehtävät

1. Tee ohjelma, joka toistaa sille annetun syötteen.

1. Tee paranneltu tervehtijä
    - Kysy käyttäjältä hänen nimeään ja tallenna se muuttujaan _nimi_.
    - Tulosta _Hei nimi_, jossa _nimi_ on käyttäjän antama syöte.

1. Tee ohjelma, joka kysyy käyttäjältä numeroa ja tulostaa sitten saman numeron kerrottuna kymmenellä.

1. Muuta äskeistä ohjelmaa niin, että tulostuksessa sanotaan ensin "tässä on se kerrottuna kymmenellä: ".