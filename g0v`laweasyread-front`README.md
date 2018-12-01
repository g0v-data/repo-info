# 法規亦毒氣

可將網頁中的法規、條文、大法官解釋加上連結，並可於滑鼠經過時瀏覽其內容。
[更新紀錄](changelog.md)


## 安裝

### 從各瀏覽器的官方網站

* [Chrome 擴充功能](https://chrome.google.com/webstore/detail/iedodmlnmhobigohbkalkkjlbmdkjalj)
* [Firefox 附加元件](https://addons.mozilla.org/zh-TW/firefox/addon/laweasyread/)
* Opera 延伸套件 審核中

### 手動安裝

1. 在[發布頁面](https://github.com/g0v/laweasyread-front/tree/gh-pages/dist)下載所需版本，並解壓縮之。
2. 進入瀏覽器的「擴充功能」設定頁面。
3. 開啟「開發人員模式」。
4. 點選「載入為封裝項目」，尋找步驟一解壓縮後的檔案路徑。

## 使用說明

* 使用網頁程式輸入資料（如使用 Evernote ）時請關閉，或將之加入例外清單。
* 僅針收錄於中華民國法務部的全國法規資料庫的法規。
* 頁面較複雜或資料較多時，不會瞬間轉換完畢。
* 本程式不保證資料安全與執行穩定，亦不保證提供之資料、連結之正確性。


# Development

## Files

* `README.md`: 此說明文件
* `changelog.md`: [更新紀錄](changelog.md)
* `g0v.json`: G0V 專案設定
* `package.json`: Node.js 專案設定
* `maniffest.json`: 瀏覽器擴充功能設定
* `LER.js`: 本專案主程式
* `parseData.js`: 將其他資料轉為本專案所需的資料並存為 `data.js`
* `data.json`: 法規名稱資料，由 `parseData.js` 產生
* `aliases.json`: 本專案法規簡稱資料，需手動維護


## Milestones

- [x] 比對到法規全名並加上連結
- [x] 比對法規簡稱
- [x] 將中文條號簡化
- [x] 將條號加上連結
- [x] 大法官解釋加上連結
- [ ] 裁判書連結
- [ ] 滑鼠移過時，顯示相關資訊
  - [x] 釋字
  - [x] 條文
  - [ ] 讓使用者可釘住浮動窗
- [ ] 瀏覽器外掛
  - [ ] 主流瀏覽器
    - [x] Chrome
    - [x] Firefox
    - [ ] Edge
    - [x] Opera
  - [x] 常用站台排版
    - [x] 全國法規資料庫的排版
    - [x] 立法院法律系統的排版
    - [ ] 裁判書？
    - [ ] 法源法律網？
  - [x] 設定頁面
  - [x] 更新法規名稱資料（不含法條）
  - [ ] 於頁面在例外清單中時，顯示適當標記
  - [ ] 下載法規資料庫（包含法條）
- [ ] 允許網站嵌入本專案
  - [ ] 設定轉換選項
  - [ ] 轉成 ES5
  - [ ] 支援 IE


## 重點檢查條文

* 不符合中央法規標準法所定的格式：
  * [所得稅法第4條（第1項第22款第2段）、第14條（第1項第9類第1款第2段）、第17條（第1項第2款第3目之6.(2)）](https://law.moj.gov.tw/LawClass/LawSearchNoIf.aspx?PC=G0340003&DF=&SNo=4%2c14%2c17)
  * [土地法第2條](https://law.moj.gov.tw/LawClass/LawSingleIf.aspx?Pcode=D0060001&FLNO=2)
* 多個條文引用，且條文引用包含「前段」、「但書」等字樣：
  * [行政訴訟法第131條](https://law.moj.gov.tw/LawClass/LawSingle.aspx?Pcode=A0030154&FLNO=131)
* 條文中的算式：
  * [全民健康保險藥物給付項目及支付標準第75條](https://law.moj.gov.tw/LawClass/LawSingleIf.aspx?Pcode=L0060035&FLNO=75)
* 原始資料缺漏一些標點符號：
  * [中央研究院組織法 第7條](https://law.moj.gov.tw/LawClass/LawSingle.aspx?Pcode=A0010016&FLNO=7)第2款
