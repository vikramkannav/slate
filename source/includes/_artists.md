
# Artists

## Update an Artist

```shell
curl "http://base_url/api/artist/update/id" 
-H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
   "user": {
             "first_name":"vikram" ,
             "last_name": "sharma",
             "email_id": "vikramkannav@gmail.com",
             "category": "artist"
             }
  }
```

###HTTP Request

`PUT https://base_url.com/api/artist/update/id`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    first_name| string | true | Please enter First Name | first_name  
    last_name|  string | true | Please enter Last Name |  last_name
    email_id |  email   | true | Please enter the email |  email_id
    category|   string | true | Please select Catgeory |  Artist



## Get an Artist

```shell
curl "http://base_url/api/artist_list" 
-H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
   "artist-list": {
             "artist_name":"vikram" ,
             "artist_image":"artist_image"             }
                  }
  }
```

###HTTP Request

`GET https://base_url.com/api/artist/list`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    artist_name| string | true  | Artist Name |
    artist_image| image | true  | Artist Image |

## Follow an Artist

```shell
curl "http://base_url/api/artist_follow_list" 
-H " authentication : bearer access token"

```

> The above command returns JSON structured like this:

```json
  {
   "artist-follow-list": {
             "artist_name":"vikram" ,
             "artist_image":"artist_image"             }
                  }
  }
```
###HTTP Request

`GET https://base_url.com/api/artist/follow/list`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    artist_name| string | true  | Artist Name |
    artist_image| image | true  | Artist Image |


## Un-follow an Artist

```shell
curl "http://base_url/api/artist_follow_list" 
-H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
   "artist-unfollow-list": {
             "artist_name":"vikram" ,
             "artist_image":"artist_image"             }
                  }
  }
```
###HTTP Request

`GET https://base_url.com/api/artist/unfollow/list`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    artist_name| string | true  | Artist Name |
    artist_image| image | true  | Artist Image |
