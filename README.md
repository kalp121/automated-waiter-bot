# Automated Waiter Bot Planning

######===Setup & Running Instructions===

Prerequisites: Setup your catkin workspace using following link:
http://wiki.ros.org/catkin/Tutorials/create_a_workspace


1. Copy group_15.zip to ~/catkin_ws/src folder
2. Unzip group_15.zip
3. Change permissions for all scripts in group_15 folder using the below command
	--> chmod u+x ~/catkin_ws/src/group_15/scripts/*.py
4. Excute the env_setup.sh script using the below command
	--> chmod u+x ~/catkin_ws/src/group_15/env_setup.sh && ~/catkin_ws/src/group_15/env_setup.sh
5. Run roscore using the below command
	--> roscore
6. Open a new terminal and run the server file located at ~/catkin_ws/src/group_15/scripts/server.py using the below command
	--> rosrun group_15 server.py
7. Open a new terminal and launch the maze using the below command
	--> roslaunch group_15 maze.launch
8. Open a new terminal and run move_tbot3.py using the below command
	--> rosrun group_15 move_tbot3.py
9. Open a new terminal and generate the pddl solution using the below command
	--> rosrun group_15 refinement.py -step 1
10. Refine the pddl solution and execute the actions using the below command
	--> rosrun group_15 refinement.py -step 2