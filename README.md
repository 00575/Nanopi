R2S在线升级方法:

先安装好依赖

opkg update

opkg install zstd

opkg install libzstd

然后下载脚本执行

wget -qO- https://github.com/My-Compile/nanopi-R2S/blob/master/scripts/autoupdate.sh | sh
