# Post

## Posts

This API is used for the list of post.
This API is an authentication API request in which needs to pass auth token in the request header.

```shell
 curl -X GET \
   https://base_url.com/api/posts \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
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
				"name": "vikram",
				"image": "artist_image"
			}
		},
		{
			"post_id": 1,
			"description": "post_description",
			"user": {
				"id": 2,
				"name": "vikram",
				"image": "artist_image"
			}
		}
	],
	"message": "Post created successfully"
}
 ```

###HTTP Request

`GET https://base_url.com/api/posts`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
              |         |         |             |
              |        |          |             |

<aside class="warning"> 422 Unprocessable Entity.</aside>


## Create Post

This API is used for the Post creation.
This API is an authentication API request in which needs to pass auth token in the request header.

```shell
curl -X POST \
   https://base_url.com/api/posts \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
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

###HTTP Request

`POST https://base_url.com/api/posts`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    description | string | true   | description of the post| 

 <aside class="warning"> 422 Unprocessable entry.</aside>


## Update Post

This API is used for Post update.
This API is an authentication API request in which needs to pass auth token in the request header.

```shell 
 curl -X PUT \
   https://base_url.com/api/posts/ \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
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


###HTTP Request

`PUT https://base_url.com/api/posts/:id`


### Query Parameters

     Parameter | Type | Required | Description| Default
     --------- | ------- | ------- | ----------- | -----------
     description | string | true  | description of the post| 

 <aside class="warning"> 404 Not Found</aside>


## Delete Post

This API is used for the Post delete.
This API is an authentication API request in which needs to pass auth token in the request header.

```shell
 curl -X DELETE \
   https://base_url.com/api/posts/ \
  -H 'accept: application/json' \
  -H 'authorization: Token token=treehsgstsdde3573' \
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

`DELETE https://base_url.com/api/posts/:id`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
             |          |        |              |
  

 <aside class="warning"> 404 Not Found</aside>
