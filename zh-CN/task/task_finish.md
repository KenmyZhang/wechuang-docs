---
name: 甲方确认任务完成
---
    
### Url
    /weidu/api/v1/task/finish
    
### Method
    POST

### Content-Type
    application/json      

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"

### Requst Body

    {
         "task_id": "任务id，数据类型int"
    }


### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
    }

### Response Code
    HTTP/1.1 200 OK

### Example

    curl -X POST "http://0:9004/weidu/api/v1/task/finish" -i -d '{"task_id":"5trb5tu7tj8kfe7gwk7qakfpac"}' -H "Authorization:Bearer cspaasq3qies389w3eenwi9ano"
        HTTP/1.1 200 OK
        Content-Type: application/json
        Date: Sun, 16 May 2021 06:20:50 GMT
        Content-Length: 233

    {
        "code": 200,
        "result": "ok"
    }