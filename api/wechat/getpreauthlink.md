# GetPreAuthLink - 获取预授权地址

**应用场景**

该接口提供用户对公众号授权地址获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/GetPreAuthLink](http://{BaseURL}/OpenPlatform/Login)

###### 

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| token | 是 | VmNaqQb2D9ZzCZ+2FrvW+A== | Token令牌 |
| redirect\_page | 是 | /mplist | 授权成功回调页面 |

**请求参数示例**

> redirect\_page=/mplist&token=VmNaqQb2D9ZzCZ+2FrvW+A==

**响应结果**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| code | 是 | String | 状态码 |
| msg | 是 | String | 返回信息 |
| data | 否 | Object | 响应数据 |

以下字段在code为10000的时候在data参数中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| link | 是 | String | 授权地址 |

**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success",
    "data": "{\"link\":\"https://mp.weixin.qq.com/cgi-bin/componentloginpage?component_appid=wx733b4b22562e3596&pre_auth_code=preauthcode%40%40%40NaOhkuLMmzmZwwQ0lMkzlABCKPKBd1TTAnbNZ1TIcat2zSat5_D9shcka2pXy1tV&redirect_uri=http%3A%2F%2Fyinziqiang.oicp.net%2FOpenPlatform%2FOAuthCallback%3Fredirect_page%3D%252fmplist\"}"
}
```



