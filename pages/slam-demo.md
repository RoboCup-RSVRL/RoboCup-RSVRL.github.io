---
title: SLAM
permalink: /demos/slam-demo/
---

# SLAM Demo


In order to start the mapping node for any robot, type in the following line using your robot's name instead of the default "robot1"

   ```
     $ ros2 launch rvrl_cartographer cartographer.launch.py robot_name:=robot1
     $ ros2 run rviz2 rviz2
   ```
You should see the map of the first robot in rviz now

![image](https://user-images.githubusercontent.com/27806598/147872971-9f6545a1-ba79-4e4c-b180-97391797aa04.png)

