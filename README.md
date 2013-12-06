octopress-encodeURIComponent
============================

Filter to encode URI component like JavaScript's encodeURIComponent() for Jekyll/Octopress.

# Installation

Copy `plugins/keyboardkey.rb` to your `plugins` directory. That's all!

# Usage

Use as a filter for Liquid values like

    This is original: {{site.url}}

    This is encoded: {{site.url|encodeURIComponent}}

If the `site.url` is `http://rcmdnk.github.io/`, this will be


    This is original: http://rcmdnk.github.io/

    This is encoded: http%3A%2F%2Frcmdnk.github.io%2F


This is useful especially if you want to pass uri to such tumblr's share link:

    <a href="http://www.tumblr.com/share/link?url={{page.url|encodeURIComponent}}&name={{page.title|encodeURIComponent}}&description={{page.description|strip_html|condense_spaces|truncate:150|encodeURIComponent}}" title="Share on Tumblr" class="tumblr_button" style="">Tumblr</a>

Original buttons ([Buttons | Tumblr](http://www.tumblr.com/buttons)) are provided with additional JavaScript to encode these items.
But you don't need such script with this filter and can write directly in one place.


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/rcmdnk/octopress-encodeuricomponent/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

