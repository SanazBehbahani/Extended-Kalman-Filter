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

## odom_to_trajectory package

## turtlebot_teleop package

## rviz package
