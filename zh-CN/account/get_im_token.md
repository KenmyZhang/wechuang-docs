---
name: 获取im token
---

### Url
    /weidu/api/v1/users/im/token

### Method
    GET

### Content-Type
    application/json    

### Query Param

### 限制
    需要登录带上token，eg: -H "Authorization:Bearer xxxxx"

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
         "data": {
            "token": "7b7771f6daba46c79f48df51676c2995",
            "accid": "ow4rxntfgbetifiaoxoza8w53e"
        }
    }


### Example

    curl -X GET "http://0:9004/weidu/api/v1/users/im/token" -i -H "Authorization:Bearer 7zf1u19ta7atxj193xhuz3exkw"
        HTTP/1.1 200 OK
        Content-Type: application/json
        Expires: 0
        Date: Thu, 03 Jun 2021 12:00:24 GMT
        Content-Length: 147

    {
        "code": 200,
        "data": {
            "token": "7b7771f6daba46c79f48df51676c2995",
            "accid": "ow4rxntfgbetifiaoxoza8w53e",
            "name": "",
            "icon": "",
            "gender": 0
        },
        "result": "ok"
    }