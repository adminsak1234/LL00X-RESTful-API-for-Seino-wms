# LL00X RESTful API For Seino wms
# Releases
* 2021-11-14 First update

# Table of contents
* [Base URL](#base-url)
* [Access Token](#access-token)
* [Secure endpoints](#secure-endpoints)
* [Non-secure endpoints](#non-secure-endpoints)
* [API documentation](#API-documentation)
* [Error codes](#error-codes)

# Base URL
[back to top](#Table-of-contents)
* The base URL is: http://ptg.somee.com
# Access Token
[back to top](#Table-of-contents)
#### Description:
* username = {your username} (for exam: PTGLL00X)
* password = {your password} (for exam: PTGX00LL)
* grant_type = password
* Access Token Expire in 60 Minutes
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

# Secure endpoints
[back to top](#Table-of-contents)
## LL001
Select request type as POST and add request URL as {Base URL}/api/ll001/method1
#### On Headers tab
* Add key as [Authorization] and value as "Bearer {Enter Token Here}" 
* Add key as [Content-Type] and value as "application/json"
#### On Body tab
Now click on Body – select raw – select Text as JSON (application/json), Then pass the Jason as below
```{r}
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
* Download for example -> [TestCallAPIWithToken.zip](https://github.com/adminsak1234/LL00X-RESTful-API-for-Seino-wms)
## LL003

# Non-secure endpoints
[back to top](#Table-of-contents)
## LL002 (for wms caller only)
# API documentation

* Overview
![wms interface LL00X](https://user-images.githubusercontent.com/41188202/141673089-78ba99bb-ccc5-4ce9-9b44-8f9965de67fb.png)
* LL001 Model Dictionary
![image](https://user-images.githubusercontent.com/41188202/142178539-281b76dc-0cfe-4e4f-aac8-7d56931e1f10.png)

# Error codes
[back to top](#Table-of-contents)
* Refer to the following descriptions:

Code | Description
------------ | ------------
0 | No error
1 | Invalid JSON payload
2 | Missing X-BTK-APIKEY
3 | Invalid API key
4 | API pending for activation
5 | IP not allowed
6 | Missing / invalid signature
7 | Missing timestamp
8 | Invalid timestamp
9 | Invalid user
10 | Invalid parameter
11 | Invalid symbol
12 | Invalid amount
13 | Invalid rate
14 | Improper rate
15 | Amount too low
16 | Failed to get balance
17 | Wallet is empty
18 | Insufficient balance
19 | Failed to insert order into db
20 | Failed to deduct balance
21 | Invalid order for cancellation
22 | Invalid side
23 | Failed to update order status
24 | Invalid order for lookup
25 | KYC level 1 is required to proceed
30 | Limit exceeds
40 | Pending withdrawal exists
41 | Invalid currency for withdrawal
42 | Address is not in whitelist
43 | Failed to deduct crypto
44 | Failed to create withdrawal record
45 | Nonce has to be numeric
46 | Invalid nonce
47 | Withdrawal limit exceeds
48 | Invalid bank account
49 | Bank limit exceeds
50 | Pending withdrawal exists
51 | Withdrawal is under maintenance
52 | Invalid permission
53 | Invalid internal address 
54 | Address has been deprecated
90 | Server error (please contact support)
