# Robot Localization Module: RLuTF (Robot Localization using Turning Function)

This repository contains an implementation of the **RLuTF algorithm** for 2D robot localization. The method leverages polygonal representations of real-time LiDAR sensor data and known environment maps to accurately estimate the robot's position.

---

## Key Features

- **Polygon-based localization:** Generates polygons from sensor data and simulated robot poses on a map.
- **Turning function representation:** Uses turning functions to describe polygon shapes and compares them via minimized L2 norms over circular shifts.
- **Iterative position refinement:** Searches around the best candidate location, narrowing the search radius logarithmically until achieving target accuracy.
- **Core components included:** Motion modeling, polygon construction, turning function computation, polygon comparison, and candidate selection.

---

## Repository Structure

- `main.py`  
  Entry point for running optimization and localization routines.

  ```bash
  # Run meta-goal programming optimization
  python main.py --mode goal

  # Run NSGA-II heuristic optimization
  python main.py --mode nsga2
