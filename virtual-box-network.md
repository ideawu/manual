# 网络

* 创建 Host Only Network
* 将 NAT 作为虚机的默认网卡
* 添加 Host Only Network 为第 2 网卡

Linux 配置:

```
ifconfig -a

$ cat /etc/network/interfaces
auto enp0s8
iface enp0s8 inet static
address 192.168.56.10
netmask 255.255.255.0

# ip 从 .4 开始

sudo ifconfig enp0s8 up
```

# 共享文件

#### 安装 vm tool

Devices -> Insert Guest Additions CD Image...

```
# 在虚拟机里
sudo mkdir -p /mnt/cdrom
sudo mount /dev/cdrom /mnt/cdrom
sudo /mnt/cdrom/VBoxLinuxAdditions.run
sudo adduser your-user vboxsf
```

设置共享文件夹, auto mount, permanent, dis-select read-only. 重启虚拟机.
