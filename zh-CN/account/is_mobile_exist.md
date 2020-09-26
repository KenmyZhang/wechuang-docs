---
name: 判断手机号是否已经注册过
---
    
### Url
     /weidu/api/v1/users/mobile/exist
    
### Method
    POST

### Content-Type
    application/json      

### Request Payload
    {
        "mobile":"手机号码，数据类型string，必填"
    }

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "is_exist":"是否存在，数据类型bool"
    }
    
### Response Code
    HTTP/1.1 200 OK

### Example
     curl -X POST "http://129.28.198.139:8089/weidu/api/v1/users/mobile/exist" -d '{"mobile":"13544285662"}'  -i
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
        "is_exist": true
    }
