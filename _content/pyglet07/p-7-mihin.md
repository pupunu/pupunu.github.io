## Ohjelman siistimistä

Olemme tähän asti kokeilleet ohjelmassamme paljon kaikenlaista, mutta nyt kun ohjelmoimme liikkumista, olisi kiva saada kaikki ylimääräiset asiat ohjelmasta pois. Tehdään siis uusi tiedosto, johon sitten voimme ohjelmoida ympyrän liikkumisen. Voit saada tämän tiedoston seuraamalla osien 1 ja 2 ohjeita tai kopioimalla tyhjään tiedostoon alla olevan koodin.

```Python3
import pyglet

ikkuna = pyglet.window.Window(width = 800, height = 600)
ympyrä = pyglet.shapes.Circle(x = 400, y = 300, radius = 100)

@ikkuna.event
def on_draw():
    ikkuna.clear()
    ympyrä.draw()

pyglet.app.run()
```

Huom! Muista laittaa koodi `ikkuna.clear()` ikkunatapahtuman `on_draw()` sisään. Nyt kun meillä on liikkuvia asioita, pitää ikkuna tyhjentää aina ennen uusien asioiden piirtämistä.

--- 

Kirjoita koodi juuri ennen `on_draw()`-ikkunatapahtumaa.

Hyödyllistä on tietää, että jos haluamme nyt saada tietää olemmeko menossa ylös, se on talennettuna muutujaan `suunta['ylös']`. Jos olemme menossa ylös, muuttujan arvo on `True`, eli totta, jos taas emme ole menossa ylös, se on `False`, eli epätosi.

Lisää `on_key_release` -tapahtuma, jossa suuntien arvot asetetaan epätodeksi.
1. Lisää muut suunnat. (Tämän voi tehdä myös sen jälkeen, kun yhdelle suunnalle on lisätty kaikki kappaleessa tuleva koodi)

```Python3
@ikkuna.event
def on_key_release(merkki, muuntaja):
    if merkki == pyglet.window.key.UP:
        suunta['ylös'] = False
```

Lisää ikkunatapahtuma edellisen perään ennen koodia `pyglet.app.run()`.

## Funktion aikataulutus

Jäljelle on jäänyt vain liikkumisfunktion aikataulutus. Koska haluamme että hahmomme liikkuu jatkuvasti, haluamme että ohjelma muuttaa sijaintia koko ajan.

```Python3
pyglet.clock.schedule(liiku)
```

Kirjoita uusi koodi juuri ennen koodia `pyglet.app.run()`.

Kokeile nyt ohjelmaasi ja paina näppäimistöltä nappia nuoli ylös!

## Alaspäin

Ohjelmoidaan vielä liikkuminen alaspäin. Englanniksi alas on `DOWN`, joten nappi alaspäin on `pyglet.window.key.DOWN`.

Voimme käyttää edelleen tuttuja ehtolauseita ikkunatapahtumissa:

```Python3
@ikkuna.event
def on_key_press(merkki, muuntaja):
    if merkki == pyglet.window.key.UP:
        suunta['ylös'] = True
    elif merkki == pyglet.window.key.DOWN:  #Tällä rivillä alkaa lisätty koodi
        suunta['alas'] = True               #Tämän rivin jälkeen alkaa taas vanha koodi

@ikkuna.event
def on_key_release(merkki, muuntaja):
    if merkki == pyglet.window.key.UP:
        suunta['ylös'] = False
    elif merkki == pyglet.window.key.DOWN:  #Tästä rivistä alkaa taas uusi koodi
        suunta['alas'] = False              #Tähän loppuu uusi koodi
```

Sen sijaan liikkuessa emme halua käyttää elif-komentoja. Miksi? Koska elif-komennoilla jos yksi ehto on totta, muita ehtoja ei huomioida. On kuitenkin mahdollista, että painetaan samaan aikaan sekä ylös että alas, jolloin pitäisi kulkea molempiin suuntiin (molempiin suuntiin kulkeminen on paikallaan pysymistä). Siis testataan vain jokainen suunta omalla ehtolauseellaan.

```Python3
def liiku(dt):
    if suunta['ylös'] == True:
        ympyrä.y = ympyrä.y + 10

    if suunta['alas'] == True:              #Tällä rivillä alkaa uusi koodi
        ympyrä.y = ympyrä.y - 10
```

Nyt ympyrä liikkuu ikkunassa ylös alas!

## Koodi kokonaisuudessaan

Ohjelmamme koodin pitäisi siis näyttää nyt tältä

```Python3
import pyglet

ikkuna = pyglet.window.Window(width = 800, height = 600)
ympyrä = pyglet.shapes.Circle(x = 400, y = 300, radius = 100)


suunta = {'ylös':False, 'alas':False}

@ikkuna.event
def on_draw():
    ikkuna.clear()
    ympyrä.draw()

@ikkuna.event
def on_key_press(merkki, muuntaja):
    if merkki == pyglet.window.key.UP:
        suunta['ylös'] = True
    elif merkki == pyglet.window.key.DOWN:
        suunta['alas'] = True

@ikkuna.event
def on_key_release(merkki, muuntaja):
    if merkki == pyglet.window.key.UP:
        suunta['ylös'] = False
    elif merkki == pyglet.window.key.DOWN:
        suunta['alas'] = False


def liiku(dt):
    if suunta['ylös'] == True:
        ympyrä.y = ympyrä.y + 10

    if suunta['alas'] == True:
        ympyrä.y = ympyrä.y - 10

pyglet.clock.schedule(liiku)

pyglet.app.run()
```

# Tehtävät

1. Tee ohjelma, jolla on ikkuna, ja ikkunassa ympyrä.


2. Jatka edellisen tehtävän ohjelmaa. Ohjelmoidaan ympyrä liikkumaan nappia painamalla ylöspäin.

a) Lisää ohjelmaan muuttuja, johon tallennetaan kuljetaanko ylöspäin.

b) Ohjelmoi niin, että muuttuja on tosi, kun liikutaan painetaan nuolta ylös.

c) Ohjelmoi niin, että muuttuja on epätosi jos lopetetaan näppäimen _nuoli ylös_ painaminen.

d) Tee funktio, joka muuttaa ympyrän koordinaatteja niin, että nuolta ylös painessa koordinaatit kasvavat kymmenellä.

e) Aikatauluta funktio

---

3. Jatka edellisen tehtävän ohjelmaa.

Ohjelmoi kakkostehtävää mukaillen ympyrä liikkumaan myös alaspäin nappia painamalla.

---

4. Haastavampi tehtävä

Ohjelmoidaan ympyrä liikkumaan myös vasemmalle ja oikealle. Tätä varten meidän pitää laajentaa suuntaa.

a) Muuta muuttujaa `suunta` niin, että siinä on myös suunnat vasemmalle ja oikealle: `suunta = {'ylös':False, 'alas':False, 'vasemmalle':False, 'oikealle':False}`

b) Ohjelmoi liikkuminen vasemmalle ja oikealle.
