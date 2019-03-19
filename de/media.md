---
title: Unser Media Archiv - Bilder und HTML
description: Benutze unsere Resourcen, um an den Online-Protesten am 21. März teilzuhaben.
language: de
---

## Medien

Jeder kann die Idee von Wikipedia unterstützen mit den Hochladen eines schwarzen Profilbildes oder
mit dem Abschalten seiner Webseite.

### Statische HTML-Blackout-Seiten

Es gibt verschiedene Versionen für die Blackout-Seiten. Bitte einfach deine bevorzugte Version auf deinen Webserver
kopieren oder auf unsere Variante weiterleiten.

Die `blank`-Varianten funktionieren ohne weitere Dateien. Diese bestehen nur aus dem HTML-Code mit etwas inkludiertem CSS.
Für die `wallpaper`-Varianten benötigst du evtl. das Bild `wallpaper.jpg`.

{% include static_pages.html %}

Kleiner PHP Code-Schnipsel (einfach in die `index.php` oder in die `wp-include.php` kopieren).
Falls du das Skript testen möchtest einfach das Datum verändern (`2019-03-21`).

```php
if ('2019-03-21' === (new \DateTime())->format('Y-m-d')) {
    $url = 'https://blackout21.github.io/blackout-static-pages/blackout_en.html'; // Oder benutze eine andere Version
    header('Location: ' . $url, true, 302);
    exit;
}
```

[1]: https://de.wikipedia.org/wiki/Wikipedia:Meinungsbilder/Protest_gegen_EU-Urheberrechtsreform
[2]: https://blackout21.eu/
