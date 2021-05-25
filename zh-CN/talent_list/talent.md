---
name: 人才详情
---
    
### Url
    /weidu/api/v1/users/talent
    
### Method
    GET

### Content-Type
    application/json    

### Query Param
    user_id：用户ID

### Response Body

    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int", 
        "data": {
            "user_id": "用户ID，数据类型string",
            "avatar_url": "头像地址，数据类型string",
            "nickname": "昵称，数据类型string",
            "serve_num": "服务商家数，数据类型int",
            "work_num": "案例数，数据类型int",
            "transaction_amount": "交易总金额，数据类型int",
            "bid_count": "中标次数，数据类型string",
            "transaction_praise_rte": "交易好评率，数据类型float",
            "desc":"自我介绍，数据类型string",
            "social_security_auth":"社保是否认证，数据类型bool",
            "real_name_auth":"实名认证，数据类型bool",
            "enterprise_auth":"企业认证，数据类型bool",
            "sesame_auth":"芝麻积分认证，数据类型bool",
            "score":"个人综合评分,数据类型float",
            "person_praise_rate":"个人好评率,数据类型float",
            "refund_rate":"退款率，数据类型float",
            "dispute_rate":"纠纷率,数据类型float",
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
            "work_experience_list":[{
                    "id": "唯一标识，数据类型int",
                    "user_id": "用户ID，数据类型string",
                    "company_name": "公司名称，数据类型string",
                    "position": "职位，数据类型string",
                    "begin_time": "开始时间，unix时间戳，单位秒，数据类型int",
                    "end_time": "结束时间，unix时间戳，单位秒，数据类型int",
                    "project":"参与项目,数据类型string"
                }
            ],
            "skill_list":[
                {
                    "id":"技能ID，数据类型string",
                    "user_id":"用户ID，数据类型string",
                    "score":"技能熟练程度，满分10分，数据类型int",
                    "name":"技能名称，数据类型string"
                }
            ]
        }
    }

### Example

    curl -X GET "http://8.134.37.138:9004/weidu/api/v1/users/talent?user_id=b1onnbw3ebbjtenaco9fxa16ke" -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Tue, 25 May 2021 13:36:28 GMT
        Transfer-Encoding: chunked


    {
        "code":200,
        "data":{
            "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
            "avatar_url":"20210507/users/b1onnbw3ebbjtenaco9fxa16ke/3xr7669ea7nhjpewtskhoxz8ja/1.png",
            "nick_name":"1150909",
            "serve_num":0,
            "work_num":0,
            "transaction_amount":0,
            "bid_count":0,
            "transaction_praise_rte":0,
            "desc":"自我介绍",
            "social_security_auth":false,
            "real_name_auth":true,
            "enterprise_auth":true,
            "sesame_auth":false,
            "score":9.5,
            "person_praise_rate":0,
            "refund_rate":0,
            "dispute_rate":0,
            "work_list":[
                {
                    "id":"bjx7xhnee7g7jenahpak1to4ir",
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "name":"project name",
                    "type":0,
                    "belong_type":1,
                    "link":"www.baidu.com/",
                    "file_infos":[
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
                        },
                        {
                            "id":"h8n5hftujtgpen8aqnqseec57a",
                            "user_id":"rfeaxzb4etf58cia8i6ha1jwgw",
                            "path":"20201006/users/rfeaxzb4etf58cia8i6ha1jwgw/h8n5hftujtgpen8aqnqseec57a/.",
                            "name":".",
                            "extension":"",
                            "size":0,
                            "mime_type":""
                        },
                        {
                            "id":"hhtfwf9zrifu8f7rsuh36bkgjw",
                            "user_id":"rfeaxzb4etf58cia8i6ha1jwgw",
                            "path":"20201006/users/rfeaxzb4etf58cia8i6ha1jwgw/hhtfwf9zrifu8f7rsuh36bkgjw/TOC.ini",
                            "name":"TOC.ini",
                            "extension":"ini",
                            "size":706,
                            "mime_type":""
                        }
                    ]
                },
                {
                    "id":"eoceejia8bepxfcn6r5wa7n5xw",
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "name":"肖秋雄",
                    "type":3,
                    "belong_type":1,
                    "link":"http://localhost:8080/checkin/edit?type=designer",
                    "file_infos":[
                        {
                            "id":"ngatqn11c7fpuef3xepnn44eza",
                            "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                            "path":"20210506/users/b1onnbw3ebbjtenaco9fxa16ke/ngatqn11c7fpuef3xepnn44eza/src=http___bpic.588ku.com_back_pic_05_65_51_515b7070e7e1416.jpg\u0026refer=http___bpic.588ku.jpg",
                            "preview_path":"20210506/users/b1onnbw3ebbjtenaco9fxa16ke/ngatqn11c7fpuef3xepnn44eza/src=http___bpic.588ku.com_back_pic_05_65_51_515b7070e7e1416.jpg\u0026refer=http___bpic.588ku_preview.jpg",
                            "name":"src=http___bpic.588ku.com_back_pic_05_65_51_515b7070e7e1416.jpg\u0026refer=http___bpic.588ku.jpg",
                            "extension":"jpg",
                            "size":45038,
                            "mime_type":"image/jpeg",
                            "width":1200,
                            "height":500,
                            "has_pre_img":true
                        }
                    ]
                },
                {
                    "id":"kh4rro9as7betjz7t35871bh7w",
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "name":"肖秋雄",
                    "type":2,
                    "belong_type":1,
                    "link":"http://localhost:8080/checkin/edit?type=designer",
                    "file_infos":[
                        {
                            "id":"rfaf4j16pfe39esjca37bfs7ec",
                            "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                            "path":"20210507/users/b1onnbw3ebbjtenaco9fxa16ke/rfaf4j16pfe39esjca37bfs7ec/1.png",
                            "preview_path":"20210507/users/b1onnbw3ebbjtenaco9fxa16ke/rfaf4j16pfe39esjca37bfs7ec/1_preview.jpg",
                            "name":"1.png",
                            "extension":"png",
                            "size":424776,
                            "mime_type":"image/png",
                            "width":760,
                            "height":390,
                            "has_pre_img":true
                        }
                    ]
                }
            ],
            "work_experience_list":[
                {
                    "id":"a8gozhb86bbniq75eabgjxbn8e",
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "job_desc":"",
                    "employment_certificate":false,
                    "social_security_certificate":false,
                    "company_name":"公司名称",
                    "begin_time":1620316245,
                    "end_time":1620366267,
                    "project":"参与项目"
                },
                {
                    "id":"carhhczifieiuqjbba4qwjprge",
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "job_desc":"",
                    "employment_certificate":false,
                    "social_security_certificate":false,
                    "company_name":"公司名称",
                    "begin_time":1620316245,
                    "end_time":1620366267,
                    "project":"参与项目"
                },
                {
                    "id":"sb1nwac3bign9g8tn4eehfeeph",
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "job_desc":"",
                    "employment_certificate":false,
                    "social_security_certificate":false,
                    "company_name":"公司名称",
                    "begin_time":1620316245,
                    "end_time":1620366267,
                    "project":"参与项目"
                }
            ],
            "skill_list":[
                {
                    "id":"ax85wkeexteoja3c7qtat7pf6o",
                    "user_id":"b1onnbw3ebbjtenaco9fxa16ke",
                    "score":0,
                    "name":"UI设计"
                }
            ]
        },
        "result":"ok"
    }