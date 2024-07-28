# Controlling-Robot-Arm
This repository for the second task in AI track of week 3. which is about controlling the robot arm using Rviz and MoveIt tools.
--> Task requrements.

1- Controlling the robot arm by joint_state_publisher

2- Controlling the robot arm by Moveit and kinematics

3- Explain the steps and results in GitHub.

-----------------------------------------
Setup the simulation tools
---
Create new directory called catkin_ws

    mkdir -p ~/catkin_ws/src

go to the catkin_ws using cd command( change directory)

    cd ~/catkin_ws/

Create a workspace using catkin_make

    catkin_make

    echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc

    source ~/.bashrc

go to the src directory inside catkin_ws

    cd ~/catkin_ws/src

Add "arduino_robot_arm" to src directory

    git clone https://github.com/smart-methods/arduino_robot_arm.git 

go back to catkin_ws directory

    cd ~/catkin_ws

Install dependencies

    rosdep install --from-paths src --ignore-src -r -y

    sudo apt-get install ros-noetic-moveit

    sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

    sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

    sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

Compile the package

    catkin_make

---------------------------
Controlling the robot arm by joint_state_publisher
---
    roslaunch robot_arm_pkg check_motors.launch  

Rviz GUI:

![Screenshot from 2024-07-28 18-54-45](https://github.com/user-attachments/assets/b2f499ae-e121-4888-9ea4-bbe8c9c51b9f)

joint_state_publisher control panel:

![Screenshot from 2024-07-28 19-03-23](https://github.com/user-attachments/assets/d9420143-b357-4974-86c3-f8ce3166c689)

Controlling the robot arm using joint_state_publisher:

![Screenshot from 2024-07-28 19-04-04](https://github.com/user-attachments/assets/1038ef26-cf5d-49a0-9785-d15630e60afb)

---------------------------
Controlling the robot arm by Moveit and kinematics
---
