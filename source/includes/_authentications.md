# Authentication

## OTP generation

This API is used for the OTP generation.
This is open API where Auth token is not required to be passed in header.

```shell
curl -X POST \
  https://base_url.com/api/auth \
  -H 'accept: application/json' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '{
	"mobile_number": "9876543210",
	"country_code": "+1"
}'
" 
```

> The above command returns JSON structured like this:

```json
  {
  "message": "OTP is sent successfully"
   }
```


###HTTP Request

`POST https://base_url.com/api/auth`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    mobile_number | integer |true | mobile_number | 
    country_code | integer |true | country_code      | +1
    
    
<aside class="warning">422 Unprocessable entry. Please enter the correct mobile number </aside>


## Verify OTP

This API is used for the mobile number verification with OTP number.
This API is an authentication API request in which needs to pass auth token in the request header.


```shell
curl -X POST \
   http://base_url.com/api/verify \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '{
	"mobile_number": "9876543210",
	 "otp_number" :"2345"
	"country_code": "+1"
}'
```

> The above command returns JSON structured like this:

```json
  {
  	"user": {
  		"first_name": "",
  		"last_name": "",
  		"email_id": "",
  		"category": "artist",
  		"age": "",
  		"profession": "",
  		"work_on_album": "",
  		"file_type": "",
  		"play_instrument ": "",
  		"instrument_name": ""
    	},
  	"refresh_token": "wjhdduyd6378399" ,
     "auth_token":"treehsgstsdde3573"
  }
```


###HTTP Request

`POST http://base_url.com/api/verify`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    mobile_number | integer |true | mobile_number of the user| 
    otp_number | integer |true   | otp_number recived on the number     | 
    country_code | integer |true | country_code of the user country   | +91
     
<aside class="warning">422 Unprocessable entry </aside>

## Refresh Token

This API is used for the regenerating the auth token via refresh token.
This API is an authentication API request in which needs to pass auth token in the request header.

```shell
curl -X POST \
  http://base_url/api/refresh_token \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -H 'postman-token: 61fe122e-6edc-982a-8d55-6ffa9fad4421' \
  -d '{
	"refresh_token": "wjhdduyd6378399"
}'
```

> The above command returns JSON structured like this:

```json
  {
   	"user": {
   		"first_name": "",
   		"last_name": "",
   		"email_id": "",
   		"category": "artist",
   		"age": "",
   		"profession": "",
   		"work_on_album": "",
   		"file_type": "",
   		"play_instrument ": "",
   		"instrument_name": "",
   		  		
   	},
   	"refresh_token": "wjhdduyd6378399" ,
   	"auth_token":"treehsgstsdde3573"
   }
```


###HTTP Request

`POST http://base_url.com/api/refresh_token`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    refresh_token | string |true | refresh_token of the user| 
    
     
 
<aside class="warning"> 422 Unprocessable entry. </aside>

