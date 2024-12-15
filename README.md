### ++  [openwrt-packages](https://github.com/openwrt/packages "悬停显示")  
* 默认 ip： 192.168.1.1 ~~（更改位置：[package/base-files/files/bin/config_generate](https://github.com/microdockman/001/blob/master/package/base-files/files/bin/config_generate "悬停显示")）~~
* 默认应用：
    * [~~docker~~](https://github.com/lisaac/luci-app-dockerman "悬停显示")  [passwall](https://github.com/xiaorouji/openwrt-passwall/tree/luci "悬停显示")  [zerotier]( https://github.com/openwrt/packages/tree/master/net/zerotier "悬停显示")  [~~diskman~~](https://github.com/lisaac/luci-app-diskman "悬停显示")   [~~unblockmusic~~](https://github.com/project-openwrt/luci-app-unblockneteasemusic "悬停显示")
    * ~~....+ttyd+samba4+mariadb(full)+postgreSQL(full)+php7+usb2/3+adbye+cfdisk+opkg....~~
    
### 编译
1. sudo apt-get update

2. sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libncursesw5-dev libz-dev patch python3 python2.7 unzip zlib1g-dev lib32gcc1 libc6-dev-i386      subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint      device-tree-compiler g++-multilib antlr3 gperf wget swig rsync curl llvm libtinfo5

3.    tmp  

         - [ ] 可选：    ~~sudo ln -s /lib/x86_64-linux-gnu/libtinfo.so.6 /lib/x86_64-linux-gnu/libtinfo.so.5~~  

4.    git clone https://github.com/microdockman/001

5.    cd 001

         - [ ] 可选：  ~~git clone https://github.com/smalldickman/luci-app-unblockmusic.git package/luci-app-unblockmusic~~
                 
6.    chmod 777 staging_dir/host/bin/upx staging_dir/hostpkg/bin/ninja

7.    ./scripts/feeds update -a

         - [ ] 可选：  ~~rm -f feeds/packages/net/zerotier/files/etc/init.d/zerotier~~

         - [ ] 可选：  ~~cp -i 0tmp/luci feeds/luci/modules/luci-base/root/etc/config/luci~~
         
         - [ ] 可选：  ~~cp -i 0tmp/index.htm feeds/luci/modules/luci-mod-status/luasrc/view/admin_status/index.htm~~
              
         - [ ] 可选：  ~~cp -r 0tmp/runc/* feeds/packages/utils/runc~~  
         
         - [ ] 可选：    ~~git clone https://github.com/project-openwrt/luci-app-unblockneteasemusic.git package/luci-app-unblockneteasemusic~~  
         
         - [ ] 可选：  ~~cp -r 0tmp/docker-ce/* feeds/packages/utils/docker-ce~~  
       
8.    ./scripts/feeds install -a

9.    make menuconfig

         - [ ] 可选：    cp diffconfig-latest .config && make defconfig  
 
10.    make -j4 download V=s

         - [ ] 可选：    ./scripts/diffconfig.sh > diffconfig

11.   make -j4 V=s

12.   sudo apt-get update && sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libncursesw5-dev libz-dev patch python3 python2.7 unzip zlib1g-dev libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib antlr3 gperf wget swig rsync curl llvm libtinfo5 && git clone https://github.com/microdockman/001 && cd 001 && chmod 777 staging_dir/host/bin/upx staging_dir/hostpkg/bin/ninja && ./scripts/feeds update -a && ./scripts/feeds install -a && ./scripts/feeds install -a && cp diffconfig-latest .config && make defconfig && make menuconfig && make -j3 download V=s && make -j3 download V=s && make -j3 V=s

### 库

* [openwrt](https://github.com/openwrt/openwrt "悬停显示")  [kenzok8](https://github.com/kenzok8/openwrt-packages "悬停显示")  [lede](https://github.com/coolsnowwolf/lede "悬停显示")  [lienol](https://github.com/xiaorouji/openwrt-passwall "悬停显示")  

### License

OpenWrt is licensed under GPL-2.0
