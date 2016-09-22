#揭露22K#
Source code of 22kopendata.org

##專案目的##
一個專門揭露台灣不公平薪資的公益網站。

##技術資訊##
- PHP Framework: CodeIgniter 2.1.3
- DB: MySQL

##使用方式##
1. 修改htaccess
  - 先修改 .htaccess 的 "RewriteBase /" 改為您server上的相對路徑。
  - 如果你的路徑是 "/22k-test" 則修改為 "RewriteBase /22k-test"

2. 修改網域設定
  - 開啟application/config/config.php修改$config['base_url']為您的網站路徑。
  - 如果您安裝在example.com/22k-test，則修改為$config['base_url']	= 'http://example.com/22k-test/';

3. 修改DB設定
  - 請先將22kopendata.sql匯入MySQL，再修改application/config/database.php裡面的MySQL連線設定。
