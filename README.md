# FASTER-LIO-ROS2

Migration [Faster-LIO](https://github.com/gaoxiang12/faster-lio) to ROS2 

Originally Implemented by https://github.com/GangGeon10/Faster-LIO-ROS2

## Environment
* Ubuntu 20.04 LTS
* ROS galactic version

## Known Problems
The code won't work when migrating to ROS Jazzy. Odometry drifts in the very beginning.

## Dependency
1. ROS galactic
2. glog: ```sudo apt-get install libgoogle-glog-dev```
3. eigen: ```sudo apt-get install libeigen3-dev```
4. pcl: ```sudo apt-get install libpcl-dev```
5. yaml-cpp: ```sudo apt-get install libyaml-cpp-dev```
6. [Livox-SDK2](https://github.com/Livox-SDK/Livox-SDK2) (you can ignore steps 6 and 7 by switching to the branch https://github.com/RollingOat/faster-lio-ros2/tree/faster-lio-ros2-ouster)
7. [livox_ros_driver2](https://github.com/Livox-SDK/livox_ros_driver2)

## Build

```
cd ~/<work_space>/src
git clone https://github.com/RollingOat/faster-lio-ros2.git
cd ~/<work_space>
colcon build --symlink-install
```

## Run
```
source install/local_setup.sh
ros2 launch faster_lio mapping_ouster64.launch.py
```

## Acknowledgments
Thanks to [Faster-LIO](https://github.com/gaoxiang12/faster-lio) for their research
