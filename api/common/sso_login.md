# SSO\_Login - 单点登录入口

**应用场景**

该接口提供用户验证，从各业务系统进入开放平台需要带上参数；不带参数时跳转用户系统进行统一登录。

登录成功后将重定向至开放平台。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/SSO\_Login](http://{BaseURL}/OpenPlatform/Login)

**提交方式**

> GET

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| token | 否 | 00000000-0000-0000-0000-000000000000 | Token令牌 |
| sign | 否 | d5a4145d8dbdb0e5e28cbfafc35c22c3 | 签名（Token存在时必须传入sign才能通过验证，否则会跳转用户系统进行统一登录） |

**请求参数示例**

> token=00000000-0000-0000-0000-000000000000&sign=d5a4145d8dbdb0e5e28cbfafc35c22c3

**响应结果（Cookie）**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| Cysoft\_OpenPlatform\_Token | 是 | String | Token |

**响应结果示例**

> Cysoft\_OpenPlatform\_Token=00000000-0000-0000-0000-000000000000



