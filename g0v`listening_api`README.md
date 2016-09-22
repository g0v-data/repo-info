# g0v 福利請聽 API 專案

本專案為 g0v 福利請聽的法條 api 專案。

### 開放 API

本專案開放 API 的使用，可以透過機關－法條的形式取得法條資訊。

產生的格式為 JSON 。

機關 API

    http://listening-api.g0v.tw/public/orgs.json
    http://listening-api.g0v.tw/public/orgs/:eng_name.json

法條 API

    http://listening-api.g0v.tw/public/orgs/:eng_name/rules.json
    http://listening-api.g0v.tw/public/orgs/:eng_name/rules/:id.json

或是

    http://listening-api.g0v.tw/public/rules/:id.json

AJAX 範例

    $.ajax({
      type: "GET",
      url: 'http://listening-api.g0v.tw/public/orgs/KHH/rules/1',
      dataType: 'jsonp'
    }).success(function(data){
      console.log(data);
    });

### 免責聲明

本專案內所收錄的法條，由福利請聽團隊整理自各項福利的官網資訊，且福利來源以該單位最新頒佈為準，本專案之資料僅供參考，若有不正確之處請來信與我們反應。

此外，針對收錄之內容沒有任何相關領域的專家和專業人員再對內容的完善性、正確性或可靠性進行驗證，故本專案不保證其內容正確無誤。

本專案也未作出任何明示或默示的擔保。任何使用本專案之人士，須自行承擔一切風險，本專案不會負責任何因使用、重製或散布內容而引致之損失。

### License

The MIT license.

Copyright © 2013 KUN-HANG LEE

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.