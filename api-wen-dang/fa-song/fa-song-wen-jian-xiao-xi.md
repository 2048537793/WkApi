---
description: 发送已经收到的文件消息
---

# 发送已经收到的文件消息

**简要描述：**

* 发送文件

**请求URL：**

* `http://localhost:18081/sendFile`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：login接口返回

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :--- | :--- | :--- | :--- |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 单聊被发送人账号，群聊群账号 |
| path | 是 | string | 文件url链接（从[下载文件接口](../xiao-xi-jie-shou/xia-zai-xiao-xi-nei-rong-ji-jiang-kai-fang/xia-zai-wen-jian-ji-jiang-kai-fang.md)取） |
| fileName | 是 | string | 文件名 |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a805-4715-0001-848f9a297a40",
   "wcId":"jack_623555049",
   "path": "https://xc-1300726975.cos.ap-shanghai.myqcloud.com/%E4%B8%8B%E8%BD%BD%E6%96%87%E4%BB%B6.txt",
   "fileName": "文件.txt"
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

