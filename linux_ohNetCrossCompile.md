

###Cross compile ARMV5TE
#!/bin/bash
sudo update-alternatives --set gcc "/usr/bin/arm-linux-gnueabi-gcc-4.9"
sudo update-alternatives --set g++ "/usr/bin/arm-linux-gnueabi-g++-4.9"
export CROSS_COMPILE=/usr/bin/
#export CROSS_COMPILEFLAG= -march=armv5te -mtune=xscale -mfloat-abi=softfp
#export CROSS_LINKFLAGS= -march=armv5te -mtune=xscale -mfloat-abi=softfp
export CROSS_COMPILEFLAG="-march=armv5te -mtune=xscale"
export CROSS_LINKFLAGS="-march=armv5te -mtune=xscale"
sudo rm -rf linux_ARMV5/include
sudo rm -rf linux_ARMV5/lib
cd /usr/develop/git_ext/ohNet/
make clean
make native_only=yes
make install native_only=yes prefix=/usr/develop/bin/libs/ohNet/linux_ARMV5


###Cross compile ARMV7HF
#!/bin/bash
sudo update-alternatives --set gcc "/usr/bin/arm-linux-gnueabihf-gcc-4.9"
sudo update-alternatives --set g++ "/usr/bin/arm-linux-gnueabihf-g++-4.9"
export CROSS_COMPILE=/usr/bin/
export CROSS_COMPILEFLAG=
export CROSS_LINKFLAGS=
sudo rm -rf linux_ARMV7/include
sudo rm -rf linux_ARMV7/lib
cd /usr/develop/git_ext/ohNet/
make clean
make native_only=yes
make install native_only=yes prefix=/usr/develop/bin/libs/ohNet/linux_ARMV7
