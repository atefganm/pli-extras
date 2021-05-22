# Extra repositories for PLi's OE: https://github.com/OpenPLi/openpli-oe-core

# Dreambox
* dm500hd
* dm500hdv2
* dm520
* dm7020hd
* dm7020hdv2
* dm7080
* dm800
* dm8000
* dm800se
* dm800sev2
* dm820
* dm900
* dm920

# Fulan
* spark
* spark7162

# Ubuntu 18.04 LTS setup
* sudo dpkg-reconfigure dash

Answer: No

* sudo apt-get install autoconf automake bison bzip2 cvs diffstat flex g++ gawk gcc gettext git gzip help2man ncurses-bin libncurses5-dev libc6-dev libtool make texinfo patch perl pkg-config subversion tar texi2html wget chrpath libxml2-utils xsltproc python-setuptools libc6 genromfs mtd-utils dpkg-dev sshpass poedit translate-toolkit xclip linux-firmware linux-headers-`uname -r` linux-headers-generic linux-image-generic linux-libc-dev linux-source u-boot-tools upx-ucl doxygen repo optipng python-dev libglib2.0-dev pngquant default-jdk

# How to build an image (Example: dm800)
1. Clone openpli-oe-core somewhere:
* git clone -b develop https://github.com/OpenPLi/openpli-oe-core.git

2. Enter the openpli-oe-core directory:
* cd openpli-oe-core

3. Clone pli-extras:
* git clone https://github.com/PLi-metas/pli-extras.git

4. Initialize and update all repositories:
* pli-extras/update.sh

5. Build PLi image for your machine:
* MACHINE=dm800 make image

6. (Optional) Build the feed for your machine:
* MACHINE=dm800 make feed
```
Hint: Each time you run the command from step 4 all git repositories will get updated to their latest versions.
```
