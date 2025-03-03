#Experiment-3 
## Differential Amplifier:
The differential-pair or differential-amplifier configuration is the most widely used building block in analog integrated-circuit design.It consist of two 
transistors M1 and M2, whose sources are joined together.
If two transistor are connected to the different voltage input then there current across M1 and M2 are different due to gate voltage.If in case the voltage supply at gate terminal is same then the current through the M1 and M2 are same (Im1=Im2).This configuration is called "Common Mode input voltage differential Amplifier".WHatever may be the load resistor, the MOSFET M1 and M2 should not go to the Triode region. It should be verified that MOSFET should be in Saturation Region.

![image](https://github.com/user-attachments/assets/bd20bd4e-aab5-4fa4-825d-394bbb6e2b30)


This Expereiment is Based on Common Mode Input voltage Differential Amplifier.

This Experiement is conducted in 3 stages.Where common source terminal is connected with

1.Resistor

2.Current source

3.MOSFET 

For all this circuit we need find out the AC analysis ,Transient analysis And Frequency Response.
#### To find the all the values of resistor and current value. we need solve the given queston specification.

P=3mA

Iss=P/VDD=3*10^3/3.3=0.909mA

Is1=Is2=Iss/2=0.4545mA

RD=VDD-Vocm/Iss=3.3-1.7/0.45*10^3=3.55kΩ

Rss=Vp/Iss=0.5/0.909*10^3=0.555kΩ


 Finially by solving we get

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

Av=1.76-162/1.70-1.60
=1.4

Therefore Higher the Higher resistor value reduces gain but increases bandwidth and more the  transient response.

## AC Analysis:

Frequency response is determining quantity of bandwidth and stability of a MOSFET. This is divide into three regions;

1.Low frequency

2.Mid-band Frequency

3.High Frequency

In this experiment we can observe that there is no low frequency region because of there is no bypass or coupling capacitor in the circuit.We can observe that mid band region upper value is nearear to the 3dB value which can used as parameter to check bandwidth of amplifier to maintain its gain.

![resistor AC](https://github.com/user-attachments/assets/f39d06f6-a7dc-4a95-bf76-f779e50124ae)

Gain =20*log(Av)
      =20*log(1.4)
      =2.922

By calculating from graph we can say Therotical nad experiment value of mid band frequency is approximatly equal.

### 2.Circuit 2 (Common Source terminal is connected to current source):
Same  as the ciruit in the resistor circuit we need to replace resistor by current source . We have two MOSFET connected to same voltage input forming differential pair.And current source is connected to the Drain terminal of MOSFET.

Source terminal is connected to the current source and another terminal is connected to ground.

![current](https://github.com/user-attachments/assets/9e44ec7a-05af-457f-8dfe-a9b0ad645a84)

### DC Analysis:

 We need set voltage of Vicm to maintain the desired value of the current and voltage at source point.As a result opertaing point will be given as;

 ![DC current](https://github.com/user-attachments/assets/3022bf5a-d92a-4b7b-b28c-7d331aa52b62)
 
 In the operating values we got the current flowing through the common source terminal is exactly what we had derived in intial stage of the experiment.

 ## Transient Analysis:

 The volatge gain of the ciruits inceases because of the current source drop across it is less compared to the Rs resistor drop. So the Voltage gain of circuit is more compared to the circuit 1

 ![curent transient](https://github.com/user-attachments/assets/13f3a7ca-e8e1-40a5-97cd-8d3a348774fe)

 Voltage gain= vout/vin
              
              =(1.83-1.57)/(1.69-1.63)

              =4.333

## AC Analysis:

(Still Need to be done because we need to get 13.4dB gain  but actual we are getting around 4dB  in the graph of AC analysis)


### 3. Circuit 3-(Connecting MOSFET to source terminal)

Now we are replacing the current source to the mosfet(M3) where we need to keep current Id3 as our desired value And to keep the mosfet(M1,M2,M3) in saturation region so that voltage gain will be maintained.In this ciruit MMOsfet is connected to drain of it to source terminal and to other ground.

![Mosfet](https://github.com/user-attachments/assets/49333fe7-c483-46f2-98da-55f856de3b23)

### DC Analysis:

### Transient Anlysis:

![transient mos](https://github.com/user-attachments/assets/72839a11-9d6e-492f-9d6d-76920988fb88)


### AC Analysis:

## INFERENCE:

In this experiment, we seen the working principles of a differential amplifier and its types and configuration.

There are three types of  configurations were implemented: resistor , current source , and an NMOS . All the implements work on different ways that results into the cahnge in Voltage gain and stabillity of a mosfet.

when resistor is connected it provides low CMRR,deduce gain voltage,but high bandwidth and also provide negative feedback 

But in the case of current source connection it is reciprocal of resistor connection because it has high gain volatge, high CMRR,but  slight reduce in the bandwidth compared to the resistor connection.

Highest gain volltage is drewn by the circuit of CMOSN connection

By this we can say at what time/situation is required we can use that configuration.

1.Need more Band width-Use Resistor configuration

2.Need more Gain-Use CMOSN Configuration

3.Need precise CMRR-Use current or CMOSN configuration


 

 

 



















   
   
   





