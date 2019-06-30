# 安装



## 编译安装

```bash
# 准备工作
$ yum install gcc openssl-devel
$ mkdir -p /opt/websuite/keepalived

# 下载 Keepalived
$ wget https://www.keepalived.org/software/keepalived-2.0.17.tar.gz
$ tar zxvf keepalived-2.0.17.tar.gz
$ cd keepalived-2.0.17

# 查看帮助
$ ./configure --help 
$ ./configure --prefix=/opt/websuite/keepalived --disable-lvs
$ make
$ make install
```

### 目录结构

```python
|-- bin
|   `-- genhash
|-- etc
|   |-- keepalived
|   |   |-- keepalived.conf										# 配置文件
|   |   `-- samples														# 配置示例
|   |       |-- client.pem
|   |       |-- dh1024.pem
|   |       |-- keepalived.conf.HTTP_GET.port
|   |       |-- keepalived.conf.IPv6
|   |       |-- keepalived.conf.SMTP_CHECK
|   |       |-- keepalived.conf.SSL_GET
|   |       |-- keepalived.conf.conditional_conf
|   |       |-- keepalived.conf.fwmark
|   |       |-- keepalived.conf.inhibit
|   |       |-- keepalived.conf.misc_check
|   |       |-- keepalived.conf.misc_check_arg
|   |       |-- keepalived.conf.quorum
|   |       |-- keepalived.conf.sample
|   |       |-- keepalived.conf.status_code
|   |       |-- keepalived.conf.track_interface
|   |       |-- keepalived.conf.virtual_server_group
|   |       |-- keepalived.conf.virtualhost
|   |       |-- keepalived.conf.vrrp
|   |       |-- keepalived.conf.vrrp.localcheck
|   |       |-- keepalived.conf.vrrp.lvs_syncd
|   |       |-- keepalived.conf.vrrp.routes
|   |       |-- keepalived.conf.vrrp.rules
|   |       |-- keepalived.conf.vrrp.scripts
|   |       |-- keepalived.conf.vrrp.static_ipaddress
|   |       |-- keepalived.conf.vrrp.sync
|   |       |-- root.pem
|   |       |-- sample.misccheck.smbcheck.sh
|   |       `-- sample_notify_fifo.sh
|   `-- sysconfig
|       `-- keepalived
|-- sbin
|   `-- keepalived        										# 启动脚本
`-- share
    |-- doc
    |   `-- keepalived
    |       `-- README
    |-- man
    |   |-- man1
    |   |   `-- genhash.1
    |   |-- man5
    |   |   `-- keepalived.conf.5
    |   `-- man8
    |       `-- keepalived.8
    `-- snmp
        `-- mibs

```





## Docker 方式安装 TODO

```bash
$  docker search  keepalived      
NAME                                   DESCRIPTION                                     STARS               OFFICIAL            AUTOMATED
alterway/keepalived                    Keepalived manage virtual ip between servers.   23                                      [OK]
osixia/keepalived                      Keepalived with quick start configuration vi…   9                  
...

$ docker pull alterway/keepalived


```

