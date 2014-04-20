FancyZoom: jQuery Plugin
========================

jQuery plugin of Cabel's
[FancyZoom](http://www.cabel.name/2008/02/fancyzoom-10.html). This
version of FanyZoom attempts to be as minimual as possible. No gallery
or caption support. Just a simple zoom of linked images.

Download
--------

Easiest way to get the latest version is to just download the [latest release](https://github.com/keegnotrub/jquery.fancyzoom/releases) straight from github. Once unzipped, place the contents of the `js`, `css` and `img` folders accordingly into your site.

To Use
------

Include [`js/jquery-1.11.0.min.js`](http://code.jquery.com/jquery-1.11.0.min.js) and `js/jquery.fancyzoom.min.js`
inside your `<head>` section as shown.

    <script src="http://code.jquery.com/jquery-1.11.0.min.js"></script>
    <script src="js/jquery.fancyzoom.min.js"></script>
    
You will also want to include the `fancyzoom.css` file insead your `<head>`
section. Don't forget to change the background image paths if you place
contents of the `img` folder in an different directory.

    <link rel="stylesheet" href="css/fancyzoom.css">
    
Now when you create links to images in your `HTML`, you can flag them
with a class to have the become lightboxed.

    <a href="img/big.jpg" class="fancy"><img src="img/small.jpg"></a>

Then on your Javascript's `document` ready you can fire the jQuery
`fancyZoom` selector.

    $(document).ready(function() {
        $("a.fancy").fancyZoom();
    });

FancyZoom takes only one option `minBorder` which allows you to
specify how much border should always be around your images once
lighboxed. This value is `90` pixels by default.

    $(document).ready(function() {
        $("a.fancy").fancyZoom({
            minBorder: 90
        });
    });

Contact & Help
--------------

If you have questions or find a bug, you can always
[open an issue](https://github.com/keegnotrub/jquery.fancyzoom/issues) on github.
