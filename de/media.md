---
title: Unser Media Archiv - Bilder und HTML
description: Benutze unsere Resourcen, um an den Online-Protesten am 21. März teilzuhaben.
language: de
---

## Medien

Jeder kann die Idee von Wikipedia unterstützen mit den Hochladen eines schwarzen Profilbildes oder
mit dem Abschalten seiner Webseite.


### Profilbild

Sei ein Teil von **Blackout21** und benutze ein schwarzes Profilbild am 21. März. Falls du gerade kein
schwarzes Profilbild zur Hand hast, kannst du dich auch bei uns bedienen!

{% include profile_pictures.html %}


### Statische HTML-Blackout-Seiten

Mit einer statischen Blackout-Seite kannst du deine Besucher am einfachsten über die Proteste gegen Artikel 13
(sowie 11 und 12) und die EU-Urheberrechtsreform informieren!

Es gibt verschiedene Versionen für die Blackout-Seiten. Bitte einfach deine bevorzugte Version auf deinen Webserver
kopieren oder auf unsere Variante weiterleiten.

Die `blank`-Varianten funktionieren ohne weitere Dateien. Diese bestehen nur aus dem HTML-Code mit etwas inkludiertem CSS.
Für die `wallpaper`-Varianten benötigst du evtl. das Bild `wallpaper.jpg`.

{% include static_pages.html %}

Kleiner PHP Code-Schnipsel (einfach in die `index.php` oder in die `wp-include.php` kopieren).
Falls du das Skript testen möchtest einfach das Datum verändern (`2019-03-21`).

```php
if ('2019-03-21' === (new \DateTime())->format('Y-m-d')) {
    $url = 'https://blackout21.github.io/blackout-static-pages/blackout_de.html'; // Oder benutze eine andere Version
    header('Location: ' . $url, true, 302);
    exit;
}
```


### Widget

Wenn du nicht deine komplette Seite abschalten möchtest, wird ebenso ein Popup angeboten, welches am 21. einen Hinweis
zeigen wird. Um dies vorab zu testen, kann man einfach `#showsaveyourinternet` zur URL hinzufügen. Der Code lässt sich
überall auf der Webseite platzieren (im `head`- oder `body`-Bereich) – aber wir empfehlen den Code direkt vor dem
schließenden `</body>` zu platzieren. **Hinweis:** Einige Seiten (wie bspw. die kostenlose Version von WordPress.com)
erlauben kein eigenes JavaScript.

{% include widget.md %}

Da das Widget *Open Source* ist, kannst den Source Code auch [jederzeit einsehen][3], via [NPM einbinden][4] oder [daran mitwirken][5].


[1]: https://de.wikipedia.org/wiki/Wikipedia:Meinungsbilder/Protest_gegen_EU-Urheberrechtsreform
[2]: https://blackout21.eu/
[3]: https://github.com/timonf/save-your-internet-widget/tree/master/src
[4]: https://www.npmjs.com/package/save-your-internet-widget
[5]: https://github.com/timonf/save-your-internet-widget
