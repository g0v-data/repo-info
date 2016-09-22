CommuniqueAPI
=============
[![Build Status][travis-image]][travis-url] [![Dependency Status][david-dm-image]][david-dm-url]

[G0V Communique API](http://g0v-communique-api.herokuapp.com/api/1.0/entry/all). Parsing from [g0v hackpad](https://g0v.hackpad.com/ep/group/yZ9JT9UlJf4).

## Usage

### API 1.0 for g0v.tw

- GET all data of the tag
    + /api/1.0/entry/${tag}
- GET tag's data by date (YY or YY-MM or YY-MM-DD)
    + /api/1.0/entry/{$tag}?start=YY-MM
    + /api/1.0/entry/${tag}?start=YY-MM&end=YY-MM
- GET data by limit = x
    + /api/1.0/entry/${tag}?limit=x
- GET list of tags
    + /api/1.0/tags/all
- GET specific tag's content
    + /api/1.0/tags/${tag}

### API 2.0 for g0vTxT

- Get hackpad's Data
    + /api/2.0/hackpadData
- Get hackpad's History
    + /api/2.0/hackpadHistory
- Get all hackpad List
    + /api/2.0/hackpadList
- Get all hackpad's authors
    + /api/2.0/hackpadAuthors

## Data format

### Tags
```tags.json
[
    {
        name: "對外宣傳和媒體報導",
        description: "與 g0v 相關的宣傳以及媒體報導。 g0v對外產生的資訊由新聞中心發佈。",
        urls: [
            {
                name: "新聞中心",
                url: "http://hack.g0v.tw/g0vMOC/w01v8lrMLTY"
            }
        ]
    },
]
```

### Entry
```data.json
[
    {
        date: "2014/02/05",
        padID: "6hGHxaQ0yjb",
        tags: [
            "對外宣傳和媒體報導"
        ],
        content: "g0v 社群與英國推動數位民主的非營利組織 mySociety 及智利 Ciudadano Inteligente 基金會進行 irc 聊天室群談（紀錄），介紹彼此專案與合作可能，共二十餘人參與。 ",
        comment: [],
        urls: [
            {
                name: "mySociety",
                url: "http://www.mysociety.org/"
            }
        ],
        _id: "52f3be549d718d0200000026"
    }
]
```

### hackpadData
```
[
    {
        date: "20140508",
        num: 4
    }
]
```

### hackpadHistory
```
[
    {
        padID: "NxMrvI4uYcP",
        history: [ ],
        editNum: 618,
        createTimeStamp: 1399540293.516,
        authors: [
            "Nicemaker",
            "venev",
            "Moon Chang"
        ],
        authorsNum: 3
    }
]
```

### hackpadList
```
[
    {
        title: "有關於發送活動",
        padID: "O1D4BePJzej"
    }
]
```

### hackpadAuthors
```
[
    {
        name: "Nicemaker",
        editNum: 5,
        pads: [
            "NxMrvI4uYcP",
            "926nwUKC90j"
        ]
    }
]
```
## Preinstallation

### Config

Generate `config.js`.

```config.js
module.exports = {
    hackpad: {
        site: "Your hackpad's site",
        client: "You can find it on your account page in your site",
        secret: "You can find it on your account page in your site"
    }
}
```

### Environment
[![devDependency Status][david-dm-dev-image]][david-dm-dev-url]

- Install [mongoDB](http://www.mongodb.org/)
- Install [Node.js](http://nodejs.org/)

## Installation

- Install module: `npm i`
- Open mongoDB:   `mongob`
- Start server:   `npm start`

And then open `localhost:5000/api/1.0/entry/all` to get the communiques.

## Change Log

### 2014/12/25 v0.6.0
- Use "mongodb": "^2.0.x"

### 2014/06/08 v0.5.1
- Add test

### 2014/06/07 v.5.0
- Modify Hackpad List structure
- Auto update the hackpad history, data, list and authors.

### 2014/06/04 v0.4.1
- fix url bug.

### 2014/06/01 v0.4.0
- Refactor the loader and parser structure.

### 2014/05/26 v0.3.2
- fix the bug: cannot load the pad which its history is empty.
- Update README
    + Add preinstallation

### 2014/05/08 v0.3.1
- Add new api for g0vTxT
    + api/2.0/hackpadAuthors
- Modify hackpadHistory format

### 2014/05/06 v0.3.0
- Add new api for g0vTxT
    + api/2.0/hackpadData
    + api/2.0/hackpadHistory
    + api/2.0/hackpadList

### 2014/04/15 v0.2.0
- Modify get the list of tags API.

### 2014/03/09 v0.1.3
- Change the update time.

### 2014/03/07 v0.1.2
- It parses the communique form [http://g0v.hackpad.com](http://g0v.hackpad.com) automatically.It didn't config pad's ID anymore.

### 2014/03/06 v0.1.1
- It can get entry by limit length. Like /api/1.0/entry/${tag}?limit=x

## License

The MIT License (MIT)

Copyright (c) 2014 Lee  < jessy1092@gmail.com >

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


[travis-image]: https://img.shields.io/travis/g0v/CommuniqueAPI.svg?style=flat-square
[travis-url]: https://travis-ci.org/g0v/CommuniqueAPI

[david-dm-image]: http://img.shields.io/david/g0v/CommuniqueAPI.svg?style=flat-square
[david-dm-url]: https://david-dm.org/g0v/CommuniqueAPI

[david-dm-dev-image]: http://img.shields.io/david/dev/g0v/CommuniqueAPI.svg?style=flat-square
[david-dm-dev-url]: https://david-dm.org/g0v/CommuniqueAPI#info=devDependencies
