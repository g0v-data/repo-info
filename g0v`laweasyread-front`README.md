# Introduction
* Parse the contents of webpages to view Taiwan's law articles/websites easier.
* related with [g0v/laweasyread](https://github.com/g0v/laweasyread) but functions differently and not combined together yet.

可將網頁中的法規、條文、大法官解釋、判決字號均加上連結。使用方式有三：
* 安裝為 [Firefox 附加元件](https://addons.mozilla.org/zh-TW/firefox/addon/laweasyread/)（[備份](http://g0v.github.io/laweasyread-front/dist/laweasyread.xpi)）或[Google 瀏覽器擴充功能](https://chrome.google.com/webstore/detail/iedodmlnmhobigohbkalkkjlbmdkjalj)（[測試頁面](http://g0v.github.io/laweasyread-front/browser.html)）
* 在[轉換頁面](http://g0v.github.io/laweasyread-front/userInput.html)貼上法律相關網頁或檔案的內容文章，可以立即將該文章顯示為有連結的樣貌。
* 網頁內嵌JavaScript方式，以使未安裝瀏覽器外掛的網友亦能看到自動加上連結的法規和條文。（[示範頁](http://g0v.github.io/laweasyread-front/embed.html)）

## Capability
網頁中提到法規名稱或是條文時：
* 將法規名稱加上連往[全國法規資料庫](http://law.moj.gov.tw/)看該法規全文的網頁連結。
* 將法條連向[全國法規資料庫](http://law.moj.gov.tw/)看該些條文。
* 提到大法官解釋時，即連向該號解釋的官方網頁。

如使用[Google 瀏覽器外掛](https://chrome.google.com/webstore/detail/iedodmlnmhobigohbkalkkjlbmdkjalj)，亦能：
* 運作於Facebook、[零時政府立法院](http://ly.g0v.tw.jit.su/)、[評律網](http://www.pingluweb.com/)等動態更新的內容的網頁機制（需點選網址列的按鈕）。
* 滑鼠移動到法規名稱上時，跳出浮動視窗顯示其沿革（立法、修法史）。
* 滑鼠移動到條文號碼上方時，跳出浮動視窗顯示該條文內容。
* 將下列網站稍做排版，使易於閱讀：
    * [大法官解釋](http://www.judicial.gov.tw/constitutionalcourt/p03.asp)
    * [立法院法律系統](http://lis.ly.gov.tw/lgcgi/lglaw)
    * [司法院裁判書查詢](http://jirs.judicial.gov.tw/FJUD/)
* 自動送出裁判書查詢

## Examples
* 大法官解釋（[範例網頁連結](http://www.judicial.gov.tw/constitutionalcourt/p03_01.asp?expno=617)）
![Judicial Interpretation](http://images.plurk.com/kAGZ-22KieXBnFHCtsKe8DBiD8u.jpg)
* 立法院法律系統（[範例網頁連結](http://lis.ly.gov.tw/lghtml/lawstat/reason2/01183100110400.htm)）
![Legislative Yuan](http://images.plurk.com/kAGZ-5bvO4HGPifAXwkDU9CAs3y.jpg)
* 全國法規資料庫（[範例網頁連結](http://law.moj.gov.tw/LawClass/LawSearchNo.aspx?PC=B0000001&SNo=1079.4,1079.5)）
![Laws & Regulations Database](https://fbcdn-sphotos-h-a.akamaihd.net/hphotos-ak-ash4/1014200_10152542008401393_14309567_n.jpg)
* 0.4.6 版新增（僅Chrome支援）
![0.4.6版截圖](https://f.cloud.github.com/assets/4002443/1027780/1cc38ae8-0e78-11e3-85c9-794224fed793.jpg)

# Installation

## Browser Extension
* Firefox 附加元件已停止維護。
* Google 瀏覽器請至[Chrome 線上應用程式商店](https://chrome.google.com/webstore/detail/iedodmlnmhobigohbkalkkjlbmdkjalj)安裝。

可比對安裝前後[測試頁面](http://g0v.github.io/laweasyread-front/browser.html)的顯示差異。

## Embed JavaScript in websites or blogs
[內嵌JavaScript 示範頁](http://g0v.github.io/laweasyread-front/embed.html)。

在網頁HTML原始碼中的`</head>`前加入
```html
<link href="http://g0v.github.io/laweasyread-front/stylesheets/main.css" rel="stylesheet" type="text/css" />
<script src="http://g0v.github.io/laweasyread-front/dist/laweasyread.js" type="text/javascript"></script>
<script src="http://g0v.github.io/laweasyread-front/javascripts/embedded2.js" type="text/javascript"></script>
```

## Warning
警告：部落客於編輯網誌時，請暫時關閉本外掛。

# Disclaimer
甚麼都不負責。

# License
[MIT License](http://en.wikipedia.org/wiki/MIT_License)再加上一條：
被授權人於出版發行、散布、再授權及販售軟體及軟體的副本時，應於MIT授權條款上方或下方加上此規則，並：
* 陳述被授權人對於一個以上之公共議題之立場；或
* 附上與其立場類似之文章之永久連結。

此軟體此版本設定之公共議題為「性別」，立場為「性解放」，支持十歲以上智識者均得自主與人發生性行為與性交易，「性忠貞」並不是「道德」的一部份。（參閱[反守貞地圖．哲學哲學雞蛋糕](http://phiphicake.blogspot.tw/2013/06/blog-post_4.html)。惟亦請留意諸多國家規定與未達法定年齡者合意性交、性交易仍需受刑事或行政處罰。於中華民國，與未滿十六歲者合意猥褻或性交、引誘未滿十八歲者為猥褻或性交，以及與任何人為有對價之性交或猥褻行為，均為法律所禁止。參閱[刑法第227條](http://law.moj.gov.tw/LawClass/LawSingle.aspx?Pcode=C0000001&FLNO=227)、[兒童及少年福利與權益保障法第2條、第49條第9款、第97條第1項](http://law.moj.gov.tw/LawClass/LawSearchNo.aspx?PC=D0050001&SNo=2,49,97)、[兒童及少年性交易防制條例第2條、第22條、第23條](http://law.moj.gov.tw/LawClass/LawSearchNo.aspx?PC=D0050023&SNo=2,22,23)、[社會秩序維護法第80條](http://law.moj.gov.tw/LawClass/LawSingle.aspx?Pcode=D0080067&FLNO=80)。）

## License Explanation
* 於其軟體再版時，得變更議題與立場、連結。
* 軟體之使用與修改者，無須同意原軟體授權條款中，基於本規則而對特定議題表態之立場。

# Notices
* 全國法規資料庫有收錄的均會加上連結－－除非原本已經是連結。
* 純文字元件如 `TEXTAREA` 等會跳過不處理，列表見`LER.js`的`skippingTags`。
* 在內嵌其他網域的框架時（如Facebook的留言或按讚外掛），會有瀏覽器警告（似乎不影響運作）。

# Bugs
* 可能與WYSIWYG編輯器的相互干擾!!!!
* 會發生「漩渦鳴人的 §8 尾巴出現了」和「我國的 §3 國道走山事件」
* 未能妥善處理以換行字元或`BR`標籤來排版的網頁（如[司法院裁判書查詢](http://jirs.judicial.gov.tw/FJUD/)）。

# Development

## First Idea
原本是以字串取代的方式去改變`document.body.innerHTML`，但發現有三個難處：
* 有（類似）onLoad function的網頁（如「全國法規資料庫」的首頁）即會無後續動作。
* 不知道要怎麼樣避開HTML tag的屬性中的字串，特別是要提防屬性字串中又包含特殊字元的情形。
* 不知道怎麼偵測「是否已在<a />中」，困境同上。

## Current Scheme
用遞迴方式跑過整個HTML的DOM tree，抓出textNode來處理。
因此，勢必得用`document.createElement`和`Node#appendChild`等DOM方法，而不能修改`Element#innerHTML`。

## Algorithm
參閱`LER.js`，把每個「只含文字的節點」（`TEXT_NODE`)代換成一串新的節點。

* `parseElement()`嘗試處理`document.body`的每一個child。
    * 把非純文字的child再丟給`parseElement()`去recursion；
    * 把純文字的child代換為丟去`parseText()`而得到的node array
* `parseText()`
    * 用規則一的正規表示式把字串分段，把不匹配的部份再丟給規則二
    * 規則二的正規表示式不匹配的部份，再丟給規則三
    * 依此類推，直到沒有規則可再套用
    * 所有規則均跑完後，即回傳陣列，回到`parseElement()`把原本的文字節點替換成新的節點列。
* 將 `parseInt()` 改寫為支援中文數字，參閱`parseInt.js` （授權條款同上）
* 關於「多個條號」的處理，參閱`LER.js`中註解文字「條號比對－－支援多條文」以下

## Links to regulations
將[全國法規資料庫](http://law.moj.gov.tw/)中有收錄的（包含「已廢止法規」）均加上連結。其方法為：
* 將[g0v/laweasyread-data](https://github.com/g0v/laweasyread-data)的`data/pcode.json`改為本專案的`pcode.js`（就只是灌進一個變數中）
* 將名稱中只有中文、沒有標點符號的法規（約九千個）全部以'|'為連接符號，由長至短串成一個字串（共近20萬字），生成一個巨大的正規表示式。
