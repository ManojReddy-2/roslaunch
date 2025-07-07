# Planning and Control for Mobile Robot(turtlebot 3) Navigation using A*+Kinematic controller + Potential fields


This project showcases a complete navigation system for the TurtleBot3 robot, designed to move intelligently through its environment. It brings together three key components: global path planning, local trajectory control, and obstacle avoidance. Using a custom-built A* algorithm, the robot plans an efficient route to its destination. A kinematic controller then guides the robot along this path with precision. To handle unexpected obstacles, a potential field-based method helps the robot react and adjust its movement in real time. 

# Description
This project contains implementations of the following algorithms:

- A*
- Kinematic controller
- Potential fields
- Navigation (Between kinematic and potential fields)

#Setup

1. Start by typing "roscore" in the terminal

2. To launch the file that include the world and the map
     roslaunch com_world custom_nav.launch

3. Once the RViz is open set the "intial pose using the 2D Pose Estimate" as that in Gazebo World.

4. Set the goal point where you need to TurtleBot3to go in the Gazeboworld using  2D Goal Pose.

5. The bot will follow the path and reach its goal.

# Requirements
1. Ubuntu 20.04
2. Gazebo 
3. ROS Noetic
4. TurtleBot3 Package
5. Python 3

# Detail about the scripts
-> global_planner.py: implements A* (for path planning)
-> navigator.py: manages waypoint control and obstacle response
-> potential_field.py: computes local repulsion and attraction
-> kinematic_controller.py: implements unicycle model control

# Author
Macherla Manoj Kumar Reddy
Technische Hochschule Deggendorf
    Mechatronics & CyberPhysical system
manoj.macherla@stud.th-deg.de
## Author

-   ManojReddy https://github.com/ManojReddy-2/Machaman.git

