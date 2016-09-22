# 中研院「社會變遷全記錄」半自動化計畫

Hackpad/說明： https://g0v.hackpad.com/UssOWtAVda9

# Requirements
0. git
1. Docker 1.7+
2. Docker-compose 1.6+
3. node

# Features

## 簡易查詢界面 - Grafana 版

1. Deploy Grafana + Influx 
  1. `cd visualization/dockers.grafana`
  2. `sudo docker-compose build`
  3. `sudo env GF_SECURITY_ADMIN_PASSWORD=<passwd> docker-compose -f docker-compose.yml -f prod.yml up -d`
  4. `./resetInflux.sh`
3. Setup parser 
  1. `cd parser`
  2. `npm install`
2. Insert Data
  1. `node parser/csv2influx.js data/sample.noheader.csv 100`
  2. To insert whole data set, use 1 instead of 100 for last arg
3. Setup Grafana
  1. Open grafana in browser, port 80
  2. Login as admin + <your password>, setup db
  3. Data Sources →  Add new data source 
  4. Type: InfluxDB 0.9.x, Url: http://influx:8086, Access: proxy, Database: tscs, User/Password: anything you like
  5. (optional) import example dashboard, see `visualization/data/grafana.example.json`

## 簡易查詢界面 - Kibana 版

1. Deploy Elasticsearch + Kibana
  1. `cd visualization/dockers.kibana`
  2. `sudo docker-compose build`
  3. `sudo docker-compose -f docker-compose.yml -d`
  4. `./reset.sh`
3. Setup parser 
  1. `cd parser`
  2. `npm install`
2. Insert Data
  1. `node parser/csv2elastic.js data/sample.noheader.csv 100`
  2. To insert whole data set, use 1 instead of 100 for last arg
3. Setup Kibana
  1. Open kibana in browser, port 5601
  2. Use "tscs" index as default index
  3. (optional) import example dashboards and visualizations, Settings -> Object, choose `visualization/data/kibana.example.json`
