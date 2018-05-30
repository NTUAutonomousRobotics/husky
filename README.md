husky
=====

Common ROS packages for the Clearpath Husky, useable for both simulation and
real robot operation.

 - husky_control : Control configuration
 - husky_description : Robot description (URDF)
 - husky_msgs : Message definitions
 - husky_navigation : Navigation configurations and demos

For Husky instructions and tutorials, please see [Robots/Husky](http://wiki.ros.org/Robots/Husky).

To create a custom Husky description or simulation, please fork [husky_customization](https://github.com/husky/husky_customization).

husky_desktop
=============

Desktop ROS packages for the Clearpath Husky, which may pull in graphical dependencies.

 - husky_viz : Visualization (rviz) configuration and bringup

For Husky instructions and tutorials, please see http://wiki.ros.org/Robots/Husky

husky_robot
===========

Robot ROS packages for the Clearpath Husky, for operating robot hardware.

 - husky_bringup : Bringup launch files and scripts.
 - husky_base : Hardware driver for communicating with the onboard MCU.

For Husky instructions and tutorials, please see http://wiki.ros.org/Robots/Husky

husky_simulator
==============

Simulator ROS packages for the Clearpath Husky.

 - husky_gazebo : Gazebo plugin definitions and extensions to the robot URDF.

Husky model is customized to support the addition of other sensors such as Velodyne VLP-16, HDL-32E and UR5. In order for these sensors to be properly integrated to the simulation system, the following packages need to be installed.

 - velodyne_description
 - velodyne_gazebo_plugins
 
Both of these packages can be installed as
```
sudo apt-get install ros-kinetic-velodyne-simulator
```
Currently, in order to load either the VLP-16 or HDL-32E sensor onto the robot's sensor arch, the HUSKY_URDF_EXTRAS environment variable needs to be set to the required urdf file.

For VLP-16
```
export HUSKY_URDF_EXTRAS=~/ros_kinetic_ws/src/husky_simulator/husky_description/urdf/accessories/VLP-16.urdf.xacro
```
For HDL32-E
```
export HUSKY_URDF_EXTRAS=~/ros_kinetic_ws/src/husky_simulator/husky_description/urdf/accessories/HDL-32E.urdf.xacro
```

In order to get the UR5 simulated, the set of packages come under the universal_robot stack needs to be installed 
```
sudo apt-get install  ros-kinetic-universal-robot
```


For Husky instructions and tutorials, please see http://wiki.ros.org/Robots/Husky
