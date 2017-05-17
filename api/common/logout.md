# Logout - 登出

**应用场景**

该接口提供用户登出。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/Logout](http://{BaseURL}/OpenPlatform/Login)

###### 

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| token | 是 | VmNaqQb2D9ZzCZ+2FrvW+A== | Token令牌 |



**请求参数示例**

> token=VmNaqQb2D9ZzCZ+2FrvW+A==



**响应结果**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| code | 是 | String | 状态码 |
| msg | 是 | String | 返回信息 |
| data | 否 | Object | 响应数据 |

以下字段在code为10000的时候在data参数中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| redirect\_uri | 否 | String | 回调地址 |



**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success",
    "data": "{\"redirect_uri\":\"http://{BaseURL}/Login\"}"
}
```



