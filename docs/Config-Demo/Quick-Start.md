# 入门示例



```bash
! Configuration File for keepalived

global_defs {
   router_id HA_QUICK_START
}

vrrp_instance test_vip {
    state BACKUP                   # 主备都设置为 BACKUP，通过 priority 来抢占 master
    interface eth0
    virtual_router_id 51         
    # nopreempt                    # master 设置为不抢占
    priority 100                   # master 的级别 
    
    virtual_ipaddress {
        172.16.2.77/32 dev eth0
    }
    authentication {
        auth_type PASS
        autp_pass 123456
    }
}
```

