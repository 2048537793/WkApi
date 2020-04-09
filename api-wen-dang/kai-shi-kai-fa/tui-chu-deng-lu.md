---
description: （假如出现退出失败，应该是不在线，不在线则调用批量下线微信号接口。）
---

# 退出微信

{% hint style="info" %}
* 假如出现退出失败，则调用[批量下线微信号](../wei-xin-guan-li/pi-liang-xia-xian-wei-xin-hao.md)接口。
* 建议退出微信直接调用批量下线微信号接口，此接口可忽略。
{% endhint %}

### 退出登录 <a id="&#x9000;&#x51FA;&#x767B;&#x5F55;"></a>

**简要描述：**

* 退出登录

**请求URL：**

* `http://localhost:18081/logout`

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
    "data": null
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

