# Setting Workplace in ROS

1. 建制一個空的資料夾<檔案名稱>,在此資料夾下建立一個/src的資料夾

```tsx
mkdir -p catkin_ws/src
```

![Untitled](Setting%20Workplace%20in%20ROS%201c52f3d5c75b4bf0ab6196732eebda84/Untitled.png)

1. 在src資料下執行catkin_init_workspace命令,記得要先建立環境source /opt/ros/noetic/setup.bash

```tsx
cd ~/catkin_ws/src 
catkin_init_workspace
```

![Untitled](Setting%20Workplace%20in%20ROS%201c52f3d5c75b4bf0ab6196732eebda84/Untitled%201.png)

1. 使用catkin_make指令在空間內建制套件在～/catkin_ws/資料夾下

```tsx
cd ~/catkin_ws/
catkin_make
```

![Untitled](Setting%20Workplace%20in%20ROS%201c52f3d5c75b4bf0ab6196732eebda84/Untitled%202.png)

![Untitled](Setting%20Workplace%20in%20ROS%201c52f3d5c75b4bf0ab6196732eebda84/Untitled%203.png)

會自動建立工作空間所需要的資料夾

![Untitled](Setting%20Workplace%20in%20ROS%201c52f3d5c75b4bf0ab6196732eebda84/Untitled%204.png)

1. 為了要使用工作空間中的套件，把.bashrc放在工作空間中。之後要建立工作環境中的套件可以用source指令來建立

```tsx
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

1. 測試.bashrc路徑是否正確，如果正確會顯示路徑

![Untitled](Setting%20Workplace%20in%20ROS%201c52f3d5c75b4bf0ab6196732eebda84/Untitled%205.png)

Reference:

<aside>
💡 [https://subscription.packtpub.com/book/iot-and-hardware/9781838649326/1/ch01lvl1sec11/setting-up-the-ros-workspace](https://subscription.packtpub.com/book/iot-and-hardware/9781838649326/1/ch01lvl1sec11/setting-up-the-ros-workspace)

</aside>