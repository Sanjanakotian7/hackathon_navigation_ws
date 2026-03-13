Initialize the Workspace

`
mkdir -p ~/hackathon_ws/src
cd ~/hackathon_ws
colcon build
source install/setup.bash
`

Set Up the Base Robot

`
sudo apt remove gz-tools2
sudo apt autoremove
sudo apt install ros-$ROS_DISTRO-turtlebot3 ros-$ROS_DISTRO-turtlebot3-gazebo
`

Gazebo world

`
cd ~/hackathon_ws/src

git clone -b humble https://github.com/ROBOTIS-GIT/turtlebot3_autorace.git

cd ~/hackathon_ws

colcon build

source install/setup.bash

export TURTLEBOT3_MODEL=waffle

ros2 launch turtlebot3_gazebo turtlebot3_autorace_2020.launch.py
`
