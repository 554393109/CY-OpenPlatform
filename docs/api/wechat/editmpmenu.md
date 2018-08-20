# EditMpMenu - 修改公众号自定义菜单

**应用场景**

该接口提供当前用户已授权公众号自定义菜单修改功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/EditMpMenu](http://{BaseURL}/OpenPlatform/Login)

**提交方式**

> POST

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| token | 是 | 00000000-0000-0000-0000-000000000000 | Token令牌 |
| appid | 是 | wx4da448cd29927cb7 | 公众号AppId |
| menu | 是 | {"button":\[{"url":"https://www.baidu.com/","type":"view","name":"一级菜单 1"},{"sub\_button":\[{"url":"https://www.baidu.com/","type":"view","name":"二级菜单 2-1"}\],"name":"一级菜单 2"}\]} | 自定义菜单json字符串 |

**请求参数示例**

> appid=wx4da448cd29927cb7&menu={"button":\[{"url":"https://www.baidu.com/","type":"view","name":"一级菜单 1"},{"sub\_button":\[{"url":"https://www.baidu.com/","type":"view","name":"二级菜单 2-1"}\],"name":"一级菜单 2"}\]}&token=00000000-0000-0000-0000-000000000000

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



