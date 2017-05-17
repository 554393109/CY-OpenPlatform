# 协议规则

| 规则 |  |
| :--- | :--- |
| 传输方式 | 为保证交易安全性，采用HTTPS传输（开发时可使用HTTP） |
| 提交方式 | 采用POST方法提交 |
| 数据格式 | 提交和返回数据都为JSON格式 |
| 字符编码 | 统一采用UTF-8字符编码 |
| 内容类型 | 统一采用x-www-form-urlencoded编码格式 |

# 参数示例

调用成功：

```js
{
    "code": 10000,
    "msg": "Success",
    "data": {
        "nick_name": "aaa",
        "head_img": "http://pos.cn/data/upload/201704/f_1e228c017071b7290c357a22244616d0.jpg",
        "token": "VmNaqQb2D9ZzCZ+2FrvW+A=="
    }
}
```



