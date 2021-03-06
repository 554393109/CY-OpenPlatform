# GetUserInfo - 获取用户信息

**应用场景**

该接口提供用户信息获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/GetUserInfo](http://{BaseURL}/OpenPlatform/Login)

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
| data | 否 | Object | 响应数据 |

以下字段在code为10000的时候在data字段中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| ID | 是 | Long | 用户Id |
| Name | 是 | String | 姓名 |
| CompanyName | 是 | String | 公司名称 |
| Phone | 是 | String | 手机号码 |

**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success",
    "data": "{\"Name\":\"YZQ\",\"CompanyName\":\"YZQ-公司名称\",\"ID\":3308444987384064,\"Phone\":\"17076616006\"}"
}
```



