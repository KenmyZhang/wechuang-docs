---
name: 手机号注册
---
    
### Url
    /weidu/api/v1/users/mobile/signup
    
### Method
    POST

### Content-Type
    application/json    

### Request Payload
    {
        "mobile":"手机号号，数据类型string, 必填",
        "sms_code": "验证码，数据类型string,必填",
        "passwd": "密码，数据类型string,必填",
        "captcha_token":"行为验证token，数据类型string，必填",
        "device_model": "设备型号,数据类型string，目前可以选填，后期做了安全加固后必填",
        "device_name": "设备名称，数据类型string，目前可以选填，后期做了安全加固后必填",
        "timestamp": "发送验证码时间，unix时间戳单位s，数据类型int，目前可以选填后期做了安全加固后必填",
        "device_id": "设备id，数据类型string，目前可以选填，后期做了安全加固后必填",
        "device_sign": "设置标识，由app_name、business_type、deviceid经md5、hash构成, 数据类型string，目前可以选填，后期做了安全加固后必填"
    }
    
### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int"
    }
    

### Example
    curl -X POST  "http://129.28.198.139:8089/weidu/api/v1/users/mobile/signup"  -d '{"mobile":"13544285662", "sms_code": "xxxxxx", "captcha_token":"xxxxxx",  "passwd":"xxx"}'   -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Token: n5fknzz7of8n9xkqneshjs89na
        Date: Fri, 03 xxx xxxx 11:27:59 GMT
        Content-Length: 295

    {
        "result":"ok",
        "code": 200
    }




