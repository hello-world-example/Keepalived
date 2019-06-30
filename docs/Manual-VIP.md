# 手动设置 VIP (ip)



## 示例

```bash
# 增加 VIP
$ ip addr add 172.16.2.77/23 dev eth0 

# 删除 VIP
$ ip addr del 172.16.2.77 dev eth0 
```



## 安装

```bash
$ yum install iproute iproute-doc
```



## ip 命令帮助

```bash
$ ip
Usage: ip [ OPTIONS ] OBJECT { COMMAND | help }
       ip [ -force ] -batch filename
where  OBJECT := { link | address | addrlabel | route | rule | neigh | ntable |
                   tunnel | tuntap | maddress | mroute | mrule | monitor | xfrm |
                   netns | l2tp | fou | macsec | tcp_metrics | token | netconf | ila |
                   vrf }
       OPTIONS := { -V[ersion] | -s[tatistics] | -d[etails] | -r[esolve] |
                    -h[uman-readable] | -iec |
                    -f[amily] { inet | inet6 | ipx | dnet | mpls | bridge | link } |
                    -4 | -6 | -I | -D | -B | -0 |
                    -l[oops] { maximum-addr-flush-attempts } | -br[ief] |
                    -o[neline] | -t[imestamp] | -ts[hort] | -b[atch] [filename] |
                    -rc[vbuf] [size] | -n[etns] name | -a[ll] | -c[olor]}
```

## 子命令帮助

```bash
$ ip address help
Usage: ip address {add|change|replace} IFADDR dev IFNAME [ LIFETIME ]
                                                      [ CONFFLAG-LIST ]
       ip address del IFADDR dev IFNAME [mngtmpaddr]
       ip address {save|flush} [ dev IFNAME ] [ scope SCOPE-ID ]
                            [ to PREFIX ] [ FLAG-LIST ] [ label LABEL ] [up]
       ip address [ show [ dev IFNAME ] [ scope SCOPE-ID ] [ master DEVICE ]
                         [ type TYPE ] [ to PREFIX ] [ FLAG-LIST ]
                         [ label LABEL ] [up] [ vrf NAME ] ]
       ip address {showdump|restore}
       
IFADDR := PREFIX | ADDR peer PREFIX
          [ broadcast ADDR ] [ anycast ADDR ]
          [ label IFNAME ] [ scope SCOPE-ID ]
SCOPE-ID := [ host | link | global | NUMBER ]
FLAG-LIST := [ FLAG-LIST ] FLAG
FLAG  := [ permanent | dynamic | secondary | primary |
           [-]tentative | [-]deprecated | [-]dadfailed | temporary |
           CONFFLAG-LIST ]
CONFFLAG-LIST := [ CONFFLAG-LIST ] CONFFLAG
CONFFLAG  := [ home | nodad | mngtmpaddr | noprefixroute | autojoin ]
LIFETIME := [ valid_lft LFT ] [ preferred_lft LFT ]
LFT := forever | SECONDS
TYPE := { vlan | veth | vcan | dummy | ifb | macvlan | macvtap |
          bridge | bond | ipoib | ip6tnl | ipip | sit | vxlan | lowpan |
          gre | gretap | ip6gre | ip6gretap | vti | nlmon | can |
          bond_slave | ipvlan | geneve | bridge_slave | vrf | hsr | macsec }
```



## 常用命令

- `address` 设备上的协议（IP或IPv6）地址

  - `ip a` ≈ `ip addr` ≈ `ip address` 所有网络信息
  - `ip -4 a` 只看 IPv4 先关的信息
  - `ip addr show wlan0` 查看某个设备的信息

- `route` 路由表条目

  - `ip route show` 查看路由信息
  - `ip route flush cache` 刷新路由表

- `link` 网络设备

  - `ip -s link` 显示所有网络接口的统计数据

- `rule` 路由策略数据库中的规则

- `addrlabel` 协议地址选择的标签配置

  

## Read More

> - [Linux ip命令详解](https://www.jellythink.com/archives/469)





