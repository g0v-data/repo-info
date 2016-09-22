# eia_crawler

主要工作是將環保署及各縣市環保局歷年受理審查之環境影響評估書件資料收集成 CSV 格式檔案。

資料來源：[行政院環境保護署 環評書件查詢系統](http://eiareport.epa.gov.tw/EIAWEB/Main.aspx?func=00)

## 安裝

+  Scrapy 套件 (可參考 [Scrapy Document - Installation guide](http://doc.scrapy.org/en/latest/intro/install.html))

## Vagrant

若是想用 Vagrant 也可以參考Gist上的 [Vagrant File](https://gist.github.com/dz1984/11130582) (假設已經有vagrant環境)。

``` shell
$ wget https://gist.githubusercontent.com/dz1984/11130582/raw/Vagrantfile

$ vagrant up
```

## 使用方式

分為兩個步驟：
+ Lists -  將各分頁清單抓下來，目的是要得到環評書件案號。

+ Details -  從清單中的案號，取得更詳細欄位。

``` bash
$ scrapy crawl lists

$ scrapy crawl details
```

## 產出結果

+ [results/lists.csv](results/lists.csv)

``` csv
Id, Agency, Name, DocType, Taker, Status, Notes

案號, 環評機關, 名稱, 類別, 承辦人, 審查進度,說明
```

+ [results/details.csv](results/details.csv)

``` csv
Id, DocTYpe, DevUnit, Region, DevCategory, Area, Size, Unit, Taker, Agency, SendDate, Status, ExamineDate, ExamineStatus, CommitteeDate, Notes

案號, 書件類別, 開發單位名稱, 基地行政區, 開發計畫類別, 基地面積, 開發規模, 開發規模單位, 承辨人, 目的事業主管機關, 繳費日期, 處理情形, 初審會日期, 審查結論別, 委員會日期, 備註
```

## License 

The MIT license (MIT)
