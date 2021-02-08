---
name: 新增浏览数
---
    
### Url
    /weidu/api/v1/view  (需要根据ip来去重)
    
### Method
    POST

### Content-Type
    application/json    

### Request Payload
    {
        "res_type":"资源类型, 数据类型string,必填",
        "res_id": "资源ID，数据类型string,必填"
    }

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int"
    }

### Example

    curl -X POST "http://0:9004/weidu/api/v1/view" -i -d '{"res_id":"esbng8qjsfn5jr355ikcr4aajr", "res_type":1}' -H "User-Id:esbng8qjsfn5jr355ikcr4aaj2"
        HTTP/1.1 201 Created
        Content-Type: application/json; charset=utf-8
        Date: Mon, 08 Feb 2021 08:27:19 GMT
        Content-Length: 27

    {
        "code":200,
        "result":"ok"
    }
 


