# Lab 5 - Follow Bot
Lab 5 for [COMSW4733 Computational Aspects of Robotics](http://www.cs.columbia.edu/~allen/F18/index.html) at Columbia University (Instructor: [Prof. Peter Allen](http://www.cs.columbia.edu/~allen/)).

## Introduction
In this lab, you are required to make the turtlebot follow a yellow track and action differently at intersections based on visual information. This is simulated in a Gazebo simulator.

## Usage
This ROS package allows you to load 4 different maps in Gazebo.

### Prerequisites
The package is tested on `python 2.7`, `ROS Indigo`, `Ubuntu 14.04` with `OpenCV 3.1.0` and `numpy 1.15.1`.

### Commands
To launch turtlebot and map for [part 1](#part-1-preparation-20-points)
```
roslaunch followbot launch.launch
```

To launch turtlebot and map for [part 2](#part-2-map-with-color-markers-40-points)
```
ROBOT_INITIAL_POSE="-x -2.85 -y -0.27 -Y 1.53" roslaunch followbot launch.launch world_file:=color.world
```

To launch turtlebot and map for [part 3](#part-3-map-with-shape-markers-40-points)
```
ROBOT_INITIAL_POSE="-x -2.85 -y -0.27 -Y 1.53" roslaunch followbot launch.launch world_file:=shape.world
```

To launch the map for [extra credits](#extra-credits-everything-in-the-same-color-10-points)
```
ROBOT_INITIAL_POSE="-x -2.85 -y -0.27 -Y 1.53" roslaunch followbot launch.launch world_file:=extra.world
```
## Instructions and Rubric
Related code for this lab can be found in Chapter 12 of [Programming Robotics with ROS](http://marte.aslab.upm.es/redmine/files/dmsf/p_drone-testbed/170324115730_268_Quigley_-_Programming_Robots_with_ROS.pdf). You should put your scripts under `src/`.

### Part 1: Preparation (**20 points**)
Use the command to load the map ([simple.png](worlds/simple.png)) for part 1. You should make the robot follow the yellow track nonstop. You video should show the robot following it for more than 1 round.

<p align="center">
  <img src="imgs/simple_map.png", height="450">
</p>

### Part 2: Map with color markers (40 points)
Use the command to load the map ([color.png](worlds/color.png)) for part 2. You should make the robot
- follow the yellow track when not at an intersection (**10 points**)
- turn left at the intersection with a green marker(**10 points**)
- turn right at the intersection with a blue marker (**10 points**)
- stop exactly on the red marker (**10 points**)

<p align="center">
  <img src="imgs/color_map.png", height="450">
</p>

### Part 3: Map with shape markers (40 points)
Use the command to load the map ([shape.png](worlds/shape.png)) for part 3. You should make the robot
- follow the yellow track when not at an intersection (**10 points**)
- turn left at the intersection with a triangle marker pointing left (**10 points**)
- turn right at the intersection with a triangle marker pointing right (**10 points**)
- stop exactly on the star marker (**10 points**)

<p align="center">
  <img src="imgs/shape_map.png", height="450">
</p>

### Extra credits: Everything in the same color (10 points)
Use the command to load the map ([extra.png](worlds/extra.png)) for the extra credit part. You should make the robot behave the same as part 3. There is no partial credit for this part. You either get 0 or 10.

<p align="center">
  <img src="imgs/extra_map.png", height="450">
</p>

## Submission Guidelines
- You should submit a `lab5_UNI1_UNI2.tar.gz` file which contains the modified package `followbot` that you cloned.
- It should include all files that we need to reproduce your video demos.
- You should replace everything in the existing `README.md` with the following sections:
	- Usage: how to run your code to reproduce your video demos. Clearly explain the functionalities of all added scripts.
	- Method: a brief description of your methods.
	- Video: a link to the Youtube video of working demos. You should **concatenate** demo videos of all parts into one single video.
	- Others: anything else you would like to include
- **Violation of these submission instructions will result in point deduction.**
