# ROS_Tutorials
Beginners tutorials for learning **ROS**, **TF**, **Movelt** and **Gazebo**. This tutorials were done in **ubunto 16.04 LTS** and in **Kinetic ROS version**.

More information on ROS can be consulted in the case Documents.

## Working with GitHub

See page https://guides.github.com/activities/hello-world/ for knowing the basis of GitHub, like commits, merge and pull concepts. 

## ROS

The package for the ROS tutorials is the **beginner_tutorials**.

Tutorials for ROS in: http://wiki.ros.org/ROS/Tutorials. Every tutorial, from Beginner and Intermediate Level, are working fine and are very good to understand.

## TF

The packadge for the TF tutorials is the **learning_tf**.

Tutorials for TF in: http://wiki.ros.org/tf/Tutorials. For doing the tutorials you can choose from python or c++ languages. For a better understanding, you can also do the tutorial twice for both languages. In this package I did just for python language.

Note: If you did just the python tutorials, the tutorial called **Debugging tf problems** is not very complete. Since you will be working with c++ file and you have to add:
  - Code into the bottom of CMakeLists.txt to allow the c++ file compilation
  		add_executable(turtle_tf_listener_debug src/turtle_tf_listener_debug.cpp)
		target_link_libraries(turtle_tf_listener_debug ${catkin_LIBRARIES})
  - Create a new lanch file called start_debug_demo.launch to call python and c++ files.

## Movelt





## Gazebo

