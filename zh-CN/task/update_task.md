---
name: 更新任务
---
    
### Url
     /weidu/api/v1/task/update
    
### Method
    POST

### Content-Type
    application/json      

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"



### Requst Body

    {
        "id": "任务id，数据类型int",
        "desc": "具体需求描述，数据类型string，必填",
        "abstract":"摘要 概要，数据类型string，必填"
    }

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": {
             "id": "任务id，数据类型int",
             "creator_id": "创建者id，数据类型string",
             "industry":"行业,数据类型int",
             "type":"任务类型,数据类型int",
             "style":"风格,数据类型int",
             "hire":"雇佣, 数据类型int",
             "abstract":"摘要 概要，数据类型string",
             "desc": "具体需求描述，数据类型string",
             "attachments": "附件id列表，多个附件用逗号分割，数据类型string",
             "status": "任务状态，数据类型int",
             "transaction_mode":"交易模式，数据类型int"
             "min_price": "价格范围最小值，数据类型int",
             "max_price": "价格范围最大值，数据类型int",
             "start_time": "开始时间，数据类型int",
             "end_time": "结束时间，数据类型int",
             "is_top": "是否置顶，数据类型bool",
             "priority": "是否加急优先，数据类型bool",
             "block_search": "是否屏蔽搜索，数据类型bool",
             "copyright_guard": "版权卫士，数据类型bool",
             "agree_protocol": "同意协议，数据类型bool",
             "requirements": "参与要求，数据类型string",
             "update_time":"更新时间，数据类型int",
             "create_time": "创建时间，数据类型int"
        } 
    }

### Response Code
    HTTP/1.1 200 OK

### Example

        curl -X POST "http://127.0.0.1:9004/weidu/api/v1/task/update" -i -d '{"id":"be5scu8qjp8n3bszsnn5eeeabc", "desc":"update desc","abstract":"title"}' -H "Authorization:Bearer 9qjpnee5n3g7xqb449n9b7je7a"


            HTTP/1.1 201 Created
            Content-Type: application/json
            Date: Sun, 04 Jul 2021 11:18:10 GMT
            Content-Length: 535


        {
            "code":200,
            "data":{
                "id":"be5scu8qjp8n3bszsnn5eeeabc",
                "creator_id":"cj9uqiaarjb67e5tiu1ak4b5kc",
                "industry":1,
                "type":1,
                "style":1,
                "hire":2,
                "abstract":"title",
                "desc":"update desc",
                "attachments":"",
                "status":1,
                "group_id":"",
                "transaction_mode":1,
                "price":0,
                "min_price":2000,
                "max_price":30000,
                "start_time":1626883200000,
                "end_time":1628697600000,
                "score":0,
                "is_top":true,
                "priority":false,
                "block_search":false,
                "copyright_guard":false,
                "agree_protocol":true,
                "requirements":"",
                "update_time":1625397490133,
                "create_time":1625220961215
            },
            "result":"ok"
        }