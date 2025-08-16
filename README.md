# 2.4 GHz Microstrip Patch Antenna Design | HFSS

This repository demonstrates the design, simulation, and analysis of a **2.4 GHz rectangular microstrip patch antenna** using Ansys HFSS. It includes steps for setting up the geometry, defining ports, simulating S-parameters, and generating radiation patterns.


## Key Steps

### 1. Geometry Setup
1. Create a **rectangular patch** on the top layer.
2. Create a **ground plane** underneath the substrate.
3. Draw a **thin substrate box** and perform boolean operations:
   - **Unite** the patch and substrate as needed.
   - **Subtract** the patch from the substrate for accurate mesh handling.

### 2. Port Setup
- Use **lumped ports** for feeding the antenna.
- Assign port faces on the edges of the patch.
- Define **reference ground** on the ground plane.

### 3. Radiation Setup
- Create a **radiation box** surrounding the antenna for far-field calculations.
- Assign **Boundaries**:
  - `Radiation` boundary (e.g., Rad1)
  - Perfect E (e.g., perfE1) on metallic parts.
- Ensure the box is large enough (typically >λ/4 away from the antenna).

### 4. Simulation
- Set up **S-parameters** simulation.
- Use **frequency sweep** around 2.4 GHz.
- Mesh refinement around edges and ports to ensure convergence.

### 5. Result Analysis
- Extract **S11** (return loss) and **impedance matching** data.
- Generate **E-field plots**.
- Create **far-field 3D radiation patterns** and gain vs. frequency plots.

## Folder Structure

- `HFSS-Files/` – Contains HFSS project files.
- `Documentation/` – Detailed step-by-step instructions.
- `Plots/` – Simulation results.
- `Scripts/` – Optional HFSS Python automation scripts.

## References
- [HFSS User Guide](https://www.ansys.com/products/electronics/ansys-hfss)
- Balanis, C.A. "Antenna Theory: Analysis and Design", 4th Edition
