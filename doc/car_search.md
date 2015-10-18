## 3. 二手车显示和查询 ##

#### Car List
* URL: ***GET*** `http：[service]/api/v1/car?q={json_query}&offset=1&limit=50`
* Http Query :
	```json
		{
			"source": 	["P","M"], 					//來源				(私人/車行)
			"cartype": 	["???"], 					//車類型				自選
			"area": 	["中环"], 					//地區				自選
			"motion"	[""],						//"車廠" 			自選
			"price"	:	[688899], 					//售價				自選
			"madeYear":  [1999],  					//制造年份			自選
			"tradeFrequency" : [1], 				//手數				(轉手次數)
			"meter":[12000],       					//公里數				自選
			"apacity":["1.6L","2.0T"],              //汽缸容量			自選
			"":[],									//傳動				自選	 ???
			"seatSize" : [5,7],						//座位				自選
			"status":[]								//狀態				自選 ???
			"carNo":	"HK00999"					//車盤編號			(人手輸入)	
		}
	```


* 响应实例:
	- http_code:200
	- success:
		
		```json
		{
			"meta":{
				"status_code":20000,
				"hint":"success"
			}

			data:[
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
				{
					"elementType": "ad", //广告
					"order":2,
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
				},
				.
				.
				.
			]
		} 
		```
 	- fail:
    
	- http_code:400
 	
	- status_code: 40101
	```json
		{
			"meta":{
				"status_code":40101,
				"hint":"xxxxxxxxxxx"
			}
		}
	````

#### Car Detail
* URL: ***GET*** `http：[service]/api/v1/car/{carid}`

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
					"傳動" : "" ,                  	//????
					"comment" :"好靓的车", 			//评论
					"phone" : "123456",				//电话
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
				
				}
		}
	```
    - Fails:
    
	  - http_code:400
 	
	  - status_code: 40102




#### 举报
* URL: ***POST*** `http：[service]/api/v1/car/{carid}/complaints/{typeid}`

* POST_BODY:
  "phone":"123455"




**问题**

  1. 先显示车list，当用户点击查询才显示查询term？
  2. 广告能否被点击？ 当用户 click 广告后界面怎么显示？
  
	