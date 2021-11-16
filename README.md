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
* The base URL is: http://ptg.somee.com
# Access Token
#### Description:
* username = {your username} (for exam: PTGLL00X)
* password = {your password} (for exam: PTGX00LL)
* grant_type = password
* Access Token Expire in 60 Minutes
<center><h1>step 1</h1></center>
# Secure endpoints
* LL001
* LL003
# Non-secure endpoints
* LL002
# API documentation

* Overview
![wms interface LL00X](https://user-images.githubusercontent.com/41188202/141673089-78ba99bb-ccc5-4ce9-9b44-8f9965de67fb.png)

* Request Access Token Example
![image](https://user-images.githubusercontent.com/41188202/141673281-21ccd812-c8c5-496a-bd17-797e41144dbb.png)

* Response Access Token Example
![image](https://user-images.githubusercontent.com/41188202/141671181-260ff47e-e623-4f7e-b00d-e53916ead6d9.png)

# Error codes
Refer to the following descriptions:

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
