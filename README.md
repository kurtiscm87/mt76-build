# mt76-build


install ubuntu (current version: Ubuntu 24.04.2 LTS) https://ubuntu.com/tutorials/install-ubuntu-desktop
download packages 
# Update package list
sudo apt-get update
 
# Install essential packages
sudo apt-get install -y build-essential libncurses5-dev gawk git \
    subversion libssl-dev gettext unzip zlib1g-dev file \
    libelf-dev ecj fastjar java-propose-classpath wget \
    python3 python3-distutils python3-setuptools python3-dev \
    python3-pip rsync
 
# optional packages
sudo apt-get install swig
     3. compile openwrt image MT7986 OpenWRT Trunk Image

git clone https://git.openwrt.org/openwrt/openwrt.git
cd openwrt
./scripts/feeds update -a
./scripts/feeds install -a
make menuconfig
make
