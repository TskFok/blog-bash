---
title: elasticsearch
date: 2022-06-20 13:56:35
tags: elasticsearch
categories: elasticsearch
pic: 'elasticsearch.png'
---

### elasticsearch的查询命令行

<!-- more -->

````
查看所有索引
curl -X GET "http://host:port/_cat/indices/?v"
````

````
查看某个索引
curl -X GET "http://host:port/_cat/indices/index*?v"
````

````
查看index下的10条记录
curl -X GET "http://host:port/index/_search"
````

````
查看index的数量
curl -X GET "http://host:port/index/_count"
````

````
查看index的订单123123123123123
curl -X GET "http://host:port/index/_doc/123123123123123?pretty"
````

````
查看index的订单 根据order_no查看123123123123123
curl -X GET "http://host:port/index/_search?q=order_no:123123123123123"
````

````
查看index的订单 search_key=data
curl -X GET "http://host:port/index/_search" -H "Content-Type: application/json" -d '
{
"query": {
"match": {
"search_key": "data"
}
},
"size": 5
}'
````

````
查看index的订单 search_key1=123123123123123 or search_key2=123123123123123
curl -X GET "http://host:port/index/_search" -H "Content-Type: application/json" -d '
{
"query": {
"multi_match": {
"query":"123123123123123",
"fields": ["search_key1", "search_key2"]
}
},
"size": 5
}'
````