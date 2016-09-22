nsc-projects
============

國科會計劃砍柴計畫
national science council projecti budget for every single institute since 1989


Data Source
============
https://nscnt12.nsc.gov.tw/was2/award/AsAwardMultiQuery.aspx


Data Files
============
* nsc\_projects.csv 包含78~102年度的專題研究/其他補助/委辦/代辦案, 付有各案的核定金額, 學門及子類, 機關及主持人名, 執行期間與以及計劃名稱, 並以 csv (逗點分隔純文字檔) 儲存.
* budget.json 包含 78~102年度以單位分類所申請金額組總合的雜湊表.
* please check category-mapping.txt for 案別, 學門 and 子類別 definition mapping table.


Crawler
============
under crawler/ folder.

* crawler.py - crawl data from nscnt12.nsc.gov.tw, pre-generate a csv file. downloaded files will be put under crawler/raw/ ( about 700MB.)
* parse.py   - format raw data into nsc-projects.csv and nsc-projects.refined.csv from raw/
* budget.py  - generate budget.json from nsc-projects.csv


License
============
CC-BY-SA 3.0, check: http://creativecommons.org/licenses/by-sa/3.0/
