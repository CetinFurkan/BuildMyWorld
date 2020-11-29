

# RoboND-myrobot
The **myrobot** lab part of RoboND Gazebo Basics lesson. The purpose of this lab is to learn how to build a two-wheeled robot model with the Model Editor tool in Gazebo. Include this model in an empty Gazebo World. And, finally write a plugin to interact with this world.  

### Directory Structure
```
    .BuildMyWorld                      # Project main folder 
    ├── model                          # Model files used in the world
    │   ├── myrobot
    │   │   ├── model.config
    │   │   ├── model.sdf
    │   ├── tinyHouse
    │   │   ├── model.config
    │   │   ├── model.sdf
    ├── script                         # Gazebo plugin C++ script      
    │   ├── welcome_message.cpp
    ├── world                          # Gazebo main world
    │   ├── myFirstRosWorld.world
    ├── CMakeLists.txt                 # Link libraries 
    └── myFirstRosWorld.png	       # Output Image                           
```

### Steps to launch the simulation

#### Step 1 | Update and upgrade the Workspace image
```sh
$ sudo apt-get update && sudo apt-get upgrade -y
```
#### Step 2 | Clone the lab folder in /home/workspace/
```sh
$ cd /home/workspace/
$ git clone https://github.com/udacity/RoboND-myrobot myrobot
```

#### Step 3 | Compile the code
```sh
$ cd /home/workspace/myrobot/
$ mkdir build
$ cd build/
$ cmake ../
$ make
```

#### Step 4 | Add the library path to the Gazebo plugin path  
```sh
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/myrobot/build
```

#### Step 5 | Run the Gazebo World file  
```sh
$ cd /home/workspace/myrobot/world/
$ gazebo myworld
```

### Output
The hello world message and the two-wheeled robot inside a Gazebo World should both launch as follow: 
![alt text](myFirstRosWorld.png)
