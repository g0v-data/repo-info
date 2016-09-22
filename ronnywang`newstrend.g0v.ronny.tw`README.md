newstrend.g0v.ronny.tw
======================
這是 http://newstrend.g0v.ronny.tw/ 的程式碼，主要是將 newsdiff 匯出的新聞資料匯入之後，可以對內容做統計

初始設定
--------
* 在 webdata/config.php 增加
```php
<?php
putenv('DATABASE_URL=mysql://[user]@[password]@[ip]/[db]'); // MySQL 帳號密碼
putenv('DATA_PATH=[path]'); // path 是存放新聞資料的路徑
```
* 第一次需要建立 Table ，請執行 php webdata/prompt.php ，並輸入 
```php
NameList::createTable();
NameStat::createTable();
NewsStat::createTable();
```
* 第一次要匯入完整新聞資料，可執行 php webdata/scripts/import-news.php

服務
----
* 可以用 php -S 0:12345 index.php ，然後透過 http://localhost:12345 看看是否有內容
* 需要跑 php webdata/scripts/worker.php 跑一隻 worker ，當送出需求時處理計算的 worker

License
-------
* 本程式碼是以 MIT License
* Pix Framework 是 BSD License
