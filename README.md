### 固件发布地址：
https://github.com/huyunlei2020/R2S/releases

登录IP：192.168.2.1

默认用户名：root

密码：password

++++++++++++++++++++++++++++++++++++++++++++++++++++++++

### R1S-R2S-R4S-openwrt固件 在线升级方法:  
先安装好依赖
```bash
opkg update
opkg install --force-overwrite pv fdisk
```
然后下载脚本执行
```bash
wget -qO- https://github.com/huyunlei2020/R2S/raw/master/scripts/update.sh | sh
```

++++++++++++++++++++++++++++++++++++++++++++++++++++++++

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
