# Commands


## The robot
### Launching the robot:
```bash
ros2 launch ur_robot_driver ur_control.launch.py ur_type:=ur10e robot_ip:=192.168.56.101
```

### Launching the Moveit!
```bash
ros2 launch ur_moveit_config ur_moveit.launch.py  ur_type:=ur10e  
```

### Launching the robot on Simulation
```bash
ros2 launch ur_robot_driver ur_control.launch.py ur_type:=ur10e robot_ip:=192.168.56.101 use_fake_hardware:=true fake_execution:=true
```
### Launching the moveit on Simulation
```bash
ros2 launch ur_moveit_config ur_moveit.launch.py ur_type:=ur10e use_fake_hardware:=true fake_execution:=true
```
##  Network connection Isuue solution
```bash
sudo nmcli con mod "Wired connection 2" ipv4.addresses 192.168.56.66/24
sudo nmcli con mod "Wired connection 2" ipv4.method manual
sudo nmcli con up "Wired connection 2"
```

## Runing Realsense camera
```bash
ros2 launch realsense2_camera rs_launch.py
ros2 launch realsense2_camera rs_launch.py depth_module.depth_profile:=1280x720x30 pointcloud.enable:=true
```