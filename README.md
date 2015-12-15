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

When folly or mcrouter src need to be updated

* cd submodule_directory
* git checkout v1.0
* cd ..
* git add submodule_directory
* git commit -m "moved submodule to v1.0"
* go into build-rpm.sh and update version number of fpm
* git push
