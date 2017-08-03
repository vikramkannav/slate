
# Users

## Users

This API is used for the user list.
This API is an authentication API request in which needs to pass auth token in the request header.

```shell
  curl -X GET \
    https://base_url.com/api/users \
    -H 'accept: application/json' \
    -H 'authorization: Token token=treehsgstsdde3573' \
    -H 'cache-control: no-cache' \
    -H 'content-type: application/json' \
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

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
              |         |         |            |
             |         |         |            |
   
<aside class="warning"> 422 Unprocessable Entity.</aside>
## Update User

```shell
curl -X PUT \
  http://base_url/api/users/id: \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '  {
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

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    first_name| string | true | first_name of the user |   
    last_name|  string | true | last_name of the user|  
    email_id |  string   | true | email_id of the user the user|  
    category|   string | true | category |  Artist
    age|   number | true | age of the user     |  
    profession | string | true | profession of the user |
    work_on_album | boolean | true | work_on_album of the user|
    file_type | string    | true | file_type  |
    play_instrument | boolean | true | play_instrument user |
    instrument_type | string  | true | instrument_type type of the user|

<aside class="warning"> 404 Not Found.</aside>


    
## Followers

```shell
   curl -X GET \
   https://base_url.com/api/followers \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
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

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |         |            |
             |          |         |            |
        
<aside class="warning"> 422 Unprocessable Entity. </aside>


## Following

```shell
   curl -X GET \
   https://base_url.com/api/following \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
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

### Parameters

     Parameter | Type | Required | Description| Default
        --------- | ------- | ------- | ----------- | -----------
                 |          |         |            |
                 |          |         |            |
            
<aside class="warning"> 422 Unprocessable Entity. </aside>



## Follow

```shell
curl -X POST \
  https://base_url.com/api/followers \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  ```

> The above command returns JSON structured like this:

```json
   {
     "message": "User follow successfully."
    }
  
```
###HTTP Request

`POST https://base_url.com/api/follow/:id`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |         |              |
             |          |         |               |
             
             
<aside class="warning">422 Unprocessable entry.</aside>


##Unfollow

```shell
 curl -X DELETE \
     https://base_url.com/api/unfollow/ \
     -H 'accept: application/json' \
     -H 'authorization: Token token=treehsgstsdde3573' \
     -H 'cache-control: no-cache' \
     -H 'content-type: application/json' \
```

> The above command returns JSON structured like this:

```json
   {
     "message": "User Unfollow successfully."
    }
  
```
###HTTP Request

`DELETE https://base_url.com/api/unfollow/:id`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |         |              |
             |          |         |               |
<aside class="warning"> 404 Not Found.</aside>

