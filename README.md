# 🐢 ROS2 Turtlesim on Ubuntu 22.04 (Humble)

This project shows you how to run the **Turtlesim** simulator using **ROS2 Humble** on **Ubuntu 22.04**, inside a VirtualBox virtual machine. It's a simple way to learn core ROS2 concepts like **nodes**, **topics**, and **services**.

## 📌 What You'll Learn

- Install ROS2 Humble on Ubuntu  
- Run the turtlesim simulator  
- Move the turtle using velocity commands  
- Teleport the turtle using services  
- View topics and turtle pose  
- Use keyboard control  

## 🧰 Tools Used

- ROS2 Humble  
- Ubuntu 22.04 (VirtualBox)  
- Terminal (CLI)  
- Turtlesim package  

## ▶️ Basic Commands

```bash
# Start the turtlesim GUI
ros2 run turtlesim turtlesim_node

# Control the turtle using your keyboard
ros2 run turtlesim turtle_teleop_key

# List all topics
ros2 topic list

# View the turtle's current pose
ros2 topic echo /turtle1/pose

# Move the turtle (linear and angular velocity)
ros2 topic pub /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0}, angular: {z: 1.5}}"

# Teleport the turtle to a specific position
ros2 service call /turtle1/teleport_absolute turtlesim/srv/TeleportAbsolute "{x: 4.0, y: 2.0, theta: 1.0}"

# Clear the simulator screen
ros2 service call /clear std_srvs/srv/Empty

## 🧠 Important Notes

Always **source ROS2** before running any commands in a new terminal:

```bash
source /opt/ros/humble/setup.bash
```

You must do this **every time** you open a new terminal window.

---

## ⚙️ Installation Steps

1. Install **VirtualBox** and create a virtual machine with **Ubuntu 22.04**.

2. Inside the Ubuntu VM, update your system and install required tools:

```bash
sudo apt update
sudo apt install curl gnupg2 lsb-release
```

3. Install ROS2 Humble by following the official guide:  
👉 [ROS2 Humble Installation Guide](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html)

4. Once installed, test the setup by running Turtlesim commands:

```bash
ros2 run turtlesim turtlesim_node
```

5. Make sure to source ROS2 every time before running ROS2 commands:

```bash
source /opt/ros/humble/setup.bash
```

### ✍️ Edited by: Rahaf Althobaiti (رهف الثبيتي)
