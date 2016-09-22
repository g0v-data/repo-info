g0v project hub mockup
==================

mockups for the new g0v project hub

how to join: http://g0v.github.io/project-hub-mockup/about

doc and discussion: http://g0v.github.io/project-hub-mockup/wiki

license: CC0

Development
============

Using:
* Sass
* Compass
* Semantic UI
* Jade
* jQuery
* Handlebars
* Underscore
* CSV-JS
* LiveScript

Local server and compilation:
* Fire.app
* Gulp

Deploy to gh-pages:
* for Windows: run deploy.bat on master branch
* If you commit into master, then Travis-ci would auto-deploy

Structure
------------
* assets
* livescripts
* sass
* views

Fire.app
============

Local Server
------------
* using Fire.app to preview sass and jade at 127.0.0.1:24681
* config.rb is for Fire.app
* tilt_jade.rb is for Jade and Fire.app

Jade -> HTML
------------
* using Fire.app to build views/ to public/
* if build doesn't work: jade views -o public

LiveScript -> Json
------------
* compile json.ls data: lsc -cj test.json

Gulp
============

* pre-dev:
    * install: [node](http://nodejs.org/)
    * install: ruby 2.0.0 (use [rubyuinstaller](http://rubyinstaller.org) on windows, use `rvm install 2.0.0` on linux/mac)
    * install compass (`gem install compass`)
    * install tilt (`gem install tilt`)
    * `npm i`
* devlopment:
    * `npm start`
    * open `http://localhost:3000/` to see the result.
