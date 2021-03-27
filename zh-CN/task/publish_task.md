---
name: 发布任务
---
    
### Url
     /weidu/api/v1/task/publish
    
### Method
    POST

### Content-Type
    application/json      

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"

    测试环境可以不带token，但需要带上头部参数User-Id, eg: -H "User-Id:erb4krcbbirbtcwnhwopeizz5o"   

### Requst Body

    {
        "industry":"行业,数据类型int，必填",
        "type":"任务类型,数据类型int，必填",
        "style":"风格,数据类型int，必填",
        "hire":"雇佣, 数据类型int，必填",
        "abstract":"摘要 概要，数据类型string，必填",
        "desc": "具体需求描述，数据类型string，必填",
        "attachments": "附件id列表，多个附件用逗号分割，数据类型string，选填",
        "transaction_mode":"交易模式，数据类型int，必填"
        "min_price": "价格范围最小值，数据类型int，必填",
        "max_price": "价格范围最大值，数据类型int，必填",
        "start_time": "开始时间，unix时间戳，单位毫秒，数据类型int，必填",
        "end_time": "结束时间,unix时间戳，单位毫秒，数据类型int，必填",
        "is_top": "是否置顶，默认不置顶false，数据类型bool，选填",
        "priority": "是否加急优先，默认不加急false，数据类型bool，选填",
        "block_search": "是否屏蔽搜索，默认不屏蔽false，数据类型bool，选填",
        "copyright_guard": "版权卫士，默认非版权卫士false，数据类型bool，选填",
        "agree_protocol": "同意协议，数据类型bool，必填"
    }



| 行业 | 编码 |
|---|---|
|   游戏|     1 |
| UI/UX | 2|
|   动漫|      3 |
|   影视 |     4   |
|   产品 |     5   |
|   建筑 |     6   |

|行业| 类型 | 编码 |
|--- |---|---|
|游戏 1 |   原画|     1 |
|游戏 1 |   建模|      2 |
|游戏 1 |   动作|      3 |
|游戏 1 |   特效 |     4   |
|游戏 1 |   界面 |     5   |


|行业| 类型 | 编码 |
|---|---|---|
|动漫 2 |   角色|     6|
|动漫 2 |   分镜|      7 |
|动漫 2 |   线稿|      8 |
|动漫 2 |   上色 |     9   |
|动漫 2 |   整套 |     10   |

| 风格 | 编码 |
|---|---|
|   写实|     1 |
|   卡通|      2 |

| 雇佣 | 编码 |
|---|---|
|   团队|     1 |
|   个人|      2 |


| 交易模式 | 编码 |
|---|---|
|   委托模式1|     1 |
|   直聘模式|      2 |



|任务状态 | 编码 |
|---|---|
|发布需求| 1|
|总监竞标| 2|
|设计竞标| 3|
|托管赏金| 4|
|需求制作| 5|
|任务完成| 6|


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

      curl -X POST "http://weiduchuangzao.com:9004/weidu/api/v1/task/publish" -i -H "User-Id:erb4krcbbirbtcwnhwopeizz5o" -d '{"industry":1, "type":1,"style": 1, "hire": 1,"abstract":"摘要 概要","desc": "具体需求描述","attachments": "r46n33tqcf8qnnx9gaff711jfe,cohe5c3pfpaueajo3be6bwzpge","transaction_mode": 1,"min_price": 1000,"max_price": 2000,"start_time": 1602129479000,"end_time": 1602139479000 ,"is_top": true,  "priority": true, "block_search": true, "copyright_guard": true,"agree_protocol": true}' -H "Content-Type:application/json"
            HTTP/1.1 201 Created
            Content-Type: application/json; charset=utf-8
            Date: Sat, 27 Mar 2021 14:03:21 GMT
            Content-Length: 559
        {
            "code": 200,
            "data": {
                "id": "wt6weairutbgxc8fuw7r884har",
                "creator_id": "",
                "industry": 1,
                "type": 1,
                "style": 1,
                "hire": 1,
                "abstract": "摘要 概要",
                "desc": "具体需求描述",
                "attachments": "r46n33tqcf8qnnx9gaff711jfe,cohe5c3pfpaueajo3be6bwzpge",
                "status": 1,
                "transaction_mode": 1,
                "price": 0,
                "min_price": 1000,
                "max_price": 2000,
                "start_time": 1602129479000,
                "end_time": 1602139479000,
                "score": 0,
                "is_top": true,
                "priority": true,
                "block_search": true,
                "copyright_guard": true,
                "agree_protocol": true,
                "requirements": "",
                "update_time": 1616853801590,
                "create_time": 1616853801590
            },
            "result": "ok"
        }