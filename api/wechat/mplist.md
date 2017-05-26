# MpList - 获取公众号列表

**应用场景**

该接口提供当前用户已授权公众号获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/MpList](http://{BaseURL}/OpenPlatform/Login)

**提交方式**

> POST

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| page\_index | 是 | 1 | 当前页，从1开始 |
| page\_size | 是 | 10 | 每页条数，取值范围10~100 |
| sort | 否 | desc | 排序规则，默认按添加时间降序（desc或asc） |
| token | 是 | VmNaqQb2D9ZzCZ+2FrvW+A== | Token令牌 |

**请求参数示例**

> page\_index=1&page\_size=10&token=VmNaqQb2D9ZzCZ+2FrvW+A==

**响应结果**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| code | 是 | String | 状态码 |
| msg | 是 | String | 返回信息 |
| data | 否 | Object | 响应数据 |

以下字段在code为10000时，在data参数中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| records | 是 | Int | 总记录数，若没有数据则为0 |
| pages | 是 | Int | 总页数，若没有数据则为0 |
| rows | 是 | Array | 列表记录，若没有数据则为空数组 |

以下字段在code为10000且rows有数据时，在rows参数中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| mp\_name | 是 | String | 公众号名称 |
| pages | 是 | Int | 总页数，若没有数据则为0 |

**响应结果示例**

```js
......
```



