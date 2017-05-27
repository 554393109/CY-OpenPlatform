* [ ] # GetMpMenu - 获取公众号自定菜单

**应用场景**

该接口提供当前用户已授权公众号自定义菜单获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/GetMpMenu](http://{BaseURL}/OpenPlatform/Login)

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
| data | 否 | Object | 响应数据 |

以下字段在code为10000的时候在data字段中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| button | 是 | Array | 一级菜单数组，个数应为1~3个 |

以下字段在button有数据时，在button字段中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| url | 是 | String | 网页链接，用户点击菜单可打开链接，不超过1024字节。type为miniprogram时，不支持小程序的老版本客户端将打开本url |
| type | 否 | String | 菜单的响应动作类型，view表示网页类型，click表示点击类型，miniprogram表示小程序类型；当sub\_button不为空时，该字段不返回 |
| name | 是 | String | 菜单标题，不超过16个字节，子菜单不超过60个字节 |
| sub\_button | 否 | Array | 二级菜单数组，个数应为1~5个 |

以下字段在sub\_button有数据时，在sub\_button参数中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| url | 是 | String | 网页链接，用户点击菜单可打开链接，不超过1024字节。type为miniprogram时，不支持小程序的老版本客户端将打开本url |
| type | 是 | String | 菜单的响应动作类型，view表示网页类型，click表示点击类型，miniprogram表示小程序类型 |
| name | 是 | String | 菜单标题，不超过16个字节，子菜单不超过60个字节 |

**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success",
    "data": "{\"button\":[{\"url\":\"https://www.baidu.com/\",\"type\":\"view\",\"name\":\"一级菜单 1\"},{\"sub_button\":[{\"url\":\"https://www.baidu.com/\",\"type\":\"view\",\"name\":\"二级菜单 2-1\"},{\"url\":\"https://www.baidu.com/\",\"type\":\"view\",\"name\":\"二级菜单 2-2\"},{\"url\":\"https://www.baidu.com/\",\"type\":\"view\",\"name\":\"二级菜单 2-3\"}],\"name\":\"一级菜单 2\"},{\"sub_button\":[{\"url\":\"https://www.baidu.com/\",\"type\":\"view\",\"name\":\"二级菜单 3-1\"},{\"url\":\"https://www.baidu.com/\",\"type\":\"view\",\"name\":\"二级菜单 3-2\"},{\"url\":\"https://www.baidu.com/\",\"type\":\"view\",\"name\":\"二级菜单 3-3\"},{\"url\":\"https://www.baidu.com/\",\"type\":\"view\",\"name\":\"二级菜单 3-4\"}],\"name\":\"一级菜单 3\"}]}"
}
```



