---
name: 评分
---
    
### Url
    /weidu/api/v1/score
    
### Method
    POST

### Content-Type
    application/json    

### Request Payload
    {
        "res_type":"资源类型：设计师 1、优秀案例2  数据类型string,必填", 
        "res_id": "资源ID，数据类型string,必填",
        "score": "分数, 数据类型float，必填"
    }

### 限制
    需要登录带上token，eg: -H "Authorization:Bearer xxxxx" ;


### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int"
    }

### Example

      curl -X POST "http://8.134.37.138:9004/weidu/api/v1/score" -i -H "Authorization:Bearer 8r79se5kwff5xg9tr6pxctinpr" -d '{"res_id":"ow4rxntfgbetifiaoxoza8w53e", "res_type":1, "score":10}'
            HTTP/1.1 201 Created
            Content-Type: application/json
            Date: Sun, 23 May 2021 07:48:35 GMT
            Content-Length: 27

        {
            "code":200,
            "result":"ok"
        }
 


