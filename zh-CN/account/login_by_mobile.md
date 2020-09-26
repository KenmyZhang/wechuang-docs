---
name: 手机验证码登录
---
    
### Url
    /weidu/api/v1/users/mobile/login
    
### Method
    POST

### Content-Type
    application/json    

### Request Payload
    {
        "login_id":"手机号号，数据类型string, 必填",
        "sms_code": "验证码，数据类型string,必填",
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
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "user_info": {
        	"id": "用户id，数据类型int",
        	"create_at": "创建时间,unix时间戳单位s，数据类型int",
        	"update_at": "更新时间,unix时间戳单位s，数据类型int",
        	"username": "账号名，数据类型string",
        	"nickname": "账号昵称，数据类型string",
        	"avatar_url": "头像，数据类型string",
        	"city": "城市，数据类型string",
        	"province": "省份，数据类型string",
        	"country": "国家，数据类型string",
        	"gender": "性别，数据类型string",
            "level": "等级，数据类型string",
            "major": "主营，数据类型string",
            "desc": "个人简介，数据类型string",
            "refund_rate": "退款率，数据类型float",
            "dispute_rate": "纠纷率，数据类型float",
        	"roles": "角色，数据类型string",
            "mobile": "手机号码，数据类型string",
            "email": "邮箱号码，数据类型string"
            "real_name_verified": "实名认证，数据类型bool"
        }
    }
    

### Example
    curl -X POST  "http://129.28.198.139:8089/weidu/api/v1/users/mobile/login"  -d '{"login_id":"13544285662", "sms_code": "xxxxxx", "captcha_token":"xxxxxx"}'   -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Set-Cookie: WOLVESAUTHTOKEN=n5fknzz7of8n9xkqneshjs89na; Path=/; Domain=129.28.198.139; Expires=xxx, 03 Jan xxx 11:27:59 GMT; HttpOnly
        Set-Cookie: WOLVESUSERID=4ewj68ux5j8njnshpxraxjuaaa; Path=/; Domain=129.28.198.139; Expires=xxx, 03 Jan xxx 11:27:59 GMT
        Set-Cookie: WOLVESCSRF=z46keasgcte3pnxwznk81pnk5w; Path=/; Domain=129.28.198.139; Expires=xxx, 03 Jan xxx 11:27:59 GMT
        Token: n5fknzz7of8n9xkqneshjs89na
        Date: Fri, 03 xxx xxxx 11:27:59 GMT
        Content-Length: 295

    {
        "result":"ok",
        "code": 200,
        "user_info": {
        	"id": 8970,
        	"create_at": 1578050603718,
        	"update_at": 1578050603718,
        	"username": "hello_ken",
        	"nickname": "呵呵哒,
        	"avatar_url": "http://xxxxxxx",
        	"city": "深圳",
        	"province": "广东",
        	"country": "中国",
        	"gender": "男",
            "level": "等级xx",
            "major": "主营xx",
            "desc": "个人简介",
            "refund_rate": 0.0,
            "dispute_rate": 0.0,
        	"roles": "user",
            "mobile": "13544285662",
            "email": "13544285662@163.com"
            "real_name_verified": true
        }
        
    }




