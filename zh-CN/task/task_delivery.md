---
name: 上传任务作品附件
---
    
### Url
    /weidu/api/v1/task/delivery/work

### Method
    POST

### Content-Type
    application/json      

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"

### Requst Body

    {
        "task_id":"任务ID，数据类型string", 
        "delivery_work_ids":"交付作品附件，多个文件ID用空格分割，数据类型string"
    }


### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
    }

### Response Code
    HTTP/1.1 200 OK

### Example

    curl -X POST "http://127.0.0.1:9004/weidu/api/v1/task/delivery/work" -i -H "Authorization:Bearer ufnaxsk8p7nk8jutpkwhxoette" -d '{"task_id":"wxx64tzq6ifnbcjaoz8gbftgja", "delivery_work_ids":"94psnojrpbft7f9q87nrg9tstr o9a3qoefkt8a5x8e36ib9xj3oe o38iizqeab8utcu5tafcjwnwfo"}'
        HTTP/1.1 200 OK
        Content-Type: application/json
        Date: Thu, 01 Jul 2021 03:43:25 GMT
        Content-Length: 27

    {
        "code":200,
        "result":"ok"
    }