# Post

## List all Post

```shell
curl "http://base_url/api/post-list" 
  -H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
   "post-list":{
    "id":1 ,
    "post_description":"post_description"
               }
 ```

###HTTP Request

`GET https://base_url.com/api/post/list`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    post_id   | integer | true    | Post ID    |
    post_description | string | true | Post decription


<aside class="warning"> 422 Unprocessable entry.</aside>


## Create Post

```shell
curl "http://base_url/api/post/create" 
-H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
  "post":{
      "post_id" : 1,
      "post_description" :"post_description"
     }
   }
   
   ```

###HTTP Request

`POST https://base_url.com/api/post/create`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    Post      | string | true   | Please enter you post description| NULL

 <aside class="warning"> 422 Unprocessable entry.</aside>


## Edit Post

```shell
curl "http://base_url/api/post/edit/:id" 
-H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
   {
  "post" :{
    "id": 1,
    "post_description" : "post_description"
     }
   }
```


###HTTP Request

`PUT https://base_url.com/api/post/:id/edit`


### Query Parameters

     Parameter | Type | Required | Description| Default
     --------- | ------- | ------- | ----------- | -----------
     Post      | string | true   | Please update your post| post description

 <aside class="warning"> 422 Unprocessable entry.</aside>


## Delete Post

```shell
curl "http://base_url/api/artist/update/id" 
-H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
   {
   "message":"Post is delete successfully",
   }
```

###HTTP Request

`Delete https://base_url.com/api/post/:id/delete`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    Post      |  string | true  | your post description | post description


 <aside class="warning"> 422 Unprocessable entry.</aside>
