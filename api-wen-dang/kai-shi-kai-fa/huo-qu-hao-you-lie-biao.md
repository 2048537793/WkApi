# 获取好友列表

{% hint style="info" %}
* **获取好友列表之前必须调用**[**初始化好友列表接口。**](https://docs.wkteam.cn/api-wen-dang/kai-shi-kai-fa/huo-qu-yong-hu-ji-ben-xin-xi)\*\*\*\*
* **此接口不会返回好友详细信息，如需获取详细信息，请调用**[**获取联系人信息**](../deng-lu/huo-qu-lian-xi-ren-xin-xi.md)\*\*\*\*
{% endhint %}

**请求URL：**

* `http://域名地址/getFriends`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例标识 |

**请求参数示例**

```javascript
{
    "wId": "6a696578-16ea-4edc-ac8b-e609bca39c69"
}
```

**成功返回示例**

```javascript
{
    "message": "成功",
    "code": "1000",
    "data": [
        "wxid_hzkv98xxxxxxx3",
        "wxid_vy27e0xxxxxxx2",
        "wxid_0e671xxxxxxxx2"
    ]
}
```

**错误返回示例**

```javascript
{
    "message": "失败",
    "code": "1001",
    "data": null
}
```

**返回数据：**

| 参数名 | 类型 | 说明 |
| :---: | :---: | :---: |
| code | String | 1000成功  10001失败 |
| msg | String | 反馈信息 |
| data | JSONArray | 好友微信id |

