# Extended-Kalman-Filter
Implementing EKF package inside ROS

## ROS packages used
1. turtlebot_gazebo
2. robot_pose_ekf
3. odom_to_trajectory
4. turtlebot_teleop
5. rviz

## Sensor fusion

Inside an envirenment, a robot localizes itself by collecting data from its different onboard sensors. 
Each sensor has its own limitations. 

_Extended Kalman Filter will take all the noisy measurements, compare them, filter the noise, remove the uncertainty, and provide good estimate of robot's pose._

## turtlebot_gazebo package

Gazebo launchers and worlds for TurtleBot simulation. 

### Topic graph

![p1](https://user-images.githubusercontent.com/7389485/57750001-461cad80-7695-11e9-87a3-f52e8081676e.JPG)

## robot_pose_ekf package

This package is used to estimate the 3D pose of a robot based on (partial) pose measurement coming from different sources.
It uses Extended Kalman Filter with a 6D model (3D position and D orientation) to combine measurements from wheel odometry, IMU sensor, and visual odometry. 

### Topic graph

![p2](https://user-images.githubusercontent.com/7389485/57750705-1cb15100-7698-11e9-971d-adabf42ee36a.JPG)

## odom_to_trajectory package

This package is used to append odometry values into a trajectory path. 
It consists of two nodes:
1. Subscribes to 2D unfiltered robot odometry, appends robot's last 1000 poses and publishes robot's unfiltered trajectory.
2. Subscribes to 3D filtered odometry, also appends robot's last 100 poses and publishes the filtered trajectory. 

### Topic graph

![p3](https://user-images.githubusercontent.com/7389485/57751507-d1e50880-769a-11e9-840d-4bde55472501.JPG)

## turtlebot_teleop package

This package is used to drive the robot using keyboard. 


### Topic graph

![p4](https://user-images.githubusercontent.com/7389485/57752129-d27e9e80-769c-11e9-9bcd-0f60738ca717.JPG)

## rviz package
