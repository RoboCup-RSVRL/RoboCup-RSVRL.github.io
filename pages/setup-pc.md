---
title: Setup PC
permalink: /installation/setup-pc/
---


# Requirements

Before starting to work with virtual robots, you need these requirments on your system:

  <img src="https://rvrl-wiki.github.io/assets/img/ubuntu.png" width="4%"/> [*Ubuntu 20.04 LTS “Focal Fossa”* ](https://ubuntu.com/download/desktop) 

  <img src="https://rvrl-wiki.github.io/assets/img/ros.png" width="4%"/>  [*ROS 2* Robot Operating System (ROS)](https://docs.ros.org/en/foxyInstallation/Ubuntu-Development-Setup.html)   

  <img src="https://rvrl-wiki.github.io/assets/img/gazebo.png" width="4%"/> [*Gazebo 11* ](http://gazebosim.org/tutorials?tut=install_ubuntu&cat=install)

<hr style="border:1px solid gray"/> 

# Installation

<strong> Important: </strong>

Please note that in case you are using cloud based simulation services like [The Construct Sim](https://www.theconstructsim.com/) or [AWS RoboMaker](https://aws.amazon.com/de/robomaker/), You can skip this part and proceed to [the Getting Started Page](https://rvrl-wiki.github.io/reqs/bringup/).

1. <strong> Download and Install Ubuntu on your PC </strong>
   * Dowload the [Ubuntu 20.04 LTS Desktop](https://releases.ubuntu.com/20.04/) image.
   * Install the Ubuntu 20.04 on your PC by the following instruction from [ this link ](https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview).

2. <strong> Install ROS 2 foxy version</strong> 
    
    Open a terminal console with Ctrl+Alt+T and enter the following commands one at a time. 
    ```
    sudo apt update && sudo apt install curl gnupg2 lsb-release
    sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
    sudo sed -i -e 's/ubuntu .* main/ubuntu focal main/g' /etc/apt/sources.list.d/ros2.list
    ```
    If the above installation fails, please refer to 
    [the official ROS2 Foxy installation guide.](https://index.ros.org/doc/ros2/Installation/Foxy/Linux-Install-Debians/)

3. <strong> Install Dependent ROS 2 Packages </strong>
   * Open the terminal with Ctrl+Alt+T from Remote PC.
   * Install Base Packages
    ```
    sudo apt update
    sudo apt install ros-foxy-desktop
    sudo apt install ros-foxy-ros-base
    ```
   * Install Gazebo11
    ```
    sudo apt-get install ros-foxy-gazebo-*
    ```
   * Install Cartographer
    ```
    sudo apt install ros-foxy-cartographer
    sudo apt install ros-foxy-cartographer-ros
    ```
   * Install Navigation 2
    ```
    sudo apt install ros-foxy-navigation2
    sudo apt install ros-foxy-nav2-bringup
    ```
   * Add sourcing to your shell startup script by sourcing the setup.bash file 
    ```
    echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc
    ```