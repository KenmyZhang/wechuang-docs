---
name: 类型列表
---
    
### Url
     /weidu/api/v1/homepage/task/type/list
    
### Method
    POST

### Request Payload
    {
        "types":["美工类型，包括原画original、建模model、动作action、特效special_effects、界面interface，数据类型string"]
    }

### Content-Type
    application/json        

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": [
            {
                "type":""美工类型，包括原画original、建模model、动作action、特效special_effects、界面interface，数据类型string",
                "name":"美工类型名称，数据类型string",
                "cover_link":"封面链接，数据类型string"
            }
        ]
    }




### Response Code
    HTTP/1.1 200 OK

### Example
     curl -X POST "http://129.28.198.139:8089/weidu/api/v1/homepage/task/type/list"  -i -d '{"types":["original","model","action","special_effects","interface"]}'
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
                "type":"original",
                "name":"原画",
                "cover_link":"http://xxx"
            },
            {
                "type":"model",
                "name":"建模",
                "cover_link":"http://xxx"
            },
            {
                "type":"action",
                "name":"动作",
                "cover_link":"http://xxx"
            },
            {
                "industry":"special_effects",
                "name":"特效",
                "cover_link":"http://xxx"
            },
            {
                "industry":"interface",
                "name":"界面",
                "cover_link":"http://xxx"
            }         
        ]
    }
