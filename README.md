# TurtleBot3 Simulation – ROS 2 Jazzy + Gazebo (Ubuntu 24.04)

## 📌 Setup do sistema
- Instalei **Ubuntu 24.04 (Noble Numbat)** em dual boot com Windows.
- Resolvi problemas de driver da GPU Intel Meteor Lake-P:
  - Inicialmente só funcionava com `nomodeset`.
  - Após upgrade para Ubuntu 24.04 com kernel mais novo → HDMI e aceleração gráfica funcionando normalmente.

## ⚙️ ROS 2 + Gazebo
- Instalei **ROS 2 Jazzy Jalisco**.
- Instalei o **Gazebo (gz-ionic)**.
- Adicionei integração **ros_gz** (substitui os antigos pacotes `gazebo_ros_pkgs`).
- Instalei os pacotes **TurtleBot3**:
  ```bash
  sudo apt install ros-jazzy-turtlebot3* ros-jazzy-ros-gz*
  ```

#  Simulação TurtleBot3 no ROS 2 Jazzy + Gazebo

## 🚀 Rodando a simulação

```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
ros2 launch turtlebot3_gazebo empty_world.launch.py
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -p stamped:=true
```
