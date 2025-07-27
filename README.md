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

# WAD file info:

Shareware 1.0: 023b52175d2f260c3bdc5528df5d0a8c heretic1.wad (5,120,300 bytes)

Shareware 1.2: ae779722390ec32fa37b0d361f7d82f8 heretic1.wad (5,120,920 bytes)

Registered 1.0 (3 episodes): 3117e399cdb4298eaa3941625f4b2923 heretic.wad (11,096,488 bytes)

Registered 1.2 (3 episodes): 1e4cb4ef075ad344dd63971637307e04 heretic.wad (11,095,516 bytes)

Retail 1.3 (Shadow of the Serpent Riders, extended, 5 episodes): 66d686b1ed6d35ff103f15dbd30e0341 heretic.wad (14,189,976 bytes)
