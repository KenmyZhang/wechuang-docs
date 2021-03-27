---
name: 任务列表
---
    
### Url
     /weidu/api/v1/task/list
    
### Method
    GET

### Content-Type
    application/json     

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"

    测试环境可以不带token，但需要带上头部参数User-Id, eg: -H "User-Id:123"      

### Query Param
    industry:行业，数据类型int
    type:类型，数据类型int
    style:风格，数据类型int
    hire:雇佣，数据类型int
    release_time:发布时间排序，包括升序1、降序2，数据类型int
    price: 价格排序，包括升序1、降序2，数据类型int
    left_time:剩余时间排序，，包括升序1、降序2，数据类型int
    keyword: 关键词,数据类型string



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

    curl -X GET "http://www.weiduchuangzao.com:9004/weidu/api/v1/task/list?industry=1&type=1&style=1&hire=1&release_time=1&price=1&left_time=1&keyword=" -i
			HTTP/1.1 201 Created
			Content-Type: application/json; charset=utf-8
			Date: Sat, 27 Mar 2021 13:45:07 GMT
			Transfer-Encoding: chunked

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
					"transaction_mode": 1,
					"price": 1000,
					"start_time": 1602129479000,
					"end_time": 1602139479000,
					"is_top": true,
					"priority": true
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
					"id": "ofargqanbpeeinswoigjae9rpe",
					"creator_id": "esbng8qjsfn5jr355ikcr4aajr",
					"industry": 1,
					"type": 1,
					"style": 1,
					"hire": 1,
					"abstract": "摘要 概要",
					"desc": "具体需求描述",
					"status": 1,
					"transaction_mode": 1,
					"price": 10,
					"start_time": 1602129479000,
					"end_time": 1602139479000,
					"is_top": true,
					"priority": true
				},
				"user_info": {
					"user_id": "esbng8qjsfn5jr355ikcr4aajr",
					"avatar": "20210208/users/esbng8qjsfn5jr355ikcr4aajr/nna9k8znspbninexatfz34fxga/fabu.jpg",
					"real_name_auth": false,
					"sesame_auth": false,
					"enterprise_auth": false
				}
			}, {
				"task": {
					"id": "x6xnpntqb3n58n6445wnzjg94h",
					"creator_id": "bjg5k3er6inf8ce16onhnhb8we",
					"industry": 1,
					"type": 1,
					"style": 1,
					"hire": 1,
					"abstract": "摘要 概要",
					"desc": "具体需求描述",
					"status": 1,
					"transaction_mode": 1,
					"price": 10,
					"start_time": 1602129479000,
					"end_time": 1602139479000,
					"is_top": true,
					"priority": true
				},
				"user_info": {
					"user_id": "bjg5k3er6inf8ce16onhnhb8we",
					"avatar": "20210208/users/bjg5k3er6inf8ce16onhnhb8we/nikjo4waktreiban6fn9aeib5o/zhizuo.jpeg",
					"real_name_auth": true,
					"sesame_auth": true,
					"enterprise_auth": true
				}
			}, {
				"task": {
					"id": "bnk7w8bhg7br5jp8xuep1to4se",
					"creator_id": "b1onnbw3ebbjtenaco9fxa16ke",
					"industry": 1,
					"type": 1,
					"style": 1,
					"hire": 1,
					"abstract": "摘要 概要",
					"desc": "具体需求描述",
					"status": 1,
					"transaction_mode": 1,
					"price": 8900,
					"start_time": 1602129479000,
					"end_time": 1602139479000,
					"is_top": true,
					"priority": true
				},
				"user_info": {
					"user_id": "b1onnbw3ebbjtenaco9fxa16ke",
					"avatar": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
					"real_name_auth": true,
					"sesame_auth": false,
					"enterprise_auth": true
				}
			}],
			"result": "ok"
		}