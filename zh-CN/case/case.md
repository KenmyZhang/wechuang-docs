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
|   品牌设计|     1 |
|   影视 |      2 |
|   企业网站建设|      3 |
|   动漫设计 |     4   |
|    游戏|     5   |
|   特效|      6 |


### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "total": "案例总数，数据类型int",
        "data": [{
            "user_id": "用户ID，数据类型int",
            "username": "用户名，数据类型string",
            "avatar_url": "用户头像，数据类型string",
            "update_time": "更新时间，数据类型int",,
            "view_cnt": "浏览数,数据类型int",
            "comment_cnt": "评论数,数据类型int",
            "like_cnt": "点赞数,数据类型int",
            "score": "案例评分.数据类型float",
            "task_id": "案例id,实际对应任务id.数据类型int",
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

        curl -X GET "http://129.28.198.139:9004/weidu/api/v1/cases/list?industry_type=1&per_page=5"

        {
            "code": 200,
            "data": [
                {
                    "avatar_url": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                    "comment_cnt": 2,
                    "files": [
                        {
                            "extension": "jpg",
                            "has_pre_img": true,
                            "height": 333,
                            "id": "biinjhnesifeiasftws8a6q95r",
                            "mime_type": "image/jpeg",
                            "name": "jianzhi.jpg",
                            "path": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                            "preview_path": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi_preview.jpg",
                            "size": 34348,
                            "task_id": "5trb5tu7tj8kfe7gwk7qakfpac",
                            "user_id": "erb4krcbbirbtcwnhwopeizz5o",
                            "width": 500
                        }
                    ],
                    "like_cnt": 3,
                    "score": 90,
                    "task_id": "5trb5tu7tj8kfe7gwk7qakfpac",
                    "update_time": 1612355363209,
                    "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                    "username": "a1356937040",
                    "view_cnt": 6
                },
                {
                    "avatar_url": "20210208/users/esbng8qjsfn5jr355ikcr4aajr/nna9k8znspbninexatfz34fxga/fabu.jpg",
                    "comment_cnt": 0,
                    "files": [
                        {
                            "extension": "jpeg",
                            "has_pre_img": true,
                            "height": 483,
                            "id": "1aeeoqnw3tgb3bjwnwp3fi9eha",
                            "mime_type": "image/jpeg",
                            "name": "zhizuo.jpeg",
                            "path": "20210301/task/ofargqanbpeeinswoigjae9rpe/users/esbng8qjsfn5jr355ikcr4aajr/1aeeoqnw3tgb3bjwnwp3fi9eha/zhizuo.jpeg",
                            "preview_path": "20210301/task/ofargqanbpeeinswoigjae9rpe/users/esbng8qjsfn5jr355ikcr4aajr/1aeeoqnw3tgb3bjwnwp3fi9eha/zhizuo_preview.jpg",
                            "size": 29608,
                            "task_id": "ofargqanbpeeinswoigjae9rpe",
                            "user_id": "esbng8qjsfn5jr355ikcr4aajr",
                            "width": 700
                        }
                    ],
                    "like_cnt": 0,
                    "score": 90,
                    "task_id": "ofargqanbpeeinswoigjae9rpe",
                    "update_time": 1612355345317,
                    "user_id": "esbng8qjsfn5jr355ikcr4aajr",
                    "username": "1356941491057987584",
                    "view_cnt": 0
                },
                {
                    "avatar_url": "20210208/users/bjg5k3er6inf8ce16onhnhb8we/nikjo4waktreiban6fn9aeib5o/zhizuo.jpeg",
                    "comment_cnt": 0,
                    "files": [
                        {
                            "extension": "jpeg",
                            "has_pre_img": true,
                            "height": 1084,
                            "id": "kh8whusa4jr1neg3q93o619taa",
                            "mime_type": "image/jpeg",
                            "name": "timg.jpeg",
                            "path": "20210301/task/x6xnpntqb3n58n6445wnzjg94h/users/bjg5k3er6inf8ce16onhnhb8we/kh8whusa4jr1neg3q93o619taa/timg.jpeg",
                            "preview_path": "20210301/task/x6xnpntqb3n58n6445wnzjg94h/users/bjg5k3er6inf8ce16onhnhb8we/kh8whusa4jr1neg3q93o619taa/timg_preview.jpg",
                            "size": 403482,
                            "task_id": "x6xnpntqb3n58n6445wnzjg94h",
                            "user_id": "bjg5k3er6inf8ce16onhnhb8we",
                            "width": 800
                        }
                    ],
                    "like_cnt": 0,
                    "score": 90,
                    "task_id": "x6xnpntqb3n58n6445wnzjg94h",
                    "update_time": 1612355259349,
                    "user_id": "bjg5k3er6inf8ce16onhnhb8we",
                    "username": "1356941446602559488",
                    "view_cnt": 0
                },
                {
                    "avatar_url": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                    "comment_cnt": 1,
                    "files": [
                        {
                            "extension": "jpg",
                            "has_pre_img": true,
                            "height": 375,
                            "id": "69fq4iqbcjn8pcrpbabwuei4uo",
                            "mime_type": "image/jpeg",
                            "name": "fabu.jpg",
                            "path": "20210301/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/69fq4iqbcjn8pcrpbabwuei4uo/fabu.jpg",
                            "preview_path": "20210301/task/bnk7w8bhg7br5jp8xuep1to4se/users/b1onnbw3ebbjtenaco9fxa16ke/69fq4iqbcjn8pcrpbabwuei4uo/fabu_preview.jpg",
                            "size": 13237,
                            "task_id": "bnk7w8bhg7br5jp8xuep1to4se",
                            "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
                            "width": 500
                        }
                    ],
                    "like_cnt": 0,
                    "score": 90,
                    "task_id": "bnk7w8bhg7br5jp8xuep1to4se",
                    "update_time": 1612348073840,
                    "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
                    "username": "a1356932923411927040",
                    "view_cnt": 1
                }
            ],
            "result": "ok",
            "total": 4
        }