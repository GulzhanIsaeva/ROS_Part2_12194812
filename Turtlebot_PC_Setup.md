# Turtlebot PC Setup using:
- Ubuntu 20.04
- ROS Foxy

# 3.1 Install ROS2 on Remote PC

```
wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros2_foxy.sh
sudo chmod 755 ./install_ros2_foxy.sh
bash ./install_ros2_foxy.sh
```

# 3.2 Install Dependent ROS2 Packages

## Install Gazebo11

```
sudo apt-get install ros-foxy-gazebo-*
```

## Install Cartographer

```
sudo apt install ros-foxy-cartographer
sudo apt install ros-foxy-cartographer-ros
```

## Install Navigation2

```
sudo apt install ros-foxy-navigation2
sudo apt install ros-foxy-nav2-bringup
```

# Install TurtleBot3 Packages

## Install TurtleBot3 via Debian Packages

```
mkdir -p ~/turtlebot3_ws/src
cd ~/turtlebot3_ws/src/
git clone -b foxy-devel https://github.com/ROBOTIS-GIT/DynamixelSDK.git
git clone -b foxy-devel https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
git clone -b foxy-devel https://github.com/ROBOTIS-GIT/turtlebot3.git
cd ~/turtlebot3_ws
colcon build --symlink-install
echo 'source ~/turtlebot3_ws/install/setup.bash' >> ~/.bashrc
source ~/.bashrc
```

# 3.4 Environment Configuration

## Set the ROS environment for PC

```
echo 'export ROS_DOMAIN_ID=30 #TURTLEBOT3' >> ~/.bashrc
source ~/.bashrc
```

















