---
name: 总监平台任务列表(B)
---
    
### Url
    /weidu/api/v1/task/director/list
    
### Method
    GET

### Content-Type
    application/json

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": [
            {
                "task":{
                    "id": "订单号，数据类型int",
                    "creator_id": "创建者id，数据类型int",
                    "industry":"行业,数据类型int",
                    "abstract":"摘要 概要 ，数据类型string",
                    "desc": "具体需求描述，数据类型string",
                    "status": "任务状态，数据类型int",
                    "sub_status": "任务子状态，数据类型int", //1 设计中、 2审核中、 3已完成、4合格
                    "start_time": "开始时间，数据类型int",
                    "end_time": "结束时间，数据类型int",
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
                },
                "user_info":{
                    "user_id": "用户id，数据类型string",
                    "avatar": "用户头像，数据类型string"
                }
            }
        ]
    }

### Response Code
    HTTP/1.1 200 OK

### Example

    curl -X GET "http://0:9004/weidu/api/v1/task/director/list" -i -H "Authorization:Bearer fkab1e9nz7a63xr6reacwxp6pw"
        HTTP/1.1 201 Created
        Content-Type: application/json
        Expires: 0
        Date: Thu, 27 May 2021 13:00:43 GMT
        Transfer-Encoding: chunked

    {
        "code":200,
        "data":[
            {
                "task":{
                    "id":"5trb5tu7tj8kfe7gwk7qakfpac",
                    "creator_id":"szasc68seig9jrhqw4eaj9gu3h",
                    "industry":1,
                    "type":1,
                    "style":1,
                    "hire":1,
                    "abstract":"摘要 概要",
                    "desc":"具体需求描述",
                    "status":1,
                    "sub_status":0,
                    "transaction_mode":1,
                    "price":1000,
                    "min_price":1000,
                    "max_price":2000,
                    "start_time":1602129479000,
                    "end_time":1602139479000,
                    "is_top":true,
                    "priority":true,
                    "block_search":true,
                    "copyright_guard":true,
                    "create_time":0,
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
                "user_info":{
                    "user_id":"szasc68seig9jrhqw4eaj9gu3h",
                    "avatar":"20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                    "real_name_auth":true,
                    "sesame_auth":true,
                    "enterprise_auth":false
                }
            },
            {
                "task":{
                    "id":"w84sa8jaapnb5nixq5s6saeash",
                    "creator_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "industry":2,
                    "type":8,
                    "style":2,
                    "hire":1,
                    "abstract":"供应链金融平台原型设计",
                    "desc":"一、需求描述：
    类别：供应链金融平台原型设计
    进度：已经有原型图。
    功能：一个服务小微企业和核心企业的供应链金融平台的原型；您能否提供一个总的设计原则和一两个页面的示例给我们看下？
    技术：UI设计软件，Sketch

    二、人才要求：
    4年以上UI设计经验，金融产品设计经验。

    三、合作方式：
    开发方式：UI设计。
    设计周期：3天",
                    "status":1,
                    "sub_status":0,
                    "transaction_mode":2,
                    "price":0,
                    "min_price":1000,
                    "max_price":20000,
                    "start_time":1621440000000,
                    "end_time":1686067200000,
                    "is_top":true,
                    "priority":true,
                    "block_search":true,
                    "copyright_guard":true,
                    "create_time":0
                },
                "user_info":{
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "avatar":"20210507/users/b1onnbw3ebbjtenaco9fxa16ke/3xr7669ea7nhjpewtskhoxz8ja/1.png",
                    "real_name_auth":true,
                    "sesame_auth":false,
                    "enterprise_auth":true
                }
            }
        ],
        "result":"ok"
    }