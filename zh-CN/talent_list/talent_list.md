---
name: 人才列表
---
    
### Url
    /weidu/api/v1/users/talents/list
    
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
        "data": {
            "user_id": "用户ID，数据类型string",
            "avatar_url": "头像地址，数据类型string",
            "nickname": "昵称，数据类型string",
            "workyear": "工作年限，数据类型int",
            "user_type": "用户类型，1独立设计师 2小型工作室 3项目总监，数据类型int",
            "work_experience": "工作经验，数据类型string",
            "level": "信用等级，数据类型string",
            "score": "评分，数据类型float",
            "industry": "行业，数据类型int", //游戏
            "type": "类型，数据类型int", //原画 UI 产品
            "work_list": [{
                "id": "作品id，数据类型string",
                "user_id": "用户ID，数据类型string",
                "name": "项目名字，数据类型string",
                "type": "项目类型，1游戏 2动漫 3漫画 4广告 5界面 6LOGO,数据类型int",
                "belong_type": "项目归属，1个人 2团队合作，数据类型int",
                "link": "项目链接，数据类型string",
                "file_infos": [{
                    "id": "作品文件ID，数据类型string",
                    "user_id": "用户ID，数据类型string",
                    "path": "文件作品路径，数据类型string",
                    "preview_path": "作品预览路径，数据类型string",
                    "name": "作品文件名称，数据类型string",
                    "extension": "作品后缀，数据类型string",
                    "size": "作品大小，数据类型int",
                    "mime_type": "作品的mime type，数据类型string",
                    "width": "作品宽度，数据类型int",
                    "height": "作品高度，数据类型int",
                    "has_pre_img": "是否有预览图，数据类型bool"
                }]
            }]
        }
    }

### Example

    curl -X GET "http://8.134.37.138:9004/weidu/api/v1/users/talents/list?per_page=10" -i

   {
	"code": 200,
	"data": [{
		"user_id": "szasc68seig9jrhqw4eaj9gu3h",
		"workyear": 0,
		"avatar_url": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
		"nick_name": "1150911",
		"user_type": 1,
		"industry": 0,
		"type": 0,
		"work_experience": "工作经验",
		"score": 70,
		"work_list": [{
			"id": "45gbin1qn78a3fajrx3rub1upc",
			"user_id": "szasc68seig9jrhqw4eaj9gu3h",
			"name": "project name2",
			"type": 0,
			"belong_type": 1,
			"link": "www.baidu.com/",
			"file_infos": [{
				"id": "biinjhnesifeiasftws8a6q95r",
				"task_id": "5trb5tu7tj8kfe7gwk7qakfpac",
				"user_id": "erb4krcbbirbtcwnhwopeizz5o",
				"path": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi.jpg",
				"preview_path": "20201004/users/123/biinjhnesifeiasftws8a6q95r/jianzhi_preview.jpg",
				"name": "jianzhi.jpg",
				"extension": "jpg",
				"size": 34348,
				"mime_type": "image/jpeg",
				"width": 500,
				"height": 333,
				"has_pre_img": true
			}, {
				"id": "h8n5hftujtgpen8aqnqseec57a",
				"user_id": "rfeaxzb4etf58cia8i6ha1jwgw",
				"path": "20201006/users/rfeaxzb4etf58cia8i6ha1jwgw/h8n5hftujtgpen8aqnqseec57a/.",
				"name": ".",
				"extension": "",
				"size": 0,
				"mime_type": ""
			}, {
				"id": "hhtfwf9zrifu8f7rsuh36bkgjw",
				"user_id": "rfeaxzb4etf58cia8i6ha1jwgw",
				"path": "20201006/users/rfeaxzb4etf58cia8i6ha1jwgw/hhtfwf9zrifu8f7rsuh36bkgjw/TOC.ini",
				"name": "TOC.ini",
				"extension": "ini",
				"size": 706,
				"mime_type": ""
			}]
		}]
	}],
	"result": "ok",
	"total": 18
}