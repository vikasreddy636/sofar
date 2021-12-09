### Software Architecture Project

## Group:NAV_02

## Student(s): Ginne vikas reddy(5061211), Elham Mohammadi(5093904) ,Donya Mostaghni yazdi(5060506), Rohit Adapa(5065424)

## Tutor(s): Fulvio Mastrogiovanni , mohamad Alameh, Alessandro Carfi, Simone Macciò


This project is a simulation of a mobile robot which does autonomous navigation in the given environment . In this the robot(husky) is equipped with a lidar sensor, microcontroller and a four wheel drive system, The robot is expected to navigate by itself autonomously and map the surrounding simultaneously by avoiding obstacles until it reaches the destination

The main aim of the project is to produce a safe path for the robot to execute by processing the data like odometry and lidar sensors in the environment map. We create maps of environments, localize the robot in the environment, make the robots perform path planning, visualize data of the different Navigation processes and using SLAM, and configure the different Navigation nodes


## uml diagram
![Screenshot 2021-07-08 at 10 34 24 PM](https://user-images.githubusercontent.com/73032093/125801199-624b265c-c95a-44f2-a92e-4b0542e43d4f.png)

## sequential diagram
![nav02](https://user-images.githubusercontent.com/73032093/125801295-7bc6ac2b-77be-4b72-987f-ccc2ca98ab00.jpeg)

## modules that are used

# slam-gmapping

The gmapping package provides laser-based SLAM (Simultaneous Localization and Mapping), as a ROS node called slam_gmapping. Using slam_gmapping, you can create a 2-D occupancy grid map from laser and pose data collected by a mobile robot.

make sure you install the pacage in the current working directory 

`https://github.com/ros-perception/slam_gmapping.git`

In order to establish a connection of the Lidar to ROS Kinetic

`sudo apt-get install ros-noetic-lms1xx`

# Rviz

rviz is a 3d visualization tool for ROS applications. It provides a view of your robot model, captures sensor information from robot sensors, and replay captured data. It can display data from cameras, lasers, from 3D and 2D devices including pictures and point clouds.The robot state publisher helps you to broadcast the state of your robot to the tf transform library.Joint state publisher is one of the ROS packages that is commonly used to interact with each joint of the robot. The package contains the joint_state_publisher node, which will find the nonfixed joints from the URDF model and publish the joint state values of each joint in the sensor_msgs/JointState message format.

To install rviz in ros 

`sudo apt-get install -y rviz`

For installing joint state publisher

`sudo apt-get install -y joint-state-publisher`

For installing robot state publisher

`sudo apt-get install ros-noetic-robot-state-publisher`


# move_base
The move_base node provides a ROS interface for configuring, running, and interacting with the navigation stack on a robot .Running the move_base node on a robot that is properly configured results in a robot that will attempt to achieve a goal pose with its base to within a user-specified tolerance. In the absence of dynamic obstacles,

Packages that need to be installed

`cd /opt/ros/noetic/lib`

`sudo apt-get install ros-noetic-move-base-msgs`


# Planner

This shows the local costmap that the navigation stack uses for navigation. The yellow line is the detected obstacle. For the robot to avoid collision, the robot's footprint should never intersect with a cell that contains an obstacle.
In the global costmap is everything the robot knows from previous visits and stored knowledge e.g. the map. In the local costmap is everything that can be known from the current position with the sensors right now. 

# Navigation

The Navigation Stack is fairly simple on a conceptual level. It takes in information from odometry and sensor streams and outputs velocity commands to send to a mobile base. As a prerequisite for navigation stack the robot should have a tf transform tree in place, and publish sensor data using the correct ROS Message types. Also, the Navigation Stack needs to be configured for the shape and dynamics of a robot to perform at a high level. To help with this process, this manual is meant to serve as a guide to typical Navigation Stack set-up and configuration.


To install the package

`sudo apt-get install ros-noetic-navigation`



# Execution of the code

Git clone the package

`https://github.com/vikasreddy636/sofar.git`

`https://github.com/vikasreddy636/hus.git`

To launch the handshake between unity and ros

`roslaunch mobile_robot_navigation_project navigation.launch`

for localisation the robot in the environment

`roslaunch mobile_robot_navigation_project gmapping.launch`

for urdf of husky etc in rviz

`roslaunch mobile_robot_navigation_project rviz.launch`

To plan the path and navigate the robot 

`roslaunch mobile_robot_navigation_project move.launch`

for rqt graph

`rosrun rqt_graph rqt_graph`

![rosgraph](https://user-images.githubusercontent.com/73032093/125849584-219f39fc-8848-4a42-80bd-476f1e363265.png)


viedo simulation of the project

https://user-images.githubusercontent.com/73032093/125797589-5cbe51c8-5839-4468-aa29-0940e857ee6a.mp4



