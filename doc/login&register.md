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
			"token":"xxxssssss"
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
	
	account: "张三/zhangshan@email.com/xxxx.facebook" ??? 好像没定义清除。
	
	nickName: "小松"
	
	firstName:"姓"
	
	lastName:"名"
	
	password:"123"
	
	email:“zhangshan@email.com”
	
	sex: 1 男 ， 0 女
	
	myphoto: 1.jpg 


* 响应实例:
	- success:
	
	```json
		{
			"meta":{
				"status_code":20000,
				"hint":"success"
			},
			
			"userId":"3456744"
			
		}
	
	```
  - fail:
    status_code: 4000*


* ####问题
 1. 那些是必须项目？
 2. 登陆account注册时候不需要输入吧？
 3. 注册时候是否需要这样多得item，是否可以简单注册后补充？
 
	

#### facebook 第三方登陆
  *Need reseach facebook sdk.*

	
	
	
	
	
	