# Post

## Posts

This API is used for the list of post.

```shell
curl "http://base_url/api/posts" 
-H "Authentication:Bearer access token"
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

<aside class="warning"> 404 Not Found.</aside>


## Create Post

This API is used for the Post creation.

```shell
curl "http://base_url/api/posts" 
-H " authentication : bearer access token"
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
    description | string | true   | Please enter you post description| 

 <aside class="warning"> 422 Unprocessable entry.</aside>


## Update Post

This API is used for Post update.

```shell
curl "http://base_url/api/posts/:id" 
-H "Authentication:Bearer access token"
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
     description | string | true  | Please update your post| 

 <aside class="warning"> 422 Unprocessable entry.</aside>


## Delete Post

This API is used for the Post delete.

```shell
curl "http://base_url/api/artist/delete/:id" 
-H "Authentication:Bearer access token"
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
  

 <aside class="warning"> 422 Unprocessable entry.</aside>
