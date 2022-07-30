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

 Step 3 : 
 
         
 
  ### 1- install virtualbox 
  
  1- download virtualbox (VirtualBox 6.1.34 )platform packages [here](https://www.virtualbox.org/wiki/Downloads) 
  
  2- choose windows hosts 
  
  3- open file and setup the program 
  
  4- you don't need to change any options just next>next>next>finish
  
  5- open the Oracle VM VirtualBox 
  
  ![1](https://user-images.githubusercontent.com/64277741/179366616-adc5c727-3d54-40de-b673-f5240ac48b65.PNG)
  
