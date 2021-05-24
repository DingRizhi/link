
!> 支持科学上网的前提：路由器提供SSH权限或路由器固件里已有Shadowsocks 插件

!> 通常兼容 Openwrt/LEDE/老毛子/梅林固件的路由器都支持Shadowsocks 科学上网

## 路由器优势

无痛的科学上网：又称`透明代理`，指无需对连接路由器的终端设备（手机、电脑、游戏机等）进行额外的设置，即可以实现科学上网

## 路由器选择

几十百来块钱的路由器大多数不支持科学上网，推荐新兴的互联网品牌路由器：小米、极路由、斐讯、华硕等（并非所有型号都支持）

具体的支持型号，请查询 https://downloads.x-wrt.com/rom/

## Shadowsocks插件

* 进入您购买SS节点的网站，准备好`SS节点`信息！

![openwrt1](media/openwrt/1.gif ':size=600')

* 登陆路由器，进入Shadowsocks 插件设置，输入`SS节点`信息!

![openwrt2](media/openwrt/2.gif ':size=600')

* Shadowsocks 设置界面往下拉，会看到几个辅助功能，如下图。

![openwrt3](media/openwrt/3.gif ':size=600')

* Socks5代理：可使局域网内的设备通过Socks5连接路由器，实现科学上网。一般用透明代理即可，不建议开启！

* 透明代理：开启后局域网所有流量走代理。下面的忽略列表默认为国内IP段，可实现国内流量直连，国外流量走代理。

* UDP转发：这一功能需要Shadowsocks节点支持，一般我们用不到，默认不启用。

!> 常见问题

  ```shell
不知到某个选项怎么设置！
```
教程里没提到的选项，保持默认值就可以了！

高手教程 https://zzz.buzz/zh/gfw/2016/02/16/deploy-shadowsocks-on-routers/
