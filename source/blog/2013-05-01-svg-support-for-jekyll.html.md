---
title: SVG support for Jekyll
description: Setting up a new Jekll site? Here's how to get SVGs working.

tags: frontend, notes
---

I found the following solution on [Stack Overflow](http://stackoverflow.com/questions/13687030/how-do-i-configure-jekyll-to-serve-svg):

1. Create a `_plugins` directory in the root of your Jekyll project.
2. Create a file called `svg_mime_type.rb` in `_plugins`
3. Add this to `svg_mime_type.rb:`

~~~ bash
require 'webrick'
include WEBrick
WEBrick::HTTPUtils::DefaultMimeTypes.store 'svg', 'image/svg+xml'
~~~
