[首页](README.md)

[TOC]
    
##### 简要描述

- 线索次数

##### 请求URL
- ` http://172.16.46.125:30843/ac3c `

例：` http://172.16.46.125:30843/ac3c?beginDate=2020-02-09&endDate=2020-02-10&iid=4&oid=1097338 `

##### Header
Key：Host     
value：3321-2.ipaas.myqcloud.com
  
##### 请求方式
- GET 

##### 参数

|参数名|类型|说明|是否必填|
|:----    |:----- |:-----  ||-----   |
|beginDate |string |开始日期（YYYY-MM-DD）   |是|
|endDate |string |结束日期（YYYY-MM-DD）    |是|
|iid |string |type类型（1=集团id，2=区域id，3=项目群id，4=项目id）    |是|
|oid |string |组织id（与type类型相对应，如果iid=1，传集团id，iid=2，传区域id，iid=3，传项目群id，iid=4，传项目id）    |是|


##### 返回参数说明 

|参数名|类型|说明|规则|
|:-----  |:-----|----- |----- |
|project_id |varchar   |项目ID  |  |
|project_name |varchar   |项目名称  |  |
|area_id |varchar   |区域id  |  |
|area_name |varchar   |区域名称  |  |
|company_id |varchar   |公司id  |  |
|company_name |varchar   |公司名称  |  |
|group_id |varchar   |集团id  |  |
|group_name |varchar   |集团名称  |  |
|get_clue_qty |varchar   |线索次数  |线索获取时间 in 查询时间周期  线索来源不为（主动预约、全民营销）|

##### 返回示例 

``` 
  {
    "error_code": 0,
    "data": {
      "project_id": "035fa4cd626e11e9b7fd7cd30ae08090",
	  "project_name":"舟山沁园",
	  "area_id":"3875",
	  "area_name":"舟山市定海绿城昭祥房地产开发有限公司",
	  "company_id":"2967",
	  "company_name":"直管项目",
	  "group_id":"5",
	  "group_name":"绿城小镇集团（小镇事业部）",
	  "get_clue_qty":"7"
    }
  }
```

##### 备注 

- 更多返回错误代码请看首页的错误代码描述




