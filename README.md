# turtlebot4_uts
Source code untuk UTS RE702
Task dari project ini adalah bergerak ke titik A, mengaktifkan bel sekali (mendapatkan barang/benda kerja), lalu berpindah ke titik B dan mengaktifkan bel dua kali (barang/benda kerja sampai tujuan).

---
# Langkah-langkah dalam menjalankan source code
### Buat Folder Workspace
```
mkdir -p turtlebot4_ws/src
cd turtlebot4_ws/src
```
### Clone Repo 
```
git clone https://github.com/RICCY11/turtlebot4_uts.git
```
### Build 
```
colcon build
```
### Koneksikan PC ke Turtlebot4
```
ssh ubuntu@192.168.185.3 
```
### Jalankan localization launch & navigation launch (pada turtlebot4)
```
source install/setup.bash
ros2 launch turtlebot4_uts localization.launch.py
```
```
source install/setup.bash
ros2 launch turtlebot4_uts uts_navigation.launch.py
```
### Jalankan Rviz (pada PC)
```
ros2 launch turtlebot4_viz view_robot.launch.py
```
### Jalankan node program pick & place nya yang berisi koordinat awal dan tujuan (pada turtlebot4)
```
source install/setup.bash
ros2 run turtlebot4_uts koordinat_node
```
