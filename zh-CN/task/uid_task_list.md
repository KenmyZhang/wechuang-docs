---
name: 获取指定用户参与的任务列表
---
    
### Url
    /weidu/api/v1/task/uid_task_list

### Method
    GET

### Content-Type
    application/json     

### 限制

### Query Param
    user_id:用户ID


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

|订单状态| 编码|
|---|---|
|设计中| 1|
|审核中| 2|
|已完成| 3|
|合格发布需求| 4|



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
                 "abstract":"摘要 概要 ，数据类型string",
                 "desc": "具体需求描述，数据类型string",
                 "status": "任务状态，数据类型int",
                 "sub_status": "订单状态，数据类型int",
                 "transaction_mode":"交易模式，数据类型int"
                 "price": "项目价格，单位元，数据类型int",
                 "start_time": "开始时间，数据类型int",
                 "end_time": "结束时间，数据类型int",
                 "is_top": "是否置顶，数据类型bool",
                 "priority": "是否加急优先，数据类型bool"
            },
            "user_info":{
                 "user_id": "用户id，数据类型string",
                 "avatar": "用户头像，数据类型string",
				 "enterprise_auth": "企业认证，数据类型bool",
				 "sesame_auth": "芝麻认证，数据类型bool",
                 "real_name_auth": "实名认证，数据类型bool"
            }
        }]

    }

### Response Code
    HTTP/1.1 200 OK

### Example

    curl -X GET "http://0:9004/weidu/api/v1/task/uid_task_list?user_id=esbng8qjsfn5jr355ikcr4aajr" -i 
        HTTP/1.1 201 Created
        Content-Type: application/json; charset=utf-8
        Date: Wed, 26 May 2021 09:52:22 GMT
        Content-Length: 1689


    {
        "code": 200,
        "data": [{
            "task": {
                "id": "5trb5tu7tj8kfe7gwk7qakfpac",
                "creator_id": "szasc68seig9jrhqw4eaj9gu3h",
                "industry": 1,
                "type": 1,
                "style": 1,
                "hire": 1,
                "abstract": "摘要 概要",
                "desc": "具体需求描述",
                "status": 1,
                "sub_status": 0,
                "transaction_mode": 1,
                "price": 1000,
                "min_price": 1000,
                "max_price": 2000,
                "start_time": 1602129479000,
                "end_time": 1602139479000,
                "is_top": true,
                "priority": true,
                "block_search": true,
                "copyright_guard": true,
                "create_time": 0
            },
            "user_info": {
                "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                "avatar": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                "real_name_auth": true,
                "sesame_auth": true,
                "enterprise_auth": false
            }
        }, {
            "task": {
                "id": "w84sa8jaapnb5nixq5s6saeash",
                "creator_id": "b1onnbw3ebbjtenaco9fxa16ke",
                "industry": 2,
                "type": 8,
                "style": 2,
                "hire": 1,
                "abstract": "供应链金融平台原型设计",
                "desc": "一、需求描述：\n类别：供应链金融平台原型设计\n进度：已经有原型图。\n功能：一个服务小微企业和核心企业的供应链金融平台的原型；您能否提供一个总的设计原则和一两个页面的示例给我们看下？\n技术：UI设计软件，Sketch\n\n二、人才要求：\n4年以上UI设计经验，金融产品设计经验。\n\n三、合作方式：\n开发方式：UI设计。\n设计周期：3天",
                "status": 1,
                "sub_status": 0,
                "transaction_mode": 2,
                "price": 0,
                "min_price": 1000,
                "max_price": 20000,
                "start_time": 1621440000000,
                "end_time": 1686067200000,
                "is_top": true,
                "priority": true,
                "block_search": true,
                "copyright_guard": true,
                "create_time": 0
            },
            "user_info": {
                "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
                "avatar": "20210507/users/b1onnbw3ebbjtenaco9fxa16ke/3xr7669ea7nhjpewtskhoxz8ja/1.png",
                "real_name_auth": true,
                "sesame_auth": false,
                "enterprise_auth": true
            }
        }],
        "result": "ok"
    }