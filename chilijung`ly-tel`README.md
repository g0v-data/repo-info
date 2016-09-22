# tisa-call

call ly for help.

## Develop

### Install canner
Using [canner](https://github.com/canner/canner) to generate HTML files

Please reference [How to install canner?](https://github.com/canner/canner#how-to-install).

After install canner, use canner to build the HTML files.

    canner build canner.json 

then it would generate all you needed files.

### Change setting

the settings are all in `canner.json`

### template

template is in `template` folder => `default.hbs` using `handlebars.js`

### gulp

For compiling scss to css you can use `gulp`

```
npm install
```

to install gulp required packages. And enter gulp in root folder, it will compile all `scss` files in `css` folder to `css`.

### git submodule

「尋找選區立委」要正常使用請拉取 git submodule

```
$ git submodule init
$ git submodule update
```

## Contributors

#### Developers

- [@ctxhou](https://github.com/ctxhou)
- [@MrOrz](https://github.com/MrOrz)
- [@shengli1989](https://github.com/shengli1989)
- [@audreyt](https://github.com/audreyt)
- [@clkao](https://github.com/clkao)
- [@IanWang](https://github.com/IanWang)
- [@shaform](https://github.com/shaform)
- [@timdream](https://github.com/timdream)

#### 三動作圖片 License 

- 三動作護台灣由 @ChangeLin 製作，以創用CC 姓名標示-非商業性 4.0 國際 授權條款釋出。

#### 定位尋找區域立委

由 @timdream 所開發

see also:

https://github.com/timdream/rep-locator

## Thanks 

Thanks to all g0v members.

## License 

MIT
