---
name: 行业列表
---
    
### Url
     /weidu/api/v1/homepage/task/industry/list
    
### Method
    GET

### Content-Type
    application/json        

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": [
            {
                "id":"行业种类，数据类型int",
                "name":"行业名称，数据类型string",
                "cover_link":"封面链接，数据类型string"
            }
        ]
    }


| 行业 | 编码 |
|---|---|
|   品牌设计|     1 |
|   影视 |      2 |
|   企业网站建设|      3 |
|   动漫设计 |     4   |
|    游戏|     5   |
|   特效|      6 |
...

### Response Code
    HTTP/1.1 200 OK

### Example
        curl -X GET "http://129.28.198.139:9004/weidu/api/v1/homepage/task/industry/list" -i
            HTTP/1.1 200 OK
            Content-Type: application/json; charset=utf-8
            Date: Sun, 04 Oct 2020 13:44:48 GMT
            Content-Length: 551
        {
        	"code": 200,
        	"list": [{
        		"id": 1,
        		"name": "游戏",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/youxi.jpg"
        	}, {
        		"id": 2,
        		"name": "漫画",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/manhua.jpg"
        	}, {
        		"id": 3,
        		"name": "动漫",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/dongman.jpg"
        	}, {
        		"id": 4,
        		"name": "创意",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/chuangyi.jpg"
        	}, {
        		"id": 5,
        		"name": "影视",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/movie.jpg"
        	}],
        	"result": "ok"
        }
