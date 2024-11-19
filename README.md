# Dynamic System Simulation

This repository contains a Python project that simulates and analyzes the evolution of a dynamic system over time using numerical integration. The system is modeled using a set of ordinary differential equations (ODEs) and is solved using `scipy`'s `solve_ivp` function. The project includes visualization of the state variables to illustrate how the system responds under different initial conditions and input forces.

## Table of Contents
- [Introduction](#introduction)
- [System Description](#system-description)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Example Results](#example-results)
- [License](#license)

## Introduction
This project simulates the behavior of a dynamic system modeled by differential equations. The simulation provides insights into how the system evolves over time under different scenarios. The simulation results are visualized through plots of state variables, helping to understand the system dynamics.

## System Description
The system is governed by a set of linear differential equations of the form:

\[ \dot{z} = A z + B u \]

where:
- `A` is a system matrix that describes the internal dynamics.
- `B` is an input matrix that describes how external inputs influence the system.
- `z` is the state vector, consisting of four variables: `z1 (m)`, `z2 (m/s)`, `z3 (rad)`, and `z4 (rad/s)`.
- `u` is the input force vector.

### Matrices and Constants
- **Constants**: `p0`, `w0`, and their derived values are used to construct the `A` and `B` matrices.
- **Simulation Time**: The simulations are conducted over specified time intervals, converting days and hours into seconds.

## Dependencies
- `numpy`: For numerical computations.
- `scipy`: For numerical integration (solving ODEs).
- `matplotlib`: For plotting the simulation results.

## Usage
1. Run the main script to simulate and plot the system's behavior:
   ```bash
   python main.py
   ```

2. Modify initial conditions or input forces in the `main.py` file to test different scenarios.

### Parameters
- `z0`: Initial state vector.
- `u`: Input force vector.
- `time_in_sec`: Simulation duration in seconds.

### Customization
Feel free to adjust the system matrices `A` and `B`, as well as the constants, to simulate different dynamic systems.

## Example Results
The project generates plots showing the time evolution of the state variables under different conditions:

1. **Scenario 1**: Simulation with initial state `z0 = [100, 0, 0, 0]` and no external forces.
2. **Scenario 2**: Simulation with initial state `z0 = [0, 0, 0, 0]` and an external force `u = [0, -1]`.

These plots help visualize how the system's position, velocity, and angular components change over time.

