### 固件发布地址：
https://github.com/a0575/R2S/releases

登录IP：192.168.2.1

默认用户名：root

密码：password

++++++++++++++++++++++++++++++++++++++++++++++++++++++++

### 终端内在线升级方法： 

```bash
wget -qO- https://github.com/a0575/R2S/raw/master/scripts/update.sh | sh
```

slim纯净版

```bash
wget -qO- https://github.com/a0575/R2S/raw/master/scripts/update.sh | ver=-slim sh
```
++++++++++++++++++++++++++++++++++++++++++++++++++++++++

### R2S自用精简固件 在线升级:  
先安装好依赖

```bash
opkg update
opkg install zstd
opkg install libzstd
```
然后下载脚本执行

```bash
wget -qO- https://github.com/00575/nanopi-R2S/raw/master/scripts/autoupdate.sh | sh
```

