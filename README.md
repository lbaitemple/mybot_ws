# mybot_ws
URDF model for Gazebo integrated with ROS

This repository has several branches. Please checkout the appropriate branch for your needs. <br>
1) <strong>base</strong> - create simple URDF model <br>
2) <strong>base_sensors</strong> - add sensors to robot <br>
3) <strong>navigation</strong> - enable autonomous navigation (now updated for [ROS Melodic Morenia](http://wiki.ros.org/melodic))

For more information on running the code:  <br>
http://moorerobots.com/blog/post/6

```
roslaunch mybot_gazebo mybot_world.launch
roslaunch mybot_navigation gmapping_demo.launch
roslaunch mybot_description mybot_rviz_gmapping.launch
roslaunch mybot_navigation mybot_teleop.launch
rosrun map_server map_saver -f ~/environment/mybot_ws/src/mybot_navigation/maps/test_map
```
Afte that, you can recompile the code
```
colcon build
roslaunch mybot_gazebo mybot_world.launch
roslaunch mybot_navigation amcl_demo.launch
roslaunch mybot_description mybot_rviz_amcl.launch
```
