## Autonomous Drones in Gazemo ROS
---

## Purpose of Each Component

### `src/uav_description/`
Contains the **robot description** used for simulation.

- **URDF (`quadrotor.urdf`)**
  - Defines the UAV’s kinematic structure
  - Specifies inertial, visual, and collision properties
  - Serves as the source model for simulation

- **Meshes**
  - Optional geometric assets for visualization
  - Not required for minimal experiments

---

### `build/`, `install/`, `log/`
Auto-generated directories created by the build system.

- **`build/`** — Intermediate compilation outputs  
- **`install/`** — Runtime-ready artifacts  
- **`log/`** — Build and execution logs  

These directories **should not be edited manually**.

---

## Design Philosophy

- Minimal description → easier debugging
- Separation of **model definition** from **control / estimation**
- Visualization-first, realism later
- Avoid premature integration of planners or estimators

---

## Intended Use

This workspace is intended for:
- Testing UAV model definitions
- Understanding simulator ↔ model interaction
- Incrementally adding control, sensing, or estimation modules

It is **not** intended to be a complete flight stack.

---

## Extending the Workspace

Typical next additions:
- Sensor models (IMU, camera)
- Simple motion or control nodes
- Planning or estimation modules (added deliberately, not upfront)

---

## Summary

`uav_ws` is a **lightweight UAV modeling workspace** designed to support:
- Rapid iteration
- Clear structure
- Educational and exploratory experiments

Complexity is added **only when needed**.
