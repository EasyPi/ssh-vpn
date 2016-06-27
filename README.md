VPN over SSH
============

### How It Works

```

                            ///
+----------------------+    ///    +----------------------+
|        RPI           |    ///    |        VPS           |
|----------------------|----SSH--->|----------------------|
| eth0: 192.168.31.222 |    ///    | eth0: 1.2.3.4        |
| tun0: 10.0.0.200     |    ///    | tun0: 10.0.0.100     |
+----------------------+    ///    +----------------------+
                            ///

```

- RPI (树莓派-客户端)
  - 使用境外DNS服务器
  - 使用eth0, 禁用wlan0
  - 配置ssh无密码root登录

- VPS (云主机-服务端)
  - 使用境外[VPS服务器][1]
  - 启用内核IP数据包转发
  - 配置防火墙NAT地址转换


### References

- <http://man.openbsd.org/ssh>
- <https://help.ubuntu.com/community/SSH_VPN>
- <http://bodhizazen.net/Tutorials/VPN-Over-SSH>

[1]: <http://www.vultr.com/?ref=6821947>
