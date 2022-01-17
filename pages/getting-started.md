---
title: Getting Started
permalink: /installation/getting-started/
---

# Getting Started 

## On Local PC 

To getting strated, we have prepared some sample maps alongside  different robots. For Example we run house_map model with three p3at robots as following items:

* Open a terminal console with Ctrl+Alt+T and launch the     house_map world map

  ```
  git clone https://github.com/RoboCupRescueVirtualRobotLeague/RoboCup2021RVRL_Demo 

  cd ~/RoboCup2021RVRL_Demo/

  colcon build

  source install/setup.bash

  ros2 launch rvrl_gazebo house_map.launch.py
  ```

  As shown in this example, three robots are spawned in the environment, each of them can be controlled manually with the following procedure. You can also check the <strong>rvrl_gazebo/launch </strong> directory to find another or map examples. 

<center>
<img src="https://robocup-rsvrl.github.io/assets/img/getting-started-4.jpeg" width="70%"/>
</center>

* In order to see the images of the robots' cameras, open a new tab using Crtl+T, then use the following command

  ```
  $  source install/setup.bash
  $ ros2 run rviz2 rviz2
  ```

* You should be able to see this screen now

<center>
<img src="https://robocup-rsvrl.github.io/assets/img/getting-started-5.jpeg" width="70%"/>
</center>

* You have to make sure that the terminal window stays on top of the gazebo window while you're operating.

* In order to move the robots,open terminal 1 with Ctrl+Alt+T to drive the robot1 with following command:
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard cmd_vel:=robot1/cmd_vel
```

* You will see this screen on your terminal

<center>
<img src="https://robocup-rsvrl.github.io/assets/img/getting-started-6.jpeg" width="50%"/>
</center>
<br/>

* Open terminal 2 with Ctrl+Alt+T to drive the robot2 with following command: 
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard cmd_vel:=robot2/cmd_vel
```
* Open terminal 3 with Ctrl+Alt+T to drive the robot3 with following command:
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard cmd_vel:=robot3/cmd_vel
```
* Open terminal 4 with Ctrl+Alt+T to get the robots image camera with following command:
```
ros2 run rqt_image_view rqt_image_view
```

<hr style="border:1px solid gray"/> 

## On The ConstructSim

* In case you are working on ConstructSim, click on *Web shell* on the lower left part of the page.

<center>
<img src="https://robocup-rsvrl.github.io/assets/img/getting-started-1.jpeg" width="50%"/>
</center>

* You will see the terminal open, act like local pc mode
<center>
<img src="https://robocup-rsvrl.github.io/assets/img/getting-started-2.jpeg" width="50%"/>
</center>


* You can also visit the graphical intereface by followin picture

<center>
<img src="https://robocup-rsvrl.github.io/assets/img/getting-started-3.jpeg" width="70%"/>
</center>

