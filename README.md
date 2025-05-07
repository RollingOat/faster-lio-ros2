# FASTER-LIO-ROS2

This branch removes dependecies on livox driver and livox SDK2 for easier building.

Migration [Faster-LIO](https://github.com/gaoxiang12/faster-lio) to ROS2 

Originally Implemented by https://github.com/GangGeon10/Faster-LIO-ROS2

## Environment
* Ubuntu 20.04 LTS
* ROS galactic version

## Dependency
1. ROS galactic
2. glog: ```sudo apt-get install libgoogle-glog-dev```
3. eigen: ```sudo apt-get install libeigen3-dev```
4. pcl: ```sudo apt-get install libpcl-dev```
5. yaml-cpp: ```sudo apt-get install libyaml-cpp-dev```
~~6. [Livox-SDK2](https://github.com/Livox-SDK/Livox-SDK2)~~
~~7. [livox_ros_driver2](https://github.com/Livox-SDK/livox_ros_driver2)~~

## Build

```
cd ~/<work_space>/src
git clone https://github.com/frankgon1627/Faster-LIO-ROS2.git
cd ~/<work_space>
colcon build --symlink-install --cmake-args -DCMAKE_BUILD_TYPE=Release

```

## Run
```
source install/local_setup.sh
ros2 launch faster_lio mapping_ouster64.launch.py
ros2 bag play faster_lio_ros2_test_10hz --qos-profile-overrides-path qos_config.yaml 
```

## use docker and vscode
1. run the docker container
2. open vscode on your local machine, search for cmd: Attach to Running Container

## Acknowledgments
Thanks to [Faster-LIO](https://github.com/gaoxiang12/faster-lio) for their research
