grabejs
=======

What's this?
------------

1. Use phantomjs for grab and render webpage to png.
2. Use nginx for static image cache. (see config/nginx-sample.conf)
3. Use imagemagick for resize image.
4. Use phantomjs for pre-render html.

Usage
-----

Image:
- normal: http://<hostname>/shot/<graburl>
- thumbnail: http://<hostname>/shot/<graburl>_m
- original: http://<hostname>/shot/<graburl>_o original size

HTML:
- http://<hostname>/html/<graburl>

TODO
----
Save temporate file to another directory. 
