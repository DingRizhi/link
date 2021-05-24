## PAC 用户自定规则

* 如PAC模式可上`Google Youtube Facebook`等常用网站，但是不能上`xxx`网站，请添加自定规则

* 如打不开`xxx.com`网站，应该在自定规则里添加两行 `||xxx.com` 和 `||www.xxx.com`然后`确定`

![mac](media/mac/rule.gif ':size=480')

!> Windows 用户同样适用，只需要打开win文件夹，编辑`user-rule.txt`，添加同样的规则即可！

## iPhone/iPad 修改DNS

* 打开`Potatso Lite`的设置界面-->点击`自定义DNS`-->添加DNS`8.8.8.8`

![apple](media/apple/dns.gif ':size=480')

## 使用 mailgun 发送邮件

将配置文件的 email 部分替换成下面的格式：

```yaml
email:
  use: true
  type: 'mailgun'
  baseUrl: 'https://api.mailgun.net/v3/sandbox31d0f2c9c753a343f2e7c54da78ca89e.mailgun.org'
  apiKey: 'key-f1e6a7558c7c5a37a33fdba53a87ea82'
```

## 使用 sendgrid 发送邮件

将配置文件的 email 部分替换成下面的格式：

```yaml
email:
  type: 'sendgrid'
  name: 'ssmgr'
  email: 'admin@your.domain.com'
  apiKey: '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'
```

# 转发 smtp 协议

对于一些不支持 smtp 协议的 VPS，可通过代理转发的方式转到一台支持的 VPS 上面去发邮件，加上一个`proxy`参数即可：

```yaml
plugins:
  email:
    use: true
    type: 'smtp'
    username: 'username'
    password: 'password'
    host: 'smtp.your-email.com'
    proxy: 'socks://127.0.0.1:1234/'
```

# 随节点运行 shadowsocks

在 s 端运行`ssmgr`时，只需加上一个`-r`的参数，便可省去运行`ss-manager`的步骤，当然首先系统里需要安装了对应版本的 shadowsocks 才行。默认为运行 libev 版，加密方式 aes-256-cfb：

```shell
ssmgr -c xxx.yml -r
ssmgr -c xxx.yml -r libev
ssmgr -c xxx.yml -r libev:aes-256-gcm
ssmgr -c xxx.yml -r python:aes-256-gcm
ssmgr -c xxx.yml -r rust:aes-256-gcm
```

# 自定义服务器显示地址

有时候，s 端的实际地址跟想要展示给用户的地址不相同，假设原本地址是`1.1.1.1`，想给用户展示`2.2.2.2`，只需在 Web 端编辑服务器，把地址写成`1.1.1.1:2.2.2.2`，这样 m 端实际通信的地址是冒号前面部分，展示给用户的是冒号后面的部分。

# 使用端口偏移功能

在编辑服务器时，默认的“端口偏移”值为0，当这个值不为0的时候（可以是负数），会使该节点所有端口都加上这个偏移量。当需要一台机作为两个节点使用时，用这个参数可以错开端口号避免冲突。

# 自定义首页图标

在配置文件里加上 icon 参数便可指定首页图片，可使用绝对路径或者只填文件名（默认在~/.ssmgr里找），建议图片大小为 256 x 256

```yaml
plugins:
  webgui:
    use: true
    icon: 'icon.png'
```

# 使用充值码功能

在配置文件中加上 giftcard 插件即可：

```yaml
plugins:
  giftcard:
    use: true
```

# 使用 Telegram Bot

使用该插件后，管理员和用户都能够绑定 Telegram 账号，管理员可以实时收到用户注册和付费提醒，普通用户每天早上可以收到昨日流量统计。

从[@BotFather](https://telegram.me/BotFather)申请一个bot，然后在配置文件中加上 webgui_telegram 插件：

```yaml
webgui_telegram:
  use: true
  token: '191374681:AAw6RaVHR4nnP7T4Ct4a8QX-XyFQ5W53wmZ'
```

# 增加 Crisp 客服

增加该插件后，用户登陆后的首页会增加一个“客服咨询”入口。

```yaml
webgui_crisp:
  use: true
  websiteId: '6d8e3987-ec62-08b2-80a1-b3c776ad371c'
```
