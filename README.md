# 安装步骤（简）： 
# (1)

`sudo apt-get update`

# (2)
```bash
sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch python3 python2.7 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib antlr3 gperf wget curl swig rsync quilt xsltproc libxml-parser-perl mercurial bzr ecj cvs 
```

# (3)
```bash
cd openwrt/
./scripts/feeds clean
./scripts/feeds update -a && ./scripts/feeds install -a
```

(4)
```bash
git clone https://github.com/kenzok8/openwrt-packages.git package/openwrt-packages
git clone https://github.com/kenzok8/small.git package/small
git clone https://github.com/KyleRicardo/MentoHUST-OpenWrt-ipk.git package/mentohust
git clone https://github.com/KyleRicardo/802.1X-Evasi0n.git package/802.1X-Evasi0n
git clone https://github.com/BoringCat/luci-app-mentohust.git package/luci-app-mentohust
git clone https://github.com/rosywrt/luci-theme-rosy.git package/luci-theme-rosy
git clone https://github.com/apollo-ng/luci-theme-darkmatter.git package/luci-theme-darkmatter
```

# (5)
```bash
make menuconfig
make -j4 download V=s && make -j4 V=s
```

# (6) 附加

`make package/.../*/compile V=s`

# mentohust: 
https://github.com/KyleRicardo/MentoHUST-OpenWrt-ipk.git 
https://github.com/KyleRicardo/802.1X-Evasi0n.git 

# luci-app-mentohust: 
https://github.com/BoringCat/luci-app-mentohust.git    
 //https://github.com/schen39/luci-app-mentohust.git     
 //https://github.com/a1ive/luci-mentohust.git 

# luci-app-*:
https://github.com/kenzok8/openwrt-packages.git 
https://github.com/kenzok8/small.git
//https://github.com/coolsnowwolf/lede.git 

# luci-theme-*:
https://github.com/rosywrt/luci-theme-rosy.git  
https://github.com/apollo-ng/luci-theme-darkmatter.git  

本人仅为搬运工，在此感谢各位前人的努力贡献。
