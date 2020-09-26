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
                "industry":"行业种类，包括游戏game、漫画cartoon、动漫comic、创意originality、影视movies等等，数据类型string",
                "industry_name":"行业名称，数据类型string",
                "cover_link":"封面链接，数据类型string"
            }
        ]
    }




### Response Code
    HTTP/1.1 200 OK

### Example
     curl -X POST "http://129.28.198.139:8089/weidu/api/v1/homepage/task/industry/list"  -i
        HTTP/1.1 200 OK
        Content-Length: 17
        Content-Type: application/json
        Date: Thu, 07 xxx xxx 07:01:47 GMT
        Keep-Alive: timeout=38
        X-Request-Id: o85ef6pq3fde7bx7hi3rkahhbr
        X-Version-Id: 4.0.0.dev.463aa9e9f0c1d9e0d9e24172a4bde3d8

    {
        "result": "ok",
        "code": 200,
        "data": [
            {
                "industry":"game",
                "industry_name":"游戏",
                "cover_link":"http://xxx"
            },
            {
                "industry":"cartoon",
                "industry_name":"漫画",
                "cover_link":"http://xxx"
            },
            {
                "industry":"comic",
                "industry_name":"动漫",
                "cover_link":"http://xxx"
            },
            {
                "industry":"originality",
                "industry_name":"创意",
                "cover_link":"http://xxx"
            }   
                        {
                "industry":"movies",
                "industry_name":"影视",
                "cover_link":"http://xxx"
            }           
        ]
    }
