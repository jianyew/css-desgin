##  API Doc ##

***1. 主頁功能***

>**广告**

* 主页广告轮播

* URL: *GET* `http：[service]/api/v1/mainpage/ad`

* 响应实例:

```json
	{
		"meta":{
			"status_code":200,
			"hint":"success"
		}
		
		"ads":[
			{
				
				"img": "http://p2.zhimg.com/10/7b/107bb4894b46d75a892da6fa80ef504a.jpg",
				"type":"image",
				"order":1
			},
			{
				"img": "http://p2.zhimg.com/10/7b/107bb4894b46d75a892da6fa80ef504a.jpg",
				"video": "http://p2.zhimg.com/10/7b/xxxx.mp4",
				"type":"vido",
				"order":2
			}
			
		]
		
	} 
``` 
* 分析:
	- ads.type: image-> 图片， vido->视频


>**查询**
	

- ??查询什么？？

- 怎么显示查询结果？


>**在线人数**

  
* URL: *GET* `http：[service]/api/v1/lineno`
*  响应实例:


```json
	{
		"meta":{
			"status_code":200,
			"hint":"success"
		}
		
		"number":1220
	}
``` 
  





	










    
	


