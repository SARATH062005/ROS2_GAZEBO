# ROS2_GAZEBO
ros2 launch articubot_one launch_sim.launch.py 
(or)

ros2 launch articubot_one launch_sim.launch.py world:=./dev_ws/src/worlds/obstacles.world



ros2 run teleop_twist_keyboard teleop_twist_keyboard 

rviz2


# commands to view camera view

ros2 run rqt_image_view rqt_image_view 


# to launch slam

ros2 launch slam_toolbox online_async_launch.py params_file:=./bot_ws/src/config/mapper_params_online_async.yaml use_sim_time:=true

# to install nav2

sudo apt install ros-humble-navigation2 ros-humble-nav2-bringup ros-humble-turtlebot3*

ros2 run nav2_map_server map_server --ros-args -p yaml_filename:=my_map_save.yaml -p use_sim_time:=true

ros2 run nav2_util lifecycle_bringup map_server

ros2 run nav2_util lifecycle_bringup amcl


