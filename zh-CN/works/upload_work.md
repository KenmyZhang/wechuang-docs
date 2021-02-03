---
name: 上传个人作品
---
    
### Url
    /weidu/api/v1/files
    
### Method
    POST

### Content-Type
    application/json    

### Query Param
    "user_id": "用户id，数据类型string"

### Form Param
    "files": "文件路径"    

### 限制
    需要登录带上token，eg: -H "Authorization:Bearer xxxxx" ;测试环境可以不带
    
### Response Body
    {
        "result": "成功返回ok，否则返回相应错误详情，数据类型string",
        "code": "成功返回200，否则返回其他错误码，数据类型int",
    	"data": {
        		"file_infos": [{
        		"id": "文件id，数据类型string",
        		"user_id": "用户id，数据类型string",
        		"create_time": "创建时间，unix时间戳单位ms，数据类型int",
        		"update_time": "更新时间，unix时间戳单位ms，数据类型int",
        		"path": "文件路径，数据类型string",
                "preview_path": "预览图路径，数据类型string",
        		"name": "文件名，数据类型string",
        		"extension": "文件后缀，数据类型string",
        		"size": "文件大小，数据类型int",
        		"mime_type": "文件类型，数据类型string"
        	}]
        }
    }
    

### Example

   curl -X POST "http://127.0.0.1:9004/weidu/api/v1/files?user_id=rfeaxzb4etf58cia8i6ha1jwgw"  -F "files=@/Users/zhangkunming/go/src/wechuang/data/docs/TOC.ini" -i

    HTTP/1.1 100 Continue
    HTTP/1.1 201 Created
    Content-Type: application/json; charset=utf-8
    Date: Tue, 06 Oct 2020 12:54:27 GMT
    Content-Length: 363

    {
    	"code": 200,
    	"data": {
    		"file_infos": [{
    			"id": "hhtfwf9zrifu8f7rsuh36bkgjw",
    			"user_id": "rfeaxzb4etf58cia8i6ha1jwgw",
    			"create_time": 1601988867705,
    			"update_time": 1601988867705,
    			"path": "20201006/users/rfeaxzb4etf58cia8i6ha1jwgw/hhtfwf9zrifu8f7rsuh36bkgjw/TOC.ini",
    			"preview_path": "",
    			"name": "TOC.ini",
    			"extension": "ini",
    			"size": 706,
    			"mime_type": ""
    		}]
    	},
    	"result": "ok"
    }
    
 