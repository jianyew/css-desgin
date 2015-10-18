## 4. 车行 ##


#### 车行 List
* URL: ***GET*** `http：[service]/api/v1/motors?offset=1&limit=50`

* 响应实例:
	- http_code:200
	- success:
	```json
		{
			"meta":{
				"status_code":20000,
				"hint":"success"
			}

			"data":[
				{
					"id":"1"
					"name":"",
					"mobile":"88569",
					"address":"",
					"elementType":"motor",
					"images":[
						{
							"url":"http://xxxxx.com/image/1",
							"hight":"768",
							"with":"1024"	
						},
						{
							"url":"http://xxxxx.com/image/2",
							"hight":"768",
							"with":"1024"	
						}
						
					],
					"order":1     
				},
				{
					"elementType": "ad", //广告
					"order":2,
					"images":[
						{
							"id": "1",
							"url":"http://xxxxx.com/image/1",
							"hight":"768",
							"with":"1024"	
						},
						{
							"id": "2",
							"url":"http://xxxxx.com/image/2",
							"hight":"768",
							"with":"1024"	
						}
						
					],
				},

			]
		}
	```

	- http_code:400
 	
	- status_code: 40201
	```json
		{
			"meta":{
				"status_code":40201,
				"hint":"xxxxxxxxxxx"
			}
		}
	````

#### 车行 Detail
* URL: ***GET*** `http：[service]/api/v1/motor/{motorid}`

* 响应实例:
	- http_code:200
	- success:

```json
	{
		"meta":{
				"status_code":20000,
				"hint":"success"
		},
		"motor",{
			
			"name":"",
			"phone":"1234455",
			"email":"xxxxx@gmail.com",
			"www" : "www.123.com",
			"(廣告套餐)" : "?????",
			"(車行優惠)" : "????",
			"introduction":"abxcsdf23",		
			"carAmount":"12",
			"images":[
					{
							"id": "1",
							"url":"http://xxxxx.com/image/1",
							"hight":"768",
							"with":"1024"	
						},
						{
							"id": "2",
							"url":"http://xxxxx.com/image/2",
							"hight":"768",
							"with":"1024"	
						}
						
					],

		},
		cars:[
			{
				"id":1,
				"images":[
					{
							"id": "1",
							"url":"http://xxxxx.com/image/1",
							"hight":"768",
							"with":"1024"	
						},
						{
							"id": "2",
							"url":"http://xxxxx.com/image/2",
							"hight":"768",
							"with":"1024"	
						}
						
					],
				"name":""
			},
		]
	}
```
   - status_code: 40201
	```json
		{
			"meta":{
				"status_code":40202,
				"hint":"xxxxxxxxxxx"
			}
		}
	````


