发布地址：
https://github.com/My-Compile/nanopi-R2S/releases

### R2S在线升级方法:  
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
