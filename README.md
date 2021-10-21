### Nanopi-immortalwrt 18.06固件发布地址：
https://github.com/00575/Nanopi/releases

(支持设备：r1s r2s r4s r1p r1s-h3 x86 r2c )

登录IP：192.168.2.1 默认用户名：root 密码：password

### 固件特性：

slim版固件只有OpenWrt本体，但内置了“本地软件源”，包含大部分常用插件，不喜欢固件预装繁杂插件的人可以选择这个版本，进入后台软件包选装所需插件

采用ext4文件系统，刷卡之后可自行使用分区工具对sd卡扩容根分区至最大。使用在线升级时，根分区会自动扩容，方便折腾


#### 1-3分钟生成自己所需固件

[ Fork ]本项目，

编辑[ r2s.config.seed ]文件，直接删除不需要的luci app软件包配置行， 添加自己所需的软件配置

完成之后进入[ Actions ]，点击左侧[ DIY ]，

点击右侧[ Run workflow ]

输入你的设备名称（r2c r2s r4s r1s r1s-h3 r1p x86 ）

然后点击[ Run ]稍等即可在github actions构件输出处获取自己所需的固件

### 终端内在线升级方法： 

多插件版
```bash
wget -qO- https://github.com/00575/Nanopi/raw/master/scripts/autoupdate.sh | sh
```

slim纯净版
```bash
wget -qO- https://github.com/00575/Nanopi/raw/master/scripts/autoupdate.sh | ver=-slim sh
```

docker版
```bash
wget -qO- https://github.com/00575/Nanopi/raw/master/scripts/autoupdate.sh | ver=-with-docker sh
```

临时测试
```bash
wget -qO- https://github.com/00575/Nanopi/raw/master/scripts/Test-update.sh | sh
```
