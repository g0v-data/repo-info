padnews-web
===========

http://congress-text-live.herokuapp.com/

十分陽春的 hackpad parser ，若有更好的處理方式，歡迎 patch 或告知。

Usage
-----

```
gem install foreman
npm install
npm start
```

Develop
-------

Please check `src/`, gulp will generate `public/` for you.

API
---

* latest: http://congress-text-live.herokuapp.com/json/
* all: http://congress-text-live.herokuapp.com/json/all/
* single entry: http://congress-text-live.herokuapp.com/json/0/

repos
-----

* parser: https://github.com/g0v/padnews
* cli: https://github.com/g0v/padnews-cli
* web: https://github.com/g0v/padnews-web

TODO
----

* possible timestamp
* select different hackpad
