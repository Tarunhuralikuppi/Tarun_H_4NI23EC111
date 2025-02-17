# Experiment-1
## Aim:
To find DC analysis,Transient and AC analysis of CS amplifier circuit and extract different parameters associated using LT Spice.
## Equipments:
 NMOS and PMOS transistors,  1 kΩ resistor, voltage supplies of 1.8V and 0.9V, along with connecting wires.
## Theory:
MOSFETs (Metal-Oxide-Semiconductor Field-Effect Transistors) play a critical role in modern electronics due to their compact design, low power consumption, simple geometry, and compatibility with VLSI (Very Large Scale Integration) technology. These characteristics make them ideal for use in integrated circuits.
MOSFETs can be connected in three primary configurations: common drain, common gate, and common source. Among these, the common source and common drain configurations are the most commonly used, each offering unique advantages depending on the application.

When operating in the saturation region, the MOSFET functions as an amplifier. For an N-channel MOSFET, specific conditions must be met to ensure proper amplification. In the common source configuration, the signal undergoes a 180-degree phase shift between the input and the output, which is a typical feature of this setup.
### DC Analysis:
DC analysis in a common source amplifier is used to establish the transistor's operating point, ensuring that it operates in the saturation region. This is important because the transistor needs to stay in saturation to function as a proper amplifier and avoid distortion.

During DC analysis, the values for the biasing resistors are determined. These resistors set the required gate-source voltage and drain current, ensuring the transistor remains in saturation under steady-state conditions. This helps achieve a stable and predictable operating point, even in the presence of variations in temperature or power supply.

The goal of DC analysis is to set the correct biasing conditions, which prevent the MOSFET from entering undesired regions like cutoff or triode. This ensures that the amplifier operates reliably and efficiently, amplifying the input signal without distortion.

### AC Analysis :
DC analysis in a common source amplifier is used to establish the transistor's operating point, ensuring that it operates in the saturation region. This is important because the transistor needs to stay in saturation to function as a proper amplifier and avoid distortion.

During DC analysis, the values for the biasing resistors are determined. These resistors set the required gate-source voltage and drain current, ensuring the transistor remains in saturation under steady-state conditions. This helps achieve a stable and predictable operating point, even in the presence of variations in temperature or power supply.

The goal of DC analysis is to set the correct biasing conditions, which prevent the MOSFET from entering undesired regions like cutoff or triode. This ensures that the amplifier operates reliably and efficiently, amplifying the input signal without distortion.
  AC Gain is given by: Av=-gm.Rd
### Transient Analysis:
  Transient analysis in a common source amplifier studies the circuit's time-dependent behavior when subjected to varying input signals. It examines how the output responds to changes over time, accounting for charging and discharging of capacitors and other dynamic effects. The goal is to understand the amplifier's response to short-term variations, such as rise time and settling time. This analysis ensures the amplifier can handle fast-changing signals without distortion. It is crucial for evaluating the performance of the circuit in real-time applications.
## Procedure:
Step 1:Draw the circuit by placing an NMOS transistor with its drain connected to a resistor 
Rd , which is connected to VDD. Connect the source of the transistor to ground.
And connect the gate terminal to the CMOS to the voltage source for biasing the gate.

Step 2:Add a DC voltage source for VDD and a biasing voltage source for the gate to the circuit.Run the DC Operating Point simulation to verify the biasing and check the quiescent point (DC operating point) of the transistor.


Step 3:





