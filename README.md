**2D SIMPLE Solver for Incompressible Poiseuille Flow**

**Overview**

Finite volume implementation of a two-dimensional steady incompressible Navier–Stokes solver using the SIMPLE (Semi-Implicit Method for Pressure-Linked Equations) algorithm on a staggered grid. The solver is validated against the analytical solution of laminar Poiseuille flow between parallel plates and includes a structured parametric stability study.

**Project Context**

This project was completed as part of the Computational Fluid Dynamics course at Mines Saint-Étienne (October 2025).

The solver and report were developed collaboratively with Emin Khalifayev. The implementation, debugging, validation, and parametric analysis were carried out as part of the academic assignment. This repository is published for educational and portfolio purposes.

**Mathematical Formulation**

The steady incompressible Navier–Stokes equations are discretized using the finite volume method on a staggered grid:

Pressure stored at cell centers

Velocity components stored at cell faces

Diffusion terms use central differencing.
Convection terms use first-order upwind discretization.

Pressure–velocity coupling is handled using the SIMPLE algorithm with under-relaxation factors:

Velocity relaxation: αu ≈ 0.8

Pressure relaxation: αp ≈ 0.2

The solver iterates until residuals fall below 1e-6 and global continuity is satisfied.

**Validation**

The numerical solution is validated against analytical Poiseuille flow:

Parabolic velocity profile

Linear pressure gradient

At convergence:

Velocity RMSE < 3%

Pressure RMSE < 2%

Residual decay over ~1000 iterations

Representative results are included in the results/ folder.

**Parametric Study**

A structured parametric study was conducted to analyze solver stability and accuracy under variations of:

Grid size

Grid aspect ratio

Velocity relaxation factor

Pressure relaxation factor

Reynolds number

**Key observations:**

Near-square grids improved numerical isotropy

Excessive pressure relaxation triggered instability

Higher Reynolds numbers increased nonlinear convergence difficulty

Grid refinement reduced discretization error

**Repository Structure**

main.py
solve_x_momentum.py
solve_y_momentum.py
solve_P.py
correct_u_x.py
correct_u_y.py

postprocessing/
results/
report/

**How to Run**

Install dependencies:

pip install -r requirements.txt

Run the solver:

python main.py

Future Extensions

Implementation of SIMPLEC

Higher-order advection schemes

Extension to transient or multiphase flows
