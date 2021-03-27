---
name: 上传文件
---
    
### Url
    /weidu/api/v1/files
    
### Method
    POST

### Content-Type
    application/json    

### Query Param
    "user_id": "用户id，数据类型string"

### Form Param
    "files": "文件路径"    

### 限制
    需要登录带上token，eg: -H "Authorization:Bearer xxxxx" ;测试环境可以不带
    
### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
    	"data": {
        		"file_infos": [{
        		"id": "文件id，数据类型string",
        		"user_id": "用户id，数据类型string",
        		"create_time": "创建时间，unix时间戳单位ms，数据类型int",
        		"update_time": "更新时间，unix时间戳单位ms，数据类型int",
        		"path": "文件路径，数据类型string",
                "preview_path": "预览图路径，数据类型string",
        		"name": "文件名，数据类型string",
        		"extension": "文件后缀，数据类型string",
        		"size": "文件大小，数据类型int",
        		"mime_type": "文件类型，数据类型string",
                "width": "宽度，数据类型int",
                "height": "高度，数据类型int",
                "has_pre_img": "是否有预览图，数据类型bool"
        	}]
        }
    }
    

### Example

     curl -X POST "http://www.weiduchuangzao.com:9004/weidu/api/v1/files?user_id=esbng8qjsfn5jr355ikcr4aajr"  -F "files=@/Users/zhangkunming/Downloads/fabu.jpg" -i
            HTTP/1.1 100 Continue

            HTTP/1.1 201 Created
            Content-Type: application/json; charset=utf-8
            Date: Mon, 08 Feb 2021 07:02:46 GMT
            Content-Length: 519

        {
            "code": 200,
            "data": {
                "file_infos": [{
                    "id": "nna9k8znspbninexatfz34fxga",
                    "user_id": "esbng8qjsfn5jr355ikcr4aajr",
                    "create_time": 1612767766778,
                    "update_time": 1612767766778,
                    "path": "20210208/users/esbng8qjsfn5jr355ikcr4aajr/nna9k8znspbninexatfz34fxga/fabu.jpg",
                    "preview_path": "20210208/users/esbng8qjsfn5jr355ikcr4aajr/nna9k8znspbninexatfz34fxga/fabu_preview.jpg",
                    "name": "fabu.jpg",
                    "extension": "jpg",
                    "size": 13237,
                    "mime_type": "image/jpeg",
                    "width": 500,
                    "height": 375,
                    "has_pre_img": true
                }],
                "client_ids": []
            },
            "result": "ok"
        }