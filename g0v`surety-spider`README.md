# surety-spider
蒐集嫌疑人交保資料的爬蟲

## 工具
* 語言：Python 3
* 搜尋：Headless browser、Selenium、WebDriver
* 解體：BeautifulSoup 4
* 儲存：Google 試算表

## 作法
1. 用 Google 找上個月的新聞，關鍵字使用 "萬交保"、"億交保"、"元交保"
1. 記住新聞連結與標題，新聞來源接受 "蘋果"、"聯合"、"自由"
1. 閱讀新聞，用解體程式拆出內文
1. 分析內文中的關鍵資訊
1. 不考慮重複問題，存入 Google 試算表
1. 完成整個月份的資料後，跑一次去重複化程式

## 參考資料
* Python
* * [Getting started](http://selenium-python.readthedocs.io/getting-started.html)
* * [WebDriver](https://seleniumhq.github.io/selenium/docs/api/py/webdriver_remote/selenium.webdriver.remote.webdriver.html#module-selenium.webdriver.remote.webdriver)
* * [Wait](https://seleniumhq.github.io/selenium/docs/api/py/webdriver_support/selenium.webdriver.support.wait.html#module-selenium.webdriver.support.wait)
* * [Element](https://seleniumhq.github.io/selenium/docs/api/py/webdriver_remote/selenium.webdriver.remote.webelement.html#module-selenium.webdriver.remote.webelement)
* [Selenium Ruby Bindings](http://seleniumhq.github.io/selenium/docs/api/rb/index.html)
* [Google 搜尋參數](https://support.google.com/websearch/answer/2466433?hl=zh-Hant)
