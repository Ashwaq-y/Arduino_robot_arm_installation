# Arduino robot arm installation
In this repository I will show the steps of installing arduino IDE and the robot arm package.
First we will install the arduino IDE.
# Arduino IDE installation
Download the arduino IDE from [here](https://www.arduino.cc/en/software), then extract the file move it to home and rename it to arduino for simplicity.

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




