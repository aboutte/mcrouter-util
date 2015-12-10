# mcrouter-util

To build rpm:

* launch centos 7 AMI
* yum update -y
* yum install -y git vim
* cd /root/
* git clone https://github.com/aboutte/mcrouter-util.git
* cd mcrouter-util
* git submodule init
* git submodule update
* cd fpm
* ./build-rpm.sh









To update the submodule reference:

git pull
git submodule foreach git pull origin master