﻿OpenWrt-dist LuCI
===

适用项目
---
 > 默认不带相应的 UCI 配置文件, 需要搭配以下软件包使用  

 Name                     | Description
 -------------------------|-----------------------------------
 [openwrt-chinadns][5]    | ChinaDNS for OpenWrt
 [openwrt-redsocks2][R]   | RedSocks2 for OpenWrt
 [openwrt-shadowvpn][8]   | ShadowVPN for OpenWrt
 [openwrt-shadowsocks][7] | Shadowsocks-libev for OpenWrt

编译说明
---
 > 从 OpenWrt 的 [SDK][S] 编译  

```bash
# luci-app 为全平台通用
tar xjf OpenWrt-SDK-ar71xx-for-linux-x86_64-gcc-4.8-linaro_uClibc-0.9.33.2.tar.bz2
cd OpenWrt-SDK-ar71xx-*
# 获取 Makefile
git clone https://github.com/fo369/openwrt-dist-luci.git package/openwrt-dist-luci
# 选择要编译的包 LuCI -> 3. Applications
make menuconfig
# 开始编译
make V=99
```


  
  [5]: https://github.com/fo369/openwrt-chinadns
  [7]: https://github.com/fo369/openwrt-shadowsocks
  [8]: https://github.com/fo369/openwrt-shadowvpn
  [R]: https://github.com/fo369/openwrt-redsocks2
  [S]: http://wiki.openwrt.org/doc/howto/obtain.firmware.sdk
