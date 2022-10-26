# Turtlebot_PC_Setup using:
- Ubuntu 20.04
- ROS Foxy

# 3.1 Install ROS2 on Remote PC

```
wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros2_foxy.sh
sudo chmod 755 ./install_ros2_foxy.sh
bash ./install_ros2_foxy.sh
```

# 3.2 Install Dependent ROS2 Packages

###### Install Gazebo11

```
sudo apt-get install ros-foxy-gazebo-*
```

###### Install Cartographer

```
sudo apt install ros-foxy-cartographer
sudo apt install ros-foxy-cartographer-ros
```

###### Install Navigation2

```
sudo apt install ros-foxy-navigation2
sudo apt install ros-foxy-nav2-bringup
```
