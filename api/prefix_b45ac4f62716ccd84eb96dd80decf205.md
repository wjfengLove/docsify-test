[首页](README.md)

[TOC]
    
##### 简要描述

- 线索与来访趋势-来访量

##### 请求URL
- ` http://172.16.46.125:30843/99c5 `

例：` http://172.16.46.125:30843/99c5?beginDate=2019-09&endDate=2019-11&iid=1&oid=20 `

##### Header
Key：Host     
value：3324-2.ipaas.myqcloud.com
  
##### 请求方式
- GET 

##### 参数

|参数名|类型|说明|是否必传|
|:----    |:----- |:-----   |-----   |
|beginDate |string |开始日期（YYYY-MM）   |是|
|endDate |string |结束日期（YYYY-MM）    |是|
|iid |string |type类型（1=集团id，2=区域id，3=项目群id，4=项目id）    |是|
|oid |string |组织id（与type类型相对应，如果iid=1，传集团id，iid=2，传区域id，iid=3，传项目群id，iid=4，传项目id）    |是|


##### 返回参数说明 

|参数名|类型|说明|规则|
|:-----  |:-----|----- |----- |
|id |bigint   |主键id  |  |
|month_code |varchar   |统计粒度  |  |
|year |varchar   |年  |  |
|month |varchar   |月  |  |
|group_id |varchar   |集团id  |  |
|group_name |varchar   |集团名称  |  |
|area_id |varchar   |区域id  |  |
|area_name |varchar   |区域名称  |  |
|company_id |varchar   |公司id  |  |
|company_name |varchar   |公司名称  |  |
|project_id |varchar   |项目ID  |  |
|project_name |varchar   |项目名称  |  |
|etl_time |datetime   |etl加载时间  |  |
|clue_visit_d_qty |bigint   |线索量  |来访日期 in 查询时间周期内 线索来源不为（全民营销、）  |


##### 返回示例 

``` 
  {
    "error_code": 0,
    "data": {
	  "id":"1",
	  "month_code":"2019-07",
	  "year":"2019",
	  "month":"07",
	  "group_id":"19",
	  "group_name":"浙西区域集团",
	  "area_id":"2450",
	  "area_name":"杭州绿城银湖置业有限公司",
	  "company_id":"7673",
	  "company_name":"杭西片区",
      "project_id": "a979725084af11e88c837cd30a51802e",
	  "project_name":"杭州雲栖桃花源",
	  "clue_visit_d_qty":"1",
	  "etl_time":"2022-07-08 02:40:16.0"
    }
  }
```

##### 备注 

- 更多返回错误代码请看首页的错误代码描述




