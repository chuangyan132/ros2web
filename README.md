# Solution to visualize URDF in web
## Description
- This project is a solution to visualize URDF
(from ROS2) in web(demo:urdf_demo_URrobot.html).
- It is based on ros3djs and roslibjs. The former is one client from roslibjs, which is a client library for ROS. The latter is a library for web development.
- main changes:
    1. add TF2Client.js in roslibjs to support action mode.
    2. updates in cobotta_cell_description
    3. fork tf2_web_republisher to support action mode.
## Requirements
- ROS2_site
    - ROS2
    - rosbridge_suite
    - tf2_web_republisher (with action mode)
    - rosbridge_suite (branch:dependabot/github_actions/actions/setup-python-5.1.0)
- 3rd
    - ros3d.js
    - roslib.js (with TF2Client.js)

## demo
- urdf_demo_URrobot.html

## How to use
```bash
ros2 launch rosbridge_server rosbridge_websocket_launch.xml 
ros2 run tf2_web_republisher tf2_web_republisher # new terminal
ros2 launch ur_description view_ur.launch.py ur_type:=ur5e # new terminal
# open urdf_demo_URrobot.html in browser
```