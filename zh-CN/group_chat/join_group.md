
---
name: 入群
---
    
### Url
    /weidu/api/v1/group/join

### Method
    POST

### Content-Type
    application/json      

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"

### Requst Body

    {
        "task_id":"任务ID，数据类型string"
    }


### Response Body
    {
        "group_id": "群组id，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
    }

### Response Code
    HTTP/1.1 200 OK

### Example

    curl -X POST "http://127.0.0.1:9004/weidu/api/v1/group/join" -i -d '{"task_id": "wxx64tzq6ifnbcjaoz8gbftgja"}' -H "Authorization:Bearer ufnaxsk8p7nk8jutpkwhxoette"
        HTTP/1.1 201 Created
        Content-Type: application/json
        Date: Thu, 01 Jul 2021 03:46:04 GMT
        Content-Length: 37

    {
        "code":200,
        "group_id":"3883770878"
    }