# Active-Grasp-my-working-setup-
<br>
This is my working version of the caktin workspace that allows me to run active grasp:
https://github.com/ethz-asl/active_grasp

### Notes on what helped me to run Active Grasp:
1. Apart from vgn, active_grasp, and robot_helpers, do not git clone the other required packages. Instead, use: sudo apt install ros-noetic-\<package name\>
2. The requirements.txt file do not include all the required dependencies to get active_grasp running, like numpy for example. There are many dependencies you will have to install manually before active_grasp can run, so pay attention to the error messages. Also note, you will need the appropriate version of these dependencies.
3. When running starting the ros master and trying to run the simulation experiment using the run.py file in the scripts folder, it seems that it attempts to detect vgn's path file in the models folder which would be in the assets folder. But the path file is actually in the models folder in the data folder. I copied the models folder of the data folder into the assets folder to get it to detect vgn.
4. You can find a folder called vgn in the source folder of vgn in the catkin workspace. In this vgn folder, you can find a file called utils.py. I ran into an error where PointCloud2() could not be detected on line 96. I removed the import line regarding PointCloud outside of the try except block. This seemed to resolve the issue.
5. This is not an exhaustive list of all the issues you can run into, but some notes on what I can recall based on the issues I ran into.
