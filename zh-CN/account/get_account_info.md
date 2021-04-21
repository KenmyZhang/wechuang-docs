---
name: 获取入驻信息
---
    
### Url
    /weidu/api/v1/users/accountinfo
    
### Method
    GET

### Content-Type
    application/json    

### Query Param
    user_id: 用户ID
    
### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int", 
        "data": {
            "user_id": "用户ID，数据类型string",
            "avatar_url": "头像地址，数据类型string",
            "username": "用户名，数据类型string",
            "real_name": "姓名，数据类型string",
            "gender": "性别， 0未知 1男性 2女性，数据类型int",
            "user_type": "用户类型，1独立设计师 2小型工作室，数据类型int",
            "work_experience": "工作经验，数据类型string",
            "mobile": "联系手机，数据类型string",
            "identity_number": "身份证号，数据类型string",
            "desc": "自我介绍，数据类型string",
            "industry": "行业，数据类型int",
            "type": "类型，数据类型int",
            "business_license_file_id": "营业执照文件ID，数据类型string",
            "business_license_info":{
                "id": "文件ID，数据类型string",
                "user_id": "用户ID，数据类型string",
                "path": "营业执照文件路径，数据类型string",
                "preview_path": "预览路径，数据类型string",
                "name": "文件名称，数据类型string",
                "extension": "作品后缀，数据类型string",
                "size": "大小，数据类型int",
                "mime_type": "mime type，数据类型string",
                "width": "宽度，数据类型int",
                "height": "高度，数据类型int",
                "has_pre_img": "是否有预览图，数据类型bool"
            },
            "work_list": [{
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
            "work_experience_list": [
                {
                    "id": "唯一标识，数据类型int",
                    "company_name": "公司名称，数据类型string",
                    "position": "职位，数据类型string",
                    "begin_time": "开始时间，unix时间戳，单位秒，数据类型int",
                    "end_time": "结束时间，unix时间戳，单位秒，数据类型int",
                    "project":"参与项目,数据类型string"
                }
            ]
        }
    }
    

### Example

        curl -X GET  "http://129.28.198.139:9004/weidu/api/v1/users/accountinfo?user_id=szasc68seig9jrhqw4eaj9gu3h" -i
            HTTP/1.1 200 OK
            Content-Type: application/json; charset=utf-8
            Date: Wed, 21 Apr 2021 08:07:23 GMT
            Content-Length: 1889

        {
            "code": 200,
            "data": {
                "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                "avatar_url": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                "username": "a1356937040",
                "real_name": "realname-hihi",
                "gender": 1,
                "user_type": 1,
                "identity_number": "",
                "industry": 0,
                "type": 0,
                "work_experience": "工作经验",
                "mobile": "175120530765",
                "desc": "desc",
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
                    "id": "hue15ruriirf8qkcai9oju5bho",
                    "user_id": "szasc68seig9jrhqw4eaj9gu3h",
                    "job_desc": "",
                    "employment_certificate": false,
                    "SocialSecurityCertificate": false,
                    "company_name": "aaa",
                    "begin_time": 1612355006,
                    "end_time": 1612355006,
                    "project": ""
                }]
            },
            "result": "ok"
        }


