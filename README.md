### Tutorial Interfacing ROS Kinetic with V-REP
- This tutorial is for V-Rep 3.4 or upper

#### Required.
```
sudo apt-get install xsltproc
```

#### Clone VRepRosInterface inside catkin workspace src subdirectory.
```
mkdir -p ~/catkin_ws/src/
cd ~/catkin_ws/ && catkin init 
cd ~/catkin_ws/src/ && git clone --recursive https://github.com/CoppeliaRobotics/v_repExtRosInterface.git vrep_ros_interface
```

#### Open the bashrc with gedit
```
gedit ~/.bashrc &
```
#### Add the following line at the end of the file
```
export VREP_ROOT="/home/user/vrep/"
```
#### Build
 ```
 cd ~/catkin_ws/ && catkin build
```
#### And then copy the plugin library from the catkin_ws/devel/lib/ to V-REP executable directory.
```
cp -iv ~/catkin_ws/devel/lib/libv_repExtRosInterface.so "$VREP_ROOT/"
```

#### References
   http://blog.mwang.de/2017/03/17/ros-kinetic-and-v-rep-interface/
   http://analuciacruz.me/articles/RosInterface_kinetic/
