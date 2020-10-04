---
name: 发送手机验证码
---
    
### Url
    /weidu/api/v1/users/mobile/sms
    
### Method
    POST

### Content-Type
    application/json    

### Request Payload
    {
        "mobile":"手机号码，数据类型string, 必填",
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
    curl -X POST  "http://0:9004/weidu/api/v1/users/mobile/sms"  -d '{"mobile":"13544285662", "captcha_token":"xxxxxxxx"}'   -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Sun, 04 Oct 2020 08:27:42 GMT
        Content-Length: 27

    {
        "code":200,
        "result":"ok"
    }

 ### 备注
    测试环境并未开启发送验证码，可以直接使用验证码 068168 进行校验   


