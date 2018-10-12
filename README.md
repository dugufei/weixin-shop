# weixin-app-shop

## 项目介绍
该小程序商城可直接部署对接H5活动之家微商城，与微商城共用一套商城配置信息和数据

### 一、捷微小程序商城快速对接H5活动之家微商城
#### 1. 小程序项目代码下载
```
源码下载地址：https://gitee.com/jeecg/weixin-app-shop
```
#### 2. 小程序项目配置
##### （1）配置H5活动之家微商城id
```
登录H5活动之家（http://www.h5huodong.com）找到需要对接的微商城，没有微商城可以创建一个微商城，进入菜单【商城类】-【小程序商城】-【商城管理】创建自己的商城。
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12164635_Xdg6.png "在这里输入图片标题")

##### （2）商城创建后进入商城后台管理，获取商城id

![输入图片说明](https://static.oschina.net/uploads/img/201810/12164733_csh9.png "在这里输入图片标题")

##### （3）商城id配置到小程序项目中/dist/utils/wxRequest.js文件中

![输入图片说明](https://static.oschina.net/uploads/img/201810/12165152_lYSv.png "在这里输入图片标题")
#### 3、商城小程序支付配置
```
进入商城后台管理，【支付中心】-【小程序支付配置】
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12171011_5VgX.png "在这里输入图片标题")
```
配置支付信息：
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12171053_PWvq.png "在这里输入图片标题")
```
小程序id：AppID(小程序ID)  例如：wxd930ea5d5a258f4f
小程序密钥：AppSecret(小程序密钥)  例如：ibuaiVcKdpRxkhJA
商户号：支付商户商户号   例如：10000100
支付密钥：商户平台设置的密钥key 例如：192006250b4c09247ec02edce69f6a2d
证书： 微信支付接口中，涉及资金回滚的接口会使用到商户证书，包括退款、撤销接口。
商家在申请微信支付成功后，收到的相应邮件后，可以按照指引下载API证书，
也可以按照以下路径下载：微信商户平台(pay.weixin.qq.com)-->账户设置-->API安全-->证书下载 
（见下图）
上传pkcs12格式(apiclient_cert.p12）证书即可
配置完成后，订单支付退款功能即可使用。
备注：证书不上传不能退款操作，但是可以进行订单支付，其他的配置信息必须得正确。
```
#### 4. 发布小程序
```
小程序发布，需要通过微信开发者工具上传项目，上传者需扫码微信开发者工具，
该登录微信号必须是当前小程序的开发者。
1、发布前准备
授权开发者权限，小程序后台管理员授权微信用户为开发者【用户身份-成员管理】添加成员
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12165423_DkBh.png "在这里输入图片标题")
```
服务器域名配置：
小程序后台，进入【设置-开发设置】，服务器域名设置app.h5huodong.com 改配置授权H5活动之家提供服务支持。
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12172743_EdRx.png "在这里输入图片标题")
```
2、下载微信开发者工具
下载地址：
https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html
下载后安装开发者工具
```
```
3、开发者工具导入项目
扫码登录，选择小程序项目开发者模式。
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12165657_QxgO.png "在这里输入图片标题")
![输入图片说明](https://static.oschina.net/uploads/img/201810/12165708_4NEq.png "在这里输入图片标题")
```
选择小程序代码工程目录（即选择下载的解压的小程序代码dist目录），填写小程序appid,填写一个项目名称，点击确定。
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12165903_gM2z.png "在这里输入图片标题")
```
进入开发页面后，点击编译，然后点击上传，上传小程序到服务器。
上传是填写版本号，项目备注。
版本号命名规则 例如：1.0.1
项目备注，备注项目名称，发布更新的功能
填写后点击上传，即可上传到服务器，可在小程序管理后台看到
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12170301_sJsf.png "在这里输入图片标题")
```
小程序管理后台【开发管理】，可以看到上传的开发版本
```
![输入图片说明](https://static.oschina.net/uploads/img/201810/12170422_sTtS.png "在这里输入图片标题")
```
开发版本可以设置为体验版本，具有体验权限的人可以扫码访问，进行测试验证，测试商城数据等没有问题即可提交审核，发布上线。
备注：提交审核后，需等待微信官方审核，审核通过后才可发布上线
```
小程序对接完毕！！！
