## 6. 车上传 ##

#### upload Car 
* URL: ***POST*** `http：[service]/api/v1/car`
* POST_Body:
   
   "number":"HK088"	

   "price":128900					//售價

   "discount":1234   				//减價

   "color":"#e60000"				//hex , 顏色

   "couponInfor":""     			//???? 優惠資料

   "trademark":"大众"				//品牌

   "type":"SUV"					//車類型

   "madeYear":"2012"			//制造年份
					
   "meter":"100000"				 //行駛公里
					
   "傳動" : ""                   	//????

   "location": "x,y"

   "images" : "[***.jpg,***.jpg]"


* 响应实例:
	- success
    
     http_code: 200
 	
    ```json
	{
		"meta":{
			"status_code":200,
			"hint":"success"
		}
		"carid":123
	}
   ``` 
   - Fails
   
   http_code: 400
   
    ```json
	{
		"meta":{
			"status_code": 40600,
			"hint":"fails xxxxx"
		}
		"carid":123
	}
   ```

**问题**
   1. 录入的和显示的有些属性不一致？？ 需要check一下。
   2. 那些不是必要要条件？？
   3. 录入后界面调转到哪里?
   4. operation 项目有哪些可选值？
   