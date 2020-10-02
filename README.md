# Hector_slam
Hector slam on Raspberry Pi using ROS and YDlidar X4


1. Connect the motors to the arduino board. And then run roscore
2. Run the Arduino code and then connect the Arduino to ros by

rosrun rosserial\_python serial\_node.py /dev/ttyACM0

1. For tutorial [http://wiki.ros.org/rosserial\_arduino/Tutorials/Arduino%20IDE%20Setup](http://wiki.ros.org/rosserial_arduino/Tutorials/Arduino%20IDE%20Setup)
2. The Arduino then connects to ROS using serial bridge and subscribes to cmd\_vel node.
3. Place the folder in catkin\_ws/src and them compile it using catkin\_make .
4. Connect the lidar using the adapter and the run the lidar.launch to publish the lidar data or lidar\_view.launch to visualize the data on Rviz.
![alt text](https://haeyeonlab.files.wordpress.com/2019/11/image-4.png "Lidar view")
5. Then run the all\_nodes.launch to start hector slam node., then rviz will start on rviz. ![alt text](https://static.wixstatic.com/media/db4869_6e4623f0111144b5a037770aa73de63e~mv2.png/v1/fit/w_408,h_322,al_c,q_80/file.png "Hector slam")
6. Then run rosrun teleop\_twist\_keyboard teleop\_twist\_keyboard.py
