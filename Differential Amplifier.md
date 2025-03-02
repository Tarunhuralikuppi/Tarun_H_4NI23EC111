# Experiment-3 

Date-24/2/2025

### Aim:Design and Analyze the MOS differential amplifier circuit for the following specifcations and Perform DC analysis,Transient Analysis,Frequency response and extract parmeter

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
#### To find the all the values of resistor and current value. we need solve the given queston specification.
![IMG_20250302_214918](https://github.com/user-attachments/assets/7885abaf-d118-4a5f-a16b-a4f459aaec14)

By solving we get

Iss=0.909mA

I1=I2=0.4545mA

RD=3.55kΩ

Rss=0.555kΩ

By tis value circuit is been built with respective to the values derived.(Note:This value may change while getting  the desired values in the saturation wise or some constant terms needs to set)

## 1.Circuit 1 (Common Source terminal is connected to resistor):
   In this circuit we have two MOSFET connected to same voltage input forming differential pair.And Load Resistor is coonected to the Drain terminal of MOSFET.
   Source terminal is connected resistor and another terminal is connected to ground this is called source degenration resistor.
   
   CIRCUIT:
   
   ![resitor](https://github.com/user-attachments/assets/0cef0b81-492c-4a48-a9a0-a1d6a0eed07e)
  
   The resistor applied at the common source terminal leads to change in the voltage gain ,input impedence in the circuit and the lineraity.So the linearity increases and the impedence.
   As this is closed loop amplifier this leads to causes a feedbakback amplifier for all elements connecting to the common source terminal.

   ### DC analysis:
To do circit analysis first we need to check that the Both the  MOSFET should be in the  Saturation Region which should satisfy this;

 VDS > VGS - Vth

![resistor DC](https://github.com/user-attachments/assets/f5c7ab92-1f1f-4656-987e-57e60cba1e37)
### Transient Analysis:
The transient analysis explain the  circuit response at a particular instant of  time when a time-varying signal is applied at the inputs.In this experiment we can see a complete phase shift of 180 degree output to the input signal.As with respect to context of voltage gain, as the volatge gain is more leads to the smaller the bandwidth size.At the particular time output wave changes with respect input in the amplitude.

![resistor transient](https://github.com/user-attachments/assets/cbaafa66-111f-4f86-97a3-2b7ba339c8a4)

Voltage Gain of this circuit is given by= Vout-Vin

Av=1.76-162/1.70-1.60=1.4

Therefore Higher the Higher resistor value reduces gain but increases bandwidth and more the  transient response.

## AC Analysis:

Frequency response is determining quantity of bandwidth and stability of a MOSFET. This is divide into three regions;

1.Low frequency

2.Mid-band Frequency

3.High Frequency

In this experiment we can observe that there is no low frequency region because of there is no bypass or coupling capacitor in the circuit.We can observe that mid band region upper value is nearear to the 3dB value which can used as parameter to check bandwidth of amplifier to maintain its gain.

![resistor AC](https://github.com/user-attachments/assets/f39d06f6-a7dc-4a95-bf76-f779e50124ae)

### 2.Circuit 2 (Common Source terminal is connected to current source):
Same  as the ciruit in the resistor circuit , we have two MOSFET connected to same voltage input forming differential pair.And current source is coonected to the Drain terminal of MOSFET.

Source terminal is connected to the current source and another terminal is connected to ground.

![current](https://github.com/user-attachments/assets/9e44ec7a-05af-457f-8dfe-a9b0ad645a84)














   
   
   





