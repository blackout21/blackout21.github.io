---
title: Our media archive – Images and HTML
description: Use one of our media resources to be part of the online protests on March 21st, 2019.
language: en
---

## Media

Everyone can support Wikipedia's online protest by uploading a black profile picture or by shutting down their
own website. You will also find code snippets for JavaScript, HTML and PHP below.


### Profile picture

Take part of **Blackout21** and use a black profile picture on March 21st! If you can't find any blank profile
picture, you can just use this one:

{% include profile_pictures.html %}


### Story images

You can use this picture to use as story on WhatsApp, Snapchat, Instagram or Facebook:

{% include stories.html %}


### Banners

There are some banners, which informs users about the protests against Article 13:

{% include banners.html %}


### Static blackout pages

You can inform your visitors easily about the protests and the EU copyright directive using a static blackout page.

There are different versions. You can just copy you favorite version to your webserver or redirect to our version!
The `blank` versions work without any external resources. It's pure HTML with some inline CSS. For the `wallpaper`
versions you need the additional `wallpaper.jpg`.

{% include static_pages.html %}

If you need any help, please contact <a href="https://twitter.com/Blackout21_EU">Blackout21_EU</a> on Twitter.


#### PHP

Small PHP code snippet (just copy it to your `index.php` or `wp-include.php`). You can modify the date (`2019-03-21`), if
you want to test it.

```php
if ('2019-03-21' === (new \DateTime())->format('Y-m-d')) {
    $url = 'https://blackout21.github.io/blackout-static-pages/blackout_en.html'; // Or use another version
    header('Location: ' . $url, true, 302);
    exit;
}
```


#### HTML

You can also use simple **HTML** meta tag to redirect your visitors:

```html
<!-- add this to your head tag -->
<meta http-equiv="refresh" content="0; url=https://blackout21.github.io/blackout-static-pages/blackout_en.html">
```


#### JavaScript

And you can additionally use a single line of **JavaScript**, too:

```html
<script>location.href = "https://blackout21.github.io/blackout-static-pages/blackout_en.html";</script>
```


### Widget

If you don't want to disable your whole website, you can also show a big popup to your visitors. If you include this 
script on your page, the popup will only show on March 21st. You can also test it by adding `#showsaveyourinternet` to
page's URL). You can put this code snippet everywhere on your page (`head` or `body`) – but we recommend to place it
right before `</body>`. **Warning:** Some sites does not allow custom JavaScript (like free version of WordPress.com)!

Click on "Preview" to see this widget in action on our page.

{% include widget.md %}

This widget is *open source*. So you can [explore the code][3], [use it via npm][4] or [contribute to it][5]!

If you are unsure or worried by the server location, you could

* upload the script to your own server
* or use version by _blackout21.eu_: `https://blackout21.eu/static/syi-widget.js`.


[1]: https://de.wikipedia.org/wiki/Wikipedia:Meinungsbilder/Protest_gegen_EU-Urheberrechtsreform
[2]: https://blackout21.eu/
[3]: https://github.com/timonf/save-your-internet-widget/tree/master/src
[4]: https://www.npmjs.com/package/save-your-internet-widget
[5]: https://github.com/timonf/save-your-internet-widget
