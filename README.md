# Fermi-Pasta-Ulam (FPU) Simulation

This script simulates the dynamics of a Fermi-Pasta-Ulam (FPU) lattice system, which models a chain of particles connected by nonlinear springs. The system demonstrates interesting energy-sharing dynamics between modes, often studied in nonlinear physics.

## Features

- **Quadratic Nonlinearity (Alpha Model):** Simulates the dynamics using a quadratic interaction term.
- **Cubic Nonlinearity (Alpha-Beta Model):** Includes both quadratic and cubic interaction terms for more complex dynamics.
- **Initial Velocity Cases:** Two different initial velocity configurations:
  1. Zero initial velocity
  2. Non-zero sinusoidal initial velocity

## Requirements

The code requires the following Python libraries:
- `numpy`
- `matplotlib`
- `scipy`

You can install these dependencies using pip:
- `pip install numpy matplotlib scipy`

# Usage
1. **Define the System**: 
   - Number of points in the lattice (`n`)
   - Nonlinearity parameters (`alpha` and `beta`)
   - Initial displacements and velocities

2. **Run Simulations**:
   - The script uses `solve_ivp` from `scipy.integrate` to solve the differential equations over a specified time range (`t_span`) and evaluation points (`t_eval`).

3. **Plot Results**:
   - Four scenarios are simulated and visualized:
     1. Quadratic nonlinearity with zero initial velocity
     2. Quadratic nonlinearity with non-zero initial velocity
     3. Cubic nonlinearity with zero initial velocity
     4. Cubic nonlinearity with non-zero initial velocity

4. **Save Plots**:
   - The results are saved as PNG files with the following names:
     - `fpu_quadratic_velocity_0.png`
     - `fpu_quadratic_velocity_non_zero.png`
     - `fpu_cubic_velocity_0.png`
     - `fpu_cubic_velocity_non_zero.png`

# Code Structure 
- **`fpu_system` Function**:
  Defines the equations of motion for the FPU system. It calculates accelerations based on the current displacements, velocities, and the nonlinearity parameters (`alpha` and `beta`).

- **Simulations**:
  Each simulation involves defining initial conditions and solving the system using `solve_ivp`. Results are plotted and saved for each scenario.

- **Visualization**:
  Displacement of each particle in the lattice is plotted as a function of time.

