[首页](README.md)

[TOC]
    
##### 简要描述

- 客户意向决定性指标

##### 请求URL
- ` http://172.16.46.125:30843/d141?statday=2022-06-21&projectid=9c1b1a0e7637ea11a8279cfd06e72529&phone=18067592565&oneid=1895a375cf1903800aa002dd2c9a2efb `

##### Header
Key: Host   
value: 3330-2.ipaas.myqcloud.com
  
##### 请求方式
- GET 

##### 参数

|参数名|类型|说明|是否必填|
|:----    |:----- |-----   |-----   |
|statday |string |数据日期（YYYY-MM-DD）   |是|
|projectid |string |项目id   |是|
|phone |string |手机号    |是|
|oneid |string |one_id    |否|



##### 返回参数说明 

|参数名|类型|说明|备注|
|:-----  |:-----|----- |----- |
|id |int   |主键ID  |                        |
|one_id |varchar   |one_id  |                        |
|uid |varchar   |客户ID  |                        |
|user_phone |varchar   |手机号  |                        |
|project_id |varchar   |项目ID  |                        |
|project_name |varchar   |项目名称  |                        |
|is_owner |varchar   |绿城业主  |等级：普通、良好、优质、null|
|subscribe_visit_online |varchar   |线上预约到访  |等级：普通、null|
|subscribe_advertising_online |varchar   |线上广告预约  |等级：普通、null|
|incoming_call |varchar   |来电  |等级：普通、null|
|other_project_visit |varchar   |其他项目有到访  |等级：普通、良好、优质、null|
|other_project_counsel |varchar   |其他项目有咨询  |等级：普通、null|
|active_online |varchar   |线上活跃  |等级：普通、null|
|add_WeCom |varchar   |添加企微  |等级：普通、null|
|etl_time |datetime   |etl时间  |                        |
|stat_date |varchar   |数据时间  |时间：yyyy-mm-dd|

##### 返回示例 

``` 
  {
    "error_code": 0,
    "data": {
      "id": "37263074",
	  "uid": "000122B5-1067-4141-9016-D3C1CC209371",
      "one_id": "0a7a7b9e5febc4681f7f3b7f5c156699",
      "user_phone": "18106556784",
      "project_id": "ff1418af6c8fea11a8279cfd06e72529",
	  "project_name":"宁波春月金沙",
	  "is_owner":"良好",
	  "subscribe_visit_online":"",
	  "subscribe_advertising_online":"",
	  "incoming_call":"",
	  "other_project_visit":"",
	  "other_project_counsel":"",
	  "add_WeCom":"",
	  "etl_time":"2022-06-22 04:34:44.391",
	  "stat_date":"2022-06-21"
    }
  }
```

##### 备注 

- 更多返回错误代码请看首页的错误代码描述




