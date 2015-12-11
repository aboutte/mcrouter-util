# mcrouter-util

To build rpm:

* launch centos 7 AMI
* yum update -y
* yum install -y git vim screen
* cd /root/
* git clone https://github.com/aboutte/mcrouter-util.git
* cd mcrouter-util
* git submodule init
* git submodule update
* cd fpm
* ./build-rpm.sh

Installing rpm

yum install -y epel-release
yum install -y mcrouter-0.14.0-0.x86_64.rpm
echo "PATH=$PATH:/usr/local/bin/" >> /root/.bashrc
source /root/.bashrc
Add /usr/local/lib to /etc/ld.so.conf and refresh the cache with sudo ldconfig ((https://lonesysadmin.net/2013/02/22/error-while-loading-shared-libraries-cannot-open-shared-object-file/))

When folly or mcrouter src need to be updated

* cd submodule_directory
* git checkout v1.0
* cd ..
* git add submodule_directory
* git commit -m "moved submodule to v1.0"
* go into build-rpm.sh and update version number of fpm
* git push
