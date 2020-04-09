---
description: 修改好友备注
---

# 修改好友备注

### 修改好友备注 <a id="&#x4FEE;&#x6539;&#x597D;&#x53CB;&#x5907;&#x6CE8;"></a>

**简要描述：**

* 修改好友备注

**请求URL：**

* `http://localhost:18081/modifyRemark`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 好友微信号 |
| remark | 是 | string | 好友备注 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a2aa-9089-0001-32dbe7c94132",
   "wcId": "wxid_ao4ziqc2g9b922",
   "remark": "备注"
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

