---
name: 案例和设计师推广
---
    
### Url
     /weidu/api/v1/cases/list
    
### Method
    GET

### Content-Type
    application/json

### Query Param
    case_type: 案例 1、设计师推广 2

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": [{
            "user_id": "用户ID，数据类型int",
            "username": "用户名，数据类型string",
            "label": "标签，多个标签空格分隔，数据类型string",
            "desc": "个人简介,数据类型string",
            "task_id": "任务ID.数据类型string",
            "files": [{
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
    		    "mime_type": "文件类型，数据类型string"
                "width": "宽度，数据类型int",
                "height": "高度，数据类型int",
                "has_pre_img": "是否有预览图，数据类型bool"
            }]
        }
    }
    
### Response Code
    HTTP/1.1 200 OK

### Example
    
    curl -X GET "http://0:9004/weidu/api/v1/cases/list?case_type=1" -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Wed, 03 Feb 2021 12:35:45 GMT
        Content-Length: 1152

    {
        "code": 200,
        "data": [{
            "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
            "username": "1356932923411927040",
            "label": "985 211 ä¸–ç•Œäº”ç™¾å¼º",
            "desc": "æè¿°",
            "task_id": "bnk7w8bhg7br5jp8xuep1to4se",
            "files": [{
                "id": "9epzckzagtau7qgtnexuxae4ba",
                "task_id": "bnk7w8bhg7br5jp8xuep1to4se",
                "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
                "create_time": 1612353695782,
                "update_time": 1612353695782,
                "path": "20210203/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/9epzckzagtau7qgtnexuxae4ba/fabu.jpg",
                "preview_path": "20210203/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/9epzckzagtau7qgtnexuxae4ba/fabu_preview.jpg",
                "name": "fabu.jpg",
                "extension": "jpg",
                "size": 13237,
                "mime_type": "image/jpeg",
                "width": 500,
                "height": 375,
                "has_pre_img": true
            }, {
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
            }, {
                "id": "k9qptarhiifenginc1s1igu86e",
                "task_id": "bnk7w8bhg7br5jp8xuep1to4se",
                "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
                "create_time": 1612353350568,
                "update_time": 1612353350568,
                "path": "20210203/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/k9qptarhiifenginc1s1igu86e/svc.png",
                "preview_path": "20210203/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/k9qptarhiifenginc1s1igu86e/svc_preview.jpg",
                "name": "svc.png",
                "extension": "png",
                "size": 272655,
                "mime_type": "image/png",
                "width": 2368,
                "height": 1338,
                "has_pre_img": true
            }]
        }, {
            "user_id": "bjg5k3er6inf8ce16onhnhb8we",
            "username": "1356941446602559488",
            "label": "666 kfc",
            "desc": "5621æè¿°",
            "task_id": "x6xnpntqb3n58n6445wnzjg94h",
            "files": [{
                "id": "aa9jz17gapr17psnatuf4p5toa",
                "task_id": "x6xnpntqb3n58n6445wnzjg94h",
                "user_id": "bjg5k3er6inf8ce16onhnhb8we",
                "create_time": 1612356195074,
                "update_time": 1612356195074,
                "path": "20210203/task/x6xnpntqb3n58n6445wnzjg94h/users/bjg5k3er6inf8ce16onhnhb8we/aa9jz17gapr17psnatuf4p5toa/zhizuo.jpeg",
                "preview_path": "20210203/task/x6xnpntqb3n58n6445wnzjg94h/users/bjg5k3er6inf8ce16onhnhb8we/aa9jz17gapr17psnatuf4p5toa/zhizuo_preview.jpg",
                "name": "zhizuo.jpeg",
                "extension": "jpeg",
                "size": 29608,
                "mime_type": "image/jpeg",
                "width": 700,
                "height": 483,
                "has_pre_img": true
            }]
        }],
        "result": "ok"
    }