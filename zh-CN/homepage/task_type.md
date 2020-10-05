---
name: 类型列表
---
    
### Url
     /weidu/api/v1/homepage/task/type/list
    
### Method
    POST

### Request Payload
    {
        "industry_id": "行业，数据类型int",
        "types":["类型，数据类型int"]
    }


|行业| 类型 | 编码 |
|--- |---|---|
|游戏 1 |   原画|     1 |
|游戏 1 |   建模|      2 |
|游戏 1 |   动作|      3 |
|游戏 1 |   特效 |     4   |
|游戏 1 |   界面 |     5   |


|行业| 类型 | 编码 |
|---|---|---|
|漫画 2 |   角色|     6|
|漫画 2 |   分镜|      7 |
|漫画 2 |   线稿|      8 |
|漫画 2 |   上色 |     9   |
|漫画 2 |   整套 |     10   |

### Content-Type
    application/json        

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": [
            {
                "id":""美工类型，数据类型int",
                "name":"美工类型名称，数据类型string",
                "cover_link":"封面链接，数据类型string",
                "industry_id": "行业id，数据类型int"
            }
        ]
    }




### Response Code
    HTTP/1.1 200 OK

### Example
      curl -X POST "http://129.28.198.139:9004/weidu/api/v1/homepage/task/type/list" -i -d '{"industry_id":2, "type_ids":[6,7]}'
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Mon, 05 Oct 2020 08:57:09 GMT
        Content-Length: 276
        
        {
        	"code": 200,
        	"list": [{
        		"id": 6,
        		"name": "è§’è‰²",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/juese.jpg",
        		"industry_id": 2
        	}, {
        		"id": 7,
        		"name": "åˆ†é•œ",
        		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/fenjing.jpg",
        		"industry_id": 2
        	}],
        	"result": "ok"
        }
        

    curl -X POST "http://129.28.198.139:9004/weidu/api/v1/homepage/task/type/list" -i -d '{"industry_id":2}'
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Mon, 05 Oct 2020 08:59:05 GMT
        Content-Length: 638

    {
    	"code": 200,
    	"list": [{
    		"id": 6,
    		"name": "è§’è‰²",
    		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/juese.jpg",
    		"industry_id": 2
    	}, {
    		"id": 7,
    		"name": "åˆ†é•œ",
    		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/fenjing.jpg",
    		"industry_id": 2
    	}, {
    		"id": 8,
    		"name": "çº¿ç¨¿",
    		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/xiangao.jpg",
    		"industry_id": 2
    	}, {
    		"id": 9,
    		"name": "ä¸Šè‰²",
    		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/shangse.jpg",
    		"industry_id": 2
    	}, {
    		"id": 10,
    		"name": "æ•´å¥—",
    		"cover_link": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfw/zhengtao.jpg",
    		"industry_id": 2
    	}],
    	"result": "ok"
    }
        
