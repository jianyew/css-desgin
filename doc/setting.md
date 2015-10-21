## 9. 我的设定 ##

### My profile
* URL: ***PUT*** `http：[service]/api/v1/profile`
* POST_Body:
   
    userId:""
 
    nickName: "小松"
	
    firstName:"姓"
	
    lastName:"名"
	
    password:"123"
	
    email:“zhangshan@email.com”
	
    sex: 1 男 ， 0 女
	
    myphoto: 1.jpg
   
    phone:""

    image:{file}


* 响应实例:
	- success
    
     http_code: 200
 	
    ```json
	{
		"meta":{
			"status_code":200,
			"hint":"success"
		}
		"userId":123
	}
   ``` 

  - Falis
  
  xxxxxxxxxxxxxxxxxxxxxxx



### My Car

* URL: ***GET*** `http：[service]/api/v1/mycars/{userid}`

* 响应实例:
	- success
    
     http_code: 200
```json
	{
			"meta":{
				"status_code":20000,
				"hint":"success"
			}
			cars:[
				{
					"carid":"1"
					"number":"HK088",				
					"price":128900,					//售價
					"discount":1234,   				//减價	
					"color":"#e60000",				//hex , 顏色
					"couponInfor":"" ,    			//???? 優惠資料
					"trademark":"大众",				//品牌
					"type":"SUV"，					//車類型
					"madeYear":"2012",				//制造年份
					"meter":"100000",				//行駛公里
					"傳動" : ""                   	//????
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
						
					],                                                  //車照片
					"order":1,
					"elementType": "car" //车
				},	
         ]
   }
````

  
  
