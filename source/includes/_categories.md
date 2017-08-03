
#Categories

##Categories

This API is used for the list of categories. 
This API is an authentication API request in which needs to pass auth token in the request header.

```shells
  curl -X GET \
  http://base_url.com/api/categories \
 -H 'accept: application/json' \
 -H 'authorization: Token token=treehsgstsdde3573' \
 -H 'cache-control: no-cache' \
 -H 'content-type: application/json' \
```

> The above command returns JSON structured like this:

```json
  {
  	"categories": [{
  			"id": 1,
  			"type": "musician"
  		},
  		{
  			"id": 2,
  			"type": "gitarist"
  		}
  	]
  }
```

###HTTP Request

`GET http://base_url.com/api/categories`

### Parameters

    Parameter | Type | Required | Description| Default
    --------- | ------- | ------- | ----------- | -----------
              |         |         |             |
              |         |         |             |
        
 <aside class="warning"> 422 Unprocessable Entity.</aside>
