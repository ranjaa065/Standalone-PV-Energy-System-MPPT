:::writing{variant="document" id="63821"}
# Stand-Alone PV Energy System Using MATLAB/Simulink

## About the Project

This project focuses on studying a stand-alone Solar Photovoltaic (PV) energy system using MATLAB/Simulink. The main aim is to understand the electrical characteristics of a PV module and explore Maximum Power Point Tracking (MPPT) to obtain maximum power from the solar panel.

## Objectives

1. To find the voltage, current, and power of a PV module.
2. To generate the I-V and P-V characteristics of the PV module.
3. To implement the Maximum Power Point Tracking (MPPT) algorithm.

## Tools Used

- MATLAB
- Simulink
- Simscape Electrical
- MATLAB Function Block

## Working Principle

The PV module converts solar energy into DC electrical energy. In this model, solar irradiance is set to **1000 W/m²**.

The output voltage (Vpv) and current (Ipv) are measured, and the output power is calculated using:

**P = V × I**

A variable resistor is used to change the load and observe the changes in PV voltage, current, and power.

An XY Graph is used to study the PV characteristics, while a MATLAB Function block is included to implement an MPPT algorithm based on the Perturb and Observe (P&O) approach.

## Simulation Results

The simulation graph shows the typical shape of a PV P-V characteristic.

From the uploaded graph, the approximate maximum power is **162 W**, at a voltage of around **24 V**. These values are visual estimates from the graph and may vary with simulation conditions.

The model also provides voltage, current, and power measurement signals.

### Simulink Model

![Simulink Model](images/simulink-model.png)

### PV Characteristic Graph

![PV P-V Characteristic](images/pv-pv-characteristic.png)

## MPPT Algorithm

The MATLAB Function block takes PV voltage and current as inputs and generates a reference voltage (Vref).

The initial parameters in the supplied code are:

- Initial voltage = 52 V
- Initial current = 0.001 A
- Voltage step size = 0.11 V
- Initial calculated power = 0.052 W

The algorithm compares PV power and adjusts the voltage reference with the aim of reaching the Maximum Power Point.

**Note:** The current implementation needs improvement because previous voltage and power values are not stored between function executions. The MPPT output also needs to be connected to the actual load-control system to demonstrate complete closed-loop MPPT operation.

## Conclusion

Through this project, I studied the working of a stand-alone PV energy system using MATLAB/Simulink. I explored PV voltage, current, power, and the P-V characteristic curve. I also worked on implementing the Perturb and Observe MPPT technique to understand how maximum power can be extracted from a solar PV module.

This project helped me gain practical knowledge of solar PV modelling, simulation, and renewable energy systems.

## Repository Contents

- `Solar.slx` – MATLAB Simulink model.
- `images/simulink-model.png` – Simulink block diagram.
- `images/pv-pv-characteristic.png` – Simulation graph.
- `README.md` – Project documentation.
:::
