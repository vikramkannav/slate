# Post

## Posts

```shell
curl "http://base_url/api/posts" 
  -H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
 ```

###HTTP Request

`GET https://base_url.com/api/posts`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
              |         |         |             |
              |        |          |             |

<aside class="warning"> 422 Unprocessable entry.</aside>


## Create Post

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

```shell
curl "http://base_url/api/posts/:id" 
-H " authentication : bearer access token"
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

```shell
curl "http://base_url/api/artist/delete/:id" 
-H " authentication : bearer access token"
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
