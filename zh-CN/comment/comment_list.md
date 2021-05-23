---
name: 评论列表
---

### Url
    /weidu/api/v1/comment/list

### Method
    GET

### Content-Type
    application/json

### Query Param

    user_id：用户ID
    per_page：每页返回记录条数
    page:第几页


### 限制


### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
        "data": [{
            "id": "评论ID，数据类型string",
            "content": "评论内容,数据类型string",
            "score": "评分，数据类型float",
            "tags": ["标签,数据类型string"]
        }]
    }

### Example

    curl -X GET "http://0:9004/weidu/api/v1/comment/list?user_id=ow4rxntfgbetifiaoxoza8w53e&per_page=20" -i  -H "Authorization:Bearer 8r79se5kwff5xg9tr6pxctinpr"
        HTTP/1.1 201 Created
        Content-Type: application/json
        Expires: 0
        Date: Sun, 23 May 2021 10:44:57 GMT
        Content-Length: 452

    {
        "code": 200,
        "data": [{
            "id": "6tewi6ewb3eoec3aaj7se4hwih",
            "content": "789",
            "score": 5,
            "tags": ["经验丰富", "逻辑能力强"]
        }, {
            "id": "9r366a7r3pg3fns9p348feznxo",
            "content": "123",
            "score": 5,
            "tags": ["经验丰富", "逻辑能力强"]
        }, {
            "id": "g57j1peabpnwbe4qaw6u3iceoh",
            "content": "567",
            "score": 5,
            "tags": ["经验丰富", "逻辑能力强"]
        }, {
            "id": "t4ujrr3xuia6bgwngex31o835h",
            "content": "123",
            "score": 5,
            "tags": ["经验丰富", "逻辑能力强"]
        }],
        "result": "ok"
    }

