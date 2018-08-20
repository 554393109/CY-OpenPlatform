# GetAccessToken - 获取公众号AccessToken

**应用场景**

该接口提供当前用户已授权公众号AccessToken获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/GetAccessToken](http://{BaseURL}/OpenPlatform/Login)

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
| authorizer\_access\_token | 是 | String | 授权方AccessToken |

**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success",
    "data": "{\"authorizer_access_token\":\"UFDZ496N8091TmHlSi37ugERpEL5xYGo-229WYydZjGDHUL6xnfkHoRwdQhIAZL_lutCCRksK3fY33lKRvLBM_oGFMDpbPCRP5P_gR_z_QAY-vZiK6YbRORYRuK8z9_JXRVaAEDTNR\"}"
}
```



