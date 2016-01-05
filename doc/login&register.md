##2. 登陆和注册功能

#### 登陆

* URL: *POST* `http：[service]/api/v1/login`

* POST_BODY: 
	
	account:"张三"	
	password:"1234567" 
	
* 响应实例:
	- success:
	
	```json
		{
			"meta":{
				"status_code":20000,
				"hint":"success"
			},
			"token":"xxxssssss",
			"user" : {user_object}
		}
	
	```
	- 错误:
	
	```json
		{
			"meta":{
				"status_code":40001,
				"hint":"用户或者密码错误"
			}
		}
	
	```
	
<!--* remark：-->


#### 注册

* URL: *POST* `http：[service]/api/v1/register`
* POST_BODY:
	
	nickName: "小松"
	
	password:"123"
	
	email:“zhangshan@email.com”
	
	gender: 1 男 ， 0 女
	
	myphoto: 1.jpg (option)

	firstName: (option)
	
	lastName: (option)
	
	phone: (option)
	
	gender: (option)
	
	favoiter : [1,2,3,4] 服务器端是否有表存这个？**感兴趣的产品**
	
* 响应实例:
	- success:
	
	```json
		{
			"meta":{
				"status_code":20000,
				"hint":"success"
			},
			
			"user":userobjcet
			
		}
	
	```
  - fail:
    status_code: 4000*



 #### 图片上传
 
 * URL: *POST* `http：[service]/api/v1/image/update?type=h/c` (h:头像， c：车)
 
 * 响应实例:
	- success:
	
	```json
		{
			"meta":{
				"status_code":20000,
				"hint":"success"
			},
			
			"images":[
				{
					name:xxxxx.jpg
					
				}
			
			
			]
			
		}
	
	```
  - fail:
    status_code: 40010
 
 
	

#### facebook 第三方登陆
	
* URL: *POST* `http：[service]/api/v1/fblogin`
* POST_BODY:

	   "fbid": user.fbId!
	   
      "fbHeadImage": user.fbHeadImage!
      
      "fbName":user.fbName!
      
      "fbEmail":user.fbEmail!
      
      "fbGender": 1:男， 2；女， 0：猜

* 响应实例:
	- success:
	
	```json
		{
			"meta":{
				"status_code":20000,
				"hint":"success"
			},
			
			"token":"xxxssssss",
			"user" : {user_object}
			
		}	
	```


* #### case
	
	1. 创建一个facebook table. 
		* clouments: fbid , fbHeadImage, fbName, fbEmail, fbGender ， userid（FK）	
	2. 每次facebook登陆，用facebookid 去query user， 如果有，就返回。
	如果没有就新建一个user，然后返回给我。
	