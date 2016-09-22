# dc.vtaiwan.tw

[匯流五法：線上徵詢](SUMMARY.md)

# 開發

需要安裝 [__Node.js__](https://nodejs.org/)。安裝好後，開啟 Terminal 視窗按下列步驟執行指令。

1. `$ npm install`
2. `$ npm start`
3. 開啟瀏覽器鍵入 `http://localhost:3000`

(Node.js 0.10.x+ 也可用來開發，但部署時仍建議使用 4.x。)

# 設定

按 GitBook Markdown 格式編輯 SUMMARY.md 即可設定議題。

每次更新後，執行 `npm run update` 來產生 JSON 格式的設定檔。

# 部署

本系統使用 [zombie.js](http://zombie.js.org/) 搭配 [reactjs](https://facebook.github.io/react/) 的 server-side render 產生靜態網頁，並且使用 [gh-pages](https://pages.github.com/) 作為部署環境。請按照下列步驟執行指令。

1. `$ npm run static`
2. `$ npm run deploy`

# 貢獻方式

如果您對我們的專案有興趣或者找到錯誤，歡迎您一起幫忙修正，讓專案變得更好。請按照下列步驟進行。

1. 將 repo fork 到個人帳號下。
2. 按照開發一節，建立開發環境並且修正錯誤。
3. 將修正好的 commit 推到個人帳號下的 repo。
4. 建立一個新的 pull request，等待審核和 merge。

如果 merge 成功，恭喜您成為我們的一份子：）

# 貢獻者

請見[貢獻者名單](https://github.com/g0v/dc.vtaiwan.tw/graphs/contributors)。

# 授權

[CC0 1.0 Universal](LICENSE)
