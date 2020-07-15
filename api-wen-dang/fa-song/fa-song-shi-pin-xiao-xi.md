---
description: 发送视频消息
---

# 发送视频消息

**请求URL：**

* `http://localhost:18081/sendVideo`

**请求方式：**

* POST

**参数：**

| 参数名 | 必选 | 类型 | 说明 |
| :---: | :---: | :---: | :---: |
| wId | 是 | string | 微信实例ID |
| wcId | 是 | string | 微信号/群号 |
| path | 是 | string | 视频url链接 |
| thumbPath | 是 | string | 视频封面url链接，可自定义（也可自己服务器获取视频首帧） |

**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
	"wId": "0000016e-a1f1-f0d9-0002-425ea1a28d22",
	"wcId": "jack_623555049",
	"path": "https://wkgjonlines.oss-cn-shenzhen.aliyuncs.com/movies/20191113/d7c616569ac342ad1fa8e3301682844e.mp4",
	"thumbPath": "http://pic23.nipic.com/20120902/8068495_150602391000_2.jpg"
}
```

**成功返回示例**

```text
{
    "message": "发送成功",
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

