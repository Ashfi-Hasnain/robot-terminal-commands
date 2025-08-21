# robot-terminal-commands
Open in edit mode to properly read

## gazebo
colcon build
source install/setup.bash
ros2 launch my_bot launch_sim.launch.py

## robot
colcon build
source install/setup.bash
ros2 launch my_bot rsp.launch.py use_sim_time:=false
ros2 run controller_manager spawner.py diff_cont
ros2 run controller_manager spawner.py joint_broad
ros2 launch my_bot rplidar.py
