# ROS_Tutorials
Beginners tutorials for learning **ROS**, **TF**, **Configuring and Using the Navigation Stack**, **Movelt** and **Gazebo**. These tutorials were done in **ubuntu 16.04 LTS** and in **Kinetic ROS version**.

More information on ROS can be consulted in the case Documents.

## Working with GitHub 

See page [GitHub Tutorials](https://guides.github.com/activities/hello-world/) for knowing the basics of GitHub, like commits, merge and pull concepts. 

## ROS Tutorials

Tutorials for ROS in: [ROS Tutorials](http://wiki.ros.org/ROS/Tutorials). All the files from these tutorials are in the case **ROS Tutorials**. 

Note 1: Every tutorial, from Beginner and Intermediate Level, are working fine and are very good to understand.

## TF Tutorials

Tutorials for TF in: [TF Tutorials](http://wiki.ros.org/tf/Tutorials). For doing the tutorials you can choose from python or c++ languages. For a better understanding, you can also do the tutorial twice for both languages. In this package, I did just for python language. All the files from these tutorials are in the case **TF Tutorials**. 

Note 1: If you did just the python tutorials, the tutorial called [Debugging tf problems](http://wiki.ros.org/tf/Tutorials/Debugging%20tf%20problems) is not very complete. Since you will be working with c++ file and you have to add:
  - Code into the bottom of CMakeLists.txt to allow the c++ file compilation
```
add_executable(turtle_tf_listener_debug src/turtle_tf_listener_debug.cpp)
target_link_libraries(turtle_tf_listener_debug ${catkin_LIBRARIES})
```
  - Create a new lanch file called start_debug_demo.launch to call python and c++ files.

 Note 2: The package **geometry_tutorial** was cloned from [geometry_tutorial](https://github.com/ros/geometry_tutorials), since this package is used in the tutorial **Using Stamped datatypes with tf:: MessageFilter** and the default package was corrupt and missing files.

Note 3: For the tutorial [Using urdf with robot_state_publisher](http://wiki.ros.org/urdf/Tutorials/Using%20urdf%20with%20robot_state_publisher) is necessary to install the robot_state_publisher package though: 
```
sudo apt-get install ros-kinetic-robot-state-publisher
```
Further, in the rviz the fixed referential is the Odom referential.

## Configuring and Using the Navigation Stack Tutorials

Tutorials for **Configuring and Using the Navigation Stack** in: [Navigation Stack Tutorials](http://wiki.ros.org/navigation/Tutorials). This tutorial is a step by step for configuring your own robot sensors. Thus, you will have to put the sensor drive names on the launch file and configure everything as the tutorial explains. Since I did not have a real robot and sensors, I read and understood the tutorials, creating the files needed for future tuning of the files. All the files from these tutorials are in the case **Configuring and Using the Navigation Stack Tutorials**. 

Note 1: The tutorial [Setting up your robot using tf](http://wiki.ros.org/navigation/Tutorials/RobotSetup/TF)appears also in the TF tutorials.

Note 2: The tutorial [Setup and Configuration of the Navigation Stack on a Robot](http://wiki.ros.org/navigation/Tutorials/RobotSetup) must be done first that the [Basic Navigation Tuning Guide](http://wiki.ros.org/navigation/Tutorials/Navigation%20Tuning%20Guide) tutorial.

## MoveIt Tutorials

The MoveIt! Setup Assistant is in: [MoveIt Tutorials](http://docs.ros.org/kinetic/api/moveit_tutorials/html/doc/setup_assistant/setup_assistant_tutorial.html). All the files from these tutorials are in the case **MoveIt Tutorials**.

Note 1: In this tutorial, the robot fourth joint limit is -0.0698 rad and not 0, since the real robot joint limit is [-176, -4] [°], as presented in the robot datasheet in the case **Documents/MoveIt**.

## Gazebo Tutorials

Firts you must cheack what is the correct Gazebo version for the your ROS distribution: [Gazebo version](http://gazebosim.org/tutorials/?tut=ros_wrapper_versions). Gazebo Tutorials are in: [Gazebo Tutorials](http://gazebosim.org/tutorials?cat=connect_ros). All the files from these tutorials are in the case **Gazebo Tutorials**. 

Note 1: In the tutorial [Intermediate: Control plugin](http://gazebosim.org/tutorials?cat=guided_i&tut=guided_i5)to install Gazebo headers you must see your version of Gazebo for doing ```sudo apt install libgazebo8-dev``` and replace the 8 for the number of your Gazebo version. For killing the Gazebo server use the command ```killall gzserver```. Further in the file **velodyne.world** put:
```
<plugin name="velodyne_control" filename="./libvelodyne_plugin.so"/> 
```
instead of 
```
<plugin name="velodyne_control" filename="libvelodyne_plugin.so"/>.
```

Note 2: The Advanced tutorials are only advisable if you want to contribute to Gazebo development.