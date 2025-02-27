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


Step 3:Replace the gate biasing with a small AC signal source and then set up an AC Analysis to simulate the frequency response.

Step 4:Run the simulation to observe the voltage gain and frequency response.Look at the output signal and compare it with the input to calculate the gain.Add an AC signal source to the gate .Set up Transient Analysis with a stop time and time step.

Step 5:Run the Transient Analysis to observe the time-domain response.Check the output waveform for any distortion or rise time issues.

Step 6:  Review the results for DC, AC, and Transient analyses.Make adjustments to biasing or component values.

## Circuit:


## Calulation:
Power = 50uW

The drain current (ID):

Power=Vcc*ID

ID=Power/Vcc

ID=27.7uA

Loop Equation: Vdd=Vds+Id*Rd

Gain: Av~ -10

## Result:
### DC Analysis:
![image](https://github.com/user-attachments/assets/e8aa518e-870e-4765-a5a4-aa471d5e71d4)

Power=50W

ID=27.2uA

Width=2.015um

### Trainsient Analysis:
![image](https://github.com/user-attachments/assets/cbe9d184-526c-4c54-ad39-5aa30faef752)
There is a phase shift of 180 degree in between input waveform and output waveform.

### AC Analysis:
![image](https://github.com/user-attachments/assets/35e42c62-4293-40a4-8615-7ed607cb9af7)
Gain=-46dB

## Inference:
1.The gain of a MOSFET amplifier varies with frequency, with optimal performance typically found in the mid-band range.

2,The MOSFET must operate in the saturation region. This ensures a stable gain and allows the circuit to provide consistent signal amplification.

3.Increasing the MOSFET’s width allows more current to flow, directly influencing its performance.

4.Q-point prevents distortion and ensures reliable signal processing.
# Circuit 2:
![fmhjgkj](https://github.com/user-attachments/assets/67af7152-38dd-494e-a171-8cf8b90332ed)

## Procedure:

1.Open LTSpice and import the necessary library files to ensure accurate NMOS and PMOS transistor models.


2.Select the required components for the circuit: one PMOS, one NMOS, three voltage sources (1.8V, 0.9V, and -5V), and a ground connection.


3.Arrange and connect these components according to the given circuit diagram.


4.Assign the MOSFET properties, including threshold voltage, temperature, and other relevant parameters.


5.Perform a DC Analysis by selecting the .op simulation option. Once executed, the simulation will display the corresponding DC operating point values.


6.Proceed with Transient Analysis by setting a 5 ms cycle. This will generate both individual and combined input-output waveforms for five complete cycles.


7.For AC Analysis, modify the DC source to a sinusoidal waveform with parameters .Then, select the AC simulation option . Finally, place a node at the output waveform to observe the response.

### DC Analysis:
![ffgf](https://github.com/user-attachments/assets/de9cca2c-f379-4337-8783-81ed67b0431e)


Id=1.48A,voltage Applied=0.9,1.8
## AC Analysis:
![image](https://github.com/user-attachments/assets/98df8420-7496-4de6-b63f-54b384a211b4)
## Transient Analysis:
![image](https://github.com/user-attachments/assets/45bcf003-731f-47bf-bf6f-e23f94317bbd)
There is a phase shift of 180 degree in between input waveform and output waveform.



## Inference:
1.The low power budget implies that trade-offs between gain, bandwidth, and noise performance must be carefully considered.

2.The common-source amplifier design requires ensuring both NMOS and PMOS operate in saturation for proper amplification.

3.Transistor width and length can vary power consumption, gain, and frequency response by the graph.

4.From doing AC analysis ,we can find the bandwidth,gain from the given graph we can find the values.






​
 






