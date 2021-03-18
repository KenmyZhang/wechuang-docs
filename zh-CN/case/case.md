---
name: 客户案例
---
    
### Url
     /weidu/api/v1/cases/list
    
### Method
    GET

### Content-Type
    application/json

### Query Param
    industry_type: 行业，数据类型int
    per_page: 每页返回记录数，数据类型int
    page: 第几页,数据类型int

| 行业 | 编码 |
|---|---|
|   游戏|     1 |
|   UI/UX |      2 |
|   动漫|      3 |
|   影视 |     4   |
|    产品|     5   |
|   建筑|      6 |


### Response Body

    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "total": "案例总数，数据类型int",
        "data": [{
            "type": "行业类型，数据类型int",
            "user_id": "用户id，数据类型string",
            "nickname": "用户昵称，数据类型string",
            "abstract": "一句话摘要，包括标题和详情，数据类型string",
            "title": "头衔,数据类型int",
            "min_price": "价格范围最小值,数据类型int",
            "max_price": "价格范围最大值,数据类型int",
            "score": "案例评分.数据类型float",
            "task_id": "案例id,实际对应任务id.数据类型int",
            "files": [{
                "id": "文件id，数据类型string",
                "task_id": "文件id，数据类型string",
    		    "user_id": "上传文件的用户id，数据类型string",
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

        curl -X GET "http://weiduchuangzao.com:9004/weidu/api/v1/cases/list?industry_type=1&per_page=5" -i
            HTTP/1.1 200 OK
            Content-Type: application/json; charset=utf-8
            Date: Thu, 18 Mar 2021 13:55:14 GMT
            Transfer-Encoding: chunked

        {
            "code":200,
            "data":[
                {
                    "type":1,
                    "abstract":"摘要 概要",
                    "user_id":"szasc68seig9jrhqw4eaj9gu3h",
                    "nickname":"1150911",
                    "title":"总监",
                    "score":90,
                    "min_price":1000,
                    "max_price":2000,
                    "task_id":"5trb5tu7tj8kfe7gwk7qakfpac",
                    "files":[
                        {
                            "id":"biinjhnesifeiasftws8a6q95r",
                            "task_id":"5trb5tu7tj8kfe7gwk7qakfpac",
                            "user_id":"erb4krcbbirbtcwnhwopeizz5o",
                            "path":"20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                            "preview_path":"20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi_preview.jpg",
                            "name":"jianzhi.jpg",
                            "extension":"jpg",
                            "size":34348,
                            "mime_type":"image/jpeg",
                            "width":500,
                            "height":333,
                            "has_pre_img":true
                        }
                    ]
                },
                {
                    "type":1,
                    "abstract":"摘要 概要",
                    "user_id":"esbng8qjsfn5jr355ikcr4aajr",
                    "nickname":"",
                    "title":"总监",
                    "score":90,
                    "min_price":1000,
                    "max_price":2000,
                    "task_id":"ofargqanbpeeinswoigjae9rpe",
                    "files":[
                        {
                            "id":"1aeeoqnw3tgb3bjwnwp3fi9eha",
                            "task_id":"ofargqanbpeeinswoigjae9rpe",
                            "user_id":"esbng8qjsfn5jr355ikcr4aajr",
                            "path":"20210301/task/ofargqanbpeeinswoigjae9rpe/users/esbng8qjsfn5jr355ikcr4aajr/1aeeoqnw3tgb3bjwnwp3fi9eha/zhizuo.jpeg",
                            "preview_path":"20210301/task/ofargqanbpeeinswoigjae9rpe/users/esbng8qjsfn5jr355ikcr4aajr/1aeeoqnw3tgb3bjwnwp3fi9eha/zhizuo_preview.jpg",
                            "name":"zhizuo.jpeg",
                            "extension":"jpeg",
                            "size":29608,
                            "mime_type":"image/jpeg",
                            "width":700,
                            "height":483,
                            "has_pre_img":true
                        }
                    ]
                },
                {
                    "type":1,
                    "abstract":"摘要 概要",
                    "user_id":"bjg5k3er6inf8ce16onhnhb8we",
                    "nickname":"1150910",
                    "title":"总监",
                    "score":90,
                    "min_price":1000,
                    "max_price":2000,
                    "task_id":"x6xnpntqb3n58n6445wnzjg94h",
                    "files":[
                        {
                            "id":"kh8whusa4jr1neg3q93o619taa",
                            "task_id":"x6xnpntqb3n58n6445wnzjg94h",
                            "user_id":"bjg5k3er6inf8ce16onhnhb8we",
                            "path":"20210301/task/x6xnpntqb3n58n6445wnzjg94h/users/bjg5k3er6inf8ce16onhnhb8we/kh8whusa4jr1neg3q93o619taa/timg.jpeg",
                            "preview_path":"20210301/task/x6xnpntqb3n58n6445wnzjg94h/users/bjg5k3er6inf8ce16onhnhb8we/kh8whusa4jr1neg3q93o619taa/timg_preview.jpg",
                            "name":"timg.jpeg",
                            "extension":"jpeg",
                            "size":403482,
                            "mime_type":"image/jpeg",
                            "width":800,
                            "height":1084,
                            "has_pre_img":true
                        }
                    ]
                },
                {
                    "type":1,
                    "abstract":"摘要 概要",
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "nickname":"1150909",
                    "title":"总监",
                    "score":90,
                    "min_price":1000,
                    "max_price":2000,
                    "task_id":"bnk7w8bhg7br5jp8xuep1to4se",
                    "files":[
                        {
                            "id":"69fq4iqbcjn8pcrpbabwuei4uo",
                            "task_id":"bnk7w8bhg7br5jp8xuep1to4se",
                            "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                            "path":"20210301/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/69fq4iqbcjn8pcrpbabwuei4uo/fabu.jpg",
                            "preview_path":"20210301/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/69fq4iqbcjn8pcrpbabwuei4uo/fabu_preview.jpg",
                            "name":"fabu.jpg",
                            "extension":"jpg",
                            "size":13237,
                            "mime_type":"image/jpeg",
                            "width":500,
                            "height":375,
                            "has_pre_img":true
                        }
                    ]
                }
            ],
            "result":"ok",
            "total":4
        }