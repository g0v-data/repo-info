LetsFuMouAPI
=============

The FuMou Public Hearing's Data API for [Let's FuMou](https://www.facebook.com/LetssFuMou).

API: [http://letsfumou-api.herokuapp.com/api/1.0/all](http://letsfumou-api.herokuapp.com/api/1.0/all)

## Usage

- api/1.0/all?[index={index}][&hearingName={hearingName}][&hearingProfession={hearingProfession}][&date={date}]
    + index: The index of the public hearing.
    + hearingName: The Name of the public hearing.
    + hearingProfession: The professions of the public hearing.
        * 貿易協定, 環境服務, 資訊工業 etc.
    + date: The date of the the public hearing.

## Data format

``` publicHearing.json
[
    {
        hearingName: "「海峽兩岸服務貿易協議」第一場公聽會",
        hearingProfession: 
        [
            "貿易協定",
            "市場管理",
            "就業輔導",
            "大陸政策"
        ],
        date: "7/31/2013",
        data: [
            {
                speaker: "徐偉群",
                title: "中原大學財經法律學系副教授",
                profession: "",
                youtubeLink: "https://www.youtube.com/watch?v=mJpVwXDZmIA",
                content: "主席、各位委員.... "
            }
        ]
    }
]
```

## Change Log

### 2014/04/07 v0.0.2
- Add query parameter.

### 2014/04/04 v0.0.1
- 0.0.1 API.

## Installation

`npm i`

`npm start`

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
