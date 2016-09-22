
全國 BOT 地圖
=============

資料來源 <http://ppp.pcc.gov.tw/PPP.Website/Case/AnnounceView.aspx>

1. 爬資料下來以後, 找出內文的地址或地號
2. 用 Google Map API 從地址對出 polygon, 或用 <http://maps.nlsc.gov.tw/> 或 <http://easymap.land.moi.gov.tw/> 人工查出資料, 例 <http://landmaps.nlsc.gov.tw/S_Maps/qryTileMapIndex?callback=jQuery164018557332758791745_1386087757286&type=2&flag=2&office=WA&sect=0186&landno=04030048&alpah=0.5f&_=1386088000593>
3. GeoJSON 釋出.

Install
-------

```
npm i
node crawler/crawler.js
```
