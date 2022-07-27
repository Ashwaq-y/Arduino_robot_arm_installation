# Arduino IDE and robot arm package installation
In this repository I will show the steps of installing arduino IDE and the robot arm package.
First we will install the arduino IDE.
## Arduino IDE installation
Download the arduino IDE from [here](https://www.arduino.cc/en/software), then extract the file move it to home, and rename it to arduino.

Go to the terminal and type the following commmands:

```
cd arduino

sudo ./install.sh
```
```
./arduino
```
and the program should open.

Then to connect it with ROS andinstall the ros_lib library, follow the commands:

<ins>if you still in the arduino directory just type cd

```
sudo apt-get install ros-noetic-rosserial-arduino
sudo apt-get install ros-noetic-rosserial

```

got to the home and look for a file named sketchbook sometime it has a diffrent name in my case it was Arduino then open it and go the library file, open it in terminal and type the following command
```
 rm -rf ros_lib
 rosrun rosserial_arduino make_libraries.py .
```
you will find the library in the aurdino IDE like this:

![Screenshot 2022-07-27 223738](https://user-images.githubusercontent.com/108296165/181357508-3c3575da-ec33-48df-81c8-971292584772.png)


## Robot arm package installation
install the robot arm package using the following commandsa:
```
source /opt/ros/noetic/setup.bash
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
cd ~/catkin_ws/src
  ```
 ```
sudo apt install git
git clone https://github.com/smart-methods/arduino_robot_arm
```
### Dependencies
 
 ```
 sudo apt install python3-rosdep2
 rosdep update
 
 rosdep install --from-paths src --ignore-src -r -y
 sudo apt-get install ros-noetic-moveit
 sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
 sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
 sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
 ```
 
 ```
 catkin_make
 cd
 sudo nano ~/.bashrc
 ```
 the command sudo nano ~/.bashrc will open (bashrc) file add the follwing line at the end of the file 
 source /home/ashwaq/catkin_ws/devel/setup.bash
 
 <ins> Note that ashwaq is my account name you should replace it with your account name
 
  
  ![Screenshot 2022-07-27 233145](https://user-images.githubusercontent.com/108296165/181366550-19d9dfd2-ecc2-4123-be7d-a18d2e9ac5e7.png)
 
  Then type:
  
  ctrl+o
  
  Enter
  
  ctrl+x
  
  ```
  source ~/.bashrc
  roslaunch robot_arm_pkg check_motors.launch
  ```
  Then RViz program should open
  
  ![Screenshot 2022-07-27 233617](https://user-images.githubusercontent.com/108296165/181367304-1229da5f-8ab6-4d89-993e-3c268e4f335c.png)


  
 
 
 
