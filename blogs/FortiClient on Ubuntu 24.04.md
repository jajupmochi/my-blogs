在Ubuntu 24.04系统下安装FortiClient VPN会出现一些依赖库缺失的错误。可使用以下方法依次安装依赖库和FortiClient VPN：

```
# 切换当前文件夹以下载deb库：
cd $HOME/Downloads/

# 依次下载和安装依赖库：
wget http://ftp.de.debian.org/debian/pool/main/liba/libayatana-indicator/libayatana-indicator7_0.9.3-1_amd64.deb
sudo dpkg -i libayatana-indicator7_0.9.3-1_amd64.deb
wget http://ftp.de.debian.org/debian/pool/main/libd/libdbusmenu/libdbusmenu-gtk4_18.10.20180917\~bzr492+repack1-3_amd64.deb
sudo dpkg -i libdbusmenu-gtk4_18.10.20180917\~bzr492+repack1-3_amd64.deb
wget http://ftp.de.debian.org/debian/pool/main/liba/libayatana-appindicator/libayatana-appindicator1_0.5.92-1_amd64.deb
sudo dpkg -i libayatana-appindicator1_0.5.92-1_amd64.deb
wget http://ftp.de.debian.org/debian/pool/main/n/nss/libnss3-tools_3.87.1-1_amd64.deb
sudo dpkg -i libnss3-tools_3.87.1-1_amd64.deb

# 下载和安装FortiClient VPN：
wget https://www.fortinet.com/support/product-downloads/forticlient
sudo dpkg -i forticlient_vpn_7.4.0.1636_amd64.deb
```

完成！

FortiClient VPN 也可在以下链接下载：Product Downloads | Fortinet Product Downloads | Support。选择“DOWNLOAD VPN for Linux .deb”。目前版本为7.4.0.1636_amd64。

依赖软件包均可在以下网站搜索下载，找到下方“Download”中的“Binary Package”使用 wget 下载即可：
[​pkgs.org/](https://pkgs.org/)
