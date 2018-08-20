# GetComponentInfo - 获取开放平台授权信息

**应用场景**

该接口提供当前用户已授权公众号开放平台授权信息获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/GetComponentInfo](http://{BaseURL}/OpenPlatform/Login)

**提交方式**

> POST

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| appid | 是 | wx4da448cd29927cb7 | 公众号AppId |
| sign | 是 | 00000000000000000000000000000000 | 签名 |

**请求参数示例**

> appid=wx4da448cd29927cb7&sign=00000000000000000000000000000000

**响应结果**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| code | 是 | String | 状态码 |
| msg | 是 | String | 返回信息 |
| data | 否 | Object | 响应数据 |

以下字段在code为10000的时候在data字段中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| component\_appid | 是 | String | 开放平台AppId |
| component\_access\_token | 是 | String | 开放平台AccessToken |

**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success",
    "data": "{\"component_appid\":\"wx733b4b22562e3596\",\"component_access_token\":\"h4AON8jEElwMJ0PeOBC3HjMAvlGwyJrY3CjcaBVOeOGIBoB7Zro6G3PrkSYQmcdUU_IWBDh0K1yhb3yMV7DEWhUlLacdhVWd-BVJgynS4Djql3OuZva7DdOYj75f5-3WOBXgAEAERM\"}"
}
```



