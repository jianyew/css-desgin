## 7. 服务上传 ##

#### upload Service 
* URL: ***POST*** `http：[service]/api/v1/service`
* POST_Body:
	1)	服務				
	2)	服務類別				
	3)	地區				
	4)	售价 				
	5)	開始日期				
	6)	到期日期 				
	7)	標題 				
	8)	詳情 				
	9)	優惠及條款				
	10)	產品照片 				

   "name" : ""	                    //服務
   
   "type" : ""

   "area" : ""

   "title": ""
 
   "price":128900					//售價

   "startdate":""				

   "enddate":""     			
   
   "details":""

   "term":""

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
			"status_code": 40700,
			"hint":"fails xxxxx"
		}
		"carid":123
	}
   ```

**问题**
   1. 怎么区分私人还是商号？
   