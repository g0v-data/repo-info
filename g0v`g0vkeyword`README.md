政府關鍵字
========
設定 Setup
------
1. 設定 [plurk loso 斷詞切字](https://github.com/Plurk/loso) 
    * 需要 redis db
    * 這邊要餵中文 lexicon，可以用[蔡志浩先生製作的中文 lexicon](http://technology.chtsai.org/wordlist/) `python setup.py feed -f lexicon_file_path`
    * 建立完 lexicon 之後，打開 server  `python setup.py serve`
2. 從 [twlyreader prototype](https://github.com/g0v/twlyreader-prototype) 下載  json 公報原始檔
3. 使用 process_people.php ，處理指定人物的 json raw data `php process_people 蔣委員孝嚴`
4. 在 index.php 可以改要顯示哪些人物的分析資料

授權 License
------
本程式採用 MIT 授權。

Copyright (C) 2013 Chen Jeng-Chien, Tsung-Yin Li

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.