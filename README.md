# COMP0124 Coursework: Efficient Social Attention for Autonomous Decision-Making in Varing Traffic Scenarios
This repository contains the source code for coursework 3. The objective of this coursework is to perform pick and place tasks in Gazebo, using MoveIt!
to move the robot and PCL to detect object positions and colours
## Authors
He Liang&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Jianheng Liu&nbsp;&nbsp;&nbsp;&nbsp;Yunfan Shi
## Code Directory Structure
```
├── cw1_team_7
│   ├── include
│   │   ├── cw3_class.h -> heading file
│   ├── launch
│   │   ├── run_solution.launch -> launch file
│   ├── src
│   │   ├── cw3_class.cpp -> methods for three tasks
│   │   ├── cw3_node.cpp -> main function
│   ├── srv
│   │   ├── example.srv -> define request and return messages
│   ├── CMakeLists.txt
│   ├── package.xml
```
## Build and Run
**Build**
```shell
cd comp0129_s24_labs
catkin build
source devel/setup.bash
```
**Run**  
In the same Terminal
```shell
roslaunch cw3_team_7 run_solution.launch
```
Open another Terminal
```shell
cd comp0129_s24_labs
source devel/setup.bash
rosservice call /task <task_id>
```
Note: If you try to run task 3 after running task 1 and 2 consecutively, the code may get stuck somewhere with an issue
```shell
[pcl::OrganizedNeighbor::estimateProjectionMatrix] Input dataset is not organized!
```
If that happens, simply press 'Ctrl C' and relaunch it
```shell
roslaunch cw3_team_7 run_solution.launch
```
Then open another Terminal
```shell
cd comp0129_s24_labs
source devel/setup.bash
rosservice call /task 3
```
Then the issue should be fixed.

<p align="center">
  <table>
    <tr>
      <td><img src="task1.png" width="300" /><br>Task 1</td>
      <td><img src="task2.png" width="300" /><br>Task 2</td>
      <td><img src="task3.png" width="300" /><br>Task 3</td>
    </tr>
  </table>
</p>




## Task Contribution
**Task 1**: **8** hours -- Liu (30%), Wei (40%), Liang (30%)  
**Task 2**: **14** hours -- Liu (30%), Wei (40%), Liang (30%)  
**Task 3**: **38** hours -- Liu (40%), Wei (30%), Liang (30%)

## License
Code: [MIT License](LICENSE)
