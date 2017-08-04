# Post

## Posts

This API is used for the list of post. 

This API is an authentication API request in which needs to pass auth token in the request header.

```shell
 curl -X GET \
   http//base_url.com/api/posts \
  -H 'accept: application/json' \
  -H 'authorization: Token token=hjduueuhfufu123' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
```

> The above command returns JSON structured like this:

```json
{
	"posts": [{
			"post_id": 1,
			"description": "post_description",
			"user": {
				"id": 1,
				"name": "vikram"				
			}
		},
		{
			"post_id": 1,
			"description": "post_description",
			"user": {
				"id": 2,
				"name": "vikram"				
			}
		}
	]	
}
 ```
>The above command returns JSON structured like this for failure:

###HTTP Request

`GET http://base_url.com/api/posts`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
              |         |         |             |
              |        |          |             |

<aside class="success">status:200 OK</aside>
<aside class="warning"> 401 Unauthorized.</aside>


## Create Post


This API is used for the Post creation.

This API is an authentication API request in which needs to pass auth token in the request header.

```shell
curl -X POST \
   http://base_url.com/api/post \
  -H 'accept: application/json' \
  -H 'authorization: Token token=hjduueuhfufu123' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
   -d '{
	 "description": "post_description"
}'

```

> The above command returns JSON structured like this:

```json
 {
 	"post": {
 		"post_id": 1,
 		"description": "post_description"
 	},
 	"message": "Post created successfully"
 }
   
   ```
>The above command returns JSON structured like this for failure:

```json
{
  "error": "Please enter the valid description"
}   
```

###HTTP Request

`POST http://base_url.com/api/post`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    description | string | true   | description of the post| 


<aside class="success">status:200 OK</aside>
<aside class="warning"> 422 Unprocessable entry.</aside>


## Update Post

This API is used for Post update.

This API is an authentication API request in which needs to pass auth token in the request header.

```shell 
 curl -X PUT \
   http://base_url.com/api/posts/ \
  -H 'accept: application/json' \
  -H 'authorization: Token token=hjduueuhfufu123' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
 -d '{
	"description": "post_description"
}'


```

> The above command returns JSON structured like this:

```json
   {
   	"post": {
   		"id": 1,
   		"description": "post_description"
   	},
   	 	"message": "Post Updated successfully"
   }
```
>The above command returns JSON structured like this for failure:

```json
{
  "error": "Please enter the valid description"
}   
```

###HTTP Request

`PUT http://base_url.com/api/:id/post`


### Parameters

     Parameter | Type | Required | Description| Default
     --------- | ------- | ------- | ----------- | -----------
     description | string | true  | description of the post| 

<aside class="success">status:200 OK</aside>
<aside class="warning"> 422 Unprocessable entry.6t</aside>


## Delete Post

This API is used for the Post delete.

This API is an authentication API request in which needs to pass auth token in the request header.

```shell
 curl -X DELETE \
   http://base_url.com/api/:id/post \
  -H 'accept: application/json' \
  -H 'authorization: Token token=hjduueuhfufu123' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
```

> The above command returns JSON structured like this:

```json
   {
   	"message": "Post deleted successfully"
   }
```


###HTTP Request

`DELETE http://base_url.com/api/:id/post`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |        |              |
  

<aside class="success">status:200 OK</aside>
<aside class="warning"> 401 Unauthorized </aside>