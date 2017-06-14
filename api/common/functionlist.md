# FunctionList - 获取菜单功能列表

**应用场景**

该接口提供公众号自定义菜单功能列表获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/FunctionList](http://{BaseURL}/OpenPlatform/Login)

**提交方式**

> POST

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| token | 是 | 00000000-0000-0000-0000-000000000000 | Token令牌 |

**请求参数示例**

> token=00000000-0000-0000-0000-000000000000

**响应结果**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| code | 是 | String | 状态码 |
| msg | 是 | String | 返回信息 |
| data | 否 | Array | 响应数据 |

以下字段在code为10000的时候在data字段中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| name | 是 | String | 功能名称 |
| code | 是 | String | 功能编码 |
| url | 是 | String | 地址 |
| parameters | 否 | Array | 功能参数 |

以下字段在parameters有数据时，在parameters参数中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| param\_name | 是 | String | 参数名称 |
| param\_code | 是 | String | 参数编码 |

**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success",
    "data": "[{\"name\":\"微商城\",\"code\":\"wxshop\",\"url\":\"http://www.dhy.hk/MobileOrderGoods/List?id_user={id_user}\",\"parameters\":[{\"param_name\":\"用户编号\",\"param_code\":\"id_user\"}]},{\"name\":\"进货下单\",\"code\":\"wxorder\",\"url\":\"http://www.dhy.hk/MobileOrderGoods/List?id_user={id_user}&id_xtx={id_xtx}\",\"parameters\":[{\"param_name\":\"用户编号\",\"param_code\":\"id_user\"},{\"param_name\":\"小推侠编号\",\"param_code\":\"id_xtx\"}]}]"
}
```



