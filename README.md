# Install Ubuntu
Creat ubuntu image on flashdrive and start up using that USB drive
>> Have a flash drive with Ubuntu 20.04, although mysterious graphics error exists

# Creatng a bootlable USB using Windoes
Download Ubuntu image .iso file 
Use Rufus to create Bootle USB
https://www.maketecheasier.com/use-rufus-create-bootable-flash-drive/

# Install gcc 
```
sudo apt update
sudo apt install build-essential
gcc --version
sudo apt install cmake
```

# Install Nvidia drivers
Download drivers from Nvidia wesite using computer specs
sudo sh NVIDIA....run

# Install CUDA 
Use CUDA instillation instructions, including setup guide for Linux

# Install Git
```
sudo apt install git
git --version
git config --global user.email "youremail@yourdomain.com"
git config --global user.name "username"
git config --list
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys
Enter ls -al ~/.ssh to see if existing SSH keys are present.
```

## Install large file Git
Download https://git-lfs.com/

# Install Python
```
sudo apt-get -y install python3-dev python3-pip 
pip3 --version
sudo apt install python3-pip
pip --version
sudo pip install numpy scipy matplotlib scikit-image scikit-learn ipython

# for upgrading packages in python3
python3 -m pip install --upgrade <package>


```

# Not doing this one this time around!
# Install OpenCV
```
sudo apt-get -y install libjpeg8-dev libjasper1 libpng-dev
sudo apt-get -y install libtiff-dev
sudo apt-get -y install libavcodec-dev libavformat-dev libswscale-dev libdc1394-22-dev
sudo apt-get -y install libxine2-dev libv4l-dev
sudo apt -y install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev
sudo apt-get -y install qt5-default libgtk2.0-dev libtbb-dev
sudo apt-get -y install libatlas-base-dev
sudo apt-get -y install libfaac-dev libmp3lame-dev libtheora-dev
sudo apt-get -y install libvorbis-dev libxvidcore-dev
sudo apt-get -y install libopencore-amrnb-dev libopencore-amrwb-dev
sudo apt-get -y install x264 v4l-utils
sudo apt-get -y install libprotobuf-dev protobuf-compiler
sudo apt-get -y install libgoogle-glog-dev libgflags-dev
sudo apt-get -y install libgphoto2-dev libeigen3-dev libhdf5-dev doxygen


git clone https://github.com/opencv/opencv.git
	cd opencv 
	git checkout 4.0.0 
	cd ..

	git clone https://github.com/opencv/opencv_contrib.git
	cd opencv_contrib
	git checkout 4.0.0
	cd ..

	cd opencv
	mkdir build
	cd build

# If needed 
	#  sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/g++-6 6
	#  sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-6 6

	# Last tested on 30/12/19
	cmake -D CMAKE_BUILD_TYPE=RELEASE \
	      -D CMAKE_INSTALL_PREFIX=/usr/local \
	      -D ENABLE_PRECOMPILED_HEADERS=OFF \
	      -D INSTALL_C_EXAMPLES=ON \
	      -D INSTALL_PYTHON_EXAMPLES=ON \
	      -D WITH_TBB=ON \
	      -D WITH_V4L=ON \
	      -D OPENCV_PYTHON3_INSTALL_PATH=/usr/lib/python3.6/ \
	      -D WITH_QT=ON \
	      -D WITH_OPENGL=ON \
	      -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules \
	      -D BUILD_EXAMPLES=ON \
	      -D WITH_EIGEN=ON \
	      -D OPENCV_GENERATE_PKGCONFIG=ON ..

	make -j($nproc)
	sudo make install 
	sudo ldconfig
```

# Intall ROS Noetic (Ubuntu 20.04)
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
sudo apt update
sudo apt install ros-noetic-desktop-full
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

# Install Terminator 
```
sudo apt-get install terminator
```

# Install VSCode

# Setting a Static ethernet IP address for Jetson 
- Desktop computer:
** Create new ethernet connection and in IP4 setting enable share with other devices
- Jetson:
** Most common ethernet connection name is eth0
** Create file etc/network/interfaces.d/eth0 and insert:
```
auto eth0
iface eth0 inet static
	address 10.42.0.8 # IP address you want to assigne the Jetson
	netmask 255.255.255.0
	broadcast 10.42.0.255
	gateway 10.42.0.1 # IP address from your desktop computer (Make sure bothe computers have same subnet)
```
** Reboot Jetson





