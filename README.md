# sts_bt_visualisation

## Overview

sts_behavior_tree ros visualisation node  for a behavior tree using it's sister package, the [sts_bt_library](http://gitlab_al.streetscooter.eu/al_SW_Team/sts_bt_library).

## Installation

### Building from Source

#### Dependencies

- [Robot Operating System (ROS)](http://wiki.ros.org) (middleware for robotics),
- sts_bt_library
- sudo apt-get install python-gi-cairo

#### Building

To build from source, clone the latest version from this repository into your catkin workspace and compile the package using

	cd catkin_ws/src
	git clone http://gitlab_al.streetscooter.eu/al_SW_Team/sts_bt_visualisation
	cd ../
	catkin build

## Usage

Run the main node with

	roslaunch sts_bt_visualisation sts_bt_visualisation.launch

If the sts_bt_main node is running, it will execute the behavior tree inside the sts_bt_library. The library will then send a single .xdot graph string to the visualisation, which will then display the received graph. After that, the library will only send ROS event messages, containing changes to the existing graph (color/state changes etc.), which will be applied onto the existing tree. 

You can also click the "Open dot file" button in the menu bar and select another .graphml file, which will be send back to the library and the library will stop it's execution, parse this file again and repeats the process.


## Bugs & Feature Requests

Please report bugs and request features using the [Issue Tracker](http://gitlab_al.streetscooter.eu/al_SW_Team/sts_bt_visualisation/issues).