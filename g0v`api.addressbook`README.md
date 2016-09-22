# api.addressbook

api.addressbook.g0v.tw endpoint source and utiltity scripts.

demo site: [http://pgrest.io/hychen/api.addressbook/v0/collections/](http://pgrest.io/hychen/api.addressbook/v0/collections/)

## Installation 

Install Postgresql 9.3 in your laptop and the run the following instructions:

```
$ git clone https://github.com/g0v/api.addressbook
$ cd api.addressbook && npm i
$ createdb testdb
$ lsc app.lsc --db testdb
```

### Demo Box

#### Docker

get an image.

```
$ docker pull hychen/api.addressbook
```

start service.

```
$ docker run -d -p 8888:80 hychen/api.addressbook /sbin/my_init
```

### Vagrant

bootstrap vagrant box.

```
$ cd cookbooks/addressbook.g0v.tw && vagrant up
```

## Play with the server

```
$ curl 0.0.0.0:8888/v0/collections/
```


## Setup Development Envrionment.

### Install Postgresql 

- [Postgresql.app](http://postgresapp.com)

### Populating Data

The default database is `mydb`.

```
$ git clone https://github.com/g0v/addressbook-data-converter
$ cd addressbook-data-converter
$ npm i 
$ make boot && make build
```

### Start REST server

```
$ git clone https://github.com/g0v/api.addressbook
$ cd api.addressbook
$ npm i
$ lsc app.ls --db mydb --schema pgrest
info: Available collections:
memberships organizations person posts
info: Serving `mydb` on http://127.0.0.1:3000/collections
```
