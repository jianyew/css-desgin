## 5. 服务显示和查询 ##

#### Server List
* URL: ***GET*** `http：[service]/api/v1/server?q={json_query}&offset=1&limit=50`
* Http Query :
	```json
		{
			"serviceName": 	["123","321"], 				//服務	
			"type": 	["123","211"], 					//服務類別		
			"area": 	["中环"], 						//地區	
		}
	```


* 响应实例:
	
	- success:
	  - http_code:200

		服務單編號 				
		服務類別				
		地區 				
		售价 				
		開始日 				
		到期日				
		是否銷售				
		標題				
		詳情				
		優惠及條款方				
		服務單編號 				
		商號名稱				
		聯絡人				
		地址				
		電話				
		產品照片 				
	```json
		{
			"meta":{
				"status_code":20000,
				"hint":"success"
			}

			"data"[
				{
					"elementType": "server", //服务
                    "no":"1", 
                    "category":"?????"
                    "area":"",
                    "price":"",
                    "startDate":"",
                    "endDate":"",
                    "isSell":"Y/N",
                    "title":"",
                    "detail":"",
                    "terms":"",
                    "服務單編號":"????",
                    "商號名稱":"?????",
                    "contactor":"",
                    "address":"",		
                    "phone":"",				
                    "images":[
						{
	                        "id":"1",   
							"url":"http://xxxxx.com/image/1",
							"hight":"768",
							"with":"1024"	
						},
						{
                            "id":"2",
							"url":"http://xxxxx.com/image/2",
							"hight":"768",
							"with":"1024"	
						}
					]
				},
				{
					"elementType": "ad", //广告
					"order":2,
					"images":[
						{
	                        "id":"1",   
							"url":"http://xxxxx.com/image/1",
							"hight":"768",
							"with":"1024"	
						},
						{
                            "id":"2",
							"url":"http://xxxxx.com/image/2",
							"hight":"768",
							"with":"1024"	
						}
						
					],
				},


			]
		}
	```

   - fail:
    
	- http_code:400
 	
	- status_code: 40101
	```json
		{
			"meta":{
				"status_code":40301,
				"hint":"xxxxxxxxxxx"
			}
		}
	````


#### Server Detail
* URL: ***GET*** `http：[service]/api/v1/server/{serverid}`
* 响应实例:
*
	- success:
	  - http_code:200
		```json
         {
            "meta":{},
            "car":{
					"elementType": "server", //服务
                    "no":"1", 
                    "category":"?????"
                    "area":"",
                    "price":"",
                    "startDate":"",
                    "endDate":"",
                    "isSell":"Y/N",
                    "title":"",
                    "detail":"",
                    "terms":"",
                    "服務單編號":"????",
                    "商號名稱":"?????",
                    "contactor":"",
                    "address":"",		
                    "phone":"",				
                    "images":[
						{
	                        "id":"1",   
							"url":"http://xxxxx.com/image/1",
							"hight":"768",
							"with":"1024"	
						},
						{
                            "id":"2",
							"url":"http://xxxxx.com/image/2",
							"hight":"768",
							"with":"1024"	
						}
					]
				},
         }
		```