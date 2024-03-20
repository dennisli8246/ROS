# Setting environment with ROS&ROS2

Reference:

[https://docs.ros.org/en/foxy/Installation/Alternatives/Ubuntu-Development-Setup.html](https://docs.ros.org/en/foxy/Installation/Alternatives/Ubuntu-Development-Setup.html)

[https://github.com/PacktPublishing/ROs-Robotics-Projects-SecondEdition/tree/master/](https://github.com/PacktPublishing/ROs-Robotics-Projects-SecondEdition/tree/master/)

使用alias加入腳本

1. 使用指令呼叫bash腳本
    
    ```tsx
    sudo gedit ~/.bashrc
    ```
    
    co
    
2. 加入以下兩行
    
    ```tsx
    alias initros1='source /opt/ros/noetic/setup.bash'
    ```
    
    ```tsx
    alias initros2='source ~/ros2_foxy/install/local_setup.bash'
    ```
    
3. 將下免兩行註解,使其不能使用
    
    ```tsx
    source /opt/ros/noetic/setup.bash
    source ~/catkin_ws/devel/setup.bash
    ```
    

![Untitled](Setting%20environment%20with%20ROS&ROS2%207c13495cebd2400488c3b9c86f01115b/Untitled.png)

1. 修改完bash檔案後在一次source bash腳本就能夠使用alias指令
    
    ```tsx
    source ~/.bashrc
    ```
    
2. 這樣就可以使用initros1或是initros2來執行ros1或是ros2的環境
3. 測試運行
    1. 各開兩個視窗執行
    
    ```tsx
    initros2
    ```
    
    一個視窗執行talker
    
    ```tsx
    ros2 run demo_nodes_cpp talker
    ```
    
    另外一個執行listener
    
    ```tsx
    ros2 run demo_nodes_py listener
    ```
    
    ![Untitled](Setting%20environment%20with%20ROS&ROS2%207c13495cebd2400488c3b9c86f01115b/Untitled%201.png)
    
    可以使用ros2 topic list觀察目前有執行的topic
    
    ```tsx
    ros2 topic list
    ```
    
    ![Untitled](Setting%20environment%20with%20ROS&ROS2%207c13495cebd2400488c3b9c86f01115b/Untitled%202.png)