# MenuList - 获取系统菜单

**应用场景**

该接口提供左侧系统菜单获取功能。

###### 

**接口链接**

> [http://{BaseURL}/OpenPlatform/MenuList](http://{BaseURL}/OpenPlatform/Login)

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
| data | 否 | Array | 响应数据 |

以下字段在code为10000的时候在data参数中返回

| 字段名 | 必填 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| menu | 是 | String | 菜单名称 |
| ico | 否 | String | 菜单图标CSS名 |
| link | 否 | String | 地址 |
| sub | 否 | Array | 子菜单，结构相同 |



**响应结果示例**

```js
{
    "code": "10000",
    "msg": "Success",
    "data": "[{\"menu\":\"一级菜单\",\"link\":\"menu_list\"},{\"menu\":\"一级菜单2\",\"ico\":\"ico_mp\",\"sub\":[{\"menu\":\"二级菜单2-1\",\"link\":\"sub_menu_list-1\"},{\"menu\":\"二级菜单2-2\",\"link\":\"sub_menu_list-2\"}]}]"
}
```



