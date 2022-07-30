# install-arm-packeg-in-ROS1-


## Table of contents
* [Introduction](#Introduction)
* [Algorithm](#Algorithm)

## Introduction
  
 Robot arm packages install in  ROS  that can be used to plan and execute motion trajectories for a robot arm in simulation and real-life. 
 made by Smart method company , These packages were tested under ROS noetic , The robot arm uses Moveit plugin to apply kinematics by the KDL solver. These packages can be tested in the gazebo simulation tool 
 ## Algorithm
 
 Step 1 : Open the terminal , create the directories :
          
            mkdir -p ~/catkin_ws/src
            
            cd ~/catkin_ws/

            catkin_make

            cd ~/catkin_ws/src
            


 
 Step 2 : Put in folder catkin_make the packages of arm from smart method 
         
             git clone https://github.com/smart-methods/arduino_robot_arm.git 
             
             cd ~/catkin_ws

 Step 3 : Install dependency of a arm package
   
   
         rosdep install --from-paths src --ignore-src -r -y

         sudo apt-get install ros-kinetic-moveit

         sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui

         sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher

         sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control

         sudo nano ~/.bashrc

 Step 4 : at the end of the (bashrc) file add the follwing line
             
             (source /home/wafaa/catkin_ws/devel/setup.bash)
              then 
             ctrl + o
              then 
             ctrl + x
            
             source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch

 
 
  ![1](https://user-images.githubusercontent.com/64277741/179366616-adc5c727-3d54-40de-b673-f5240ac48b65.PNG)
  
