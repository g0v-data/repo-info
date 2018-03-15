# democracy_common
https://www.wikidata.org/wiki/Wikidata:WikiProject_every_politician

## Setup
Follow [procedure](https://www.wikidata.org/wiki/Wikidata:Bots) to register an bot account in Wikidata
* [Creating a Wikidata bot](https://www.wikidata.org/wiki/Wikidata:Creating_a_bot)
* [Python 3 Tutorial](https://www.wikidata.org/wiki/Wikidata:Pywikibot_-_Python_3_Tutorial)

## Run Scripts
```
$ cd core
core$ python3 -m taiwan.current_legislators
core$ python3 -m taiwan.setup_councils_and_position
```

## Run Crawler
```
$ cd crawler/south_korea
crawler/south_korea$ scrapy runspider assembly.py -o ../../core/south_korea/data/assembly.json -s FEED_EXPORT_ENCODING=utf-8
crawler/south_korea$ scrapy runspider flacs_mayor.py -o ../../core/south_korea/data/flacs_mayor.json -s FEED_EXPORT_ENCODING=utf-8
crawler/south_korea$ scrapy runspider sub_mayor.py -o ../../core/south_korea/data/sub_mayor.json -s FEED_EXPORT_ENCODING=utf-8
crawler/south_korea$ scrapy runspider flacs_councilor.py -o ../../core/south_korea/data/flacs_councilor.json -s FEED_EXPORT_ENCODING=utf-8
crawler/south_korea$ scrapy runspider sub_councilor.py -o ../../core/south_korea/data/sub_councilor.json -s FEED_EXPORT_ENCODING=utf-8
```
