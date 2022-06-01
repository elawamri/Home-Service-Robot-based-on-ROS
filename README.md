# Home-Service-Robot-based-on-ROS
## Introduction
The main mission of any autonomous mobile robot is to reach its goal
with high accuracy and precision, and to do so, some problems need to
be solved.

- **_Localization_** Problem:

using ```AMCL``` package in ROS the robot could localize itself through
Monte Carlo localization algorithm which is a probabilistic localization
system for a robot moving in 2D, and uses a particle filter to track the
pose of a robot against a known map

- **_Mapping_** Problem:

and using ```RTAB-Map``` Package which is a Graph-Based SLAM approach
based on an incremental appearance-based loop closure detector.

- **_Navigation_** Problem:

and for that, we used ROS Navigation Stack which implements
Dijkstra's algorithm for path planning, It takes in information from
odometry and sensor streams and outputs velocity commands to send
to a mobile base, and for the scope of this project there is more packages to talk about,


![mapScreenshot](https://user-images.githubusercontent.com/105011124/171307707-529e2372-510e-4ae1-a0d2-bac12dfe65b8.PNG)
## Packages Description 
1. ```pick_objects```:
it contains a cpp node that is responsible to
move the mobile robot autonomously towards a certain pickup point,
then move again to a certain drop-off point.

2. ```add_markers```: 
it contains a cpp node that is responsible to
show a marker in the pickup point and whenever the robot reaches this
point the marker disappear, as the robot picked it up, then the marker
will appear again in the drop-off point as the robot dropped it off.

3. ```rviz_config```: 
this folder contains the config files of rviz , it saves us the
time to add the same objects every time we run the simulation.

4. ```scripts```: 
this folder contains the shell scripts files, the shell script Is a
type of executable file, that saves us the time we write terminal
commands, it’s a single file that runs all the commands needed to run
the simulation with all it’s nodes.

5. ```slam_gmapping```:
the gmapping package provides laser-based SLAM to
the simulation.

6. ```turtlebot_interactions```:
in this package we use the
turtlebot_rviz_launchers sub package to launch rviz file.

7. ```turtlebot_simulator```:
the package responsible to launch the gazebo
environment with our mobile robot and the designed world
## Robot's Test
### Run ```home_service.sh``` script:
```bash
$ cd /home/workspace/catkin_ws/
$ source devel/setup.bash
$ cd src/scripts
$ cd ./home_service.sh
```
