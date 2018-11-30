# Introduction

* 新版，預計用 ES6 實作，並參考（或直接使用） React 。
* 法規名稱資料（暫定）不再從 g0v/laweasyread-data 抓，而是從 kong0107/mojLawSplitJSON 抓。詳見 `parseData.js` 。

## Files

* `README.md`: 此說明文件
* `g0v.json`: G0V 專案設定
* `package.json`: Node.js 專案設定
* `maniffest.json`: Google Chrome 擴充功能設定
* `icon.png`: Google Chrome 擴充功能圖示
* `LER.js`: 本專案主程式
* `parseData.js`: 將其他資料轉為本專案所需的資料並存為 `data.js`
* `demo.html`: 測試用
* `data.json`: 法規名稱資料，由 `parseData.js` 產生
* `aliases.json`: 本專案法規簡稱資料，需手動維護

## Milestones

- [x] 比對到法規全名並加上連結
- [x] 將中文條號簡化
- [x] 將條號加上連結
  - [x] 判斷該頁面的「預設法規」
  - [x] 判斷為剛提到的法規的所屬法條
  - [x] 判斷施行細則中提到的「本法」或「本條例」的條文
- [x] 比對到法規簡稱
- [x] 大法官解釋
- [ ] 裁判書連結
- [ ] 滑鼠移過時，顯示相關資訊
  - [x] 釋字
  - [x] 條文
  - [ ] 讓使用者可釘住浮動窗
- [ ] Chrome 外掛專屬
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
  - [ ] 支援 IE !?
- [ ] Firefox 外掛

### 不打算再支援

* 日期轉換
* 法院、檢察署的網站連結

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

## TODO

* 宣告 LER 時就直接讀取瀏覽器資料？
