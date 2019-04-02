This repo creates an interface from dwm1001 dev-board into ROS enviroment

## Steps to get this package working with dwm1001
In order to get the dwm1001 dev-board working with ROS, we first need to create an RTLS network between the tag and anchors.
This package at the moment supports 4 anchors and 1 tag, however I'm looking to make it more dynamic. Feel free to open any issue.

### Follow the steps in this pdf (https://www.decawave.com/wp-content/uploads/2018/08/mdek1001_quick_start_guide.pdf) in order to create an RTLS network, you will need an android phone or tablet.

Once you have created RTLS network make sure that it works on the app from the grid view. 


### Download this package
Clone this package into your workspace in src folder ~/catkin_ws/src/

### Plug the usb of the tag into your laptop

### Check the name of the usb(in my case is /dev/ttyACM0)
You can change the name of the usb in the launch file or in in the code dwm1001_main.py

### Now launch the package with rosrun or roslaunch
It will ask you to enter your password since it requires permission to enter the usb, Once you launch the package it will get all the informations about the network (tag and anchors) into topics. For example you will see /dwm1001/anchor0 /dwwm1001/anchor1, /dwwm1001/anchor2, /dwwm1001/anchor3 and /dwm1001/tag

### Now you should see your tag and anchor info
