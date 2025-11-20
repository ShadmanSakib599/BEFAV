# BEFAV – Motor Mount Assembly

This repository contains the CAD models and technical drawing for a motor mount assembly designed for **BEFAV (Bio-Inspired Environmentally Friendly Aerial Vehicle)** – a conceptual VTOL/eVTOL-style aerial vehicle. The mount is intended to securely support an electric propulsion unit while minimizing weight and maintaining sufficient stiffness and strength.

The repository showcases the full design progression from an initial solid/truss concept to a **topology-optimized** motor mount suitable for integration into a lightweight aerial platform.

---

## Project Overview

The motor mount is a structural interface between the airframe and an electric motor/propeller (or ducted fan). It is designed to:

- Carry **thrust, torque, and bending loads** from the propulsion unit.
- Interface with an airframe rib, pylon, or nacelle structure via a defined bolt pattern.
- Minimize structural mass while maintaining stiffness and limiting stress.
- Be manufacturable using common processes such as CNC machining or additive manufacturing.

This component is part of a broader BEFAV concept that explores efficient, electrically powered aerial vehicles with bio-inspired and environmentally conscious design principles.

---

## Repository Contents

The repository currently includes the following files:

| File name                                      | Type | Description |
| ---------------------------------------------- | ---- | ----------- |
| `Complete motor mount assembly.step`           | STEP | CAD-neutral model of the complete motor mount assembly for integration into other CAD projects or simulation environments. |
| `Complete motor mount assembly.stl`            | STL  | Triangulated version of the complete mount, suitable for 3D printing / rapid prototyping or visualization. |
| `Motor mount assembly (Truss).step`           | STEP | Intermediate **truss-style** motor mount concept emphasizing efficient load paths and reduced material usage. |
| `Motor mount assembly (Truss).stl`            | STL  | Export of the truss-style motor mount for printing or mesh-based analysis. |
| `Topology optimized motor mount.step`          | STEP | Final **topology-optimized** motor mount geometry, refined for weight reduction while preserving stiffness and strength. |
| `Topology optimized motor mount.stl`           | STL  | Mesh version of the topology-optimized design for additive manufacturing or rendering workflows. |
| `FDRW25B_SSR_Rev_B .pdf`                       | PDF  | Technical drawing of the motor mount, including dimensions, tolerances, and key fabrication / inspection details. |

All 3D models are provided in **STEP** (CAD-neutral) and **STL** (mesh) formats so they can be used across most modern CAD and CAE tools.

---

## Design Goals & Constraints

The motor mount was designed with the following typical constraints in mind:

- **Loads**
  - Axial thrust from the electric motor and propeller.
  - Motor torque reaction transmitted through the mounting pattern.
  - Bending loads due to offset mass and aerodynamic forces.
- **Performance Targets**
  - Minimize mass while maintaining adequate stiffness to limit deflection.
  - Keep maximum stress within a safe factor of the material yield strength.
- **Interfaces**
  - Bolt pattern and mounting surfaces compatible with a small electric motor and airframe structure.
  - Clearances for motor body, wiring, and fasteners.
- **Manufacturability**
  - Geometry suitable for machining, or optionally for metal / high-strength polymer additive manufacturing.
  - Inclusion of fillets and transitions to reduce stress concentrations where appropriate.

> **Note:** Exact material choice and detailed load cases can be tuned by the user depending on the specific motor, airframe, and mission profile.

---

## Design & Optimization Workflow

The design of the motor mount followed a typical **concept → refinement → optimization** workflow:

1. **Baseline Concept**
   - Begin with a conservative solid / plate-based geometry that satisfies all load paths.
   - Ensure clean mounting interfaces and sufficient stiffness.

2. **Truss-Style Refinement**
   - Convert the baseline into a truss-inspired mount where material is primarily located along critical load paths.
   - Reduce non-load-bearing material while maintaining robust connection regions around bolt holes and mounting surfaces.

3. **Topology-Optimized Design**
   - Further refine the geometry using a topology-style approach:
     - Identify low-stress regions and remove unnecessary material.
     - Preserve boundary conditions and interface regions.
   - Result: a lighter, more efficient structural component that maintains stiffness and strength targets.

4. **Validation (Intended)**
   - Import the optimized geometry into FEA software.
   - Apply representative thrust, torque, and boundary conditions to verify:
     - Maximum von Mises stress levels.
     - Deflections at the motor face.
     - Overall safety factor relative to chosen material.

---

## How to Use These Models

### Viewing and Editing the CAD

You can open the **STEP** files in most CAD tools, for example:

- SolidWorks  
- Autodesk Inventor / Fusion 360  
- CATIA  
- Siemens NX  
- FreeCAD (open-source)

The **STL** files are ideal for:

- 3D printing prototypes.
- Importing into mesh-based simulation tools.
- Visualization in tools like Blender or MeshLab.

### Integrating into Your Own Design

1. **Import the chosen STEP file** into your CAD assembly.
2. **Align the mount** with your airframe rib or pylon using the bolt pattern defined in the drawing.
3. **Adapt mounting interfaces** (hole sizes, spacing, fillet radii, etc.) to match:
   - Your motor’s mounting pattern.
   - Your airframe’s structural members and fastener hardware.
4. Optionally, **re-run FEA** on the adapted geometry for your own load cases and materials.

---

## Possible Applications

While this mount was developed as part of the BEFAV VTOL/eVTOL concept, the geometry can be adapted for:

- RC aircraft and UAV motor mounts.
- Multirotor or tilt-rotor prototypes.
- Test rigs for propulsion units.
- Educational projects involving structural optimization and lightweight design.

---


