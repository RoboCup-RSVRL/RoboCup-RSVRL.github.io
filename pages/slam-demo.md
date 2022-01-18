---
title: SLAM
permalink: /demos/slam-demo/
---

# SLAM Demo

In the following video, you will see how to load the map of a robot on this cloud simulation:
<br/>
<center>
<iframe width="560" height="315" src="https://www.youtube.com/embed/_v5EA5bBa3w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</center>
<br/>

In order to start the mapping node for any robot, type in the following line using your robot's name instead of the default "robot1"

   ```
     ros2 launch rvrl_cartographer cartographer.launch.py robot_name:=robot1
     ros2 run rviz2 rviz2
   ```
You should see the map of the first robot in rviz now

![image](https://user-images.githubusercontent.com/27806598/147872971-9f6545a1-ba79-4e4c-b180-97391797aa04.png)

