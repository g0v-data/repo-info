# META.G0V.TW

蒐集g0v project的metadata

## 資料來源

根據Projects目錄下的每一個project, 抓取該project repo的g0v.json與github open issue

結果存在data目錄下

## 想加入我的project，怎麼作？

加一個YOUR_PROJECT_NAME.json到projects/底下，內容：

```
{
    "repo": "YOUR GITHUB REPO URL"
}
```

即可

## Usage

you need:

* Ruby
  * gem i github_api


Github有60 req per hour的api rate limit，為了避免撞到此上限，需要登入再執行github crawler。登入方式為：將scripts/底下的config.json.sample rename成config.json，填入你的github username and password

then

```
ruby scripts/main.rb
```
