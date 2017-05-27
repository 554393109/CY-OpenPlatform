# MpList - 获取公众号列表

**应用场景**

该接口提供当前用户已授权公众号获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/MpList](http://{BaseURL}/OpenPlatform/Login)

**提交方式**

> POST

**请求参数**

| 参数 | 必填 | 示例值 | 说明 |
| :--- | :--- | :--- | :--- |
| token | 是 | 00000000-0000-0000-0000-000000000000 | Token令牌 |
| page\_index | 是 | 1 | 当前页，取值范围1~N |
| page\_size | 是 | 10 | 每页条数，默认值：10，取值范围1~100 |
| sort | 否 | desc | 排序规则，按添加时间排序，默认desc降序，取值desc、asc |

**请求参数示例**

> page\_index=1&page\_size=10&token=00000000-0000-0000-0000-000000000000

**响应结果**

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| code | 是 | String | 状态码 |
| msg | 是 | String | 返回信息 |
| data | 否 | Object | 响应数据 |

以下字段在code为10000时，在data字段中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| records | 是 | Int | 总记录数，若没有数据则为0 |
| pages | 是 | Int | 总页数，若没有数据则为0 |
| rows | 是 | Array | 列表记录，若没有数据则为空数组 |

以下字段在rows有数据时，在rows字段中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| appid | 是 | String | 公众号AppId |
| nick\_name | 是 | Int | 公众号昵称 |
| user\_name | 是 | String | 公众号原始ID，如：gh\_b86f76c4642e |
| alias | 是 | String | 公众号所设置的微信号，可能为空 |
| head\_img | 是 | String | 公众号头像图片URL |
| qrcode\_url | 是 | String | 公众号二维码图片URL |
| service\_type\_info | 是 | Int | 公众号类型，0代表订阅号，1代表由历史老帐号升级后的订阅号，2代表服务号 |
| verify\_type\_info | 是 | Int | 授权方认证类型，-1代表未认证，0代表微信认证，1代表新浪微博认证，2代表腾讯微博认证，3代表已资质认证通过但还未通过名称认证，4代表已资质认证通过、还未通过名称认证，但通过了新浪微博认证，5代表已资质认证通过、还未通过名称认证，但通过了腾讯微博认证 |
| rq\_create | 是 | Datetime | 授权时间，格式yyyy-MM-dd HH:mm:ss |

**响应结果示例**

```js
{
    "records": 1,
    "pages": 1,
    "rows": [
        {
            "appid": "wx4da448cd29927cb7",
            "nick_name": "广州超赢",
            "user_name": "gh_b76f77c4672e",
            "alias": "chaoyingsoft",
            "head_img": "http://wx.qlogo.cn/mmopen/CSFFlccWvq50C0FD5TgAp7JJe5nqpibbZ6X75EiaHgU95zJaHWYTiaEBHsHzTNRIEE3bUvNGRQ5gVAsZpCY6hZchQnE7Zwe9Etg/0",
            "qrcode_url": "http://mmbiz.qpic.cn/mmbiz_jpg/OdJTgL8MssMvQ6n5iaNRFrrhESre1d2hFTBp2bsM6v4vM9KiacpoXa5OeaK7iaK6ESvdhVRhO7l2tvbiapfuIFxlVQ/0",
            "service_type_info": 2,
            "verify_type_info": 0,
            "rq_create": "2017-05-26T15:26:33.207"
        }
    ]
}
```



