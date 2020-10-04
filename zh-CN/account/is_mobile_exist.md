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
         Content-Type: application/json; charset=utf-8
         Date: Sun, 04 Oct 2020 08:12:05 GMT
         Content-Length: 44

    {
        "result": "ok",
        "code": 200,
        "is_exist": true
    }