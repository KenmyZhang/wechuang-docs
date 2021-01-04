---
name: 账号密码登录(手机号)
---
    
### Url
    /weidu/api/v1/users/login
    
### Method
    POST

### Content-Type
    application/json    

### Request Payload
    {
        "login_id":"账号（手机号/邮箱号），数据类型string, 必填",
        "password": "密码，数据类型string,必填",
        
        "captcha_token":"行为验证token，数据类型string，选填，仅在帐号存在异常的情况下才需要",
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
        	"id": "用户id，数据类型string",
        	"create_at": "创建时间,unix时间戳单位s，数据类型int",
        	"update_at": "更新时间,unix时间戳单位s，数据类型int",
        	"username": "账号名，数据类型string",
            "real_name_verified": "实名认证，数据类型bool",
        	"nickname": "账号昵称，数据类型string",
        	"avatar_url": "头像，数据类型string",
        	"city": "城市，数据类型string",
        	"province": "省份，数据类型string",
        	"country": "国家，数据类型string",
        	"gender": "性别，数据类型string",
            "roles": "角色，数据类型string",
            "desc": "个人简介，数据类型string",
            "level": "等级，数据类型string",
            "major": "主营，数据类型string",
            "refund_rate": "退款率，数据类型float",
            "dispute_rate": "纠纷率，数据类型float",
            "serve_num": "服务数量，数据类型int",
        	"work_num": "作品数,数据类型int",
            "last_password_update": "最后更新密码时间，unix时间戳单位s，数据类型int"
        }
    }
    

### Example
    curl -X POST  "http://129.28.198.139:9004/weidu/api/v1/users/login"  -d '{"login_id":"13544285663", "password": "Zk12345678", "captcha_token":"xxxxxx"}'   -i
            HTTP/1.1 200 OK
            Content-Type: application/json; charset=utf-8
            Set-Cookie: weichuangAUTHTOKEN=3r6ebp6gabf6unbee35eu8u6bo; Path=/; Domain=0.0.0.0; Expires=Sun, 04 Oct 2020 09:19:55 GMT; HttpOnly
            Set-Cookie: weichuangUSERID=7s75e5gin7r9ianisq7ic13pno; Path=/; Domain=0.0.0.0; Expires=Sun, 04 Oct 2020 09:19:55 GMT
            Set-Cookie: weichuangCSRF=8q7tskhertbqfb74znhhzanpra; Path=/; Domain=0.0.0.0; Expires=Sun, 04 Oct 2020 09:19:55 GMT
            Token: 3r6ebp6gabf6unbee35eu8u6bo
            Date: Sun, 04 Oct 2020 09:19:56 GMT
            Content-Length: 400

        {
        	"code": 200,
        	"result": "ok",
        	"user_info": {
        		"id": "7wnaasfa47bebbtjbazajef3eh",
        		"create_at": 1601963204584,
        		"update_at": 1601963204584,
        		"username": "1313354987295739904",
        		"mobile": "******",
        		"real_name_verified": false,
        		"nickname": "",
        		"avatar_url": "",
        		"city": "",
        		"province": "",
        		"country": "",
        		"gender": 0,
        		"roles": "general_user",
        		"desc": "",
        		"major": "",
        		"level": "",
        		"refund_rate": 0,
        		"dispute_rate": 0,
        		"serve_num": 0,
        		"work_num": 0,
        		"last_password_update": 0
        	}
        }
         







