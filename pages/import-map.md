---
title: Import New Map
permalink: /installation/import-map/
---

# Import New Map to Virtual Robot Project

In order to add a new map to to the project, you need to open the *house_map.launch.py* file in the *rvrl_gazebo/launch* directory.


<center>
<img src="https://robocup-rsvrl.github.io/assets/img/import-map-1.jpg" width="90%"/>
</center>
<br/>

<br/>

<br/>

On line 28, change the 'house_world.model' to any map you want from the available maps in the directory *rvrl_gazebo/worlds*. 

After that, open the terminal and write the following:

 ```
     colcon build
 ```
