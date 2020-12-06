# Package_has_no_installation_candidate
E: Package 'package_name' has no installation candidate

mpogian@debian:~$ sudo apt update
Hit:1 http://deb.debian.org/debian buster-updates InRelease                  
Hit:2 http://security.debian.org/debian-security buster/updates InRelease    
Hit:3 http://packages.microsoft.com/repos/vscode stable InRelease            
Hit:4 http://deb.i2p2.no unstable InRelease   
Reading package lists... Done
Building dependency tree       
Reading state information... Done
15 packages can be upgraded. Run 'apt list --upgradable' to see them.

mpogian@debian:~$sudo apt install default-jdk
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Package default-jdk is not available, but is referred to by another package.
This may mean that the package is missing, has been obsoleted, or
is only available from another source

E: Package 'default-jdk' has no installation candidate

mpogian@debian:~$ sudo featherpad /etc/apt/sources.list

put inside the sources.list the above "urls".

i. deb http://deb.debian.org/debian buster main
ii. deb-src http://deb.debian.org/debian buster main

once you done it.
mpogian@debian:~$ sudo apt update
sudo apt update
Hit:1 http://security.debian.org/debian-security buster/updates InRelease
Get:2 http://deb.debian.org/debian buster InRelease [121 kB]
Hit:3 http://deb.debian.org/debian buster-updates InRelease
Get:4 http://deb.debian.org/debian buster/main Sources [7,842 kB]            
Hit:5 http://packages.microsoft.com/repos/vscode stable InRelease            
Hit:6 http://deb.i2p2.no unstable InRelease                                  
Get:7 http://deb.debian.org/debian buster/main amd64 Packages [7,907 kB]     
Get:8 http://deb.debian.org/debian buster/main Translation-en [5,971 kB]     
Fetched 21.8 MB in 1min 40s (219 kB/s)                                       
Reading package lists... Done
Building dependency tree       
Reading state information... Done
54 packages can be upgraded. Run 'apt list --upgradable' to see them.

mpogian@debian:~$ sudo apt install default-jdk
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  default-jdk-headless libice-dev libpthread-stubs0-dev libsm-dev libx11-dev
  libxau-dev libxcb1-dev libxdmcp-dev libxt-dev openjdk-11-jdk
  openjdk-11-jdk-headless openjdk-11-jre openjdk-11-jre-headless
  x11proto-core-dev x11proto-dev xorg-sgml-doctools xtrans-dev
Suggested packages:
  libice-doc libsm-doc libx11-doc libxcb-doc libxt-doc openjdk-11-demo
  openjdk-11-source visualvm fonts-ipafont-gothic fonts-ipafont-mincho
  fonts-wqy-microhei | fonts-wqy-zenhei fonts-indic
The following NEW packages will be installed:
  default-jdk default-jdk-headless libice-dev libpthread-stubs0-dev
  libsm-dev libx11-dev libxau-dev libxcb1-dev libxdmcp-dev libxt-dev
  openjdk-11-jdk openjdk-11-jdk-headless x11proto-core-dev x11proto-dev
  xorg-sgml-doctools xtrans-dev
The following packages will be upgraded:
  openjdk-11-jre openjdk-11-jre-headless
2 upgraded, 16 newly installed, 0 to remove and 52 not upgraded.
Need to get 269 MB/269 MB of archives.
After this operation, 247 MB of additional disk space will be used.
Do you want to continue? [Y/n] 

enter Y or y and the packages will start to install.

//I hope that helped you.

