# 🟪 Isaac Sim Onboarding & Robot Simulation Pipeline

## Objective
Learn the basics of NVIDIA Isaac Sim and build a working simulation pipeline for our robot platform.

---

## 1. Isaac Sim Installation & Basics

### Tasks
- Install Isaac Sim (latest version).
- Learn UI: stage tree, viewport, render settings.
- Create a simple scene with primitives.
- Run and modify sample scenes.

### Deliverables
- Screenshot of your custom Isaac Sim scene.

---

## 2. Importing a Robot into Isaac Sim

### Tasks
- Import URDF/USD model of any robot.
- Add articulation controller.
- Add sensors: LIDAR, depth camera, IMU.
- Configure ROS2 Bridge for Jazzy.

### Deliverables
- Robot imported and publishing ROS2 topics.

---

## 3. ROS2 Bridge Setup

### Tasks
- Connect Isaac Sim ↔ ROS2 Jazzy using ros2_bridge.
- Verify `/cmd_vel`, `/scan`, `/joint_states`, `/tf`.
- Control robot with teleop in ROS2.

### Deliverables
- Video showing teleop controlling robot inside Isaac Sim.

---

## 4. Creating a Simple Environment

### Tasks
- Build an obstacle course or maze.
- Add friction, physics, materials.
- Save as `.usd`.

### Deliverables
- Custom Isaac Sim environment.

---

## 5. Autonomous Navigation (Isaac + Nav2)

### Tasks
- Load robot + environment.
- Run ROS2 Nav2.
- Send navigation goal from RViz.
- Observe path planning inside Isaac Sim.

### Deliverables
- Short recording of autonomous navigation.

---

## Final Output (GitHub Repo Structure)

```
isaac_sim_project/
  models/
  worlds/
  launch/
  ros2_bridge_setup.md
  nav2_integration.md
  demo_video.mp4
```
