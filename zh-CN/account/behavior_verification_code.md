---
name: 行为验证码校验
---
    
### Url
     /weidu/api/v1/users/behavior/verification
    
### Method
    POST

### Content-Type
    application/json      

### Request Payload
    {
        "captcha_id": "行为验证码id，数据类型string，必填",
    }

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "captcha_token":"行为验证token，数据类型string"
    }
    
### Response Code
    HTTP/1.1 200 OK

### Example
     curl -X POST "http://129.28.198.139:8089/weidu/api/v1/users/behavior/verification" -d '{"captcha_id":"xxxx"}'  -i
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
        "captcha_token":"xxx"
    }
