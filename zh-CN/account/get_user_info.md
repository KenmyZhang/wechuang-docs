---
name: 查询个人信息
---
    
### Url
    /weidu/api/v1/users/info"
    
### Method
    GET

### Content-Type
    application/json    

### Query Param
        	"user_id": "用户id，数据类型string"

### 限制
    需要登录带上token，eg: -H "Authorization:Bearer xxxxx" ;测试环境可以不带
    
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
            "mobile": "电话号码，若手机验证过，该字段返回打码后的字符串，否则不返回该字段，数据类型string",
            "email": "邮箱号码，若手机验证过，该字段返回打码后的字符串，否则不返回该字段，数据类型string",
            "last_password_update": "最后更新密码时间，unix时间戳单位s，数据类型int"
        }
    }
    

### Example

    curl -X GET "http://129.28.198.139:9004/weidu/api/v1/users/info?user_id=erb4krcbbirbtcwnhwopeizz5o" -i 
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Tue, 06 Oct 2020 06:36:40 GMT
        Content-Length: 500

    {
    	"code": 200,
    	"result": "ok",
    	"user_info": {
    		"id": "erb4krcbbirbtcwnhwopeizz5o",
    		"create_at": 1601965101771,
    		"update_at": 1601965101771,
    		"username": "z3133549872957399",
    		"password": "$2a$10$yGAm72GzG3nITRIMfpv3buCNPzqcEKexesKZbqSBm6wqcDMObgq8K",
    		"mobile": "13544285662",
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