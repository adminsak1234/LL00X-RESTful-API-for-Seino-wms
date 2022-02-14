# LL00X RESTful API For Seino wms
# Releases
* 2021-12-24 v. 0.0.7 update base url, LL001 Cancel
* 2021-12-15 v. 0.0.6 update error code, LL001 cancel document request
* 2021-12-07 v. 0.0.5 update template spec
* 2021-11-25 v. 0.0.4
* 2021-11-19 LL002 demo get request v. 0.0.3
* 2021-11-18 LL001, LL003 demo v. 0.0.2
* 2021-11-14 First update v. 0.0.1

# Table of contents
* [API documentation](#API-documentation)
* [Base URL](#base-url-UAT-SERVER)
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

# Base URL UAT SERVER
[back to top](#Table-of-contents)
* Need to connect vpn
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
![image](https://user-images.githubusercontent.com/41188202/147317005-ac2dce3e-f46b-4bab-b1ac-6e090305320e.png)
* Response Json form
```javascript
{
    "access_token": "PQxjgHlm_QqcR6au7KvhTFsYf5j5YMwZpRJcIfXET72Qw43Qbom9bgK8HahDr1WnGOUp0hrNSkWKXzDF4Gy2hh39D0XUlltozvGvz2hIdpAVKj0ysW3zBjil8EJ0zMUFMUQ9XjkL20H7UBjCx4wnY8rBbC5Ma_LuuOeEnw2e8VVmuWo57wJoXNMoOhGPagtOmZ05hfKgYTHIbQE2gl6kM0-C3VPcAf7MryCZCMbUfdyTD9wHGatsv0w-DBZp3DruBfgTm0AACPDbamVkw2sq0sSdEaUIeXKpTvPC60sM9YA",
    "token_type": "bearer",
    "expires_in": 599
}
```

# LL001
[back to top](#Table-of-contents)
* Select request type as POST and add request URL as {Base URL}/api/ll001/method1 
![image](https://user-images.githubusercontent.com/41188202/147317157-83e1a871-534d-451f-a8a3-8373a46fe228.png)

#### On Headers tab
* Add key as [Authorization] and value as "Bearer {Enter Token Here}" 
* Add key as [Content-Type] and value as "application/json"
![image](https://user-images.githubusercontent.com/41188202/147317244-bf18e158-259e-4ea6-b917-88853ef51ab9.png)

#### On Body tab
* Now click on Body – select raw – select Text as JSON (application/json), Then pass the Jason as below
![image](https://user-images.githubusercontent.com/41188202/147331524-a2f1e804-1081-4238-903a-5391c00c3b1f.png)
```javascript
[{
    "SRC_NAME": "PUN",
    "TARGET_NAME": "WMS",
    "DOCUMENTNO": "GQ-P795-0000086",
    "DOCUMENTDATE": "20210501",
    "COMP_CODE": "1022",
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
    "SRC_NAME": "PUN",
    "TARGET_NAME": "WMS",
    "DOCUMENTNO": "GQ-P795-0000086",
    "DOCUMENTDATE": "20210501",
    "COMP_CODE": "1022",
    "PICKINGTYPECODE": "12",
    "CUSTOMERCODE": "P795",
    "WAREHOUSECODE": "DP02",
    "ITEM_NO": "2",
    "PRODUCTCODE": "250000171",
    "PRODUCTQTY": "3",
    "ITEMSTATUSCODE": "01",
    "PRODUCTUNITCODE": "BOX",
    "DESCRIPTION": "TEST LL001",
    "CREATEBY": "INF",
    "UPDATEBY": "INF"
}]
```
#### Response
![image](https://user-images.githubusercontent.com/41188202/147331772-226dc507-2848-4681-8423-eadb83468dda.png)
```javascript
{
    "error": "00",
    "error_description": "No Error, Hello LL001 : your data 2 row"
}
```
# LL001 To Cancel
[back to top](#Table-of-contents)
* Select request type as GET and add request URL as {Base URL}/api/ll001/method2?doc={documentNo}&comp_code={company code} 
![image](https://user-images.githubusercontent.com/41188202/147332031-b8c52532-0558-4487-842c-b0dd925b75ad.png)

#### On Headers tab
* Add key as [Authorization] and value as "Bearer {Enter Token Here}" 
* Add key as [Content-Type] and value as "application/json"
![image](https://user-images.githubusercontent.com/41188202/147332451-23913d18-9e52-4a22-8372-b48055546387.png)
#### On Params tab
* Now click on Params, Then add key as [doc] and values as {documentNo} and add key as [company code] and values as {comp_code}
![image](https://user-images.githubusercontent.com/41188202/147332785-68a18d74-302e-42d5-a997-61ddbd2328d5.png)

#### Response:
![image](https://user-images.githubusercontent.com/41188202/147333506-e276eea5-e4a8-4fae-bb53-843ae120793b.png)
```javascript
{
    "error": "00",
    "error_description": "No error"
}
```
* Download for example -> [TestCallAPIWithToken.zip](https://github.com/adminsak1234/LL00X-RESTful-API-for-Seino-wms)
# LL003
* Select request type as POST and add request URL as {Base URL}/api/ll003/method1 
![image](https://user-images.githubusercontent.com/41188202/153827705-e4f964d4-7ae7-4f97-b169-db172fdcd481.png)

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
![image](https://user-images.githubusercontent.com/41188202/153827597-7f04e4c4-8d2f-48d7-bf70-3586fc43dd53.png)

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
14 | Found multi ITEMSTATUSCODE in request
15 | Not Found ITEMSTATUSCODE in request
90 | Server error (please contact support)

## Invalid JSON for example
##### 1![image](https://user-images.githubusercontent.com/41188202/143983445-f0a20b2d-b51b-424a-9adc-87cd0c20c9bf.png)
##### 2![image](https://user-images.githubusercontent.com/41188202/143983677-ec8fdc9b-8c24-4120-bf85-daac79ab8f2d.png)
##### 3![image](https://user-images.githubusercontent.com/41188202/143983856-a1d43758-dd69-4539-942b-baecdb952760.png)
## Fix value is wrong for example
##### 1![image](https://user-images.githubusercontent.com/41188202/144006444-600f6304-7725-4ce5-a292-af7d70741f39.png)



