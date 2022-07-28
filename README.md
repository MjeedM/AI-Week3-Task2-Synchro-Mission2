# AI-Week3-Task2-Synchro-Mission2

Week 3 Tasks:

Task 2: Installing the the arm package with it's dependences. and running it on RVIZ simulator.

Synchronization mission 2: Installing the real arm and controlling it via the simulator.

## Table of Contents
* [Task 1: Installing the the arm package](#1)
* [Synchronization mission 2: Installing and controlling the real arm](#2)


<a name= "1"></a>
## Task 1: Installing the the arm package
First, I had to create a catkin work space
then, inside the work space src file I ran this instruction:

```git clone https://github.com/smart-methods/arduino_robot_arm.git ```

and inside the work space, I downloaded all the packages by these instructions:
```
$ sudo apt-get install ros-noetic-moveit
$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
I also add the source isntruction of the catkin work space to the .bashrc file

```source /home/mjeed/catkin_ws2/devel/setup.bash```


### Results:


### Resources
- [https://www.youtube.com/watch?v=8uxd9RBQvmQ]

<a name= "2"></a>
## Synchronization mission 2: Installing and controlling the real arm


### Step 1:
- First we Connected the motors with the arduino uno and the breadboard 
### Step 2
- Second we connected the laptop with the arunio uno and uploaded the sweep code that gives the motors its initial positions.
### Step 3
- Then we Ran this instruction inside the *[arduino / libraries]* terminal 

```$ sudo chmod 777 /dev/ttyUSB0 ```
### Step 4
- After that we uploaded the arduino arm code to the arduino uno
### Step 5
- To control it using RIVS: run these instructions inside a new terminal 
```roslaunch robot_arm_pkg check_motors.launch```

  and inside another terminal 
```rosrun rosserial_python serial_node.py _port:=/dev/ttyUSB0 _baud:=115200```
### Step 6
- To control it using moveit: run these instructions inside a new terminal 
```$ roslaunch moveit_pkg demo.launch``` 

  and inside another terminal 
```rosrun rosserial_python serial_node.py _port:=/dev/ttyUSB0 _baud:=115200```

### Results:
check the video alos..
