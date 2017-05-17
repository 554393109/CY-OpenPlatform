# 协议规则

| 规则 | 描述 |
| :--- | :--- |
| 传输方式 | 为保证交易安全性，采用HTTPS传输（开发时可使用HTTP） |
| 提交方式 | 采用POST方法提交 |
| 数据格式 | 提交和返回数据都为JSON格式 |
| 字符编码 | 统一采用UTF-8字符编码 |
| 内容类型 | 统一采用x-www-form-urlencoded编码格式 |

# 签名验证



# 返回格式

| 参数名 | 类型 | 描述 |
| :--- | :--- | :--- |
| code | String | 状态码，10000-成功，10001-错误，10002-令牌无效 |
| msg | String | 返回信息，若调用失败则为错误原因 |
| data | Struct | 当调用成功或接口有具体数据响应，则有返回，类型不确定。 |
| sign | String | 签名 |

###### 成功示例

```js
{
    "code": "10000",
    "msg": "Success",
    "data": {
        "nick_name": "aaa",
        "head_img": "http://pos.cn/data/upload/201704/f_1e228c017071b7290c357a22244616d0.jpg",
        "token": "VmNaqQb2D9ZzCZ+2FrvW+A=="
    }
}
```

###### 失败示例

```js
{
    "code": "10001",
    "msg": "密码不能为空",
    "sign": "BEAD90B01728016E0B4C8024300B644D"
}
```



