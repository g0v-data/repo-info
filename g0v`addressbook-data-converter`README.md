# addressbook-data-convert

To convert Taiwan government organization rawdata from multiple sources in [popolo project] (http://popoloproject.com) specification.

The sources of rawdata can be found in file `data-index.json`.

[Document](http://g0v.github.io/addressbook-data-converter)


# Prerequisite

- [Node.js](https://nodejs.org/) [npm](https://www.npmjs.com/)


## Installation

Change your current working directory to the (addressbook-data-convert) project root

```
$ cd /path/to/addressbook-data-convert
```

Use npm to install packages

```
$ npm i
```

## Update Source Properties

You should run this command after adding new rawdata source in `config.ls`.

```
$ lsc update-data-index.ls
$ lsc fetch-data.ls
```

## Generate Final Data

The database name for building is `mydb` by default
and you don't need to create it manually. The `make boot`
command will do it.

```
$ make boot
$ make build
```

## Re-Generate Final Data

```
$ make rebuild
```

NOTED: if your pg module got some errors, try `npm rebuild pg`

After building, an dumped sqlfile can be find in `output/addressbook.sql`.

## Test

```
$ npm test
```

## Build Documents

```
$ pip install Pygments
$ npm i groc
$ ./node_modules/groc/.bin/groc
```

The documents will be in the gh-pages branch.
