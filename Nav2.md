# 🧭 ROS2 Jazzy – Nav2 Onboarding Assignment

## Objective
Set up a full Nav2 navigation pipeline on our robot using ROS2 Jazzy.  
By completing this, you will learn the fundamentals of ROS2, robot description, simulation, mapping/localization, and Nav2 bring-up.

---

## 1. ROS2 Foundation Tasks

### Goal  
Become comfortable with core ROS2 concepts needed for Nav2.

### Tasks
- Install ROS2 **Jazzy**.
- Create a workspace (`ros2_ws`) and build a simple package with:
  - one publisher node (Python)
  - one subscriber node
- Run nodes using `ros2 run`.
- Inspect topics (`ros2 topic echo`) and parameters (`ros2 param`).

### Deliverables
- A minimal publisher–subscriber demo package running successfully.

---

## 2. Robot Description Setup

### Goal  
Prepare the robot model that Nav2 will use.

### Tasks
- Create or adapt a URDF for our robot containing:
  - `base_link`
  - wheel links
  - inertial & collision tags
  - LIDAR or depth sensor
- Add a `robot_state_publisher` launch file.
- Verify the TF tree in RViz.

### Deliverables
- URDF + RViz visualization working correctly.

---

## 3. Simulation Integration

### Goal  
Get the robot running inside a simulation.

### Tasks
- Spawn the robot in Gazebo (or our chosen simulator).
- Add required plugins:
  - wheel controller (diff-drive or mecanum)
  - LIDAR sensor plugin
- Verify:
  - `/scan` topic exists
  - `/cmd_vel` moves the robot
  - Odometry and TF tree are correct
- Test teleoperation using `teleop_twist_keyboard`.

### Deliverables
- Simulation setup + working robot model with valid sensor output.

---

## 4. Nav2 Core Concepts Overview

### Goal  
Understand the components involved in the Nav2 stack.

### Topics to Learn
- Costmaps (global and local)
- AMCL
- Planners and Controllers (DWB, RPP, etc.)
- Behavior Trees
- Map server & lifecycle nodes
- SLAM vs. localization

### Deliverables
- A one-page Markdown summary explaining each Nav2 component.

---

## 5. Nav2 Bring-Up on Our Robot

### Goal  
Create the full navigation stack for our robot in ROS2 Jazzy.

### Tasks
- Create a `nav2_params.yaml` file tuned for our robot’s dimensions and sensors.
- Create `bringup_nav2.launch.py` that launches:
  - Map server
  - AMCL (or SLAM if used)
  - Planner
  - Controller
  - Behavior Tree
  - Global & Local costmaps
- Load an existing map or generate one using SLAM.
- Test navigation by sending goals in RViz.

### Deliverables
- Working autonomous navigation in simulation:
  - localization
  - path planning
  - static obstacle avoidance
  - goal reaching

---

## 6. Final Submission Package

### Required GitHub Repository Structure
```
my_robot_nav2/
  my_robot_description/
    urdf/
  my_robot_simulation/
    launch/
  my_robot_bringup/
    launch/
      bringup_nav2.launch.py
    config/
      nav2_params.yaml
    maps/
      map.yaml
      map.pgm
  docs/
    nav2_components_overview.md
    instructions.md
```

### Required Items
- URDF model
- Simulation launch files
- Nav2 bring-up launch file
- Nav2 parameter file
- Map files (YAML + PGM)
- Documentation
- A short screen recording (5–10 min) showing:
  - robot spawning  
  - map loading / SLAM  
  - AMCL working  
  - reaching multiple navigation goals
