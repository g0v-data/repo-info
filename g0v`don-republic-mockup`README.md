# don-republic: Social eDemocracy

動民主

[![Stories in Ready](https://badge.waffle.io/g0v/don-republic.png?label=ready)](http://waffle.io/g0v/don-republic)

[Prototype Demo](http://g0v.github.io/don-republic-mockup/)

Using:

* Sass
* Compass
* Semantic UI
* Jade
* Angular JS
* Firebase
* AngularFire

# Preparing

* Notice: if your compass version is 0.12.6, make sure it is not [conflict](https://rubygems.org/gems/compass) to sass.

clone the repository

    git clone https://github.com/g0v/don-republic.git

## Mac

* Install Brew
    * http://brew.sh/

## Windows

* now using Fire.app build views/ to public/
* if build doesn't work: jade -w views -o public
* compile json.ls fake data: lsc -cj test.json

# Development

## Install dependency

    $ npm install
    $ bundle install

## Start development

    $ gulp dev

# Deploy

just execute the script to update prototype. Of course you already granted permission to update gh-pages.

    $ git push
    $ ./deploy

# License

License: http://g0v.mit-license.org/

