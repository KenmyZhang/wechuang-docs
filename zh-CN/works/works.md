---
name: 个人作品列表
---
    
### Url
    /weidu/api/v1/files/me
    
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
    	"data": [{
    		"id": "文件id，数据类型string",
    		"user_id": "用户id，数据类型string",
    		"create_time": "创建时间，unix时间戳单位ms，数据类型int",
    		"update_time": "更新时间，unix时间戳单位ms，数据类型int",
    		"path": "文件路径，数据类型string",
            "preview_path": "预览图路径，数据类型string",
    		"name": "文件名，数据类型string",
    		"extension": "文件后缀，数据类型string",
    		"size": "文件大小，数据类型int",
    		"mime_type": "文件类型，数据类型string"
    	}
    }
    

### Example

    curl -X GET "http://129.28.198.139:9004/weidu/api/v1/files/me?user_id=erb4krcbbirbtcwnhwopeizz5o" -i

        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Tue, 06 Oct 2020 12:09:24 GMT
        Content-Length: 1311

    {
    	"code": 200,
    	"data": [{
    		"id": "ruhiuq4o7pn3ffi7xbhnghbnho",
    		"user_id": "erb4krcbbirbtcwnhwopeizz5o",
    		"create_time": 1601811849680,
    		"update_time": 1601811849680,
    		"path": "20201004/users/123/ruhiuq4o7pn3ffi7xbhnghbnho/README.md",
            "preview_path": "preview/path/0000",
    		"name": "README.md",
    		"extension": "md",
    		"size": 1270,
    		"mime_type": ""
    	}, {
    		"id": "wfinhatigjngfaaenwg6jsa63c",
    		"user_id": "erb4krcbbirbtcwnhwopeizz5o",
    		"create_time": 1601812208486,
    		"update_time": 1601812208486,
    		"path": "20201004/users/123/wfinhatigjngfaaenwg6jsa63c/fabu.jpg",
            "preview_path": "preview/path/0001",
    		"name": "fabu.jpg",
    		"extension": "jpg",
    		"size": 13237,
    		"mime_type": "image/jpeg",
    		"width": 500,
    		"height": 375,
    		"has_pre_img": true
    	}, {
    		"id": "biinjhnesifeiasftws8a6q95r",
    		"user_id": "erb4krcbbirbtcwnhwopeizz5o",
    		"create_time": 1601812213793,
    		"update_time": 1601812213793,
    		"path": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
            "preview_path": "preview/path/0002",
    		"name": "jianzhi.jpg",
    		"extension": "jpg",
    		"size": 34348,
    		"mime_type": "image/jpeg",
    		"width": 500,
    		"height": 333,
    		"has_pre_img": true
    	}, {
    		"id": "p75zea7ze3n8z8rw4tkrrhjfwh",
    		"user_id": "erb4krcbbirbtcwnhwopeizz5o",
    		"create_time": 1601812244337,
    		"update_time": 1601812244337,
    		"path": "20201004/users/123/p75zea7ze3n8z8rw4tkrrhjfwh/zhizuo.jpeg",
            "preview_path": "preview/path/0006",
    		"name": "zhizuo.jpeg",
    		"extension": "jpeg",
    		"size": 29608,
    		"mime_type": "image/jpeg",
    		"width": 700,
    		"height": 483,
    		"has_pre_img": true
    	}],
    	"result": "ok"
    }
    