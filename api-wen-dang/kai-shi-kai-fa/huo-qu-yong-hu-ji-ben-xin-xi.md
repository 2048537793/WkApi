---
description: 获取联系人列表(群、好友)
---

# 获取联系人列表\(群、好友\)

{% hint style="info" %}
* **此接口也包含群列表。**
* **此接口假如返回“初始化中”，需用户等待5S调用，直至调用成功。**
{% endhint %}

**简要描述：**

* 获取联系人列表（群/好友/公众号）

**请求URL：**

* `http://localhost:18081/getAllContact`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| public | json | 公众号 |
| friend | json | 好友 |
| group | json | 群组 |
| userName | String | 微信号 |
| aliasName | String | 别名 |
| bigHead | String | 头像 |
| smallHead | String | 头像（缩略图） |
| sex | String | 性别：1：男；2：女 |
| signature | String | 签名 |
| country | String | 国家 |
| province | String | 省份 |
| city | String | 城市 |

**请求参数示例**

```text
{
    "wId": "0000016e-63eb-f319-0001-ed01076abf1f"
}
```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": {
       "public": [
            {
                "userName": "gh_765004365c98",
                "aliasName": null,
                "nickName": "豆瓣读书",
                "bigHead":     "http://wx.qlogo.cn/mmhead/Q3auHgzwzM4ZEYadrntHhXR5BWsxDaUvhlWVRUCicicVKDFVWb5o8PQA/0",
                "smallHead": "http://wx.qlogo.cn/mmhead/Q3auHgzwzM4ZEYadrntHhXR5BWsxDaUvhlWVRUCicicVKDFVWb5o8PQA/132",
                "sex": 0,
                "signature": "豆瓣读书官方订阅号。在这里，遇见好书。在阅读中，多活几次。",
                "country": "中国",
                "province": "北京",
                "city": "朝阳"
            }
        ],
      "friend": [
            {
                "userName": "wxid_vao3ptfez4p22",
                "aliasName": null,
                "nickName": "朋友",
                "bigHead": "http://wx.qlogo.cn/mmhead/ver_1/icJ4nKc9ATfTkkH7Fb8eVO693konq1ibdFWic4icTSe5aLNXNetMGkIe3BlRU4moTpYbeBKAlaO2Nyf0WqzMMPK3wA/0",
                "smallHead": "http://wx.qlogo.cn/mmhead/ver_1/icJ4nKc9ATfTkkH7Fb8eVO693konq1ibdFWic4icTSe5aLNXNetMGkIe3BlRU4moTpYbeBKAlaO2Nyf0WqzMMPK3wA/132",
                "sex": 1,
                "signature": null,
                "country": null,
                "province": null,
                "city": null
            }
         ],
    "group": [
            {
                "userName": "22156949594@chatroom",
                "aliasName": null,
                "nickName": "从来处来从去处去",
                "bigHead": null,
                "smallHead": "http://wx.qlogo.cn/mmcrhead/jclQZ73SnwFCXB4Pk1p34vfXvSicF6r5oN6ALLrktEIflSByugvYuHVV059o9RSw5vYXoHLtWO81zk1ja31QbKOfzAKpUl2wA/0",
                "sex": 0,
                "signature": null,
                "country": null,
                "province": null,
                "city": null
            }
    ]
    }
}
```

**错误返回示例**

```text
{
    "message": "失败",
    "code": "1001",
    "data": null
}
```

