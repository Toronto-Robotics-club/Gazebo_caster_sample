Caster Wheel Example for Gazebo
===============================

At the present time I have not been able to locate any practical guides for
building a caster wheel. This packages is part of this question (http://answers.gazebosim.org/question/24474/caster-wheel-sample-code/) and will hopefully be a resource on how to implement a caster wheel for use in Gazebo. The name of the robot is "jimmy".

Package Contents
================

 - jimmy_description : this directory contains all the xacro files for building the robot urdf.
 - jimmy_gazebo : contains a blank world and a launch file to start Gazebo.


Launching Simulation
====================
This package is varified working in Gazebo7 ver 7.16, ROS Kinetic, on/in Ubuntu 16.04. 
It is assumed you have all this software installed and working. 

Terminal 1:
 1. put these files into ~/Desktop/workspace/src directory
 2. navigate to the directory with the files, and build the project:
 > $ cd Desktop/workspace
 > $ catkin_make
 3. run a setup script:
 > $ source devel/setup.bash 
 4. run the project:
 > $ roslaunch jimmy_gazebo jimmy_world.launch

Terminal 2:
 5. To give commands to the diff_drive controller to see motion use the TAB-TAB completion:
 > $ rostopic pub /cmd_vel geometry_msgs/Twist "linear:
  x: 0.0
  y: 0.0
  z: 0.0
angular:
  x: 0.0
  y: 0.0
  z: 0.0" 
 
NOTE: to see rotation enter values in angular.z and to see linear motion enter values in linear.x

Viewing URDF
============
If you want to see the actual URDF file and not the xacro files, navigate to the location 
where the xacro files are located and run this command:
  > rosrun xacro xacro jimmy.xacro > readme.txt




