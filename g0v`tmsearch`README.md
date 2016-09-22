# Parse tmsearch.tipo.gov.tw

There's [open data](http://www.tipo.gov.tw/ct.asp?xItem=531533&ctNode=7127&mp=1) available in bulk, but this allows using search function on tmsearch, until someone builds a search engine based on the data.

## Install

* docker.
* nodejs.  run `npm i` and `npm i -g LiveScript`

## Usage

Run the big5/utf-8 proxy:

    % docker run --rm -p 5000:5000 -e PROXY_CHARSET=big5 -e PROXY_HOST=http://tmsearch.tipo.gov.tw/ -t clkao/utf8proxy

Get list of trademarks based on company name:

    % curl 'http://localhost:5000/TIPO_DR/servlet/InitApplicantIPOList' --data 'hdexcel=YES&intStartIdx=&hdnQueryTitle=申請人查詢&cboTMarkClass=&hdnTMarkClassName=全部&txtApplicantName={{COMPANY_NAME}}&hdnApplicantLabel=申請人/商 標/標章權人&hdnApplicantNameNationality=中文&cboApplicantNameNationality=c&cboApplicantNameWay=likeHead&hdnApplicantNameWay=字首相同&cboDateKind=APPL_DATE&hdnDateKindName=申請日期&txtStartDate=&txtEndDate=&cboPageNO=1&hdnContentPage=ApplicantIPOContent.html&hdnPageType=' | lsc list.ls /dev/stdin

Parse specific entry given SKEY from the list:

    % lsc entry.ls {{SKEY}}

Get trademark image with SKEY:

    http://tmsearch.tipo.gov.tw/TIPO_DR/servlet/ShowPicture_Serv?apply_no={{SKEY}}

## License

CC0
