# Robotic Arm PID Computed-Torque Control

## Description

This project simulates a PID-controlled robotic arm. The control is based on calculating torque values for both arms based on the desired trajectories. This control strategy aims to make the robotic arm reach the target positions and velocities.

The project is based on the initial code taken from the [instructor's GitHub repository](https://abukhalaf.github.io/UZB438E-Spring-2025/), with the following improvements:

1. **PID Control Parameter Adjustments**: The PID control parameters have been optimized for better stability.
2. **Dynamic System Model Improvements**: Some parts of the robotic arm's dynamic model have been optimized.
3. **Code Structure Enhancements**: Some functions and variable names have been changed for better readability and modularity.

## Usage

### Requirements
- MATLAB or a similar environment.
- The `ode45` function in MATLAB will be used to solve differential equations.

### Getting Started
1. Open the `main.m` file in MATLAB and run it.
2. The simulation results, which show the PID-controlled robotic arm's response to the desired trajectories, will be visualized in three plots.
3. The `RoboticArm.m` function contains the dynamic model of the robotic arm and the control algorithm.

### Running the Simulation

When the simulation is run, the following three main graphs will be displayed:
1. **Position Angles vs. Time**: Shows how the angles of the two arms change over time.
2. **Position Errors**: Displays the difference between the actual position and the desired position.
3. **Torque Input Vectors**: Shows the torque values calculated by the PID control algorithm over time.

## Functions

### `RoboticArm(t, x)`

This function calculates the dynamics of the robotic arm. Given the time (`t`) and the state vector (`x`), it computes the velocities, accelerations, and control inputs (torques) for the robotic arm.

### `desiredTrajectory(t)`

This function calculates the desired trajectories for both arms of the robotic arm. The desired position, velocity, and acceleration are determined using sine and cosine functions.

## Control Parameters

- **Kp**: Proportional (P) gain (100)
- **Kv**: Derivative (D) gain (20)
- **Ki**: Integral (I) gain (500)

These parameters are used in the PID control algorithm.


## References

- The initial code was taken from the [instructor's GitHub repository](https://abukhalaf.github.io/UZB438E-Spring-2025/).
- F. Lewis, D. Dawson, and C. Abdallah, *Robot Manipulator Control: Theory and Practice* (Automation and Control Engineering), CRC Press, 2003, ISBN: 9780203026953. [Online]. Available: [https://doi.org/10.1201/9780203026953](https://doi.org/10.1201/9780203026953).

## License

You are free to use this project, but please make sure to cite the original sources.
