### R2S在线升级方法:
(注意:目前仅支持R2S，仅能升级到minimal版本固件，如果你使用的是Lienol版也不要用此方法升级)  
先安装好依赖
```bash
opkg update
opkg install zstd
opkg install libzstd
```
然后下载脚本执行
```bash
wget -qO- https://github.com/My-Compile/nanopi-R2S/blob/master/scripts/autoupdate.sh | sh
```
