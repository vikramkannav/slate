
# Users

## Users

This API is used for the user list. 

This API is an authentication API request in which needs to pass auth token in the request header.

```shell
  curl -X GET \
    http://base_url.com/api/users \
    -H 'accept: application/json' \
    -H 'authorization: Token token=hjduueuhfufu123' \
    -H 'cache-control: no-cache' \
    -H 'content-type: application/json' \
  ```

> The above command returns JSON structured like this:

```json
  {
    	"users": [{
    			"id": 1,
    			"name": "vikram"
    		},
    		{
    			"id": 2,
    			"name": "sumit"
    	    }
    	]
    }
```

###HTTP Request

`GET http://base_url.com/api/users`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
              |         |         |            |
             |         |         |            |

<aside class="success">status:200 OK</aside>
<aside class="warning">status:401 Unauthorized </aside>

## Update User

This API is used for the user update. 

This API is an authentication API request in which needs to pass auth token in the request header.

```shell
curl -X PUT \
  http://base_url/api/users \
  -H 'accept: application/json' \
  -H 'authorization: Token token=hjduueuhfufu123' \
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
>The above command returns JSON structured like this for failure:

```json
{
"error" :{
    "email": "email incorrect"
    "file_type":"invalid"
    }
```


###HTTP Request

`PUT http://base_url.com/api/user`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    first_name| string | true | First name of the user |   
    last_name|  string | true | Last name of the user|  
    email_id |  string   | true | Email adrees of the user|  
    category|   string | true | Category select by the user |  Artist
    age|   number | true | Age of the user     |  
    profession | string | true | Profession of the user |
    work_on_album | boolean | true | Work on album by the user|
    file_type | string    | true | File type select by the user  |
    play_instrument | boolean | true | Play instrument play by user |
    instrument_type | string  | true | Instrument type select by the user|

<aside class="success">status:200 OK</aside>
<aside class="warning">status:422 Unprocessable. </aside>


    
## Followers

This API is used for the show followers

This API is an authentication API request in which needs to pass auth token in the request header.

```shell
   curl -X GET \
   http://base_url.com/api/followers \
  -H 'accept: application/json' \
  -H 'authorization: Token token=hjduueuhfufu123' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 ```

> The above command returns JSON structured like this:

```json
  {
  	"users": [{
  			"id": 1,
  			"name": "vikram"
  		},
  		{
  			"id": 2,
  			"name": "vikram"  		
  		}
  	]
  }
```

###HTTP Request

`GET http://base_url.com/api/followers`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |         |            |
             |          |         |            |
        
<aside class="success">status:200 OK</aside>
<aside class="warning"> 401 Unauthorized </aside>


## Following

This API is used for the show following.

This API is an authentication API request in which needs to pass auth token in the request header.



```shell
   curl -X GET \
   http://base_url.com/api/following \
  -H 'accept: application/json' \
  -H 'authorization: Token token=hjduueuhfufu123' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
```

> The above command returns JSON structured like this:

```json
 {
 	"users": [{
 			"id": 3,
 			"name": "sumit"
 		},
 		{
 			"id": 6,
 			"name": "ram"
 		}
 	]
 }
```

###HTTP Request

`GET http://base_url.com/api/following`

### Parameters

     Parameter | Type | Required | Description| Default
        --------- | ------- | ------- | ----------- | -----------
                 |          |         |            |
                 |          |         |            |
            
<aside class="success">status:200 OK</aside>
<aside class="warning">401 Unauthorized </aside>



## Follow

This API is used for the follow.

This API is an authentication API request in which needs to pass auth token in the request header.


```shell
curl -X POST \
  http://base_url.com/api/users/:id/follow \
  -H 'accept: application/json' \
  -H 'authorization: Token token=hjduueuhfufu123' \
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

`POST http://base_url.com/api/users/:id/follow`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |         |              |
             |          |         |               |
             
<aside class="success">status:200 OK</aside>
<aside class="warning">422 Unprocessable entry.</aside>


##Unfollow

This API is used for the unfollow.

This API is an authentication API request in which needs to pass auth token in the request header.


```shell
 curl -X DELETE \
     http://base_url.com/api/unfollow/ \
     -H 'accept: application/json' \
     -H 'authorization: Token token=hjduueuhfufu123' \
     -H 'cache-control: no-cache' \
     -H 'content-type: application/json' \
```

> The above command returns JSON structured like this:

```json
   {
     "message": "User un follow successfully."
    }
```

###HTTP Request

`DELETE http://base_url.com/api/users/:id/unfollow`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |         |              |
             |          |         |               |

<aside class="success">status:200 OK</aside>
<aside class="warning"> 401 Unauthorized </aside>