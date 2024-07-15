## Luodaan pelaajahahmo

Luodaan seuraavaksi tiedosto, missä luomme ja mihin säilömme kaiken pelin datan. Lisätään kansioon uusi tiedosto nimeltä `data.py`. Avaa tiedosto.

Tässäkin tiedostossa pitää muistaa ensin ottaa pyglet käyttöön. Kannattaa myös tallentaa haluttuja värejä vakiomuuttujiin tiedoston alussa. Voit kopioida hyödylliset värit alla olevasta koodista tiedoston alkuun.

```Python3
PUNAINEN = 255, 0, 0
SININEN = 0, 0, 255
VIHREÄ = 0, 255, 0
VALKOINEN = 0, 0, 0
```

Luodaan pelaaja. Ympyrä sopii hyvin.

data.py tiedosto näyttää nyt siis suunnilleen seuraavalta:

```Python3
import pyglet

PUNAINEN = 255, 0, 0
SININEN = 0, 0, 255
VIHREÄ = 0, 255, 0
VALKOINEN = 0, 0, 0

pelaaja = pyglet.shapes.Circle(x = 100, y = 100, color = PUNAINEN, radius = 40)
```

## Laitetaan ikkuna piirtämään pelaaja

Nyt laitetaan pelaaja näkymään ikkunassa. Kirjoitetaan ikkunatapahtumat tiedostoon `keräilypeli.py`.

Lisätään tiedostoon keräilypeli.py ikkunatapahtuma `on_draw`. Jotta voimme ikkunatapahtumassa piirtää pelaajahahmon, meidän tulee ottaa käyttöö tiedosto, jossa pelaajahahmo luodaan. Lisätään siis `import pyglet`in jälkeen `import data`.

Nyt voimme käyttää pelaajaa. keräilypeli.py:ssä koodilla `data.pelaaja`. Keräilypeli.py:n pitäisi näyttää nyt suunnilleen seuraavalta:

```Python3
import pyglet
import data

ikkuna = pyglet.window.Window(width = 800, height = 600, caption = 'Keräilypeli')

@ikkuna.event
def on_draw():
    ikkuna.clear()
    data.pelaaja.draw()

pyglet.app.run()
```

## Ohjelmoidaan pelaajan liikkuminen

Toteutetaan liikkuminen niin, että tallennetaan muistiin mihin suuntaan ollaan liikkumassa, ja liikkumissuunnan perusteella liikutetaan koko ajan hahmoa. Meidän tarvitsee siis:
1. Luoda mihin tallennamme tiedon liikkumissuunnasta
2. Ohjelmoida napin painaminen muuttamaan liikkumissuntaa
3. Ohjelmoida napin painamisen lopettaminen muuttamaan liikkumissuuntaa
4. Luoda funktio, joka liikuttaa hahmoa liikkumissuunnan mukaisesti.
5. Aikatauluttaa funktio.

Aloitetaan!

### Tallennetaan suunta

Liikkumissuunta on pelin dataa. Luodaan se siis tiedostossa `data.py`.

Liikkumissuunta kannattaa tallentaa dictionaryyn. Käytetään seuraavanlaista:

```Python3
liikkumissuunta = ['ylös' : False, 'alas' : False, 'vasemmalle' : False, 'oikealle' : False]
```

Nyt jos haluamme tietää esimerkiksi liikutaanko ylös, tieto siitä löytyy dictistä komennolla `liikkumissuunta['ylös']`. Tällä hetkellä kaikkien suuntien arvo on `False` eli epätosi. Toisin sanoen mihinkään ei liikuta.

### Liikkumissuunnan muuttuminen

Tehdään seuraavaksi funktio, joka muuttaa liikkumissuunnan napinpainamisen mukaan. Nuolinäppäinten nimet ovat pygletissä: 
- Ylösnuoli on `pyglet.window.key.UP`
- Alasnuoli on `pyglet.window.key.DOWN`
- Nuoli vasemmalle on `pyglet.window.key.LEFT`
- Nuoli oikealle on `pyglet.window.key.RIGHT`

Ohjelmoidaan ensin vain ylöspäin liikkuminen. Siihen tarvitsemme ikkunatapahtuman `on_key_press` tiedostoon `keräilypeli.py`

Ikkunatapahtuman rakenne on seuraavanlaien:

```Python3
@ikkuna.event
def on_key_press(merkki, muuntaja):
    if merkki == pyglet.window.key.UP:
        data.liikkumissuunta['ylös'] = True
```

Kiinnitä huomiota siihen, että liikkumissuunta on tallennettu erilliseen tiedostoon, joten siihen tulee viitata `data.liikkumissuunta`.

### Liikkumisen loppuminen

Halutaan että liikkuminen loppuu, kun napin painaminen lopetetaan. Liikkumissuunta pitää siis muutta epätodeksi, kun napin painaminen loppuu.

Tehdään tämäkin ensin vain suunnalle ylös ikkunatapahtumaan `on_key_release`, tiedostoon keräilypeli.py.

```Python3
@ikkuna.event
def on_key_release(merkki, muuntaja):
    if merkki == pyglet.window.key.UP:
        data.liikkumissuunta['ylös'] = False
```

### Pelaajaa liikuttava funktio

Nyt meillä on tieto siitä painetaan nuolta ylöspäin, mutta emme tee tiedolla vielä mitään. Ohjelmoidaan seuraavaksi funktio, joka muuttaa pelaajan sijaintia jos sen liikkumissuunta on ylös.

Voisimme kirjoittaa funktion suoraan keräilypeli.py-tiedosotoon, mutta on hyvätapaista jakaa pelin koodia loogisesti. Hahmon liikkuminen on pelin loogista toimintaa, joten tehdään sitä varten oma tiedostonsa nimeltä `logiikka.py`.

Siirrytään uuteen tiedostoon ja luodaan funktio `pelaajan_liikkuminen`. Muistetaan importata `data`, koska tavitsemme tietoa liikkumissuunnasta funktiota varten.

```Python3
import data

def pelaajan_liikkuminen(dt):
    if data.liikkumissuunta['ylös'] = True:
        data.pelaaja.y += 10
```

Funktio siis kasvattaa pelaajan y-koordinaattia, jos liikkumissuunta on ylös.

### Liikkumisfunktion aikataulutus

Jotta pelaaja vielä lähtisi liikeelle, meidän tulee muistaa aikatauluttaa liikkumisfunktio. Mennään tiedosoton `keräilypeli.py` ja aikataulutetaan funktio juuri ennen `pyglet.app.run()`-komentoa. Jotta voimme käyttää liikkumisfunktiota toisesta tiedostosta, meidän tulee ottaa logiikka.py käyttöön. Lisätään siis keräilypeli.py-tiedoston alkuu `import logiikka`. Sitten lisätään tiedoston loppuun ennen `pyglet.app.run()`-komentoa:

```Python3
pyglet.clock.schedule(logiikka.pelaajan_liikkuminen)
```

### Toteutetaan muut liikkumissuunnat

Ylösliikkumisen pitäisi nyt toimia. Lisätään seuraavaksi nappien painalluksia tarkistaviin funktioihin ja pelaajan liikkumisen hoitavaan funktioon loput suunnista.

