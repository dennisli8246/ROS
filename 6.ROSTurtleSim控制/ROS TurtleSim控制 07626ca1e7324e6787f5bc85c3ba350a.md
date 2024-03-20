# ROS:TurtleSim控制

需要先安裝ROS

注意要先安裝package

A. 控制套件

```python
sudo apt install ros-noetic-rqt-robot-steering
```

B. mvsim軟件套件

```python
sudo apt install ros-noetic-mvsim
```

1. 開啟一個terminal輸入roscore
    
    ```python
    roscore
    ```
    
    ![Untitled](ROS%20TurtleSim%E6%8E%A7%E5%88%B6%2007626ca1e7324e6787f5bc85c3ba350a/Untitled.png)
    
2. 開啟一個terminal,開啟控制器
    
    ```python
    rosrun rqt_robot_steering rqt_robot_steering
    ```
    
3. 開啟TurtleSim
    
    ```python
    rosrun turtlesim turtlesim_node
    ```
    
4. 修改節點
    1. 顯示目前topic
    
    ```python
    rostopic list 
    ```
    
    ![Untitled](ROS%20TurtleSim%E6%8E%A7%E5%88%B6%2007626ca1e7324e6787f5bc85c3ba350a/Untitled%201.png)
    
    1. 在節點上修改為turtle1/cmd_vel
    
    ![Untitled](ROS%20TurtleSim%E6%8E%A7%E5%88%B6%2007626ca1e7324e6787f5bc85c3ba350a/Untitled%202.png)
    

顯示結果無下

![Untitled](ROS%20TurtleSim%E6%8E%A7%E5%88%B6%2007626ca1e7324e6787f5bc85c3ba350a/Untitled%203.png)

Reference:

[https://blog.51cto.com/u_12897/8028029](https://blog.51cto.com/u_12897/8028029)