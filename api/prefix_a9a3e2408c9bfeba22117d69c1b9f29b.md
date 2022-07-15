[首页](README.md)

[TOC]
    
##### 简要描述

- 经纪人来访排行

##### 请求URL
- ` http://172.16.46.125:30843/df17 `

例：` http://172.16.46.125:30843/df17?beginDate=2019-09&endDate=2019-11&projectid=5edc0ac3354611eb81c67cd30ae45b6a `

##### Header
Key：Host     
value：3302-2.ipaas.myqcloud.com
  
##### 请求方式
- GET 

##### 参数

|参数名|类型|说明|是否必传|
|:----    |:----- |:-----   |-----   |
|beginDate |string |开始日期（YYYY-MM）   |是|
|endDate |string |结束日期（YYYY-MM）    |是|
|projectid |string |项目id    |是|


##### 返回参数说明 

|参数名|类型|说明|规则|
|:-----  |:-----|----- |----- |
|id |int   |主键ID  |  |
|month_code |varchar   |统计粒度  |  |
|year |varchar   |年  |  |
|month |varchar   |月  |  |
|project_id |varchar   |项目ID  |  |
|project_name |varchar   |项目名称  |  |
|area_id |varchar   |区域ID  |  |
|area_name |varchar   |区域名称  |  |
|company_id |varchar   |项目群ID  |  |
|company_name |varchar   |项目群  |  |
|group_id |varchar   |集团ID  |  |
|group_name |varchar   |集团  |  |
|etl_time |datetime   |etl加载时间  |  |
|followuser_name |varchar   |经纪人  |  |
|vist_qty |bigint   |到访人数  |求和|


##### 返回示例 

``` 
  {
    "error_code": 0,
    "data": {
      "id": "1",
      "month_code": "2019-08",
      "year": "2019",
      "month": "08" ,
      "project_id": "202948",
      "project_name": "青岛理想之城",
	  "area_id":"354",
	  "area_name":"青岛绿城华川置业有限公司",
	  "company_id":"4827",
	  "company_name":"青岛项目群",
	  "group_id":"24",
	  "group_name":"中原区域公司",
	  "followuser_name":"黄丽容",
	  "vist_qty":"1",
	  "etl_time":"2022-07-08 02:32:51.0"
    }
  }
```

##### 备注 

- 更多返回错误代码请看首页的错误代码描述




