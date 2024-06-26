# CFD Analysis of Martian Helicopter Ingenuity and Thrust Calculation

## Overview:
This repository contains the code and documentation for a Computational Fluid Dynamics (CFD) analysis of **NASA's Martian Helicopter Ingenuity** to determine the thrust produced by its coaxial rotors in the **Martian CO2 atmosphere.**

## Motivation:
NASA's Mars Helicopter Ingenuity represents a groundbreaking advancement in planetary exploration. Understanding the aerodynamic performance of its rotors and the thrust generated in the unique Martian atmosphere was crucial for optimizing its operations and mission success. I am personally interested in Space tech and Rockets. Analysing the Ingenuity was not only exciting but also educational and informative.

## Methodology:
- **Software Used:** ANSYS Workbench 2023 R1/ANSYS Fluent
- **Turbulence Model:** Hybrid RANS/Spalart-Allmaras (SA) with Detached Eddy Simulation (DES).
- **3D Modeling & Mesh Generation:** I created a 3d model in SolidWorks and then imported the geometry in ANSYS. I employed a Face sizing of 10mm at the propeller surfaces and 50mm at the fluid domain. 
- **Simulation Setup:**
  - The fluid used was Carbon Dioxide (CO2) as in Martian Atmosphere with following properties:
    - Density: 0.017kg/m^3
    - Viscousity: 1.46e-5 N/kg
    - Temp: 293K
    - Gravity = 3.71 m/s^2 ( Earth Gravity = 9.81m/s^2)
  - The blade walls were set to adiabatic, no-slip boundary condition.
  - Transient solution calculated over 250 timesteps of 0.001s each.
- **Post-processing:** Analysis of results using ANSYS CFD-Post Software.
  - The velocity and pressure contours were made along verticle plane.
  - Plots of Velocity and Pressure along the verticle axis (Y-Axis) were made.
  - Hand calculation was made using the MATLAB ( F_th = 0.5*rho*A*(v_e^2 - v_o^2) )
 
## Directory Structure:
- Solidworks_Files: contains 3D models and the files used in the simulation setup.
- Results_OnePropeller: contains the graphs and contours for the simulation done using only one propeller with a RPM of 2200
- Results_TwoPropeller: contains the graphs and contours for the simulation done using both of the coaxial propellers with RPM of 2200 but in opposite directions.

## Results:
The CFD analysis provided valuable insights into the aerodynamic performance of the Martian Helicopter Ingenuity and the thrust generated by its rotors. Detailed results, including velocity profiles, pressure distributions, and thrust calculations, are available in the documentation.

## Acknowledgments:
I would like to express my gratitude to the following sources of information, which were instrumental in the success of this project:
- YouTube Tutorial: How to Calculate Thrust Force on a Rotating Propeller Blade Using CFD ANSYS (Fluent) 19.1
  - https://youtu.be/sHTSyWL_gds?si=MGWV6f7nw-kRVa4y
  - https://youtu.be/9xnubvVsvyM?si=VOaKCnh-Bvoci8KF
- Research Papers:
  - Koning, W.J., Allan, B.G., Romander, E.A. and Johnson, W., 2023, September. **Comparing 3D and 2D CFD for Mars Helicopter Ingenuity Rotor Performance Prediction**. In 49th European Rotorcraft Forum 2023.
  - Schulman, P., Berndt, S., Roman, C., and Tan, X. (October 13, 2023). **"Computational Fluid Dynamics Modeling Analysis of a Martian Rotorcraft With Individual Blade Control."** ASME. Letters Dyn. Sys. Control. April 2023; 3(2): 021005. https://doi.org/10.1115/1.4063482

## I hope you enjoyed my work. I would really appreciate any suggestions and improvements. Thanks.
