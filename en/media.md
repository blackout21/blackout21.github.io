---
title: Our media archive – Images and HTML
description: Use one of our media resources to be part of the online protest on March 21st, 2019.
language: en
---

## Media

Everyone can support Wikipedia's online protest by uploading a black profile picture or by shutting down your
own website.

### Static blackout pages

There a different versions. You can just copy you favorite version to your webserver or redirect to our version!

The `blank` versions work without any external resources. It's pure HTML with some inline CSS. For the `wallpaper`
versions you need the additional `wallpaper.jpg`.

{% include static_pages.md %}

Small PHP code snippet (just copy it to your `index.php` or `wp-include.php`). You can modify the date (`2019-03-21`), if
you want to test it.

```php
if ('2019-03-21' === (new \DateTime())->format('Y-m-d')) {
    $url = 'https://blackout21.github.io/blackout-static-pages/blackout_en.html'; // Or use another version
    header('Location: ' . $url, true, 302);
    exit;
}
```

[1]: https://de.wikipedia.org/wiki/Wikipedia:Meinungsbilder/Protest_gegen_EU-Urheberrechtsreform
[2]: https://blackout21.eu/
