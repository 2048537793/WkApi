# 获取通讯录列表（好友/群）

{% hint style="info" %}
* **获取通讯录列表之前必须调用**[**初始化通讯录列表接口。**](https://docs.wkteam.cn/api-wen-dang/kai-shi-kai-fa/huo-qu-yong-hu-ji-ben-xin-xi)\*\*\*\*
* **此接口不会返回好友/群的详细信息，如需获取详细信息，请调用**[**获取联系人信息**](../deng-lu/huo-qu-lian-xi-ren-xin-xi.md)\*\*\*\*
{% endhint %}

**请求URL：**

* `http://域名地址/getAddressList`

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
    "code": "1000",
    "message": "获取通讯录成功",
    "data": {
        "chatrooms": [
            "246147705@chatroom",
            "194347282@chatroom",
            "232913013@chatroom",
            "2179356830@chatroom"
        ],
        "friends": [
            "weixin",
            "wxid_hzkv9806n62p22",
            "wxid_vy27e0ucnm9x22",
            "wxid_0e671x6mb8s412",
            "wxid_b5dtontdi53l22"
        ],
        "ghs":[
            "gh_3dfda90e39d6",
            "gh_1c7d6d317951",
            "gh_d45429d1a396"
        ],
        "others": [
            "fmessage",
            "medianote",
            "floatbottle"
        ]
    }
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
| data | JSONArray |  |
|  chatrooms | JSONArray | 群号id  |
| friends | JSONArray | 好友微信id |
| ghs | JSONArray | 公众号id |
| others | JSONArray | 官方相关id（安全中心类似） |

