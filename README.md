# ROS-Installation-On-Ubuntu

# Firstly Download Virtual Box  & Ubuntu


## 1.	Download virtual box from: https://www.virtualbox.org/wiki/Downloads

### VirtualBox is a free open-source software that’s developed by Oracle Corporation. It’s a visualization tool and it’s used in this task to run another operating system inside windows.


## 2.	Download Ubuntu: https://releases.ubuntu.com/16.04/


## 3.	Start Oracle VirtualBox and chose the name, type and version. Fill in the name and chose the Linux type with Ubuntu version.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/3.VirtualBoxStart.png)



## 4.	Choose the (RAM) memory size.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/4.MemorySize.png)



## 5.	Choose create a virtual hard disk

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/5.VirtualHardDisk.png)



## 6.	Chose the hard disk file type (as default).

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/6.HardDiskFileType.png)


## 7.	Choose dynamically allocated storage.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/7.StorageOnPhysicalHardDisk.png)



## 8.	Choose the ubuntu OS capacity and it’s recommended to be 30 GB or 40 GB.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/8.FileLocatioAndSize.png)



## ## ## ## 9.	Upload the Ubuntu file to Virtual Box by going to the Virtual Box setting/storage and choose the controller optical drive to be the Ubuntu disk file that has been downloaded in step 2.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/9.UploadUbuntuToVirtualBox.png)



## ## ## 10.	Click “Start” to start the Ubuntu OS.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/10.StartUbuntu.png)



## ## 11.	Choose the Ubuntu disk and start.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/11.ChooseTheUbuntuDisk.png)



## 12.	Choose Install Ubuntu.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/12.ChooseInstallUbuntu.png)



## ## ## 13.	Choose to install third-party software… and continue.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/13.ChooseInstallThird-PartySoftware….png)



## ## 14.	Choose “Erase disk and install Ubuntu”.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/14.ChooseEraseDisk.png)



## 15.	Choose region, language, name and password then wait and restart.

![](Steps%20Pictures/Download%20VirtualBox%20&%20Ubuntu/15.ChooseRegionLanguageNameAndPasswordThenRestart.png)


# After restarting, now Ubuntu Operation System is ready to use by VirtualBox.




# Then Install ROS on Ubuntu


## 1.	Start Ubuntu from VirtualBox and set up:


          a.	sources.list by the code: 
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

     b.	Key:
    
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

    c.	Update:
    
sudo apt-get update

    d.	Install full ROS Kinetic desktop:
    
sudo apt-get install ros-kinetic-desktop-full

![](Steps%20Pictures/Install%20ROS/1.a-d.UbuntuStart&ROS_Setup.png)



    e.	Environment setup: 
    
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc

source ~/.bashrc

    f.	Dependencies for building packages:
    
sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

![](Steps%20Pictures/Install%20ROS/1.e-f.UbuntuStart&ROS_Setup.png)



    g.	Initialize rosdep:
    
sudo apt install python-rosdep

sudo rosdep init

rosdep update

![](Steps%20Pictures/Install%20ROS/1.g.UbuntuStart&ROS_Setup.png)



### 2.	Check environment:

printenv | grep ROS

![](Steps%20Pictures/Install%20ROS/2.EnvironmentCheck.png)



#### 3.	Ensure that ROS is installed properly by running the ROS master code, it can be done by running “roscore”.

![](Steps%20Pictures/Install%20ROS/3.EnsureInstallation.png)


## The istallation is finished now and ROS is ready to use.


References:
1. https://www.udemy.com/course/ros-basics-program-robots/
2. http://wiki.ros.org/kinetic/Installation/Ubuntu
