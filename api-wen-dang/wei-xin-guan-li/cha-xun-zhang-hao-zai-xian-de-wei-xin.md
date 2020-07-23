# 查询账号在线的微信

**简要描述：**

* 查询账号下所有在线的微信号

**请求URL：**

* `http://localhost:18081/queryLoginWx`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| 无 | 无 | 无 | 无 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |
| data |  |  |
| wcId | string | 微信id |
| wId | string | 微信实例id |

**请求参数示例**

**成功返回示例**

```text
{
    "code": "1000",
    "message": "成功",
    "data": [
        {
            "wcId": "wxid_ylxtflcg0p8b22",
            "wId": "0454d174-1e05-47db-a0d7-bd012709e336"
        }
    ]
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

