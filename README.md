### Software Architecture Project

## Group:NAV_02

## Student(s): Ginne vikas reddy(5061211), Elham Mohammadi(5093904) ,Donya Mostaghni yazdi(5060506), Rohit Adapa(5065424)

## Tutor(s): Fulvio Mastrogiovanni , mohamad Alameh, Alessandro Carfi, Simone Maccio


This project is a simulation of a mobile robot which does autonomous navigation in the given environment . In this the robot(husky) is equipped with a lidar sensor, microcontroller and a four wheel drive system, The robot is expected to navigate by itself autonomously and map the surrounding simultaneously by avoiding obstacles until it reaches the destination

The main aim of the project is to produce a safe path for the robot to execute by processing the data like odometry and lidar sensors in the environment map. We create maps of environments, localize the robot in the environment, make the robots perform path planning, visualize data of the different Navigation processes and using SLAM, and configure the different Navigation nodes



















# simmulation of the code

To launch the handshake between unity and ros

roslaunch mobile_robot_navigation_project navigation.launch

for localisation 

roslaunch mobile_robot_navigation_project gmapping.launch

for urdf of husky etc in rviz

roslaunch mobile_robot_navigation_project rviz.launch


to navigate
roslaunch mobile_robot_navigation_project move.launch


viedo simulation of the project
!https://user-images.githubusercontent.com/73032093/125796922-58fea1ea-4299-4829-b455-b36f528ede5a.mp4

