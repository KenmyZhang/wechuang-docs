---
name: 制作任务
---
    
### Url
     /weidu/api/v1/task/implement
    
### Method
    POST

### Content-Type
    application/json      

### 限制
    正式环境需要校验token，token值放在头部参数Authorization, eg： -H "Authorization:Bearer xxxxxx"

    测试环境可以不带token，但需要带上头部参数User-Id, eg: -H "User-Id:123"   

### Requst Body

    {
         "id": "任务id，数据类型int"
    }


### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int"
    }

### Response Code
    HTTP/1.1 200 OK

### Example
