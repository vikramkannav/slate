
#Categories

##List of all categories

```shells
curl "http://base_url/api/categories-list" 
 -H " authentication : bearer access token"
```

> The above command returns JSON structured like this:

```json
  {
  "categories" :[
    "1" : "musician",
    "2" : "gitarist",
     ]
  }
```

###HTTP Request

`GET http://base_url.com/api/categories-list`

### Query Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
    categories_id|integer|true | Categories id number | id:1      
    categories_name|string|true |Categories name | Artist    
 
 <aside class="warning"> 422 Unprocessable entry.</aside>
