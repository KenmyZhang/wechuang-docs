---
name: 类型列表
---
    
### Url
     /weidu/api/v1/homepage/task/type/list
    
### Method
    GET

### Request Payload
    {
        "industry_id": "行业，数据类型int",
        "types":["类型，数据类型int"]
    }

### Content-Type
    application/json        

### Response Body

### Response Code
    HTTP/1.1 200 OK

### Example
      
	  curl -X GET "http://8.134.37.138:9004/weidu/api/v1/homepage/task/type/list" -i
			HTTP/1.1 200 OK
			Content-Type: application/json; charset=utf-8
			Date: Wed, 09 Jun 2021 13:46:21 GMT
			Content-Length: 760

		{
			"code": 200,
			"list": [{
				"id": 1,
				"name": "游戏",
				"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/youxi.jpg",
				"types": [{
					"id": 1,
					"name": "建模",
					"cover_link": "",
					"industry_id": 0
				}, {
					"id": 2,
					"name": "动作",
					"cover_link": "",
					"industry_id": 0
				}, {
					"id": 3,
					"name": "特效",
					"cover_link": "",
					"industry_id": 0
				}, {
					"id": 4,
					"name": "界面",
					"cover_link": "",
					"industry_id": 0
				}]
			}, {
				"id": 2,
				"name": "漫画",
				"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/manhua.jpg",
				"types": [{
					"id": 1,
					"name": "分镜",
					"cover_link": "",
					"industry_id": 0
				}, {
					"id": 2,
					"name": "动作",
					"cover_link": "",
					"industry_id": 0
				}, {
					"id": 3,
					"name": "线稿",
					"cover_link": "",
					"industry_id": 0
				}, {
					"id": 4,
					"name": "上色",
					"cover_link": "",
					"industry_id": 0
				}, {
					"id": 5,
					"name": "整套",
					"cover_link": "",
					"industry_id": 0
				}]
			}],
			"result": "ok"
		}