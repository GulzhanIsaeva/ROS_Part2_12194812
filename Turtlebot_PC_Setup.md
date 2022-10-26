# Turtlebot PC Setup using:
- Ubuntu 20.04
- ROS Foxy

# 3.1 Install ROS2 on Remote PC

```
wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros2_foxy.sh
```

![image](https://user-images.githubusercontent.com/90166739/197957125-6e1cb46b-4060-4e3d-8bc1-08ea4b25adef.png)


```
sudo chmod 755 ./install_ros2_foxy.sh
bash ./install_ros2_foxy.sh
```

![image](https://user-images.githubusercontent.com/90166739/197955991-3959f72b-b620-467a-9d43-b615322d50e1.png)


# 3.2 Install Dependent ROS2 Packages

## 1 Install Gazebo11

```
sudo apt-get install ros-foxy-gazebo-*
```

## 2 Install Cartographer

```
sudo apt install ros-foxy-cartographer
sudo apt install ros-foxy-cartographer-ros
```

![image](https://user-images.githubusercontent.com/90166739/197956208-2a06a126-ffbf-485b-8b1c-18ab72aff11b.png)


## 3 Install Navigation2


```
sudo apt install ros-foxy-navigation2
sudo apt install ros-foxy-nav2-bringup
```

# 3.3 Install TurtleBot3 Packages

## Install TurtleBot3 via Debian Packages

```
mkdir -p ~/turtlebot3_ws/src
cd ~/turtlebot3_ws/src/
```

![image](https://user-images.githubusercontent.com/90166739/197956707-c845ddd4-3d0f-4ed9-8f1d-85ff670a3d8d.png)

```
git clone -b foxy-devel https://github.com/ROBOTIS-GIT/DynamixelSDK.git
git clone -b foxy-devel https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
git clone -b foxy-devel https://github.com/ROBOTIS-GIT/turtlebot3.git
cd ~/turtlebot3_ws
colcon build --symlink-install
echo 'source ~/turtlebot3_ws/install/setup.bash' >> ~/.bashrc
source ~/.bashrc
```

![image](https://user-images.githubusercontent.com/90166739/197956805-495f4fcd-eb3d-453d-9931-84dd348ff2e0.png)




# 3.4 Environment Configuration

## Set the ROS environment for PC

```
echo 'export ROS_DOMAIN_ID=30 #TURTLEBOT3' >> ~/.bashrc
source ~/.bashrc
```

![image](https://user-images.githubusercontent.com/90166739/197956575-adbfd261-3812-4235-b972-6dff0ad16db4.png)

















