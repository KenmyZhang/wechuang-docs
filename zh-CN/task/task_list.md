---
name: 任务列表
---
    
### Url
     /weidu/api/v1/task/list
    
### Method
    GET

### Content-Type
    application/json      

### Query Param
    industry:行业，数据类型int
    type:类型，数据类型int
    style:风格，数据类型int
    hire:雇佣，数据类型int
    release_time:发布时间，数据类型int
    price:价格，数据类型int
    left_time:剩余时间，数据类型int
    keyword: 关键词,数据类型string



| 行业 | 编码 |
|---|---|
|   游戏|     1 |
|   漫画|      2 |
|   动漫|      3 |
|   创意 |     4   |
|   影视 |     5   |

| 类型 | 编码 |
|---|---|
|   原画|     1 |
|   建模|      2 |
|   动作|      3 |
|   特效 |     4   |
|   界面 |     5   |


| 风格 | 编码 |
|---|---|
|   写实|     1 |
|   卡通|      2 |

| 雇佣模式 | 编码 |
|---|---|
|   团队|     1 |
|   个人|      2 |


| 交易模式 | 编码 |
|---|---|
|   委托模式1|     1 |
|   直聘模式|      2 |


### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": [{
            "task":{
                 "id": "任务id，数据类型int",
                 "creator_id": "创建者id，数据类型int",
                 "industry":"行业,数据类型int",
                 "type":"任务类型,数据类型int",
                 "style":"风格,数据类型int",
                 "hire":"雇佣, 数据类型int",
                 "abstract":"摘要 概要，数据类型string",
                 "desc": "具体需求描述，数据类型string",
                 "status": "任务状态，数据类型int",
                 "transaction_mode":"交易模式，数据类型int"
                 "min_price": "价格范围最小值，数据类型int",
                 "max_price": "价格范围最大值，数据类型int",
                 "start_time": "开始时间，数据类型int",
                 "end_time": "结束时间，数据类型int",
                 "is_top": "是否置顶，数据类型bool",
                 "priority": "是否加急优先，数据类型bool"
            },
            "user_info":{
                 "user_id": "用户id，数据类型int", 
                 "avatar": "用户头像，数据类型string",
                 "real_name_authentication": "实名认证，数据类型bool",
                 "email_authentication": "邮箱认证，数据类型bool",
                 "mobile_authentication": "手机认证, 数据类型bool"
            }
        }]

    }

### Response Code
    HTTP/1.1 200 OK

### Example

    curl -X POST "http://0:9004/weidu/api/v1/task/publish" -i -d '{"creator_id": 123, "industry":1, "type":1, "style":1, "hire":1, "abstract":"xxxxxabstract", "desc":"xxxxdesc", "transaction_mode":1, "min_price":123, "max_price":568, "start_time":343, "end_time":8987, "is_top":true,  "priority":true, "block_search":true, "copyright_guard":true, "agree_protocol":true}' -i
         HTTP/1.1 201 Created
         Content-Type: application/json; charset=utf-8
         Date: Thu, 01 Oct 2020 13:03:12 GMT
         Content-Length: 383

    {
      "code": 200,
      "result": "ok",
      "data": {
        "id": 4,
        "creator_id": 123,
        "industry": 1,
        "type": 1,
        "style": 1,
        "hire": 1,
        "abstract": "xxxxxabstract",
        "desc": "xxxxdesc",
        "transaction_mode": 1,
        "min_price": 123,
        "max_price": 568,
        "start_time": 343,
        "end_time": 8987,
        "is_top": true,
        "priority": true,
        "block_search": true,
        "copyright_guard": true,
        "agree_protocol": true,
        "update_time": 1601557392423,
        "create_time": 1601557392423
      }
    }
