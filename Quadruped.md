# 🟩 Quadruped Robot (Robot Dog) Control Assignment

## Objective
Build a quadruped robot simulation, implement joint control, leg IK, and basic gait generation.

---

## 1. Quadruped Model Setup

### Tasks
- Import an open-source quadruped robot (Go1/Laikago/Spot-like).
- Ensure joints are configured:
  - Hip abduction/adduction
  - Hip flexion/extension
  - Knee flexion/extension
- Add sensors: IMU, depth camera, LIDAR.

### Deliverables
- Quadruped model visible with correct articulation.

---

## 2. Basic Joint Control

### Tasks
- Write ROS2 node to read joint states and command joint targets.
- Test poses: stand, crouch, sit.

### Deliverables
- Robot transitions between poses.

---

## 3. Inverse Kinematics (Single Leg)

### Tasks
- Implement 3-DOF IK:
  - Input: desired foot x,y,z
  - Output: hip, thigh, knee angles
- Move one leg along a trajectory.

### Deliverables
- Working IK demo for one leg.

---

## 4. Gait Generation

### Tasks
- Implement crawl gait (one leg at a time).
- Implement trot gait (diagonal pairs).
- Use IK to generate foot trajectories.

### Deliverables
- Short recording of quadruped walking.

---

## 5. Basic Balancing

### Tasks
- Use IMU orientation.
- Keep body level using PID.
- Adjust leg offsets to maintain balance.

### Deliverables
- Robot stabilizes itself while walking.

---

## Final Output (GitHub Repo Structure)

```
quadruped_project/
  models/
  controllers/
    ik_leg.py
    gait_controller.py
  launch/
  videos/
  docs/
    explanation.md
```
