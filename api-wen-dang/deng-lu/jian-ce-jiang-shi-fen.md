---
description: 检测僵尸粉
---

# 检测僵尸粉

{% hint style="danger" %}
**本接口调用需要间隔3-5S**
{% endhint %}

**简要描述：**

* 获取联系人列表

**请求URL：**

* `http://XX/checkZombie`

**请求方式：**

* POST 

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | String | 微信实例标识 |
| wcId | 是 | String | 好友微信多个以","分隔,每次最多支持个20 |

**请求参数示例**

```javascript
{
    "wId": "01377f33-544c-4dc4-9184-bcbbcd3b05d0",
    "wcId": "wxid_6rw5a5bpf4qg12,wxid_mv3azvtjaltu12,wxid_ez4qv5fzty422,wxid_c40ur7180psu12,wxid_jtwdho0jvo5w12,xid_1rfsa01c46m222,wxid_gb5vd0e8vtfz22"
}
```

**成功返回示例**

```javascript
{

    "message": "成功",
    "code": "1000",
    "data": [
        {
            "userName": "wxid_6rw55bpf4qg12",
            "status": 6
        },
        {
            "userName": "wxid_mv3aztjaltu12",
            "status": 6
        },
        {
            "userName": "wxid_e4qv5fzty422",
            "status": 0
        },
        {
            "userName": "wxid_c4ur7180psu12",
            "status": 0
        },
        {
            "userName": "wxid_jtdho0jvo5w12",
            "status": 0
        },
        {
            "userName": "",
            "status": 0
        },
        {
            "userName": "wxid_b5vd0e8vtfz22",
            "status": 0
        }
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
| data | JSONObject |  |
| userName | String | 微信号 |
| status | int | 0: 正常   1: 被删除   2: 被拉黑   3: 双方互拉黑   4: 我拉黑的好友   5: 我删除的好友   6: 互删好友 |

