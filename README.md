# Ros_SwBot
Autonomous bot using ROS


Husky Robot Documentation 
1. https://www.clearpathrobotics.com/assets/guides/kinetic/ros/Drive%20a%20Husky.html
2. https://www.clearpathrobotics.com/assets/guides/melodic/husky/DrivingHusky.html
3. https://clearpathrobotics.com/blog/2013/11/husky-simulation-in-gazebo/

Dependencies

    fath_pivot_mount_description: $ sudo apt-get install ros-noetic-fath-pivot-mount-description
    flir_camera_description: $ sudo apt-get install ros-noetic-flir-camera-description
    velodyne_description: $ sudo apt-get install ros-noetic-velodyne-description
    realsense2_description: $ sudo apt install ros-noetic-realsense2-description
    LMS1xx: $ sudo apt-get install ros-noetic-lms1xx
    robot_localization: $ sudo apt-get install ros-noetic-robot-localization
    interactive_marker_twist_server: $ sudo apt-get install ros-noetic-interactive-marker-twist-server
    twist_mux: $ sudo apt-get install ros-noetic-twist-mux
    teleop_twist_keyboard: $ sudo apt-get install ros-noetic-teleop-twist-keyboard
    teleop_twist_joy: $ sudo apt-get install ros-noetic-teleop-twist-joy
    rviz_imu_plugin: $ sudo apt-get install ros-noetic-rviz-imu-plugin
    gmapping: $ sudo apt-get install ros-noetic-gmapping

Installation

    Create a Catkin workspace (if not already present)

$ mkdir -p catkin_ws/src

    Change directory to the source space (src) of your Catkin workspace

$ cd catkin_ws/src

    Clone this repository:

$ git clone https://github.com/livinghumanz/Ros_SwBot

    Change directory back to the Catkin workspace:

$ cd ..

    Build the packages:

$ catkin_make

Usage:

Keyboard Teleoperation:

$ roslaunch husky_gazebo husky_playpen.launch
$ roslaunch my_teleoperation_launcher teleop_keyboard.launch

Map-Less Navigation:

$ roslaunch cpr_agriculture_gazebo agriculture_world.launch
$ roslaunch my_navigation_launcher map_less_navigation.launch

Map-Based Navigation:

$ roslaunch husky_gazebo husky_playpen.launch
$ roslaunch my_navigation_launcher map_based_navigation.launch


To save generated map to current working directory, run:

$ rosrun map_server map_saver -f <filename>




