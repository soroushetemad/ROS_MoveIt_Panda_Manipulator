# Panda Robot Manipulator Control with MoveIt

This C++ code demonstrates a simple application to control a robot manipulator using MoveIt library within ROS (Robot Operating System). The program moves the robot arm (named "panda_arm") to two different poses while controlling a gripper or hand (named "panda_hand") to open and close.

## Overview

The code is structured as follows:
- Initialization of ROS node and MoveIt interfaces.
- Setting up start state to the current robot state.
- Defining two target poses (`pose1` and `pose2`) for the robot arm.
- Planning and executing motion to `pose1`, opening the hand.
- Planning and executing motion to `pose2`, closing the hand.
- Finally, moving the robot back to the start position.

## Code Explanation

### Libraries Used
- `memory`: For smart pointers.
- `rclcpp/rclcpp.hpp`: ROS 2 C++ API.
- `moveit/move_group_interface/move_group_interface.h`: MoveIt! library for robot motion planning.

### Functions
- `open_hand`: Opens the robot hand by setting joint positions.
- `close_hand`: Closes the robot hand by setting joint positions.

### Main Function
- Initializes ROS and creates a node named "manipulator".
- Creates MoveIt! MoveGroup interfaces for the arm (`panda_arm`) and hand (`panda_hand`).
- Sets the start state of the arm and hand to the current robot state.
- Defines `pose1` and `pose2` for the arm's target positions.
- Plans and executes motion to `pose1`, then opens the hand.
- Plans and executes motion to `pose2`, then closes the hand.
- Moves the arm back to the "home" position.
- Shuts down ROS and exits.

## How to Use
1. Ensure ROS and MoveIt! are properly installed.
2. Compile the code using a C++ compiler (`g++` recommended).
3. Run the executable, which will:
   - Initialize ROS.
   - Move the arm to `pose1` while opening the hand.
   - Move the arm to `pose2` while closing the hand.
   - Return the arm to the "home" position.

## Dependencies
- ROS 2: Ensure ROS 2 is installed.
- MoveIt! library: For motion planning and control.
- C++ Compiler: To compile and run the code.

## Video Links

- RVIZ Simulation: https://youtu.be/Qs8nekDoCMs
- Setup Assistant configuration: https://youtu.be/uP3c0ydvTdQ 
