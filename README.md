# obot-autonomy-stack
# Robot Autonomy Stack (ROS2)

A ROS2-based autonomous navigation and exploration system built for differential-drive robots using LiDAR.

This project demonstrates a full autonomy pipeline:
**mapping → localization → planning → control**, designed to work in unknown environments.

## Demo
🎥 Autonomous exploration and exit behavior  
(see `demo/`)

## System overview
- SLAM-based mapping of unknown environments
- Frontier-based exploration
- Global planning with A*
- Fallback planning with RRT when maps are incomplete
- EKF + particle filter localization
- PID velocity control for differential-drive robots

## Tech stack
- ROS2
- C++
- LiDAR
- SLAM Toolbox
- RViz2

## Architecture
The system is composed of modular ROS2 nodes:
- **Mapping**: SLAM Toolbox
- **Localization**: particle filter + EKF fusion
- **Planning**: A* with cost smoothing and obstacle penalties
- **Exploration**: frontier detection and scoring
- **Control**: PID velocity controller

## My contributions
- Implemented frontier-based exploration and scoring
- Built A* planner with obstacle distance grid and penalties
- Integrated RRT fallback planning
- Tuned EKF + particle filter for centimeter-level pose accuracy
- Debugged LiDAR tilt and frame alignment issues

## How to run (high level)
This repo is intended as a demonstration of system design and algorithms.
Code is structured to be readable and modular rather than fully plug-and-play.

## Notes
See `notes/design.md` for algorithm details and design decisions.
