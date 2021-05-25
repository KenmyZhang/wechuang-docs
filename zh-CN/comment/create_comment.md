---
name: 评论
---
    
### Url
    /weidu/api/v1/comment
    
### Method
    POST

### Content-Type
    application/json    

### Request Payload
    {
        "res_type":"资源类型：设计师 1、优秀案例2  数据类型string,必填",
        "res_id": "资源ID，数据类型string,必填",
        "content": "内容，数据类型string,必填"
    }

### 限制
    需要登录带上token，eg: -H "Authorization:Bearer xxxxx" 

### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int"
    }

### Example

    curl -X POST "http://0:9004/weidu/api/v1/comment" -i -d '{"res_type":1, "res_id":"szasc68seig9jrhqw4eaj9gu3h", "content":"123"}' -H "User-Id:b1onnbw3ebbjtenaco9fxa16k3"
        HTTP/1.1 201 Created
        Content-Type: application/json; charset=utf-8
        Date: Mon, 08 Feb 2021 03:00:58 GMT
        Content-Length: 27

    {
        "code":200,
        "result":"ok"
    }
 


