# repo-info
整合 g0v repo 列表。</br>
資料定時更新至 [g0v-data/repo-info](https://github.com/g0v-data/repo-info).

## 目的
除 [org: g0v](https://github.com/g0v) 外，許多 g0v 專案仍各屬其作者。目前整合方式乃透過 [awesome-g0v](https://github.com/g0v/awesome-g0v) 工人整理。為避免每當有需求就得自己寫 script 整合兩邊資訊，透過單一 [datasource](https://github.com/g0v-data/repo-info) 可節省貢獻者時間。

## 設定
從 template 拷貝 config:
```
$ cp config_template.json _data/
$ mv _data/config_template.json _data/config.json
```
編輯 config.json:
```
{
    "token": "自己的 github personal access token",
    "backup_repo": "要備份到的 repo_url",
}
```

## 執行時間
根據 repo 數量多寡而定，目前約 350+ 個 repos, 全部掃完 ≈ 4 mins.