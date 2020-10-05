---
name: 开始使用 START
---
    
### Url
     /weidu/api/v1/homepage/startlist
    
### Method
    GET

### Content-Type
    application/json      

### Request Payload

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "list": [
            {
                "id":"操作类型id，包括发布1、监制2、制作3，数据类型int",
                "name": "名称，数据类型string",
                "cover_link":"封面链接，数据类型string"
            }
        ]
    }
    
### Response Code
    HTTP/1.1 200 OK

### Example
     
        curl -X GET "http://129.28.198.139:9004/weidu/api/v1/homepage/startlist" -i 
            HTTP/1.1 200 OK
            Content-Type: application/json; charset=utf-8
            Date: Sun, 04 Oct 2020 12:07:00 GMT
            Content-Length: 395

        {
        	"code": 200,
        	"list": [{
        		"id": 1,
        		"name": "发布",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/fabu.jpg"
        	}, {
        		"id": 2,
        		"name": "监制",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/jianzhi.jpg"
        	}, {
        		"id": 3,
        		"name": "制作",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/zhizuo.jpg"
        	}],
        	"result": "ok"
        }