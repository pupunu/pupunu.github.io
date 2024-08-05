

## Aloitetaan!

Luodaan ensin kansio mihin tulemme luomaan kaikki tiedostot koodia varten. Nimeä kansio `keräilypeli`.

Luodaan kansioon seuraavaksi päätiedosto, jonka käynnistämällä peli lähtee käyntiin. Annetaan sen nimeksi `keräilypeli.py`.

Avataan tämä tiedosto ja luodaan peliä varten ikkuna. Muista lisätä ensin pyglet! Laitetaan vielä ikkuna aukeamaan.

Tiedosto näyttää nyt siis jotakuinkin tältä:

```Python3
import pyglet

ikkuna = pyglet.window.Window(width = 800, height = 600, caption = 'Keräilypeli')

pyglet.app.run()
```

Kaikki ikkunatapahtumat tullaa kirjoittamaan tähän tiedostoon.



