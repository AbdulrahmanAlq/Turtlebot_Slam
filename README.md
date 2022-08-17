# Turtlebot_Slam

First step is installing Turtlebot3 on your ubunto. And to install it just follow the guide on their website https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/ and make sure to choose the right ubunto version.

Then after installing you can run SLAM by typing this command 

$ export TURTLEBOT3_MODEL=waffle_pi
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping.

If you install all the required packages and dependeceis it should run fine.


To save the map you Launch the map_saver node in the map_server package to create map files. by typing the following command:

$ rosrun map_server map_saver -f ~/map

The -f option specifies a folder location and a file name where files to be saved.
With the above command, map.pgm and map.yaml will be saved in the home folder ~/(/home/${username}).


The map uses two-dimensional Occupancy Grid Map (OGM), which is commonly used in ROS. The saved map will look like the figure below, where white area is collision free area while black area is occupied and inaccessible area, and gray area represents the unknown area. This map is used for the Navigation.
