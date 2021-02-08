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
                "user_name": "用户名，数据类型string",
                "desc": "用户简介，数据类型string",
                "avatar_url": "用户头像，数据类型string",
                "award_info": "获奖情况，数据类型string",
                "score": "评分，数据类型int",
                "like_cnt": "点赞数,数据类型int",
                "view_cnt": "浏览数,数据类型int"
            }]
    }
    

### Example

   curl -X GET "http://0:9004/weidu/api/v1/users/excellent/list?per_page=5" -i


        HTTP/1.1 200 OK
        Content-Type: application/json; charset=utf-8
        Date: Mon, 08 Feb 2021 09:49:29 GMT
        Content-Length: 964

    {
        "code": 200,
        "data": [{
            "user_id": "esbng8qjsfn5jr355ikcr4aajr",
            "user_name": "1356941491057987584",
            "desc": "2221æè¿°",
            "avatar_url": "20210208/users/esbng8qjsfn5jr355ikcr4aajr/nna9k8znspbninexatfz34fxga/fabu.jpg",
            "score": "70",
            "comment_cnt": 4,
            "like_cnt": 5,
            "view_cnt": 5
        }, {
            "user_id": "bjg5k3er6inf8ce16onhnhb8we",
            "user_name": "1356941446602559488",
            "desc": "5621æè¿°",
            "avatar_url": "20210208/users/bjg5k3er6inf8ce16onhnhb8we/nikjo4waktreiban6fn9aeib5o/zhizuo.jpeg",
            "score": "70",
            "comment_cnt": 0,
            "like_cnt": 0,
            "view_cnt": 0
        }, {
            "user_id": "szasc68seig9jrhqw4eaj9gu3h",
            "user_name": "1356941364390006784",
            "desc": "1æè¿°",
            "avatar_url": "20210208/users/szasc68seig9jrhqw4eaj9gu3h/e5asiqn49tgz8pnru1rj6hnz9c/jianzhi.jpg",
            "score": "70",
            "comment_cnt": 1,
            "like_cnt": 3,
            "view_cnt": 0
        }, {
            "user_id": "b1onnbw3ebbjtenaco9fxa16ke",
            "user_name": "1356932923411927040",
            "desc": "æè¿°",
            "avatar_url": "",
            "score": "70",
            "comment_cnt": 0,
            "like_cnt": 0,
            "view_cnt": 0
        }],
        "result": "ok",
        "total": 4
    }