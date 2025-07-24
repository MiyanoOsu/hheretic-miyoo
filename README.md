# Hheretic
A port of Hheretic v0.2.4 from https://hhexen.sourceforge.net/hheretic.html for miyoo cfw

# How to build
You need docker, debian linux or arch linux
~~~
# if you first time build code, run this command to set up toolchain
docker pull miyoocfw/toolchain-shared-uclibc:latest

# to compile
docker run --volume ./:/src/ -it miyoocfw/toolchain-shared-uclibc:latest
cd src
./configure --disable-gl --enable-fullscreen --host=arm-linux CC=arm-linux-gcc
make -j $(nproc)
~~~