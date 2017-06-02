# UnbindMP - 解绑公众号

**应用场景**

该接口提供当前用户已授权公众号解绑功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/UnbindMp](http://{BaseURL}/OpenPlatform/Login)

**提交方式**

> POST

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| token | 是 | 00000000-0000-0000-0000-000000000000 | Token令牌 |
| appid | 是 | wx4da448cd29927cb7 | 公众号AppId |

**请求参数示例**

> appid=wx4da448cd29927cb7&token=00000000-0000-0000-0000-000000000000

**响应结果**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| code | 是 | String | 状态码 |
| msg | 是 | String | 返回信息 |

**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success"
}
```



