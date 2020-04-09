---
description: 用于状态异常处理场景和批量或者单个下线场景！！！
---

# 批量下线微信号

**简要描述：**

* 下线某个或某些已登录的微信号

**请求URL：**

* `http://localhost:18081/member/offline`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| account | 是 | string | 账号 |
| wcIds | 是 | list | 须下线的wcId\(可从[查看账号下已登录的微信号](cha-xun-zhang-hao-xia-yi-deng-lu-de-wei-xin-hao.md)获取\) |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |

**请求参数示例**

```text
{

   "account": "1234567890",
   "wcIds": ["wxid_1r6wafuhou3e22","wxid_wl9qchkanp9u22"]

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

