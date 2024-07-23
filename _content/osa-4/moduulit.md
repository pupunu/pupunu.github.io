# Moduulien käyttö

## Kirjastot

Kaikkea ohjelmoidessa ei kannata tehdä itse. Sen sijaan ohjelmoidessa kannattaa käyttää apuna muiden tekemiä _kirjastoja_. Kirjastojen idea on, että joku muu on tehnyt koodia, jota voi kätevästi käyttää itse niin, että säästyy suurelta määrältä työtä.

Tässä osiossa esitellään kaksi Pythonin mukana asennettua kirjastoa. Myöhemmin opitaan asentamaan myös täysin uusia kirjastoja.

## Kirjastojen käyttäminen ja moduulit

Kirjastot koostuvat moduuleista. Yksi moduuli sisältää komentoja johonkin tiettyyn rajattuun tarkoitukseen. Käyttäessään kirjastoa voi joko käyttää vain osaa sen moduuleista tai kaikkia moduuleja. Toisaalta joissain kirjastoissa voi olla vain yksi moduuli.

Kokonaisen kirjaston voi ottaa käyttöön komennolla `import kirjastonNimi`. Tällöin koodissa pitää mainita, kirjaston nimi kun käytetään sen komentoja. Esimerkiksi jos käytämme turtle-kirjastoa, sen komennot ovat muotoa `turtle.komento()`.

Jos haluamme vain osan kirjaston moduuleista, voimme käyttää komentoa `from kirjasto import x`, jossa _x_:n tilalla on haluttu moduuli.

Kun otamme käyttöön yksittäisiä moduuleja, ei tarvita komentoihin erikseen mainintaa kirjastosta. Samalla komennolla voimme ottaa käyttöö myös kaikki moduulit, jolloin meidän ei tarvitse mainita kirjaston nimeä. `form kirjasto import *` ottaa käyttöön kaikki kirjaston moduulit ja kirjaston ei tarvitse komentoja käyttäessä mainita (* tarkoittaa _kaikki_).

Import-komento kannattaa laittaa ohjelman tiedoston alkuun. Komennon jälkeen kyseisessä ohjelmassa voi käyttää lisättyjä komentoja.

## Esimerkkejä

|komento| mitä tekee|
|---|---|
|import kirjasto| ottaa kirjaston käyttöön|
| from kirjasto import moduuli| ottaa tietyn moduulin käyttöön kirjastosta|
|from kirjasto import *| ottaa käyttöön kaikki kirjaston moduulit käyttöön|

