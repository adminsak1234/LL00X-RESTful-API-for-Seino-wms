# LL00X RESTful API For Seino wms
# Releases
* 2021-12-15 v. 0.0.6 update error code, LL001 cancel document request
* 2021-12-07 v. 0.0.5 update template spec
* 2021-11-25 v. 0.0.4
* 2021-11-19 LL002 demo get request v. 0.0.3
* 2021-11-18 LL001, LL003 demo v. 0.0.2
* 2021-11-14 First update v. 0.0.1

# Table of contents
* [API documentation](#API-documentation)
* [Base URL](#base-url-(UAT-SERVER))
* [Access Token](#access-token)
* [LL001 (wms provides)](#ll001)
* [LL001 To Cancel (wms provides)](#LL001-To-Cancel)
* [LL003 (wms provides)](#ll003)
* [LL003 To Cancel (wms provides)](#ll003-To-Cancel)
* [Error codes](#error-codes)

# API documentation
* Overview
![wms interface LL00X](https://user-images.githubusercontent.com/41188202/141673089-78ba99bb-ccc5-4ce9-9b44-8f9965de67fb.png)
* LL001 Model Dictionary
![image](https://user-images.githubusercontent.com/41188202/143969934-8f3f0ec2-67ef-4829-ba2b-4479f928cbf8.png)
* LL003 Model Dictionary
![image](https://user-images.githubusercontent.com/41188202/143969955-b6c5a9da-8f6c-472c-884c-4cfca3f58f42.png)
* Spec [click](https://seinosaha-my.sharepoint.com/:w:/g/personal/itssl_sslog_co_th/EWkxt6dRU-tIuF5_Y6wCQ94B8wqWAK5VVGsPotmfjwla7A?e=U5ZaUg)
* Template spec [click](https://seinosaha-my.sharepoint.com/:x:/g/personal/itssl_sslog_co_th/ESwfT-49cPFDlpTdWzSkvuoBJAYs1atNMDsjsAN71WRDsA?e=C0FxVn)

# Base URL (UAT SERVER)
[back to top](#Table-of-contents)
* The base URL is: http://172.16.112.41:8081
# Access Token
[back to top](#Table-of-contents)
#### Description:
* username = {your username} (for exam: PTGLL00X)
* password = {your password} (for exam: PTGX00LL)
* grant_type = password
* Access Token Expire in 10 Minutes
#### Example by Postman:
* POST/{Base URL}/token
![image](https://user-images.githubusercontent.com/41188202/141952070-1d9c5ca1-90e5-42c8-98ac-8fb94e89ba4d.png)
* Response Json form
```javascript
  {
    "access_token": "or8grkUIuiFYaUsqFgD3ZXPAS_tyn5brTv3FgSI8El_zhTDrC6Joya_Papt6j_W92txK-s2gJmv9bDSlTSpCI9rK1aRvJ_IZVF3c-lX4wi2PaqypIpl32bK9VOCUAZSltELB3d4PY53vQgy8XlMdpwhpHP4s_CYevnKpJUwC5FjCDWzoN7DQ7W14hkIyeUEb6YjecWQlgp1y2FmUkk6TlqiPl4J8IPTadrWXW6uBI-dheX_T4HamEmYK85mbB9pN42fOFCc--uG-MJ22RTCeTRxwvJFxDpEysw9ETIaEAvc",
    "status": "ok",
    "message": ""
  }
```

# LL001
[back to top](#Table-of-contents)
* Select request type as POST and add request URL as {Base URL}/api/ll001/method1 
![image](https://user-images.githubusercontent.com/41188202/142390596-ad1ccde4-6efd-4a54-9a83-a257b18c051a.png)

#### On Headers tab
* Add key as [Authorization] and value as "Bearer {Enter Token Here}" 
* Add key as [Content-Type] and value as "application/json"
![image](https://user-images.githubusercontent.com/41188202/142391080-a91b7ccb-6595-4dda-9a79-fa6c024f19fb.png)

#### On Body tab
* Now click on Body – select raw – select Text as JSON (application/json), Then pass the Jason as below
![image](https://user-images.githubusercontent.com/41188202/142391790-f0734fa8-8847-4a28-aaf0-e50da332df3b.png)
```javascript
[{
    "TXLL_ID": "6710927",
    "SRC_NAME": "PUN",
    "TARGET_NAME": "WMS",
    "DOCUMENTNO": "GQ-P795-0000083",
    "DOCUMENTDATE": "20210501",
    "COMP_CODE": "1021",
    "PICKINGTYPECODE": "12",
    "CUSTOMERCODE": "P795",
    "WAREHOUSECODE": "DP02",
    "ITEM_NO": "1",
    "PRODUCTCODE": "250000038",
    "PRODUCTQTY": "40",
    "ITEMSTATUSCODE": "01",
    "PRODUCTUNITCODE": "BAG",
    "DESCRIPTION": "TEST LL001",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
},
{
    "TXLL_ID": "6710927",
    "SRC_NAME": "PUN",
    "TARGET_NAME": "WMS",
    "DOCUMENTNO": "GQ-P795-0000083",
    "DOCUMENTDATE": "20210501",
    "COMP_CODE": "1021",
    "PICKINGTYPECODE": "12",
    "CUSTOMERCODE": "P795",
    "WAREHOUSECODE": "DP02",
    "ITEM_NO": "2",
    "PRODUCTCODE": "250000171",
    "PRODUCTQTY": "3",
    "ITEMSTATUSCODE": "01",
    "PRODUCTUNITCODE": "BAG",
    "DESCRIPTION": "TEST LL001",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
},
{
    "TXLL_ID": "6710927",
    "SRC_NAME": "PUN",
    "TARGET_NAME": "WMS",
    "DOCUMENTNO": "GQ-P795-0000083",
    "DOCUMENTDATE": "20210501",
    "COMP_CODE": "1021",
    "PICKINGTYPECODE": "12",
    "CUSTOMERCODE": "P795",
    "WAREHOUSECODE": "DP02",
    "ITEM_NO": "3",
    "PRODUCTCODE": "250000200",
    "PRODUCTQTY": "3",
    "ITEMSTATUSCODE": "01",
    "PRODUCTUNITCODE": "BAG",
    "DESCRIPTION": "TEST LL001",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
},
{
    "TXLL_ID": "6710927",
    "SRC_NAME": "PUN",
    "TARGET_NAME": "WMS",
    "DOCUMENTNO": "GQ-P795-0000083",
    "DOCUMENTDATE": "20210501",
    "COMP_CODE": "1021",
    "PICKINGTYPECODE": "12",
    "CUSTOMERCODE": "P795",
    "WAREHOUSECODE": "DP02",
    "ITEM_NO": "4",
    "PRODUCTCODE": "250000837",
    "PRODUCTQTY": "1",
    "ITEMSTATUSCODE": "01",
    "PRODUCTUNITCODE": "BAG",
    "DESCRIPTION": "TEST LL001",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
},
{
    "TXLL_ID": "6710927",
    "SRC_NAME": "PUN",
    "TARGET_NAME": "WMS",
    "DOCUMENTNO": "GQ-P795-0000083",
    "DOCUMENTDATE": "20210501",
    "COMP_CODE": "1021",
    "PICKINGTYPECODE": "12",
    "CUSTOMERCODE": "P795",
    "WAREHOUSECODE": "DP02",
    "ITEM_NO": "5",
    "PRODUCTCODE": "250000057",
    "PRODUCTQTY": "2",
    "ITEMSTATUSCODE": "01",
    "PRODUCTUNITCODE": "BAG",
    "DESCRIPTION": "TEST LL001",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
},
{
    "TXLL_ID": "6710927",
    "SRC_NAME": "PUN",
    "TARGET_NAME": "WMS",
    "DOCUMENTNO": "GQ-P795-0000083",
    "DOCUMENTDATE": "20210501",
    "COMP_CODE": "1021",
    "PICKINGTYPECODE": "12",
    "CUSTOMERCODE": "P795",
    "WAREHOUSECODE": "DP02",
    "ITEM_NO": "6",
    "PRODUCTCODE": "250000229",
    "PRODUCTQTY": "1",
    "ITEMSTATUSCODE": "01",
    "PRODUCTUNITCODE": "BAG",
    "DESCRIPTION": "TEST LL001",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
}]
```
#### Example by Postman:
* On Headers tab, Follow below.
![image](https://user-images.githubusercontent.com/41188202/142135270-7b022a98-4e76-4dbe-bff6-02e4a2938d4e.png)
* On Body tab, Follow below.
![image](https://user-images.githubusercontent.com/41188202/142368057-6cbaf2a6-b176-4afd-bb2d-b54f5b36192f.png)
* Response Json form
![image](https://user-images.githubusercontent.com/41188202/142178293-dbf0e42f-6c81-4fc1-9b07-d5b37e8bba1b.png)
```javascript
{
    "error": "00",
    "error_description": "No Error, Hello LL001 : your data 6 row"
}
```
# LL001 To Cancel
[back to top](#Table-of-contents)
* Select request type as GET and add request URL as {Base URL}/api/ll001/method2?doc={documentNo}&comp_code={comp_code} 
![image](https://user-images.githubusercontent.com/41188202/143394815-d4c95de7-c5a8-4528-a22e-57f2f13c1f51.png)

#### On Headers tab
* Add key as [Authorization] and value as "Bearer {Enter Token Here}" 
* Add key as [Content-Type] and value as "application/json"
![image](https://user-images.githubusercontent.com/41188202/142392304-b864d5e8-c10b-46d2-a0fc-8136f934b219.png)
#### On Params tab
* Now click on Params, Then add key as [doc] and values as {documentNo}
![image](https://user-images.githubusercontent.com/41188202/143395316-b7c65284-f692-49a3-bd23-8a245b06099a.png)

#### Example by Postman:
* On Headers tab, Follow below.
![image](https://user-images.githubusercontent.com/41188202/143396579-d9b60b53-b46e-4d90-adce-48d80c06e8b8.png)
* On Params tab, Follow below.
![image](https://user-images.githubusercontent.com/41188202/143396743-1067ab91-1eb8-47c0-8a0d-073af4526b7c.png)
* Response Json form
![image](https://user-images.githubusercontent.com/41188202/143397046-179dab77-981e-4bb1-bd2c-da39a08da5f1.png)
```javascript
{
    "error": "00",
    "error_description": "No Error, Hello LL001 To Cancel : your doc TEST1234"
}
```
* Download for example -> [TestCallAPIWithToken.zip](https://github.com/adminsak1234/LL00X-RESTful-API-for-Seino-wms)
# LL003
* Select request type as POST and add request URL as {Base URL}/api/ll003/method1 
![image](https://user-images.githubusercontent.com/41188202/142393992-16c09866-5c37-4a00-b8d6-8b2c3f60b5da.png)

#### On Headers tab
* Add key as [Authorization] and value as "Bearer {Enter Token Here}" 
* Add key as [Content-Type] and value as "application/json"
![image](https://user-images.githubusercontent.com/41188202/142392304-b864d5e8-c10b-46d2-a0fc-8136f934b219.png)
#### On Body tab
* Now click on Body – select raw – select Text as JSON (application/json), Then pass the Jason as below
![image](https://user-images.githubusercontent.com/41188202/142392462-327a5b9c-b230-4f06-a66a-4caa1fa145e0.png)
```javascript
[{
    "TXLL_ID": "908762",
    "DOCUMENT_NO": "312100015059",
    "DOC_DATE": "20211105",
    "SRC_NAME": "VRM",
    "TARGET_NAME": "VRM",
    "COMP_CODE": "1012",
    "DOC_TYPE": "ZGEN",
    "VENDOR": "21001921",
    "PLANT": "1200",
    "PO_ITEM": "00010",
    "MATERIAL": "600000397",
    "QUANTITY": "1.00",
    "QTY_CONFIRM": "1.00",
    "PO_UNIT": "AU",
    "NET_PRICE": "1000000.0000",
    "PRICE_UNIT": "1000000.0000",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
},
{
    "TXLL_ID": "908764",
    "DOCUMENT_NO": "312100015059",
    "DOC_DATE": "20211105",
    "SRC_NAME": "VRM",
    "TARGET_NAME": "VRM",
    "COMP_CODE": "1012",
    "DOC_TYPE": "ZGEN",
    "VENDOR": "21001921",
    "PLANT": "1205",
    "PO_ITEM": "00030",
    "MATERIAL": "600000397",
    "QUANTITY": "1.00",
    "QTY_CONFIRM": "1.00",
    "PO_UNIT": "AU",
    "NET_PRICE": "1000000.0000",
    "PRICE_UNIT": "1000000.0000",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
},
{
    "TXLL_ID": "908765",
    "DOCUMENT_NO": "312100015059",
    "DOC_DATE": "20211105",
    "SRC_NAME": "VRM",
    "TARGET_NAME": "VRM",
    "COMP_CODE": "1012",
    "DOC_TYPE": "ZGEN",
    "VENDOR": "21001921",
    "PLANT": "DM02",
    "PO_ITEM": "00040",
    "MATERIAL": "600000397",
    "QUANTITY": "1.00",
    "QTY_CONFIRM": "1.00",
    "PO_UNIT": "AU",
    "NET_PRICE": "1000000.0000",
    "PRICE_UNIT": "1000000.0000",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
}]
```
#### Example by Postman:
* On Headers tab, Follow below.
![image](https://user-images.githubusercontent.com/41188202/142376073-5fc2e661-c7d9-4833-a7ae-e6369368c87e.png)
* On Body tab, Follow below.
![image](https://user-images.githubusercontent.com/41188202/142376264-d6a8a07f-1ffb-48aa-aa09-2ee7ef191d8c.png)
* Response Json form
![image](https://user-images.githubusercontent.com/41188202/142385526-c64f7408-91f8-4a3d-823e-81874c62f15e.png)
```javascript
{
    "error": "00",
    "error_description": "No Error, Hello LL003 : your data 3 row"
}
```
# LL003 To Cancel
[back to top](#Table-of-contents)
* Select request type as GET and add request URL as {Base URL}/api/ll003/method2?doc={documentNo} 
![image](https://user-images.githubusercontent.com/41188202/143399546-65fcf6eb-086b-4354-8cf4-ff87c53cc063.png)

#### On Headers tab
* Add key as [Authorization] and value as "Bearer {Enter Token Here}" 
* Add key as [Content-Type] and value as "application/json"
![image](https://user-images.githubusercontent.com/41188202/143399903-f0d5479c-73ea-4b56-a521-91939b57233f.png)
#### On Params tab
* Now click on Params, Then add key as [doc] and values as {documentNo}
![image](https://user-images.githubusercontent.com/41188202/143395316-b7c65284-f692-49a3-bd23-8a245b06099a.png)

#### Example by Postman:
* On Headers tab, Follow below.
![image](https://user-images.githubusercontent.com/41188202/143399662-0a0b9553-097e-4106-b53f-fd7b8cf81cee.png)
* On Params tab, Follow below.
![image](https://user-images.githubusercontent.com/41188202/143396743-1067ab91-1eb8-47c0-8a0d-073af4526b7c.png)
* Response Json form
![image](https://user-images.githubusercontent.com/41188202/143399761-5cd0bd5e-46e2-44bc-aeef-6325535cb528.png)
```javascript
{
    "error": "00",
    "error_description": "No Error, Hello LL003 To Cancel : your doc TEST1234"
}
```
* Download for example -> [TestCallAPIWithToken.zip](https://github.com/adminsak1234/LL00X-RESTful-API-for-Seino-wms)


# Error codes
[back to top](#Table-of-contents)
* Refer to the following descriptions:

Code | Description
------------ | ------------
00 | No error
01 | Invalid JSON [click](#Invalid-JSON-for-example)
02 | Document is duplicate
03 | Document cannot change because warehouse work in process
04 | SRC_NAME not found, please check
05 | COMP_CODE not found, please check
06 | CUSTOMERCODE not found, please check
07 | WAREHOUSECODE not found, please check
08 | PRODUCTCODE not found, please check
09 | PRODUCTUNITCODE not found, please check
10 | Found multi Document in request
11 | Fix value is wrong, please check [click](#Fix-value-is-wrong-for-example)
12 | COMP_CODE, PRODUCTCODE, PRODUCTUNITCODE, WAREHOUSECODE Not matching
13 | Document not found
90 | Server error (please contact support)

## Invalid JSON for example
##### 1![image](https://user-images.githubusercontent.com/41188202/143983445-f0a20b2d-b51b-424a-9adc-87cd0c20c9bf.png)
##### 2![image](https://user-images.githubusercontent.com/41188202/143983677-ec8fdc9b-8c24-4120-bf85-daac79ab8f2d.png)
##### 3![image](https://user-images.githubusercontent.com/41188202/143983856-a1d43758-dd69-4539-942b-baecdb952760.png)
## Fix value is wrong for example
##### 1![image](https://user-images.githubusercontent.com/41188202/144006444-600f6304-7725-4ce5-a292-af7d70741f39.png)



