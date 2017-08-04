# Authentication

## OTP generation

This API is used for the OTP generation. 

This is open API where Auth token is not required to be passed in the header.

```shell
curl -X POST \
  http://base_url.com/api/auth \
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
>The above command returns JSON structured like this for failure:

```json
  {
    "error": {
       "message": "Please enter the valid email mobile number"
    }
  }
```


###HTTP Request

`POST http://base_url.com/api/auth`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    mobile_number | integer |true | mobile_number | 
    country_code | integer |true | country_code      | +1
    
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>


## Verify OTP

This API is used for the mobile number verification with OTP number. 

This is open API where Auth token is not required to be passed in the header.


```shell
curl -X POST \
   http://base_url.com/api/verify \
  -H 'accept: application/json' \
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
>The above command returns JSON structured like this for failure:

```json
  {
    "error": {
       "message": "Please enter the correct OTP number"
    }
  }
```

###HTTP Request

`POST http://base_url.com/api/verify`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    mobile_number | integer |true | mobile_number of the user| 
    otp_number | integer |true   | otp_number recived on the number     | 
    country_code | integer |true | country_code of the user country   | +1
     
<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable entry.</aside>


## Retrieve access Token

This API is used for the regenerating the auth token via refresh token.
This API is an authentication API request in which needs to pass auth token in the request header.

```shell
curl -X POST \
  http://base_url/api/refresh_token \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
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
   	"refresh_token": "absgdtydiid123" ,
   	"auth_token":"hjduueuhfufu123"
   }
```
>The above command returns JSON structured like this for failure:

```json
  {
    "error": {
       "message": "Employee not found"
    }
  }
```

###HTTP Request

`POST http://base_url.com/api/refresh_token`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    refresh_token | string |true | refresh_token of the user| 
    
     
<aside class="success">status:200 OK</aside>
<aside class="warning">status: 422 Unprocessable entry. </aside>

