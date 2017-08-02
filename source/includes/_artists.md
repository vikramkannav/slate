
# Users

## Users

```shell
curl "http://base_url/api/artist_list" 
-H "Authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
    	"users": [{
    			"id": 1,
    			"name": "vikram",
    			"image": "artist_image"
    		},
    		{
    			"id": 2,
    			"name": "vikram",
    			"image": "artist_image"
    		}
    	]
    }
```

###HTTP Request

`GET https://base_url.com/api/users`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
              |         |         |            |
             |         |         |            |
   
<aside class="warning"> 422 Unprocessable entry.</aside>
## Update User

```shell
curl "http://base_url/api/users/id:" 
-H "Authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
  	"user": {
  		"first_name": "vikram",
  		"last_name": "sharma",
  		"email_id": "vikramkannav@gmail.com",
  		"category": "artist",
  		"age": 30,
  		"profession": "vikram@gmail.com",
  		"work_on_album": "no",
  		"file_type": "song.mp3",
  		"play_instrument ": "yes",
  		"instrument_name": "gitar"
  	}
  }
```

###HTTP Request

`PUT https://base_url.com/api/users/id:`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    first_name| string | true | Please enter First Name |   
    last_name|  string | true | Please enter Last Name |  
    email_id |  string   | true | Please enter the email |  
    category|   string | true | Please select Catgeory |  Artist
    age|   number | true | Please enter you age       |  
    profession | string | true | Please enter you email |
    work_on_album | boolean | true | Please enter work on album |
    file_type | string    | true | Please upload video or audio |
    play_instrument | boolean | true | Play instrument Yes or No |
    instrument_type | string  | true | Please enter the instrument name|

<aside class="warning"> 422 Unprocessable entry.</aside>


    
## Followers

```shell
curl "http://base_url/api/artist_follow" 
-H "Authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
  	"users": [{
  			"id": 1,
  			"name": "vikram",
  			"image": "artist_image"
  		},
  		{
  			"id": 2,
  			"name": "vikram",
  			"image": "artist_image"
  		}
  	]
  }
```
###HTTP Request

`GET https://base_url.com/api/followers`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |         |            |
             |          |         |            |
        
<aside class="warning"> 422 Unprocessable entry.</aside>


## Followings

```shell
curl "http://base_url/api/followings" 
-H "Authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
   {
   	"users": [{
   			"id": 3,
   			"name": "sumit",
   			"image": "artist_image"
   		},
   		{
   			"id": 6,
   			"name": "ram",
   			"image": "artist_image"
   		}
   	]
   }
```
###HTTP Request

`GET https://base_url.com/api/followings`

### Query Parameters

     Parameter | Type | Required | Description| Default
        --------- | ------- | ------- | ----------- | -----------
                 |          |         |            |
                 |          |         |            |
            
<aside class="warning"> 422 Unprocessable entry.</aside>



## Follow/Unfollow

```shell
curl "http://base_url/api/follow" 
-H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
  	"user": {
  		"following_id": 1,
  		"status": true
  	}
  }
```
###HTTP Request

`POST https://base_url.com/api/follow`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |         |              |
             |          |         |               |
