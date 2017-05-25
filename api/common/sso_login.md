# SSO\_Login - 单点登录入口

**应用场景**

该接口提供用户验证，从各业务系统进入开放平台需要带上参数；不带参数时跳转用户系统进行统一登录。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/SSO\_Login](http://{BaseURL}/OpenPlatform/Login)

**提交方式**

> GET

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| token | 否 | d7550b92-ec5b-4b63-b8f7-2a8528bf4d5b | Token令牌 |
| sign | 否 | d5a4145d8dbdb0e5e28cbfafc35c22c3 | 签名（Token存在时必须传入sign才能通过验证，否则会跳转用户系统进行统一登录） |

**请求参数示例**

> token=d7550b92-ec5b-4b63-b8f7-2a8528bf4d5b&sign=d5a4145d8dbdb0e5e28cbfafc35c22c3

**响应结果（Cookie）**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| Cysoft\_OpenPlatform\_Token | 是 | String | Token |

**响应结果示例**

```js
Cysoft_OpenPlatform_Token=d7550b92-ec5b-4b63-b8f7-2a8528bf4d5b
```



