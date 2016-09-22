# Kuansim - [Project detailed description](http://goo.gl/Qy4h65)

This project is built on top of two MVC-like concepts. It is designed to leverage on the power of Rails to manipulate back-end API logics, along with taking advantage of the powerful front-end framework AngularJS to further delegate front-end rendering to the client.

## Code structure

```
kuansim-rails/
├── app
├── config
├── coverage
├── db
├── doc
├── features
├── kuansim
├── kuansim-frontend @ kuansim-frontend cal branch
├── lib
├── log
├── public -> kuansim-frontend/bin
├── script
├── spec
├── test
├── tmp
└── vendor
```

The code base is divided to two different repos: [kuansim-rails](https://github.com/g0v/kuansim-rails) and [kuansim-frontend (cal branch)](https://github.com/g0v/kuansim-frontend/tree/cal). We use git submodule to link to `kuansim-frontend` cal branch, so we can use a symbolic link `public` pointing to the build folder in `kuansim-frontend` repo.

Notice that `kuansim-frontend` serves as a single web application which it does not depend on Rails back-end to run. Instead, it uses AJAX calls to communicate with Rails.

## How to build the project

The rails part is fairly straightforward:

- Clone this project: (Notice the `--recursive` flag is needed here due to the submodule)

```sh
git clone --recursive git@github.com:g0v/kuansim-rails.git
```
- Install rails gems and run the server:

```sh
$ bundle install --without production
$ rake db:migrate db:test:prepare db:seed
$ rails s
```

The front-end AngularJS project needs a bit of work, please consult the [documentation](https://github.com/g0v/kuansim-frontend/blob/cal/README.md) for a detail walk-through. Note that the AngularJS build files are already included in `kuansim-frontend/bin` directory.

A brief instruction:

- cd into kuansim-frontend directory
- install necessarily dependencies (note: npm is required)

```sh
$ sudo npm -g install grunt-cli karma bower
$ npm install
$ bower install
```

- build the project

```sh
$ grunt
```

Now after the above steps, a running app should be available at `http://localhost:3000/`

## Test

- Rails:

`rake cucumber` and `rake spec` suffices. Though in the near future, we can no longer leverage on cucumber to do sophisticated integration tests.

- AngularJS: ([detail explanation available here](https://github.com/g0v/kuansim-frontend/blob/cal/README.md))

After installing GruntJS, invoking `grunt karma` command will trigger Jasmine unit tests as well as end-to-end tests. Or `grunt karma:unit` and `grunt karma:e2e` for running them individually. Note that, it is recommended to run all of the tests by invoking `grunt watch` or `grunt` command. Since the karma end-to-end test depends on the building process, it may fail due to not recognizing the browser path. (can be fixed by altering the navigation path but not recommended)










