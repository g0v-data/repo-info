Baddriver API server
============

This is BadDriver.tw back-end server. 


BadDriver f2e (Use Yeoman & AngularJS):
[click here](https://github.com/g0v/BadDriver.tw)

#API Lists

[click it](http://api.dont-throw.com/youmeb/routes.json)

##Usage

1. `npm install youmeb-cli`
2. `npm i`
3. `mkdir 'config'`
4. `cd config`
5. `vim default.json`
    
  ```javascript
    {
    "port": 3001,
    "host": "localhost",
    "controllers": "controllers",
    "error": {
      "format": "{level:1}{module:3}{code:2}",
      "file": "errors"
    },
    "logger": {
      "level": "debug",
      "dir": "log",
      "filename": "%s.log"
    },
    "packages": {
        "sequelize": {
            "db": "dbname",
            "username": "user",
            "password": "psd",
            "options": {
                "host": "router"
            }
        }
      }
    }
    
  ```
6. `youmeb sequelize:migrate`
7. `youmeb`




##專案構想
https://g0v.hackpad.com/BadDriver-sDcFsbD58zo


##待爬資料


##架構
__Backend__: nodejs(Youmeb.js)+Mysql

__f2e__: angular.js(Yeoman)

##Any Question? Fixe Bugs?
Please open issue or pull request.

