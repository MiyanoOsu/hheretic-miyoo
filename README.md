# Hheretic
A port of Hheretic v0.2.4 from https://hhexen.sourceforge.net/hheretic.html for miyoo cfw

# Keymap
*NOTE: due to weapon have 7 slots, use combo keys to switch slot manual from 1 to 7, 
~~~
Up : go ahead
Down: step back
Right: look to the right
Left: look to the left
A: fire
B: strafe
	(B + Left: strafe left)
	(B + Right: strafe right)
X: use
Y: run
Reset: open map
L + Left: move selection inventory to left
L + RIGHT: move selection inventory to right
L + Up: fly up
L + Down: fly down
R + Left: switch weapon slot down (default is slot 1)
R + Right: switch weapon slot up (inscrease slot number)
R + Up: look up
R + Down: look down
~~~
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
