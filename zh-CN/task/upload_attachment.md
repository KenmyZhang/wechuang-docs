---
name: 上传附件到任务中
---

### Url
     /weidu/api/v1/files
    
### Method
    POST

### Content-Type
    application/json    

### Query Param
    "user_id": "用户id，数据类型string"
    "task_id": "任务id，数据类型string"

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
            "task_id": "文件id，数据类型string",
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
### Response Code
    HTTP/1.1 200 OK

### Example

        curl -X POST "http://127.0.0.1:9004/weidu/api/v1/files?user_id=b1onnbw3ebbjtenaco9fxa16ke&task_id=bnk7w8bhg7br5jp8xuep1to4se" -F "files=@/Users/zhangkunming/Downloads/fabu.jpg" -i
HTTP/1.1 100 Continue

            HTTP/1.1 201 Created
            Content-Type: application/json; charset=utf-8
            Date: Wed, 03 Feb 2021 12:04:53 GMT
            Content-Length: 609

        {
            "code": 200,
            "data": {
                "file_infos": [{
                    "id": "apqbhonw8p8h7k1zueakcre14w",
                    "task_id": "bnk7w8bhg7br5jp8xuep1to4se",
                    "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
                    "create_time": 1612353893174,
                    "update_time": 1612353893174,
                    "path": "20210203/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/apqbhonw8p8h7k1zueakcre14w/fabu.jpg",
                    "preview_path": "20210203/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/apqbhonw8p8h7k1zueakcre14w/fabu_preview.jpg",
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