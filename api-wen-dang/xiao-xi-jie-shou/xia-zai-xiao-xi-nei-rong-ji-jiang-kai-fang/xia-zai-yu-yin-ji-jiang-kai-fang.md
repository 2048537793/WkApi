---
description: 下载语音
---

# 下载语音

**简要描述：**

* 下载消息中的语音

**请求URL：**

* `http://localhost:18081/getMsgVoice`

**请求方式：**

* POST

**请求头Headers：**

* Content-Type：application/json
* Authorization：Authorization值（登录获取二维码信息接口中返回的认证信息值）

**参数：**

<table>
  <thead>
    <tr>
      <th style="text-align:left">&#x53C2;&#x6570;&#x540D;</th>
      <th style="text-align:left">&#x5FC5;&#x9009;</th>
      <th style="text-align:left">&#x7C7B;&#x578B;</th>
      <th style="text-align:left">&#x8BF4;&#x660E;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">wId</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x5FAE;&#x4FE1;&#x5B9E;&#x4F8B;ID</td>
    </tr>
    <tr>
      <td style="text-align:left">msgId</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x6D88;&#x606F;id&#xFF08;&#x56DE;&#x8C03;&#x6D88;&#x606F;&#x83B7;&#x53D6;&#xFF09;</td>
    </tr>
    <tr>
      <td style="text-align:left">length</td>
      <td style="text-align:left">&#x662F;</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p>&#x8BED;&#x97F3;&#x7684;&#x957F;&#x5EA6;</p>
        <p>&#xFF08;&#x56DE;&#x8C03;&#x6D88;&#x606F;&#x83B7;&#x53D6;&#xFF0C;xml&#x6570;&#x636E;&#x4E2D;&#x7684;length&#x5B57;&#x6BB5;&#xFF09;</p>
      </td>
    </tr>
  </tbody>
</table>**返回数据：**

| 参数名 | 类型 | 说明 |
| :--- | :--- | :--- |
| code | int | 1000成功，10001失败 |
| msg | string | 反馈信息 |

**请求参数示例**

```text
{
   "wId": "0000016f-a3f4-7ac2-0001-4686486bb6c6",
   "msgId": 1102684152,
   "length" :2995
}

```

**成功返回示例**

```text
{
    "message": "成功",
    "code": "1000",
    "data": "https://xc-1300726975.cos.ap-shanghai.myqcloud.com/msgVoice/e17dd0a9-5c59-4a54-a3cd-1a4817f5dd29-1579005558791.silk"
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



