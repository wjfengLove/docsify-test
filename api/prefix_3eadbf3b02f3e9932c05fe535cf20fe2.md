[首页](README.md)

[TOC]
    
##### 简要描述

- 线索流失经纪人排行

##### 请求URL
- ` http://172.16.46.125:30843/1ce9 `

例：` http://172.16.46.125:30843/1ce9?beginDate=2021-11&endDate=2022-01&projectid=a3107e92e93011eb81c67cd30ae45b6a `

##### Header
Key：Host     
value：3306-2.ipaas.myqcloud.com
  
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
|:-----  |:-----|-----  |-----  |
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
|followuser_name |varchar   |经纪人  |  |
|off_qty |bigint   |线索来访次数  |流失时间 in 查询时间周期内 转化状态=有效
线索来源不为（全民营销、）|
|etl_time |datetime   |etl加载时间  |  |

##### 返回示例 

``` 
  {
    "error_code": 0,
    "data": {
      "id": "2720",
      "month_code": "2021-10",
      "year": "2021",
      "month": "10" ,
      "project_id": "86",
      "project_name": "杭州山澜桂语轩",
	  "area_id":"5936",
	  "area_name":"杭州绿城浙兴置业有限公司",
	  "company_id":"7674",
	  "company_name":"杭东片区",
	  "group_id":"19",
	  "group_name":"浙西区域集团",
	  "followuser_name":"全民经纪人",
	  "off_qty":"3",
	  "etl_time":"2022-07-08 02:32:51.0"
    }
  }
```

##### 备注 

- 更多返回错误代码请看首页的错误代码描述




