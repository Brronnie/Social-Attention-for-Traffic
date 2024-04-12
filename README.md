# COMP0124 Coursework: Efficient Social Attention for Autonomous Decision-Making in Varing Traffic Scenarios
This repository contains the source code for coursework paper: Efficient Social Attention for Autonomous Decision-Making in Varing Traffic Scenarios. Thr experiment environment is forked from: [HighwayEnv](https://github.com/Farama-Foundation/HighwayEnv) and [rl-agents](https://github.com/eleurent/rl-agents).  We modify the code to diploy our proposed method.
## Authors
He Liang, &nbsp;&nbsp;Jianheng Liu, &nbsp;&nbsp;Yunfan Shi
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



## License
Code: [MIT License](LICENSE)
