
#Categories

##Categories

This API is used for the list of categories. 
This is open API where Auth token is not required to be passed in header.

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
        
 