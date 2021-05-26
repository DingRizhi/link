
!> 直接测试节点的连通性，可快速排除服务器问题！

## iPhone/iPad

* 打开小火箭-->选择节点-->`连通性测试`：节点后显示`xxx ms`说明节点可用；显示`超时`说明节点不可用！

![test](media/apple/test.gif ':size=480')

## 配置路由表

假设网卡名为`ens3`

```
sudo iptables -t filter -A FORWARD -i wg0 -j ACCEPT
sudo iptables -t filter -A FORWARD -o wg0 -m state --state RELATED,ESTABLISHED -j ACCEPT
sudo iptables -A FORWARD -i wg0 -o ens3 -j ACCEPT
sudo iptables -A FORWARD -i ens3 -o wg0 -m state --state ESTABLISHED,RELATED -j ACCEPT
sudo iptables -t nat -A POSTROUTING -o ens3 -j MASQUERADE
```

## 开启转发功能

```
echo 1 >/proc/sys/net/ipv4/ip_forward
```

## 生成密钥

```shell
wg genkey > privatekey
wg pubkey < privatekey > publickey
```
其中 private key 写在配置文件里，public key 在 web 端增加服务器时填写

## 增加配置文件

```
[Interface]
Address = 10.100.0.1/16 
PrivateKey = 8REGzY7PA3p81VN9KQ4mKM7d8oFZBu2wD7Pbs8ppPkW= 
ListenPort = 50000
```

## 启动 WireGuard

```shell
sudo wg-quick up ./wg0.conf
```

## 启动 s 端

使用[shadowsocks-manager-wireguard](https://github.com/gyteng/shadowsocks-manager-wireguard)作为 s 端即可
```
node index --gateway 10.100.0.1 \
           --manager 0.0.0.0:6789 \
           --password 123456 \
           --interface wg0 \
           --db /your/data.json
```
