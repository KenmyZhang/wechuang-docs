---
name: 更新头像
---
    
### Url
    /weidu/api/v1/users/avatar
    
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

        curl -X PUT "http://0:9004/weidu/api/v1/users/avatar" -i -H "User-Id:esbng8qjsfn5jr355ikcr4aajr" -d '{"avatar_file_id":"nna9k8znspbninexatfz34fxga"}' 
            HTTP/1.1 200 OK
            Content-Type: application/json; charset=utf-8
            Date: Mon, 08 Feb 2021 07:14:48 GMT
            Content-Length: 692

        {
            "code": 200,
            "result": "ok",
            "user": {
                "id": "esbng8qjsfn5jr355ikcr4aajr",
                "create_at": 1612355036879,
                "update_at": 1612355036879,
                "username": "1356941491057987584",
                "mobile": "******",
                "real_name_verified": false,
                "nickname": "",
                "avatar_url": "20210208/users/esbng8qjsfn5jr355ikcr4aajr/nna9k8znspbninexatfz34fxga/fabu.jpg",
                "award_info": "",
                "city": "",
                "province": "",
                "country": "",
                "gender": 0,
                "roles": "general_user",
                "description": "2221æè¿°",
                "major": "",
                "level": "",
                "skill": "",
                "refund_rate": 0,
                "dispute_rate": 0,
                "serve_num": 0,
                "work_num": 0,
                "label": "222 kfc",
                "transaction_amount": 0,
                "transaction_praise_cnt": 0,
                "last_password_update": 0
            }
        }