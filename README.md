# isaac_ros_vslam
forked from https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_visual_slam


# clone the code
```
git clone https://github.com/zhj-buffer/isaac_ros_vslam.git
cd ./isaac_ros_vslam
vcs import src < isaac_ros2.repos
```

# install the dependences
```
sudo apt-get install python3-rosdep -y
sudo rosdep init 
rosdep update
rosdep install -i --from-path src --rosdistro galactic --skip-keys=librealsense2 -y
```

# build the project (source the ros2 distro first)
```
colcon build
```

# Run the test, more information pls refer to https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_visual_slam
```
alan@nvdia-desktop:/home/sdcard/isaac_ros$ ros2 launch isaac_ros_visual_slam isaac_ros_visual_slam_realsense.launch.py
[INFO] [launch]: All log files can be found below /home/alan/.ros/log/2022-04-25-14-17-12-479727-yongming-desktop-18776
[INFO] [launch]: Default logging verbosity is set to INFO
1650867432.831963 [0]       ros2: using network interface eth0 (udp/10.19.207.168) selected arbitrarily from: eth0, docker0
[INFO] [component_container-1]: process started with pid [18789]
[INFO] [realsense2_camera_node-2]: process started with pid [18790]
[component_container-1] 1650867432.965553 [0] component_: using network interface eth0 (udp/10.19.207.168) selected arbitrarily from: eth0, docker0
[realsense2_camera_node-2] 1650867433.051994 [0] realsense2: using network interface eth0 (udp/10.19.207.168) selected arbitrarily from: eth0, docker0
[realsense2_camera_node-2] [INFO] [1650867433.087704574] [camera]: RealSense ROS v3.2.3
[realsense2_camera_node-2] [INFO] [1650867433.087974924] [camera]: Built with LibRealSense v2.50.0
[realsense2_camera_node-2] [INFO] [1650867433.088071249] [camera]: Running with LibRealSense v2.50.0
[realsense2_camera_node-2] [WARN] [1650867433.094412567] [camera]: No RealSense devices were found!
[component_container-1] [INFO] [1650867433.174449738] [visual_slam_launch_container]: Load Library: /home/sdcard/isaac_ros/install/isaac_ros_visual_slam/lib/libvisual_slam_node.so
[component_container-1] [INFO] [1650867433.202947012] [visual_slam_launch_container]: Found class: rclcpp_components::NodeFactoryTemplate<isaac_ros::visual_slam::VisualSlamNode>
[component_container-1] [INFO] [1650867433.203143694] [visual_slam_launch_container]: Instantiate class: rclcpp_components::NodeFactoryTemplate<isaac_ros::visual_slam::VisualSlamNode>
[component_container-1] [INFO] [1650867433.290594782] [visual_slam_node]: Elbrus version: 10.0
[INFO] [launch_ros.actions.load_composable_nodes]: Loaded node '/visual_slam_node' in container '/visual_slam_launch_container'
[realsense2_camera_node-2] [WARN] [1650867439.097489663] [camera]: No RealSense devices were found!
[realsense2_camera_node-2] [WARN] [1650867445.100385242] [camera]: No RealSense devices were found!
```
