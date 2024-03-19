# Install ROS -noetic in Ubuntu

**note : in virtual box**

## 1. 更新software & update

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled.png)

## 2. 設置 sources.list

```tsx
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%201.png)

## 3. 設置 key

```tsx
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%202.png)

## 4. 安裝 ROS Noetic

```tsx
sudo apt update
```

```tsx
sudo apt install ros-noetic-desktop-full
```

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%203.png)

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%204.png)

## **Environment setup**

```tsx
source /opt/ros/noetic/setup.bash
```

## 5. **Dependencies for building packages**初始 rosdep

```tsx
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

## 初始 rosdep

- rosdep 為ROS的工具套件,方便之後的加入各種套件

```tsx
source /opt/ros/noetic/setup.bash
```

```tsx
sudo rosdep init
rosdep update
```

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%205.png)

- 呼叫指令的時候會產生20-default.list檔案

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%206.png)

## 6. source bash

- 安裝完成可以用source建立ROS環境

```tsx
source /opt/ros/noetic/setup.bash
```

## ~~7. 取得rosinsatll~~

- ROS命令工具基於Python

```tsx
sudo apt-get install python-rosinstall
```

- 可能會造成錯報

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%207.png)

- 修改為python3

```tsx
sudo apt-get install python3-rosinstall
```

<aside>
💡 參考：[https://blog.csdn.net/m0_61780496/article/details/129912943](https://blog.csdn.net/m0_61780496/article/details/129912943)

</aside>

## 8. 測試

```tsx
roscore
```

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%208.png)

- 另外開啟terminal執行turtlesim測試

```tsx
source /opt/ros/noetic/setup.bash
```

```python
rosrun turlesim turlesim_node
```

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%209.png)

## 9. 缺失資料包狀況

![Untitled](Install%20ROS%20-noetic%20in%20Ubuntu%20abe98fa810884951a05f0b28045c21d5/Untitled%2010.png)

```tsx
sudo apt-get install ros-noetic-desktop-full --fix-missing
```

<aside>
💡 [https://stackoverflow.com/questions/67256536/ros-melodic-python-versions-conflict-unmet-dependencies](https://stackoverflow.com/questions/67256536/ros-melodic-python-versions-conflict-unmet-dependencies)

</aside>

Reference: 

[noetic/Installation/Ubuntu - ROS Wiki](https://wiki.ros.org/noetic/Installation/Ubuntu)