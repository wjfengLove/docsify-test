[首页](README.md)

[TOC]
    
##### 简要描述

- 业务赋能
- 基于实际营销业务发生过程，客户数据中台提供过程中相关的关键客户数据、客户标签实时精准输出能力，辅助业务执行层在实际业务中高效完成客户判客、跟客和运营。如在实际营销业务发生过程中，根据线索/客户的历史数据、实时线上线下行为数据输出线索/客户的相关数据、意向标签，帮助经纪人/置业顾问了解客户，从而制定合适的跟进和沟通引导策略；
##### 请求URL
- ` http://172.16.46.125:30843/9afc?project_id=300&user_phone=13405416688&oneid=0005742a5d4524f14fce847582b37f67 `

##### Header
Key: Host   
value: 3322-2.ipaas.myqcloud.com
  
##### 请求方式
- GET 

##### 参数

|参数名|类型|说明|是否必填|
|:----    |:----- |-----   |-----   |
|project_id |string |项目id   |是|
|user_phone |string |手机号    |是|
|oneid |string |one_id    |否|



##### 返回参数说明 

|参数名|类型|说明|规则|
|:-----  |:-----|----- |
|id |int   |主键ID  |  |
|one_id |varchar   |one_id  |  |
|uid |varchar   |客户ID  |  |
|user_name |varchar   |客户姓名  |  |
|user_phone |varchar   |手机号  |  |
|project_id |varchar   |项目ID  |  |
|project_name |varchar   |项目名称  |  |
|project_name_quarter |varchar   |客户近3个月到访楼盘（项目）  |3个月内：到访过的楼盘|
|project_name_half |varchar   |客户近6个月到访楼盘（项目）   |6个月内：到访过的楼盘|
|opinions_area |varchar   |意向楼盘城市/区域  |近期：近一个月内；浏览过的楼盘所在区域|
|opinions_project |varchar   |意向楼盘（项目）  |近期：近一个月内；频次：浏览>=3次的楼盘|
|valid_wake_pub_clue |varchar   |可唤醒公客  |当前无效的客户；(客户跟进状态：失效) 时间：近一个月内； 浏览行为：有过主动咨询 / 有过主动预约 / 主动+经纪人企微 /通过广告页面进行预约/ 浏览楼盘详情(已包含二级页面)≥20s /浏览经纪人名片≥5s / 浏览广告≥20s / 通过扫码进入楼盘详情 |
|cloud_ad |varchar   |是否浏览广告（是/否）  |浏览广告|
|cloud_meet |varchar   |预约时间  |预约情况|
|cloud_counsel |varchar   |是否咨询  |是否咨询|
|other_project_owner |int   |是否其他楼盘业主  |否：否；是：客户在绿城购买过的楼盘名称（项目）|
|cust_interval_action |int   |跟进间隙客户行为  |时间：>上次跟进时间 行为：有过主动咨询 / 有过主动预约 / 主动+经纪人企微 /通过广告页面进行预约/|

##### 返回示例 

``` 
  {
    "error_code": 0,
    "data": {
      "id": "1",
      "one_id": "00002154e803eb148f340543eb3fd85a",
      "uid": "255a2fe45b2e4d268489f11b1b5685ad",
      "user_name": "王" ,
      "user_phone": "18667159700",
      "project_id": "242",
	  "project_name":"杭州亚运村运动员村",
	  "project_name_quarter":"",
	  "project_name_half":"",
	  "opinions_area":"",
	  "valid_wake_clue":"",
	  "valid_wake_pub_clue":"",
	  "cloud_ad":"",
	  "cloud_meet":"",
	  "cloud_counsel":"",
	  "other_project_owner":"否",
	  "cust_interval_action":""
    }
  }
```

##### 备注 

- 更多返回错误代码请看首页的错误代码描述




