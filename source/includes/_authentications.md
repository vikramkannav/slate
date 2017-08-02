# Authentications

## OTP generation

This API is used for the OTP generation.

```shell
curl "http://base_url/api/auth" 
```

> The above command returns JSON structured like this:

```json
  {
  "message": "OTP is send successfully"
   }
```

auth API is using for the mobile number Authentication

###HTTP Request

`POST https://base_url.com/api/auth`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    mobile_number | integer |true | Please enter the valid mobile number | 
    country_code | integer |true | Please enter the country code      | +91
    
    
<aside class="warning"> 422 Unprocessable entry. Please enter the correct mobile number </aside>


## Verify OTP

This API is used for the mobile number verification with OTP number.

```shell
curl "http://base_url/api/verify"
-H " Authentication : bearer access token"
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
  		"refresh_token": "wjhdduyd6378399",
  		"auth_token":"treehsgstsdde3573"
  	}
  }
```


###HTTP Request

`POST http://base_url.com/api/verify`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    mobile_number | integer |true | Please enter the valid mobile number | 
    OTP number | integer |true | Please enter the correct OTP number  | 
    country_code | integer |true | Please enter the country code      | +91
     
 
<aside class="warning"> 401 Unprocessable entry. Please enter the Correct OTP </aside>

## Refresh Token

This API is used for the regenerating the auth token via refresh token.

```shell
curl "http://base_url/api/refresh_token"
-H " Authentication : bearer access token"
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
   		"refresh_token": "wjhdduyd6378399"   		
   	},
   	"auth_token":"treehsgstsdde3573"
   }
```


###HTTP Request

`POST http://base_url.com/api/refresh_token`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    refresh_token | string |true | Refresh Token | 
    
     
 
<aside class="warning"> 401 Unprocessable entry. Please enter the Correct OTP </aside>

