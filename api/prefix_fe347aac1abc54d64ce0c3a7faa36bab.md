[首页](README.md)

[TOC]
    
##### 简要描述

- 项目成交排名

##### 请求URL
- ` http://172.16.46.125:30843/e02b `

例：` http://172.16.46.125:30843/e02b?beginDate=2021-04&endDate=2022-08&areaid=7734 `

##### Header
Key：Host     
value：3297-2.ipaas.myqcloud.com
  
##### 请求方式
- GET 

##### 参数

|参数名|类型|说明|是否必传|
|:----    |:----- |:-----   |-----   |
|beginDate |string |开始日期（YYYY-MM）   |是|
|endDate |string |结束日期（YYYY-MM）    |是|
|areaid |string |区域id    |是|



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
|cust_qty |bigint   |成交人数  |认购审核时间 in 查询时间周期内 转化状态=有效 产品业态！=车位and仓储 线索来源不为（全民营销、）如果跳过认购直签的客户也算成交|
|room_qty |bigint   |成交套数  |认购审核时间 in 查询时间周期内 转化状态=有效 产品业态不为（车位and仓储）线索来源不为（全民营销、）如果跳过认购直签的客户也算成交|
|transaction_amt |decimal   |成交金额  |认购审核时间 in 查询时间周期内 线索状态=有效 产品业态！=车位and仓储 线索来源不为（全民营销、）如果跳过认购直签的客户也算成交|


##### 返回示例 

``` 
  {
    "error_code": 0,
    "data": {
      "id": "51",
      "month_code": "2022-04",
      "year": "2022",
      "month": "04" ,
      "project_id": "391",
      "project_name": "西安桂语云境",
	  "area_id":"6846",
	  "area_name":"西咸新区汇绿景意房地产开发有限公司",
	  "company_id":"7472",
	  "company_name":"北部片区",
	  "group_id":"5271",
	  "group_name":"西安城市公司",
	  "cust_qty":"1",
	  "room_qty":"1",
	  "transaction_amt":"0.000000",
	  "etl_time":"2022-07-08 02:34:13.0"
    }
  }
```

##### 备注 

- 更多返回错误代码请看首页的错误代码描述




