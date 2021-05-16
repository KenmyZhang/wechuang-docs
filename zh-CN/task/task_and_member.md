---
name: 任务详情页
---
    
### Url
     /weidu/api/v1/task/detail

### Method
    GET

### Content-Type
    application/json      

### 限制

### Query Param
    task_id: "任务id，数据类型int"

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": {
           "task":{
                "id": "任务编号,数据类型string",
                "creator_id": "创建者id，数据类型string",
                "abstract": "摘要 概要，数据类型string",
                "desc": "具体需求描述 、任务要求，数据类型string",
                "status": "任务状态： 1发布需求、2总监竞标、3设计竞标、4托管资金、5需求制作、6任务完成   数据类型int",
                "transaction_mode": "交易模式： 1 委托模式、2 直聘模式，数据类型int",
                "min_price": "价格范围最小值，数据类型int",
                "max_price": "价格范围最大值，数据类型int",
                "start_time": "开始时间，数据类型int",
                "end_time": "结束时间，数据类型int",
                "requirements": "参与要求,数据类型string",
                "create_time": "任务创建时间，毫秒，数据类型int"
            },
            "members":[
                {
                    "user_id": "用户ID，数据类型string",
                    "avatar_url": "头像地址，数据类型string",
                    "real_name_auth": "是否实名，数据类型bool",
                    "nick_name": "昵称，数据类型string",
                    "score": "评分，数据类型float",
                    "serve_num": "任务数，数据类型int",
                    "level": "信用等级，数据类型string",
                    "apply_time":"申请时间，毫秒，数据类型int"
                    "work_list": [{  //项目作品
                        "id": "作品id，数据类型string",
                        "user_id": "用户ID，数据类型string",
                        "name": "项目名字，数据类型string",
                        "type": "项目类型，1游戏 2动漫 3漫画 4广告 5界面 6LOGO,数据类型int",
                        "belong_type": "项目归属，1个人 2团队合作，数据类型int",
                        "link": "项目链接，数据类型string",
                        "file_infos": [{
                            "id": "作品文件ID，数据类型string",
                            "user_id": "用户ID，数据类型string",
                            "path": "文件作品路径，数据类型string",
                            "preview_path": "作品预览路径，数据类型string",
                            "name": "作品文件名称，数据类型string",
                            "extension": "作品后缀，数据类型string",
                            "size": "作品大小，数据类型int",
                            "mime_type": "作品的mime type，数据类型string",
                            "width": "作品宽度，数据类型int",
                            "height": "作品高度，数据类型int",
                            "has_pre_img": "是否有预览图，数据类型bool"
                        }]
                    }],
                    "work_experience_list": [ //工作经历
                        {
                            "id": "唯一标识，数据类型int",
                            "company_name": "公司名称，数据类型string",
                            "position": "职位，数据类型string",
                            "begin_time": "开始时间，unix时间戳，单位秒，数据类型int",
                            "end_time": "结束时间，unix时间戳，单位秒，数据类型int",
                            "project":"参与项目,数据类型string"
                        }
                    ],
                    "project": "参与项目，数据类型string"
                }
            ]
        } 
    }

### Response Code
    HTTP/1.1 200 OK

