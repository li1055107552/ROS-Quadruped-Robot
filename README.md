# ROS-Quadruped-Robot
ROS开发学习，四足机器人

  
启动Rviz:  
>
>    `$ roslaunch zwmvp_description rviz.launch`
>
启动Gazebo:  
>
>    `$ roslaunch zwmvp_gazebo gazebo.launch`
>
启动键盘控制器:  
>
>    `$ rosrun zwmvp_control teleop_control.py`
>
启动摄像头视角窗口:  
>
>    `$ rqt_image_view`    
>(记得在摄像头界面窗口的左上角进行绑定，才能正常显示)

---
### 额外
将xacro转成urdf格式:
>
>    `$ cd yourpath/zwmvp_description/urdf`    
>    `$ rosrun xacro xacro.py zwmvp.xacro > zwmvp.urdf`    
>

检查urdf文件格式:
>
>    `$ cd yourpath/zwmvp_description/urdf`    
>    `$ check_urdf zwmvp.urdf`    
>

生成节点图:
>
>    `$ urdf_to_graphiz zwmvp.urdf`    
>

---  
  
### ATTENTION
> `zwmvp_gazebo/worlds/zwmvp_world.world`  下有两个绝对路径，需要手动更改！    
> 此处务必使用绝对路径，不然launch只能找到world文件，却找不到world中的dae文件！！！(从launch文件出发)    
