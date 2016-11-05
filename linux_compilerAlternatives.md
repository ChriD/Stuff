
#remove alternatives
sudo update-alternatives -remove-all gcc
sudo update-alternatives -remove-all g++

# add alternatives
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/arm-linux-gnueabi-gcc-4.9 70
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/arm-linux-gnueabihf-gcc-4.9 80
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.9 90
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-5 100

sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/arm-linux-gnueabi-g++-4.9 70
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/arm-linux-gnueabihf-g++-4.9 80
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.9 90
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-5 100


# change standard compiler
sudo update-alternatives --config gcc
sudo update-alternatives --config g++
