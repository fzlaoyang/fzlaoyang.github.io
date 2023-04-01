
---
title: "APRS(Automatic Packet Report System)自动位置回报系统"
subtitle: ""
date: 2023-03-28T14:40:00+08:00
lastmod: 2023-03-28T14:40:00+08:00
draft: false
author: "BG5VGE"
authorLink: ""
description: "APRS是一种自动位置报告系统，为业余无线电中的一个项目,可使业余无线电操作者迅速的将实时事件相关的数据发布出去，并在电脑或手机上的地图软件显示这些数据(定位)的软硬件系统。可以通过电台，手机将从GPS得到的定位数据自动发送到接收端igate基站(APRS网关)再转发到互联网或直接上传到互联网上"
license: ""
images: []

tags: [APRS]
categories: [无线电]

featuredImage: ""
featuredImagePreview: ""

hiddenFromHomePage: false
hiddenFromSearch: false
twemoji: false
lightgallery: true
ruby: true
fraction: true
fontawesome: true
linkToMarkdown: false
rssFullText: false

toc:
  enable: true
  auto: true
code:
  copy: true
  maxShownLines: 50
math:
  enable: false
  # ...
mapbox:
  # ...
share:
  enable: true
  # ...
comment:
  enable: true
  # ...
library:
  css:
    # someCSS = "some.css"
    # located in "assets/"
    # Or
    # someCSS = "https://cdn.example.com/some.css"
  js:
    # someJS = "some.js"
    # located in "assets/"
    # Or
    # someJS = "https://cdn.example.com/some.js"
seo:
  images: []
  # ...
---



---
### 什么是APRS

APRS 是一种自动位置报告系统为业余无线电中的一个项目,
可使业余无线电操作者迅速的将实时事件相关的数据发布出去，
并在电脑或手机上的地图软件显示这些数据(定位)的软硬件系统。

可以通过电台，手机将从GPS得到的定位数据自动发送到接收端igate基站(APRS网关)再转发到互联网或直接上传到互联网上，

这样其他无线电爱好者可以通过电子地图（例如https://aprs.fi/ http://aprs.cn/ 实时获得对方的地理位置，行动方向和运动速度。

简单说GPS导航可以让自己知道在什么地方，APRS不但可以知道自己在哪里，也可让其他人知道你在哪里。

电台使用无连接分组基于一对多进行数据发布，类似于广播电台和听众的关系。随着APRS的发展，现在APRS的设备大抵分为`APRS节点、APRS网关(IGate)、APRS服务器`等。 


---
<br>

### 什么是APRS网络

APRS的网络一般可以理解由两个部分组成，其中一部分为电台射频网络（简称“APRS-RF”网络），另一部分为互联网服务网络（Internet Service，简称“APRS-IS”网络），而电台射频网络和互联网服务网络又可以通过互联网网关（Internet Gateway，简称“IGate”）连接起来，实现各种台站信标、气象信息、短消息等数据的双向传递，从而形成一个大型的APRS数据传输网络。

 <img src="/images/2023/aprs_net.jpg"  alt="aprs网络组成示意图"  width="600">
 
 ---
<br>

### APRS 地图网站

大家所熟悉的

[aprs.fi](https://aprs.fi)

[aprs.tv](https://aprs.tv)

[aprs.cn](http://aprs.cn)

等网站具有地图显示台站等功能的网站，其实并不是APRS互联网服务网络体系的一部分.

而是一种APRS-IS网络发展出来的一个终端服务产品，它们的工作原理是，从APRS的某个服务器中收取整个网络的实时数据，然后在地图上的实时数据显示、历史数据查询、台站覆盖范围推测（PHG）、台站收听列表显示（Heard List）等各种强大的扩展功能供爱好者读取使用。

---
<br>

### APRS使用频率

中国APRS使用`144.640MHz`频率

---
<br>

### APRS软件

APRSdroid [http://aprsdroid.org/download](http://aprsdroid.org/download)

UISS  普通电台和电脑收发APRS信号的软件

---
<br>

### APRS功能的电台列表

联畅HG-UV98

自由通AnyTone AT-D868UV

自由通AnyTone AT-D878

八重洲多款型号

威诺VR-N7500车台

威诺n75手台

---
<br>

### APRS的实现方法

*  APRS软件

: 即使没有硬件设备，你也可以向 APRS 网络发送信息。当然，前提是您已经取得了呼号，因为你通过网络发送的信息可能会通过一些双向网关转发到射频信号。


 <kbd><img src="/images/2023/aprs-baofeng.jpg"  alt="软件和普通手台实现aprs"></kbd>

: 安卓手机APP,名称`APRSdroid`，利用手机本身的定位功能收集定位数据后定时通过Internet收发到 APRS 网络。这些软件可以让你直接体验 APRS。在其它平台上也有很多优秀的多功能软件。

* APRS硬件

: 一个普通的电台连接TNC就能实现APRS,例如国内知名的马工开发的APRS盒子。

 <kbd><img src="/images/2023/aprs-tnc.jpg"  alt="TNC盒子"></kbd>

* 声卡软件

: 将声卡用作调制解调器的软件,比如 UISS 软件就内置了软件调制解调器，你只需要连接音频，它就可以收发 APRS 信号。

: 安卓软件 APRSdroid 和 HT 也具备这样的功能，只需音频线连接电台，即可收发 APRS 信号，不仅仅是位置信号，还可以发送和接收 APRS 短信。


---
<br>

### APRS验证码

  APRS网络由互联网和无线电组成，我们需要一种方法来阻止未经许可的用户被传输到无线电网络。当 APRS系统与服务器连接时，需要验证一个号码。这个号码就像一个密码，根据你的呼号计算出来，它是唯一的。也就是说，连接到互联网服务器的 I-gate网关和软件都需要验证密码，因为它们发出的信息可能会被其它电台通过无线电发送出去。

###  <kbd>如何申请APRS-IS的验证码</kbd>

  申请APRS-IS的验证码的网址https://aprsdroid.org/passcode


 <kbd><img src="/images/2023/aprs-1.jpg"  alt="如何申请APRS-IS的验证码"  width="450"></kbd>

其中Grid square：为HAM QTH 梅登黑德定位信息。
成功提交之后的几天,您的邮箱将会收到验证码了。这种方法获得验证码的时间比较慢。

---
<br>

> ### APRS验证码的计算

 * 是的APRS验证码是可以根据呼号被计算出来的,苹果手机应用商店里面就有APRS计算的app服务,不过是收费的。
 
 * `老杨免费提供APRS验证码的计算`,只需把无线电执照带呼号页面拍照并发邮件到<img src="/img/email1.png"  alt="MAIL TO BG5VGE">
 
