### 固件发布地址：
https://github.com/My-Compile/nanopi-R2S/releases

### R2S精简固件
登录IP：192.168.2.1，默认用户名是root, 密码是password

### R2S精简固件 在线升级方法:  
先安装好依赖
```bash
opkg update
opkg install zstd
opkg install libzstd
```
然后下载脚本执行
```bash
wget -qO- https://github.com/My-Compile/nanopi-R2S/raw/master/scripts/autoupdate.sh | sh
```

++++++++++++++++++++++++++++++++++++++++++++++++++++++++

### R1S-R2S-R4S-openwrt固件
登录IP：192.168.1.1，默认用户名是root, 密码是password

### openwrt固件临时说明：
暂时不要fork后自己编译，因为编译缓存工作路径不同，会导致你的编译时间非常长。

### R1S-R2S-R4S-openwrt固件 在线升级方法:  
先安装好依赖
```bash
opkg update
opkg install --force-overwrite pv fdisk
```
然后下载脚本执行
```bash
wget -qO- https://github.com/My-Compile/nanopi-R2S/raw/master/scripts/update.sh | sh
```
