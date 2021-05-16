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

### Example

    curl -X GET "http://0:9004/weidu/api/v1/task/detail?task_id=5trb5tu7tj8kfe7gwk7qakfpac" -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Sun, 16 May 2021 12:38:03 GMT
        Transfer-Encoding: chunked

    {
        "code": 200,
        "data": {
            "members": [{
                "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                "avatar_url": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                "username": "a1356937040",
                "real_name": "realname-hihi",
                "gender": 1,
                "user_type": 1,
                "team_name": "",
                "identity_number": "",
                "industry": 0,
                "type": 0,
                "work_experience": "工作经验",
                "mobile": "17512053076",
                "desc": "desc",
                "real_name_auth": true,
                "score": 70,
                "serve_num": 0,
                "level": "",
                "business_license_file_id": "hhtfwf9zrifu8f7rsuh36bkgjw",
                "business_license_info": {
                    "id": "hhtfwf9zrifu8f7rsuh36bkgjw",
                    "user_id": "rfeaxzb4etf58cia8i6ha1jwgw",
                    "path": "20201006/users/rfeaxzb4etf58cia8i6ha1jwgw/hhtfwf9zrifu8f7rsuh36bkgjw/TOC.ini",
                    "name": "TOC.ini",
                    "extension": "ini",
                    "size": 706,
                    "mime_type": ""
                },
                "work_list": [{
                    "id": "45gbin1qn78a3fajrx3rub1upc",
                    "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                    "name": "project name2",
                    "type": 0,
                    "belong_type": 1,
                    "link": "www.baidu.com/",
                    "file_infos": [{
                        "id": "biinjhnesifeiasftws8a6q95r",
                        "task_id": "5trb5tu7tj8kfe7gwk7qakfpac",
                        "user_id": "erb4krcbbirbtcwnhwopeizz5o",
                        "path": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                        "preview_path": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi_preview.jpg",
                        "name": "jianzhi.jpg",
                        "extension": "jpg",
                        "size": 34348,
                        "mime_type": "image/jpeg",
                        "width": 500,
                        "height": 333,
                        "has_pre_img": true
                    }, {
                        "id": "h8n5hftujtgpen8aqnqseec57a",
                        "user_id": "rfeaxzb4etf58cia8i6ha1jwgw",
                        "path": "20201006/users/rfeaxzb4etf58cia8i6ha1jwgw/h8n5hftujtgpen8aqnqseec57a/.",
                        "name": ".",
                        "extension": "",
                        "size": 0,
                        "mime_type": ""
                    }, {
                        "id": "hhtfwf9zrifu8f7rsuh36bkgjw",
                        "user_id": "rfeaxzb4etf58cia8i6ha1jwgw",
                        "path": "20201006/users/rfeaxzb4etf58cia8i6ha1jwgw/hhtfwf9zrifu8f7rsuh36bkgjw/TOC.ini",
                        "name": "TOC.ini",
                        "extension": "ini",
                        "size": 706,
                        "mime_type": ""
                    }]
                }],
                "work_experience_list": [{
                    "id": "aw4r9ecoppbizafntksrrc8tio",
                    "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                    "job_desc": "",
                    "employment_certificate": false,
                    "social_security_certificate": false,
                    "company_name": "aaa",
                    "begin_time": 1612355006,
                    "end_time": 1612355006,
                    "project": ""
                }, {
                    "id": "hue15ruriirf8qkcai9oju5bho",
                    "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                    "job_desc": "",
                    "employment_certificate": false,
                    "social_security_certificate": false,
                    "company_name": "aaa",
                    "begin_time": 1612355006,
                    "end_time": 1612355006,
                    "project": ""
                }, {
                    "id": "x9exrsna67r7ipe5c7ks3js37o",
                    "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                    "job_desc": "",
                    "employment_certificate": false,
                    "social_security_certificate": false,
                    "company_name": "aaa",
                    "begin_time": 1612355006,
                    "end_time": 1612355006,
                    "project": ""
                }]
            }],
            "task": {
                "id": "5trb5tu7tj8kfe7gwk7qakfpac",
                "creator_id": "szasc68seig9jrhqw4eaj9gu3h",
                "industry": 1,
                "type": 1,
                "style": 1,
                "hire": 1,
                "abstract": "摘要 概要",
                "desc": "具体需求描述",
                "attachments": "xxxxxx",
                "status": 1,
                "transaction_mode": 1,
                "price": 1000,
                "min_price": 1000,
                "max_price": 2000,
                "start_time": 1602129479000,
                "end_time": 1602139479000,
                "score": 90,
                "is_top": true,
                "priority": true,
                "block_search": true,
                "copyright_guard": true,
                "agree_protocol": true,
                "requirements": "",
                "update_time": 1612355363209,
                "create_time": 1612355363209
            }
        }
    }