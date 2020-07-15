# 获取群列表

{% hint style="info" %}
* **获取群列表之前必须调用**[**初始化群列表接口**](https://www.wkteam.cn/api-wen-dang2/deng-lu/initGroupList.html)**。**
* **此接口仅会** **获取保存到通讯录的群,聊天列表的群获取不到，未获取的群,有人在群内发消息的话会有消息回调， 开发者此刻调用**[**获取群详情接口**](https://www.wkteam.cn/api-wen-dang2/qun-cao-zuo/queryGroupDetail.html)**再保存到自己数据库中就可以了。**
* **比如说手机上三年前不说话的群，侧滑删除了，然后你换了手机也不会取到的 ，有人说了话他才会置顶，原理就是各个终端（Android、IOS、桌面版微信）取得了消息回调，又去获取群了详情 本地数据库缓存了下来 更新的ui，让用户感知的**
* **此接口不会返回群详细信息，如需获取群详细信息，也是调用**[**获取联系人接口**](https://www.wkteam.cn/api-wen-dang2/hao-you-cao-zuo/queryUserInfo.html)
{% endhint %}

**请求URL：**

* `http://域名地址/getChatRooms`

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
        "2340848117@chatroom",
        "232916813@chatroom",
        "1954631131@chatroom",
        "2260665764@chatroom",
        "2465147705@chatroom",
        "2385536808@chatroom",
        "194134007282@chatroom",
        "2229123655359@chatroom",
        "243552364656@chatroom",
        "20250945708@chatroom",
        "2179315830@chatroom"
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
| data | Array | 群id |

