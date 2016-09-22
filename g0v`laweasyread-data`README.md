# Introduction
[![Build Status](https://travis-ci.org/g0v/laweasyread-data.png)](https://travis-ci.org/g0v/laweasyread-data)
[![Dependencies Status](https://gemnasium.com/g0v/laweasyread-data.png)](https://gemnasium.com/g0v/laweasyread-data)

This is the data for [laweasyread](https://github.com/g0v/laweasyread). Please
run `npm install` if you want to use any script in this project.

# Script

## Crawler
Scripts in
[crawler](https://github.com/g0v/laweasyread-data/tree/master/crawler) are used
to crawl data and store them info [rawdata](https://github.com/g0v/laweasyread-data/tree/master/rawdata).

## Parser
Scripts in
[parser](https://github.com/g0v/laweasyread-data/tree/master/crawler) are used
to parse [rawdata](https://github.com/g0v/laweasyread-data/tree/master/rawdata)
and store them info
[data](https://github.com/g0v/laweasyread-data/tree/master/data)

The options of parser are listed as following:

* `--rawdata path`
    * Path of rawdata.
* `--output path`
    * Path of output.

Using default value will update
[rawdata](https://github.com/g0v/laweasyread-data/tree/master/rawdata) and
[data](https://github.com/g0v/laweasyread-data/tree/master/data) directories:

# Rawdata
[rawdata](https://github.com/g0v/laweasyread-data/tree/master/rawdata) contains
all raw data from government. The description of each directory are listed as
following:

* [lawstat](https://github.com/g0v/laweasyread-data/tree/master/rawdata/lawstat)
    * From [立法院法律系統](http://lis.ly.gov.tw/lgcgi/lglaw)
* [utf8_lawstat](https://github.com/g0v/laweasyread-data/tree/master/rawdata/utf8_lawstat)
    * UTF-8 version of lawstat. This is created by
      [big5\_to\_utf8.sh](https://github.com/g0v/laweasyread-data/tree/master/rawdata/big5_to_utf8.sh)
      in rawdata directory
* [LawClassList](https://github.com/g0v/laweasyread-data/tree/master/rawdata/LawClassList)
    * From [全國法規資料庫](http://law.moj.gov.tw/LawClass/LawClassList.aspx)
    * Provide name and PCode mapping.

The
[lawstat](https://github.com/g0v/laweasyread-data/tree/master/rawdata/lawstat)
is downloaded by [twlaw](https://github.com/g0v/twlaw).

# Data
[data](https://github.com/g0v/laweasyread-data/tree/master/data) contains json
files for mongodb. Use the following command to create database:

    ./node_modules/.bin/lsc import.ls

# Bugs
Please report any problem in [here](https://github.com/g0v/laweasyread-data/issues).

# Copyright
The source code is under [MIT License](https://github.com/g0v/laweasyread-data/blob/master/LICENSE).

All data in this project are not the subject matter of copyright, according to
[Copyright Act § 9](http://law.moj.gov.tw/Eng/LawClass/LawSearchNo.aspx?PC=J0070017&DF=&SNo=9).
