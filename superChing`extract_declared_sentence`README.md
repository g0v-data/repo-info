extract declared sentence
=========================


USAGE
---
###抽取宣告刑
**usage example:** `python3 extract_declared_sentence.py <directory or file path>`

**output format:** json
`["file name", {"accused1": [ ["charge1", "sentence1"], ...], "accused2":[...], ...} ]`         
Log file is generated locally.

###抽取表格cell
如果僅需要抽取cell 可以用 `tools.extract_cells(text)` 。
note：僅抽取cell內容為string，並沒有表格結構化。


####儲存表格cells
格式為python pickle, 相容於Python2。

儲存：`python3 extract_cells.py /Users/apple/verdict`


Python2 讀取:
```
import pickle
with open('cells_per_doc.pickle', 'rb') as f:
     data = pickle.load(f)
```

Description
---
抽取表格的cell內的句子,用regular expression抓取判刑pattern。

統計：
```
{'accused_extraction_fail': 4,
 'doc': 991,
 'output': 75,
 'table': 2146,
 'table_format_exception': 164,
 'table_processing_fail': 166}
```

75個doc有結果。
2146個table裡有166個table無法處理 .(紀錄在LOG)

Known Issue
---

- 多人被告pattern。
see doc of function `extract_accuseds`
- 表格內有表格的無法處理。
see doc of function `parse`.
這還好，只有不到1/10表格有問題。
- 判刑pattern的recall rate不明。需要一些test set for evaluation。
有抓出表格宣告型的doc不到1/10，如果真實數字沒那麼低的話那應該regular expression的pattern 是主要問題，at function `extract_sentences`。

