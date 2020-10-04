---
name: 制作竞标
---
    
### Url
     /weidu/api/v1/task/design
    
### Method
    GET

### Content-Type
    application/json      

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"

    测试环境可以不带token，但需要带上头部参数User-Id, eg: -H "User-Id:123"   

### Query Param
    id: "任务id，数据类型int"

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": {
           "task":{
                 "id": "任务id，数据类型int",
                 "serial_num": "任务编号",
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
                 "priority": "是否加急优先，数据类型bool",
                 "requirements": "参与要求，数据类型string"
                 
            },
            "user_info":{
                 "user_id": "用户id，数据类型int", 
                 "avatar": "用户头像，数据类型string",
                 "real_name_authentication": "实名认证，数据类型bool",
                 "email_authentication": "邮箱认证，数据类型bool",
                 "mobile_authentication": "手机认证, 数据类型bool"
            },
            "bidder_list":[
                {
                    "user_id": "竞标者uid，数据类型int",
                    "avatar": "用户头像，数据类型string",
                    "level": "信用卫士等级，数据类型int",
                    "score": "评分，数据类型int",
                    "task_num": "任务数，数据类型int",
                    "work_experience": [
                        {
                          "job_desc": "工作描述，数据类型string",
                          "employment_certificate": "工作证明，数据类型bool",
                          "social_security_certificate": "社保证明,数据类型bool"
                        }
                    ],
                    "projects": ["参与项目1，数据类型string","参与项目2,数据类型string"],
                    "works": ["项目作品,数据类型string"],
                    "application_time": "申请时间，数据类型int"
                }
            ]
        } 
    }

### Response Code
    HTTP/1.1 200 OK

### Example



