# 接入指南（必读）

###  技术要求

{% hint style="warning" %}
* 因涉及服务接口回调，需研发人员掌握任意一种[JAVA](https://www.oracle.com/technetwork/java/javase/downloads/index.html)、[Go](https://golang.google.cn/)、[PHP](https://www.php.net/)、[Python](https://www.python.org/)、[Node.js](www.baidu.com)等后端代码
* 客户需提供[外网服务器](https://zhidao.baidu.com/question/207831609.html)，在API对接中，假如您需要处理消息，则配置此地址即可接收消息
{% endhint %}

### 1. 准备工作

{% hint style="info" %}
* 需添加[客服微信](gou-mai-shuo-ming.md)（licx758），提供**公司名称**、**手机号**索要**开发者账号、密码**
{% endhint %}

### 2. 开发注意（必做）

{% hint style="success" %}
* **所有接口的请求头部Header必须包含一个参数： Authorization\(验证账号是否授权 PS：从登录接口获取\)**
* **Content-Type 设置成 application/json**
{% endhint %}

**​Header参数说明：**

| 参数 | 是否必须 | 说明 |
| :--- | :--- | :--- |
| **Authorization** | 是 | **验证账号是否授权** |
| **Content-Type** | 是 | **请求头部参数格式** |

**返回Code说明：**

| code状态码 | 状态说明 | code状态码 |
| :--- | :--- | :--- |
| 1000 | 成功 | 1000 |
| 1001 | 失败 | 1001 |
| 1002 | 无认证信息 | 1002 |
| 1003 | 认证信息无效 | 1003 |
| 1004 | 用户被禁用或到期 | 1004 |
| 1005 | 认证信息过期 | 1005 |
|  |  |  |

### 4. 消息回调配置（可选）

{% hint style="warning" %}
* **可以选择**[**接口回调**](api-wen-dang/xiao-xi-jie-shou/huo-qu-hui-tiao-xiao-xi/)**版本配置消息即可。**
* **假如不需要处理消息，可以选择忽略**
{% endhint %}

### 5.自助测试（可选）

{% hint style="info" %}
* [PostMan测试请点击这里](https://explore.postman.com/user/DCZoyMjyDryaJCD)，不知道步骤，就看[本网页左侧栏API文档](api-wen-dang/)。
* 测试如遇到步骤问题，请查看本[文档API释义](api-wen-dang/)，每个接口下面都会有教学
{% endhint %}

![](.gitbook/assets/image%20%2815%29.png)

## 加入我们   <a id="join-us"></a>

{% hint style="danger" %}
#### 如果您是公司研发人员，请扫描下方二维码，我们将与您详细沟通。
{% endhint %}

{% hint style="success" %}
#### 如果您是产品or市场调研人员，建议您将本文档熟读，我们将给予您最快的了解市场方式
{% endhint %}

 

![ &#x552E;&#x524D;&#x54A8;&#x8BE2;                                                            &#x4EA7;&#x54C1;&#x7ECF;&#x7406;](.gitbook/assets/image%20%2836%29.png)

