# Robotiq

## Installation

```bash
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
git clone git@github.com:liuyangdh/robotiq.git
cd ..
sudo apt-get update
rosdep update
rosdep install --from-paths src --ignore-src -y
catkin_make
source devel/setup.bash
```

## Network setup
detail see this [link](http://wiki.ros.org/robotiq/Tutorials/Control%20of%20a%203-Finger%20Gripper%20using%20the%20Modbus%20TCP%20Protocol)

IPv4 settings:

Address: 192.168.1.2

Netmask: 255.255.255.0

## Run demo
1st terminal: open roscore
```bash
sourc /opt/ros/noetic/setup.bash
roscore
```

2nd terminal: run the gripper driver node
```bash
source /opt/ros/noetic/setup.bash
source devel/setup.bashp
rosrun robotiq_2f_gripper_control Robotiq2FGripperTcpNode.py 192.168.1.11
```

3rd terminal: run the griper control node 
```bash
source /opt/ros/noetic/setup.bash
source devel/setup.bashp
rosrun robotiq_2f_gripper_control robotiq_2f_gripper_ctrl.py
```


## Status

As of 2021-05-28, it would appear this repository is ***unmaintained***.

Robotiq is not maintaining the packages in this repository and the last active maintainer ([jproberge](https://github.com/jproberge)) does not appear to be active any more.

The ROS-Industrial consortia are not involved: for historical reasons, the `robotiq` repository is hosted on the `ros-industrial` Github organisation, but there is no direct link with any of the other repositories there.

Please direct support requests to [dof.robotiq.com](https://dof.robotiq.com/). The tracker here is not monitored by Robotiq employees.


## ROS Distro Support

|         | Indigo | Jade | Kinetic | Melodic |
|:-------:|:------:|:----:|:-------:|:-------:|
| Branch  | [`indigo-devel`](https://github.com/ros-industrial/robotiq/tree/indigo-devel) | [`jade-devel`](https://github.com/ros-industrial/robotiq/tree/jade-devel) | [`kinetic-devel`](https://github.com/ros-industrial/robotiq/tree/kinetic-devel) | [`kinetic-devel`](https://github.com/ros-industrial/robotiq/tree/kinetic-devel) |)
| Status  |  supported | not supported |  supported |  supported |
| Version | [version](http://repositories.ros.org/status_page/ros_indigo_default.html?q=robotiq) | [version](http://repositories.ros.org/status_page/ros_jade_default.html?q=robotiq) | [version](http://repositories.ros.org/status_page/ros_kinetic_default.html?q=robotiq) | [version](http://repositories.ros.org/status_page/ros_melodic_default.html?q=robotiq) |

## Travis - Continuous Integration

Status: [![Build Status](https://travis-ci.com/ros-industrial/robotiq.svg?branch=kinetic-devel)](https://travis-ci.com/ros-industrial/robotiq)

## ROS Buildfarm

There are no up-to-date releases of these packages available from the ROS buildfarm.

[![support level: community](https://img.shields.io/badge/support%20level-community-lightgray.svg)](http://rosindustrial.org/news/2016/10/7/better-supporting-a-growing-ros-industrial-software-platform)

Robotiq meta-package.  See the [ROS wiki][] page for more information. 

## License

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

## Contents

This repo holds source code for all versions > groovy. For those versions <= groovy see: [SVN repo][]

[ROS wiki]: http://ros.org/wiki/robotiq
[SVN repo]: https://code.google.com/p/swri-ros-pkg/source/browse

