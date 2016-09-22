# Development
第一次請先執行

    $ echo 3000 > port
    $ npm i

安裝完之後打以下指令跑起 local web server

    $ npm start

然後在 browser 輸入 [http://localhost:3000](http://localhost:3000)

gulp 會自動幫你 compile jade to html, less to css, 合併 javascript, css 等。在更改任何一個檔案 gulp 也會幫你重新 compile。
