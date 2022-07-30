# install-arm-package-in-ROS1-


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
          
          sudo apt-get install ros-noetic-moveit
          
          sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
          
          sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
          
          sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
          
          sudo nano ~/.bashrc

 Step 4 : at the end of the (bashrc) file add the follwing line
             
             (source /home/wafaa/catkin_ws/devel/setup.bash)
              then 
             ctrl + o
              then 
             ctrl + x
             
 Step 5 : To update bashrc folder 
 
             source ~/.bashrc

 Step 6 : To open RViz and joint state publisher      
            
            roslaunch robot_arm_pkg check_motors.launch

   ![Screenshot 2022-07-30 100234](https://user-images.githubusercontent.com/64277741/181879125-08793dbc-5a8b-41e9-9d80-8ef0ec7b8a65.png)

  
  Figure (1): the initial point  
  
 ![Screenshot 2022-07-30 100407](https://user-images.githubusercontent.com/64277741/181879171-87316067-1089-4877-9f5f-138676d312d9.png)

  
  Figure (2): after changing value in joint state publisher 

