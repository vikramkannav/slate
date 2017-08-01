# Authentications

## \auth

```shell
curl "http://base_url/api/auth" 
```

> The above command returns JSON structured like this:

```json
  {
  "message": "OTP is send succefully"
  }
```

\auth API is using for the mobile number Auhentiaction

###HTTP Request

`POST https://base_url.com/api/auth`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    mobile_number | integer |true | Please enter the valid mobile number | 10
 
<aside class="warning"> 422 	Unprocessable entry.  In case of invalid Phone Number</aside>


## \verfify

```shell
curl "http://base_url/api/"
  -H "Authorization: " 
```

> The above command returns JSON structured like this:

```json
 {
   "mobile_number": "9953055456",
   "OTP" : "OTP_number"
 }
```

\auth API is using for the mobile number Auhentiaction

###HTTP Request

`POST http://base_url.com/api/verify`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    mobile_number | integer |true | Please enter the valid mobile number | 10
    OTP number | integer |true | Please enter the valid mobile number | 6
 
<aside class="warning">422 	Unprocessable entry.  In case of invalid Phone Number</aside>

