蚊子館parsing工具
========

這個工具是用來處理姚瑞中老師所提供的蚊子館資料, 包含的功能.
1. 將word檔轉成html
2. 將地址parse出來, 並取得地址的經緯度
3. 將資料包含名字, 地址, 經緯度上傳到google table
4. 將html上傳到google drive
5. 將html檔案在google drive上的link更新至google table

以後如果開發android, iOS, web page就可以從google table拿到相關資訊, 從google drive裡的html拿到詳細資料.  
目前使用google account為reporteroffact@gmail.com

PreRequirement:
-------------------------------
1. LibreOffice
2. NodeJS

各項功能使用方法:
-------------------------------
1: 將word檔轉成html
python tool.py 1 intput_path output_path

2: 將地址parse出來, 並取得地址的經緯度
node MapParser.js output_path
Output:NoUseAddressbook.json
 
3: 將資料包含名字, 地址, 經緯度上傳到google table
python tool.py 2 NoUseAddressbook.json 

4: 將html上傳到google drive
python tool.py 3 output_path

5: 將html檔案在google drive上的link更新至google table
python tool.py 4

如果你碰到問題:
-------------------------------
1. 如果在使用功能3, 4, 5有問題, 可以把a_credentials_file砍掉再試一次
2. 如果有其他問題, 請create issue