### 固件发布地址：
https://github.com/a0575/R2S/releases

登录IP：192.168.2.1

默认用户名：root

密码：password

### 固件特性：

slim版固件只有OpenWrt本体，但内置了“本地软件源”，包含大部分常用插件，不喜欢固件预装繁杂插件的人可以选择这个版本，进入后台软件包选装所需插件

采用ext4文件系统，刷卡之后可自行使用分区工具对sd卡扩容根分区至最大

支持usb无线网卡（RTL8821CU芯片，例如COMFAST 811AC），可以驱动无线网卡运行在5G频段

使用在线升级时，根分区会自动扩容，方便折腾

### 生成自己所需固件

因为本项目预编译的Image builder，生成固件仅需1-3分钟，如果有兴趣自定义固件可以Fork本项目，
编辑r2s.config.seed文件，删除不需要的luci app软件包配置行，
添加自己所需的软件，可用软件的列表在 https://github.com/a0575/R2S/suites/2516361744/artifacts/54479797 获取

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

