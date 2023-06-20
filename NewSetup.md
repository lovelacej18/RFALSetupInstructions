##### Specifications
GRAPHICS -> NV137/GeForce 1060, 1070, Pascal
OS -> Ubuntu 20.04

##### Installations
**gcc**
```
sudo apt update
sudo apt install build-essential
gcc --version
sudo apt install cmake
```

**NVIDIA Driver**
Running 525 - going through the Ubuntu software and updates graphical menu

**CUDA**
Installing 11.7
```
wget https://developer.download.nvidia.com/compute/cuda/11.7.0/local_installers/cuda_11.7.0_515.43.04_linux.run
sudo sh cuda_11.7.0_515.43.04_linux.run
```

Updating PATH and LD_LIBRARY_PATH with new info
```
export PATH=/usr/local/cuda-11.7/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-11.7/lib64\{LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}
```

**git**
```
sudo apt install git
git --version
git config --global user.email "youremail@yourdomain.com"
git config --global user.name "username"
git config --list
```
https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys
Enter ```ls -al ~/.ssh```  to see if existing SSH keys are present.

**LFG (large file git)**
For debian (we are running ubuntu so I'm pretty sure its fine...)
```
curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
sudo apt-get install git-lfs
```

**Python3** -> 

**ROS Noetic**
ROS1
Already installed but:
```
echo "deb http://packages.ros.org/ros/ubuntu focal main" | sudo tee /etc/apt/sources.list.d/ros-focal.list
```
```
sudo apt install ros-noetic-desktop-full
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

**Terminator**
```
sudo apt-get install terminator
```

**ZED SDK**
Downloading 3.8.2 for CUDA 11.7, Ubuntu 20
Go to the folder where the installer has been downloaded
```
sudo apt install zstd
```
Make the downloaded file executable... and then execute it! 
```
chmod +x ZED_SDK_Ubuntu20_cuda11.7_v3.8.2.zstd.run
./ZED_SDK_Ubuntu20_cuda11.7_v3.8.2.zstd.run
```

**CudNN**



##### Pre-Existing on Computer
Ubuntu 20.04
VSCode
ROS Noetic (newest version!)

---

Almost re-installed ubuntu when the network wasn't showing up - but now we're good! 

Update 6-20-23 - OpenCV version 4.2.0 already installed (assumably with ZED wrapper dependencies!)

