---
name: 优秀设计师列表
---
    
### Url
    /weidu/api/v1/users/excellent/list
    
### Method
    GET

### Content-Type
    application/json    

### Query Param
    per_page: 每页返回记录数，数据类型int
    page: 第几页,数据类型int

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "total": "总记录数，数据类型int",
        "data": [{
                "user_id": "用户ID，数据类型string",
                "nickname": "用户昵称，数据类型string",
                "desc": "用户简介，数据类型string",
                "avatar_url": "用户头像，数据类型string",
                "title": "头衔,数据类型int"
            }]
    }
    

### Example

    curl -X GET "http://www.weiduchuangzao.com:9004/weidu/api/v1/users/excellent/list?per_page=5" -i
        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Thu, 18 Mar 2021 13:53:52 GMT
        Content-Length: 1092

    {
        "code":200,
        "data":[
            {
                "user_id":"o4cnejab1ff1tece3et8xajaxw",
                "nickname":"Ken飞哥",
                "desc":"优秀设计师介绍。。。。。。",
                "avatar_url":"https://tfs.alipayobjects.com/images/partner/T1jT0bXb8XXXXXXXXX",
                "title":"总监"
            },
            {
                "user_id":"esbng8qjsfn5jr355ikcr4aajr",
                "nickname":"",
                "desc":"优秀设计师介绍。。。。。。",
                "avatar_url":"20210208/users/esbng8qjsfn5jr355ikcr4aajr/nna9k8znspbninexatfz34fxga/fabu.jpg",
                "title":"总监"
            },
            {
                "user_id":"bjg5k3er6inf8ce16onhnhb8we",
                "nickname":"1150910",
                "desc":"优秀设计师介绍。。。。。。",
                "avatar_url":"20210208/users/bjg5k3er6inf8ce16onhnhb8we/nikjo4waktreiban6fn9aeib5o/zhizuo.jpeg",
                "title":"总监"
            },
            {
                "user_id":"szasc68seig9jrhqw4eaj9gu3h",
                "nickname":"1150911",
                "desc":"优秀设计师介绍。。。。。。",
                "avatar_url":"20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                "title":"总监"
            },
            {
                "user_id":"b1onnbw3ebbjtenaco9fxa1611",
                "nickname":"112",
                "desc":"优秀设计师介绍。。。。。。",
                "avatar_url":"20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
                "title":"总监"
            }
        ],
        "result":"ok",
        "total":18
    }