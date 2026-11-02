# Lab 01: Autonomous Mobile Robot

A ROS 2 Humble and Gazebo simulation of a differential-drive robot capable of sensing its environment, avoiding obstacles, and executing navigation commands.

## Technologies
- ROS 2 Humble
- Gazebo Sim
- Python
- URDF / Xacro
- LiDAR, Depth Camera, IMU

## Features
- LiDAR-based obstacle detection.
- Depth camera and IMU integration.
- Autonomous obstacle avoidance.
- Configurable movement and turning speeds.
- Robot status reporting.
- Enable/disable and speed-control services.
- Odometry-based rotation action with feedback and cancellation.
- Square navigation.

## Project Structure

```text
lab_01/
├── diffdrive_bot/
├── lab_interfaces/
├── my_robot_interfaces/
└── my_robot_nodes/
```

## Running the Simulation

Build the workspace:

```bash
cd ~/ros2_ws
colcon build
source install/setup.bash
```

Launch Gazebo:

```bash
ros2 launch diffdrive_bot gazebo.launch.py
```

Start the controller in another terminal:

```bash
ros2 launch diffdrive_bot control.launch.py
```

Run the robot nodes:

```bash
ros2 run my_robot_nodes obstacle_avoider
ros2 run my_robot_nodes rotate_server
```

## Custom ROS 2 Interfaces

- `ObstacleInfo.msg`: Obstacle detection data.
- `RobotStatus.msg`: Robot state and obstacle distance.
- `SetTurnSpeed.srv`: Dynamic turning speed configuration.
- `Rotate.action`: Rotation goals, feedback, and results.

## Before

![Robot Before](lab01/images/robo.jpg)

## After

![Robot After](lab01/images/robotics.PNG)

## Challenges
- Docker and Gazebo GUI configuration.
- URDF/Xacro XML debugging.
- ROS 2 package and custom interface configuration.
- Python indentation and executable configuration.
- ROS 2 topic, service, and action communication.
- GitHub fork authentication and repository organization.

## Learning Outcomes
Practical experience with robot simulation, sensor integration, ROS 2 communication, custom interfaces, motion control, and autonomous navigation.

**Course:** Introduction to Robotics and Intelligent Systems  
**Institution:** Addis Ababa University  
**Lab:** 01
