---
title: Unser Media Archiv - Bilder und HTML
description: Benutze unsere Resourcen, um an den Online-Protesten am 21. März teilzuhaben.
language: de
---

## Medien

Jeder kann die Idee von Wikipedia unterstützen mit den Hochladen eines schwarzen Profilbildes oder
mit dem Abschalten seiner Webseite. Weiter unten findet man Code-Snippets für HTML, JavaScript oder
PHP.


### Profilbild

Sei ein Teil von **Blackout21** und benutze ein schwarzes Profilbild am 21. März. Falls du gerade kein
schwarzes Profilbild zur Hand hast, kannst du dich auch bei uns bedienen!

{% include profile_pictures.html %}


### Story-Bilder

Diese Bilder kannst du am 21. März als Story bei WhatsApp, Snapchat, Instagram oder Facebook hochladen:

{% include stories.html %}


### Banner

Hier sind einige Banner, die über den Online-Protest am 21. März informieren:

{% include banners.html %}


### Twitch

Auch alle Streamer auf Twitch sind dazu eingeladen, sich am 21. März zu beteiligen. Hierzu kann man in den Streams Einblendungen
anzeigen, welche die Zuschauer auf die Proteste gegen Artikel 13 aufmerksam machen!

Twitch-Streamer können diese Banner bzw. Overlays permanent einblenden oder in bestimmten Intervallen! Es gibt dabei zwei
Versionen. Für eine sollte ein Bot konfiguriert werden, der auf "!Artikel13" reagiert; die andere Version verweist auf
die Demo-Übersichts-Seite von [Save The Internet](https://bit.ly/a13demos).

{% include twitch.html %}


### Statische HTML-Blackout-Seiten

Mit einer statischen Blackout-Seite kannst du deine Besucher am einfachsten über die Proteste gegen Artikel 13
(sowie 11 und 12) und die EU-Urheberrechtsreform informieren!

Es gibt verschiedene Versionen für die Blackout-Seiten. Bitte einfach deine bevorzugte Version auf deinen Webserver
kopieren oder auf unsere Variante weiterleiten. Die `blank`-Varianten funktionieren ohne weitere Dateien.
Diese bestehen nur aus dem HTML-Code mit etwas inkludiertem CSS. Für die `wallpaper`-Varianten benötigst 
du evtl. das Bild `wallpaper.jpg`.

{% include static_pages.html %}

Falls du Hilfe benötigst, kontaktiere bitte <a href="https://twitter.com/Blackout21_EU">Blackout21_EU</a> auf Twitter.


#### PHP

Kleiner PHP Code-Schnipsel (einfach in die `index.php` oder in die `wp-include.php` kopieren).
Falls du das Skript testen möchtest einfach das Datum verändern (`2019-03-21`).

```php
if ('2019-03-21' === (new \DateTime())->format('Y-m-d')) {
    $url = 'https://blackout21.github.io/blackout-static-pages/blackout_de.html'; // Oder benutze eine andere Version
    header('Location: ' . $url, true, 302);
    exit;
}
```


#### HTML

Man kann auch eine Zeile **HTML** seiner Seite hinzufügen:

```html
<!-- add this to your head tag -->
<meta http-equiv="refresh" content="0; url=https://blackout21.github.io/blackout-static-pages/blackout_de.html">
```


#### JavaScript

Und man kann ebenso einfach eine Zeile **JavaScript** irgendwo auf seiner Seite platzieren:

```html
<script>location.href = "https://blackout21.github.io/blackout-static-pages/blackout_en.html";</script>
```


### Widget

Wenn du nicht deine komplette Seite abschalten möchtest, wird ebenso ein Popup angeboten, welches am 21. einen Hinweis
zeigen wird. Um dies vorab zu testen, kann man einfach `#showsaveyourinternet` zur URL hinzufügen. Der Code lässt sich
überall auf der Webseite platzieren (im `head`- oder `body`-Bereich) – aber wir empfehlen den Code direkt vor dem
schließenden `</body>` zu platzieren. **Hinweis:** Einige Seiten (wie bspw. die kostenlose Version von WordPress.com)
erlauben leider kein eigenes JavaScript.

Klicke auf "Preview", falls du wissen willst, wie das Widget auf unserer Seite damit aussieht.

{% include widget.md %}

Wenn du dir unsicher auf Grund des Server-Standortes bist, kannst du

* entweder das Skript auf deinen Server hochladen und verlinken
* oder die Version von _blackout21.eu_ benutzen: `https://blackout21.eu/static/syi-widget.js`.

Da das Widget *Open Source* ist, kannst den Source Code auch [jederzeit einsehen][3], via [NPM einbinden][4] oder [daran mitwirken][5].


[1]: https://de.wikipedia.org/wiki/Wikipedia:Meinungsbilder/Protest_gegen_EU-Urheberrechtsreform
[2]: https://blackout21.eu/
[3]: https://github.com/timonf/save-your-internet-widget/tree/master/src
[4]: https://www.npmjs.com/package/save-your-internet-widget
[5]: https://github.com/timonf/save-your-internet-widget
