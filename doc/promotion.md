## 6. 推廣功能 ##

**购买 有交易** ???


推廣照片					
標題					
售价					
詳情					
有效日期					
地址					
電話					
短訊聯絡					
優惠及條款					

#### Promotion List
* URL: ***GET*** `http：[service]/api/v1/promotions?offset=1&limit=50`

* 响应实例:
	
	- success:
	  - http_code:200
	  ```json

           {
			"meta":{
				"status_code":20000,
				"hint":"success"
			}
            
            data:[
				{
                     "title":"",
                     "price":"",
                     "detail":"",
                     "datetime":"",
                     "address":"",
                     "mobile":"",
                     "clause":"",
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

				{
					"elementType": "ad", //广告
                    "url":"xxxxxxxxx",
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