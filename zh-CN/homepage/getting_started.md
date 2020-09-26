---
name: 开始使用 START
---
    
### Url
     /weidu/api/v1/homepage/start/list
    
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
                "action_type":"操作类型，包括发布publish、监制superintend、制作make，数据类型string",
                "name": "名称，数据类型string",
                "cover_link":"封面链接，数据类型string"
            }
        ]
    }
    
### Response Code
    HTTP/1.1 200 OK

### Example
     curl -X POST "http://129.28.198.139:8089 /weidu/api/v1/homepage/start/list"  -i
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
        "list": [
            {
                "action_type":"publish",
                "name": "发布",
                "cover_link":"http://xxx"
            },
            {
                "action_type":"superintend",
                "name": "监制",
                "cover_link":"http://xxx"
            },
            {
                "action_type":"make",
                "name":"制作",
                "cover_link":"http://xxx"
            }
        ]
    }
