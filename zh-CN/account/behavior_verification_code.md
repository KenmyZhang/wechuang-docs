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
     curl -X POST "http://129.28.198.139:9004/weidu/api/v1/users/behavior/verification" -i -d '{"captcha_id": "xxx"}' 
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Sun, 04 Oct 2020 07:34:03 GMT
        Content-Length: 72

    {
        "code":200,
        "result":"ok",
        "captcha_token":"n5fknzz7of8n9xkqneshjs89na"
    }
