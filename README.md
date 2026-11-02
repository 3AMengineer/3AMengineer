# Hi, I'm Shourya 👋

**Field robotics @ [UAS-DTU](https://github.com/UpdeshinglyYours/UAS-DTU-Rover-Autonomy) · DARPA Triage Challenge, 2nd place (non-funded) · Mathematics & Computing @ DTU**

I build autonomy for robots that have to work outside the simulator. On UAS-DTU's DARPA Triage Challenge team I work across the full stack of our autonomous ground rover and drones: perception, localization, navigation, control, and the hardware underneath.

## What I work on

- **Real-world rover autonomy:** Blickfeld 3D LiDAR, LiDAR-inertial odometry, Nav2 and MAVROS on an ArduRover (Cube Orange+) platform with an onboard Jetson, taken from Gazebo to outdoor field runs.
- **Localization benchmarking:** GenZ-ICP, SuperOdometry, VINS-Fusion and ArduPilot EKF3 compared against RTK-GPS ground truth on the same outdoor runs; 2D maps with SLAM Toolbox for Nav2.
- **Control:** an adaptive velocity controller in ROS 2 that learns the rover's response online, with separate left- and right-turn gains, to close the gap between what Nav2 commands and what the rover actually does.
- **Drone autonomy:** autonomous lawnmower area-coverage missions on ArduPilot, DroneKit missions with a hand-written PID position controller in SITL, and build and flight prep of Tarot, ShadowX and other UAS-DTU airframes.
- **Simulation and digital twins:** a SUMO digital twin of Delhi's ITO corridor, built from real traffic data, with adaptive signal control and a live Gazebo 3D view (Team Pravah, Smart India Hackathon 2026).

## Field debugging

Most of what I've learned came from failures that don't announce themselves:

- undetected frame misalignments that left us with wrong sensor extrinsics
- LiDAR–IMU time offsets and motion distortion
- LiDAR odometry degrading in feature-poor areas
- odometry published without covariance, which our EKF couldn't fuse
- compass-driven heading drift in the flight controller
- USB 3.0 interference knocking out CAN GPS

When the robot misbehaves, I check frames, timestamps, covariances and the physical setup before I touch a single tuning parameter.

## Projects

| Project | What it is |
|---|---|
| [**UAS-DTU Rover Autonomy**](https://github.com/3AMengineer/UAS-DTU-Rover-Autonomy) *(team)* | Autonomy stack of our DARPA Triage Challenge rover: 3D LiDAR → LiDAR-inertial odometry → Nav2 → velocity control → MAVROS → ArduRover |
| [**ardurover-adaptive-velocity-controller**](https://github.com/3AMengineer/ardurover-adaptive-velocity-controller) | ROS 2 layer between Nav2 and ArduPilot that adapts its gains online, with separate left/right turn gains, field-tested on the DARPA rover |
| [**vins-fusion-d455-allan-variance**](https://github.com/3AMengineer/vins-fusion-d455-allan-variance) | VINS-Fusion on a RealSense D455 with Allan-variance IMU noise models and online camera–IMU time-offset logging |
| [**apf-navigation**](https://github.com/3AMengineer/apf-navigation) | Artificial Potential Field obstacle avoidance in ROS 2 on 2D LiDAR and a depth camera (depth → virtual laser scan) |
| [**four_wheel_diff_drive**](https://github.com/3AMengineer/four_wheel_diff_drive) | 4-wheel differential-drive rover built from scratch in ROS 2/Gazebo: URDF, 360° LiDAR, D455-style depth camera |
| [**UAV-Navigation-on-SITL**](https://github.com/3AMengineer/UAV-Navigation-on-SITL) | Autonomous UAV missions in ArduPilot SITL with DroneKit: takeoff, waypoints, square/circle trajectories, PID position control |
| [**Pravah**](https://github.com/3AMengineer/Pravah) *(team, SIH 2026)* | SUMO digital twin of Delhi's ITO corridor with adaptive signal control; I built the simulation layer |

## Tools

**Robotics:** ROS 2 · Nav2 · ArduPilot · MAVROS · DroneKit · SLAM Toolbox · robot_localization · Gazebo · SUMO / TraCI
**Sensors:** Blickfeld 3D LiDAR · 2D LiDAR · Intel RealSense D455 · RTK-GPS · XBee
**Languages and tools:** Python · C++ · Linux · Git · OpenCV · NumPy

## Contact

[LinkedIn](https://www.linkedin.com/in/shourya-sharma-6a365a341/) · [shouryabanner@gmail.com](mailto:shouryabanner@gmail.com) · open to robotics and autonomy internships (navigation, localization, perception, control)
