# CFD Study: SIMPLE Algorithm and 2D Poiseuille Flow

## **Overview**

This repository documents my study and hands-on work with fundamental Computational Fluid Dynamics (CFD) concepts, focusing on pressure–velocity coupling and the numerical solution of incompressible laminar flow using the SIMPLE (Semi-Implicit Method for Pressure-Linked Equations) algorithm.

The project was completed collaboratively by **Emin Khalifayev** and **Abel Inalegwu Onuh** as part of the Computational Fluid Dynamics course at **Mines Saint-Étienne (October 2025)**. Using a structured solver framework provided during the course, we worked on completing, debugging, validating, and analyzing the numerical solution for **2D incompressible Poiseuille flow**.

This repository is shared for **educational and portfolio purposes** to demonstrate understanding of CFD fundamentals, solver structure, and numerical convergence behavior.

---

## **Learning Objectives**

Through this project, I developed practical understanding of:

- Finite Volume Method (FVM) discretization of the Navier–Stokes equations  
- Pressure–velocity coupling using the SIMPLE algorithm  
- Use of staggered grids for numerical stability  
- Role of under-relaxation factors in ensuring convergence  
- Interpretation of residual convergence behavior  
- Validation of numerical results against analytical solutions  

---

## **Physical Problem: Poiseuille Flow**

The case studied is **steady incompressible laminar flow between two parallel plates**.

The analytical solution provides:

- Parabolic velocity distribution across the channel  
- Linear pressure decrease along the flow direction  

This benchmark allows direct validation of numerical accuracy.

---

## **Numerical Approach**

The solver framework uses:

- Finite volume discretization  
- Staggered grid arrangement  
- Central differencing for diffusion terms  
- First-order upwind discretization for convection terms  
- SIMPLE pressure-correction algorithm  

Solver convergence is achieved when **residuals fall below tolerance** and **mass conservation is satisfied**.

---

## **Validation and Results**

The numerical solution successfully reproduces expected physical behavior:

- Velocity profile converges to the analytical parabolic shape  
- Pressure varies linearly along the flow direction  
- Residuals decrease steadily until convergence  

Representative plots and solver outputs are available in the **`results/`** folder.

---

## **Parametric Study**

We investigated the influence of key numerical parameters, including:

- Grid resolution  
- Grid aspect ratio  
- Pressure relaxation factor  
- Velocity relaxation factor  
- Reynolds number  

This analysis helped build intuition about **solver stability, numerical diffusion, and convergence characteristics**.

---

## **Repository Purpose**

This repository documents my practical exposure to **CFD solver structure, numerical stability, and validation methodology**. It serves as a foundation for future **independent CFD implementations** and more advanced studies in **multiphase flow simulation**.

---

## **Authors**

**Emin Khalifayev**  
**Abel Inalegwu Onuh**  

*Mines Saint-Étienne, 2025*
