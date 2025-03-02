# Experiment-3 

Date-24/2/2025

## Aim:Design and Analyze the MOS differential amplifier circuit for the following specifcations and Perform DC analysis,Transient Analysis,Frequency response and extract parmeter

VDD=3.3v,P<=3mW,Vicm=1.65v,Vocm=1.7v,Vp=0.5v
### Components Required: MOSFET(M1,M2 and M3),Load Resistor(to be calculated),voltage supply(VDD and VG)
## Theory:

#### Differential Amplifier:
The differential-pair or differential-amplifier configuration is the most widely used building block in analog integrated-circuit design.It consist of two 
transistors M1 and M2, whose sources are joined together. If two transistor are connected to the different voltage input then there current across M1 and M2 are different due to gate voltage.If in case the voltage supply at gate terminal is same then the current through the M1 and M2 are same (Im1=Im2).This configuration is called "Common Mode input voltage differential Amplifier".WHatever may be the load resistor, the MOSFET M1 and M2 should not go to the Triode region. It should be verified that MOSFET should be in Saturation Region.

This Expereiment is Based on Common Mode Input voltage Differential Amplifier.

This Experiement is conducted in 3 stages.Where common source terminal is connected with

1.Resistor

2.Current source

3.MOSFET 

For all this circuit we need find out the AC analysis ,Transient analysis And Frequency Response.

### 1.Circuit 1 (Common Source terminal is coonected to resistor):
   In this circuit we have two MOSFET connected to same voltage input forming differential pair.And Load Resistor is coonected to the Drain terminal of MOSFET.
   Source terminal is connected resistor and another terminal is connected to ground this is called source degenration resistor.
   
   CIRCUIT:
   
   





