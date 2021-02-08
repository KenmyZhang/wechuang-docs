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
        "data": [{
            "user_id": "用户ID，数据类型int",
            "username": "用户名，数据类型string",
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

    curl -X GET "http://0:9004/weidu/api/v1/cases/list?industry_type=1&per_page=5" -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Mon, 08 Feb 2021 09:36:43 GMT
        Transfer-Encoding: chunked
    {
        "code": 200,
        "data": [{
            "user_id": "szasc68seig9jrhqw4eaj9gu3h",
            "username": "1356941364390006784",
            "update_time": 1612355363209,
            "view_cnt": 6,
            "like_cnt": 3,
            "comment_cnt": 2,
            "score": 90,
            "task_id": "5trb5tu7tj8kfe7gwk7qakfpac",
            "files": [{
                "id": "kspnaeba8tr37jit7s5ingnnwr",
                "task_id": "5trb5tu7tj8kfe7gwk7qakfpac",
                "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                "create_time": 1612355738709,
                "update_time": 1612355738709,
                "path": "20210203/task/5trb5tu7tj8kfe7gwk7qakfpac/users/szasc68seig9jrhqw4eaj9gu3h/kspnaeba8tr37jit7s5ingnnwr/fabu.jpg",
                "preview_path": "20210203/task/5trb5tu7tj8kfe7gwk7qakfpac/users/szasc68seig9jrhqw4eaj9gu3h/kspnaeba8tr37jit7s5ingnnwr/fabu_preview.jpg",
                "name": "fabu.jpg",
                "extension": "jpg",
                "size": 13237,
                "mime_type": "image/jpeg",
                "width": 500,
                "height": 375,
                "has_pre_img": true
            }]
        }, {
            "user_id": "esbng8qjsfn5jr355ikcr4aajr",
            "username": "1356941491057987584",
            "update_time": 1612355345317,
            "view_cnt": 0,
            "like_cnt": 0,
            "comment_cnt": 0,
            "score": 90,
            "task_id": "ofargqanbpeeinswoigjae9rpe",
            "files": [{
                "id": "eft1p6e73benbpxs6urnxetnkc",
                "task_id": "ofargqanbpeeinswoigjae9rpe",
                "user_id": "esbng8qjsfn5jr355ikcr4aajr",
                "create_time": 1612356636623,
                "update_time": 1612356636623,
                "path": "20210203/task/ofargqanbpeeinswoigjae9rpe/users/esbng8qjsfn5jr355ikcr4aajr/eft1p6e73benbpxs6urnxetnkc/timg.jpeg",
                "preview_path": "20210203/task/ofargqanbpeeinswoigjae9rpe/users/esbng8qjsfn5jr355ikcr4aajr/eft1p6e73benbpxs6urnxetnkc/timg_preview.jpg",
                "name": "timg.jpeg",
                "extension": "jpeg",
                "size": 403482,
                "mime_type": "image/jpeg",
                "width": 800,
                "height": 1084,
                "has_pre_img": true
            }]
        }, {
            "user_id": "bjg5k3er6inf8ce16onhnhb8we",
            "username": "1356941446602559488",
            "update_time": 1612355259349,
            "view_cnt": 0,
            "like_cnt": 0,
            "comment_cnt": 0,
            "score": 90,
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
        }, {
            "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
            "username": "1356932923411927040",
            "update_time": 1612348073840,
            "view_cnt": 1,
            "like_cnt": 0,
            "comment_cnt": 1,
            "score": 90,
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
            }]
        }],
        "result": "ok",
        "total": 4
    }