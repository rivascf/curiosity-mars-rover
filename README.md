# A Gazebo-ROS simulation of Curiosity Mars Rover v1.0 

- *From:* [The Construct](https://www.theconstructsim.com/)
  - **Source Code:** [TheConstructCore](https://bitbucket.org/theconstructcore/)/[Public Simulations](https://bitbucket.org/theconstructcore/workspace/projects/PS)/[curiosity_mars_rover](https://bitbucket.org/theconstructcore/curiosity_mars_rover/src/master/)

## Launch the simulation

A terminal will open. Type in the terminal the following command:

```console
roslaunch curiosity_mars_rover_description main_simple.launch
```

### Speed control

* Full control over the suspension and wheels. You can change the suspension configuration and move the robot through a simple **/cmd_vel** topic publish. 

To launch the keyboard control of the robot, open another terminal and then execute the following command to move the robot through the standard **teleop_twist_keyboard** keys:

```console
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
```

### Arm and mast control

* Services for **deploying the ARM and MAST**. These basic services allow you to deploy the **mast** and **arm** confortably. This is specially important for the **mast**
because it's here where a basic camera has been placed where the **CHEMCAM** would be. Here are the command you can send to open and close the arm or the mast:

```console
$ rosservice call /curiosity_mars_rover/arm_service "model_name: 'open'"

$ rosservice call /curiosity_mars_rover/arm_service "model_name: 'close'"

$ rosservice call /curiosity_mars_rover/mast_service "model_name: 'open'"

$ rosservice call /curiosity_mars_rover/mast_service "model_name: 'close'"
```
