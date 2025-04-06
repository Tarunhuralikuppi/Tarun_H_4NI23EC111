


# **CURRENT MIRROR**
## 🧪Aim
Design and Analysis of Current Mirror as Active Load in an Amplifier Circuit with the following specifications:
- **Voltage Gain (Av) > 10 V/V**
- **Supply Voltage (Vdd) = 1.8V**
- **Power Consumption (P) <= 1W**
- **Consider three cases for channel length (L):**
  - **L = 180 nm,500nm,1000nm**
  - keeping the ratio (W/L) same for all the cases.

## Theory

## 📘 What is a Current Mirror?

A **Current Mirror** is a circuit that copies a reference current (Iref) into one or more output branches. It ensures that the output current stays constant and is proportional to the reference current, even if the load changes.
## 📐 Current Ratios Explained

We explore two cases:
- **1:1 Mirror**: Output current (Iout) = Iref
- **1:2 Mirror**: Output current (Iout) = 2 × Iref

This is achieved by adjusting the **W/L ratios** (Width/Length) of the MOSFETs:
| Transistor | W/L Ratio | Current |
|------------|------------|---------|
| M1 (Reference) | 1 | Iref |
| M2 (Output - 1:1) | 1 | Iref |
| M2 (Output - 1:2) | 2 | 2 × Iref |

Current Mirrors are particularly useful in the integrated circuits, for biasing the amplifiers. The advantage of biasing the amplifiers with the current source is that it provides a high voltage gain and good biasing stability. This current source can be generated using a simple PMOS transistor or using a MOS transistor in cascode configuration (to achieve higher gain)
###Key Characteristics of a Current Mirror:

Maintains constant current irrespective of load variations.
Provides high output impedance.
Ensures precise current replication across outputs.

## Calculation

### Given:
- **Supply Voltage**: V<sub>dd</sub> = 1.8V  
- **Power Consumption**: P ≤ 1mW  

### Total Current:
### Ratio 1:1
```math
I_t = \frac{P}{V_{DD}} = \frac{1mW}{1.8V} = 0.555mA
I_{ref} = \frac{I_t}{2} = 0.2778mA
```

## L = 180 nm

![circuit dc](https://github.com/user-attachments/assets/de016b00-f74c-4a06-9691-91bfc23b89f2)

M1: 3.37um, 
M2: 3.37um, 
M3: 3.37um 

#### DC Analysis
![dc analysis](https://github.com/user-attachments/assets/4f3a64a5-ce89-40f8-8cda-4c67547f1d8a)

- Measured drain current: **Id = 0.0002789A**
 ### **Analysis by Varying L while Maintaining the Ratio (W/L) constant**

| Length| Width | Current(ID<sub>M3</sub>) |
|------------|------------|---------|
| 180nm | 3.37um | 0.0002789A |
| 500nm | 9.361um | 0.0002819A |
|1000nm | 18.722um | 0.0002805A |

#### Transient Analysis
![transient](https://github.com/user-attachments/assets/1d9b00cf-60a3-49a3-a4ef-bc8c58363afb)

Obtained gain =12.729
#### AC Analysis
![Screenshot 2025-04-03 235849](https://github.com/user-attachments/assets/2170bfa3-5c24-4056-ab11-14da7c45f81c)
Obtained gain = 22.760 dB

## Ratio 1:2
Current Calculation:
```math
I_{ref} = \frac{I_t}{3} = 0.185mA
```

W/L values:
```plaintext
M1: 2.9um / 180nm
M2: 5.8um / 180nm
M3: 5.8um / 180nm
```


### **Transient Analysis**

Obtained gain: 12.1326V/V
![Screenshot 2025-04-04 002616](https://github.com/user-attachments/assets/f2a8ccb3-5cda-4365-8fde-702007e09fff)

### **AC Response**

![Screenshot 2025-04-04 002719](https://github.com/user-attachments/assets/556a840c-2a33-46d9-a513-962d1fe76e2c)
Obtained gain (dB): 24.306 dB


## **Inference:**
- The current mirror accurately reproduces the reference current with minimal deviations.
- Altering the W/L ratio proportionally maintains a nearly constant drain current, demonstrating the robustness of the mirror circuit.
- Gain measurements slightly exceed theoretical predictions, likely due to parasitic effects or transistor mismatches.
- Increasing the mirror ratio improves gain but reduces bandwidth.
- Results align well with theoretical expectations, verifying the circuit's reliability.



# MOS Differential Amplifier With Current Mirror
## Aim

Design and analyze the MOS differential amplifier circuit for the given specifications:

- **Supply Voltage (Vdd):** 3.3V
- **Power Consumption (P):** ≤ 3mW
- **Input Common Mode Voltage (Vicm):** 1.72V
- **Output Differential Common Mode Voltage (Vdcm):** 1.81V
- **Threshold Voltage (Vp):** 0.7V
- **Current Mirror Implementation:** Used for biasing the differential amplifier

## Theory

A **current mirror** is a circuit that replicates (mirrors) the current from one active device to another, ensuring a constant current source or sink. In the context of a **MOS differential amplifier**, the current mirror plays a crucial role in biasing and ensuring proper operation.

### Key Insights into Current Mirror with Differential Amplifier:

1. **Current Biasing:** The current mirror provides a stable biasing current, ensuring consistent operation.
2. **Improved Common-Mode Rejection:** The differential amplifier rejects common-mode noise, and the current mirror enhances this performance.
3. **Matching Considerations:** The transistors used in the current mirror must be well-matched to ensure accurate current mirroring.
4. **Voltage Headroom:** Proper design ensures that the circuit operates within the given supply voltage constraints.
5. **Load Considerations:** The output impedance of the current mirror affects the gain and performance of the differential amplifier.

## Calculation

- **Determine Iss (Source Current):**\
  Iss = Power / Vdd\
  Iss = 3mW / 3.3V = 0.909mA

## Circuit 

![Screenshot 2025-03-24 234316](https://github.com/user-attachments/assets/49249614-f17f-4b81-890a-8fe5d7a3681f)

## DC Analysis

![Screenshot 2025-03-24 234328](https://github.com/user-attachments/assets/9e0c06ad-e09a-439d-9a5d-adbff2425cdd)

## Transient Analysis
![Screenshot 2025-03-24 234402](https://github.com/user-attachments/assets/2ea344f8-40b4-4a46-a28f-565a534f19aa)


## AC Analysis
![Screenshot 2025-03-25 001855](https://github.com/user-attachments/assets/d3ae10f8-5ae0-4248-9e66-eb1282e93ae4)

## Comparison of Differential Amplifier Circuits With privious Experiment

## Infernce

| Parameter                  | Ckt without Current Mirror | Ckt with Current Mirror | Inference |
|----------------------------|---------------------------|-------------------------|-----------|
| Tail Current Stability     | Varies with temperature and supply changes | Constant due to current mirror | Improved bias stability |
| Common Mode Rejection Ratio (CMRR) | Lower due to mismatch | Higher due to better matching | Reduced common-mode noise |
| Gain Stability             | Unstable, varies with tail current | More predictable | Better signal amplification |
| Output Swing               | Limited by tail current variations | Improved with regulated current | Enhanced signal integrity |
| Frequency Response         | Affected by mismatch and instability | Wider bandwidth with stable biasing | Better high-frequency performance |

### Justification for Each Change

#### Tail Current Source:
- **Ckt without Current Mirror:** Used a simple current source, possibly a resistor or a fixed current bias.
- **Ckt with Current Mirror:** Implemented a current mirror, ensuring constant tail current, improving overall performance.  
**Inference:** Better bias stability, reducing variations due to temperature or power supply fluctuations.

#### Common Mode Rejection Ratio (CMRR):
- **Ckt without Current Mirror:** Without a precise current source, mismatches in transistors cause lower CMRR.
- **Ckt with Current Mirror:** Current mirror ensures better matching, reducing common-mode signal impact.
**Inference:** Ckt with Current Mirror rejects common-mode noise more effectively, improving differential operation.

#### Gain Stability:
- **Ckt without Current Mirror:** Gain fluctuates due to variations in tail current and process mismatches.
- **Ckt with Current Mirror:** With a constant current mirror, gain is more predictable.
**Inference:** Consistent differential gain, improving signal amplification quality.

#### Output Swing:
- **Ckt without Current Mirror:** Limited by variations in tail current.
- **Ckt with Current Mirror:** With a well-regulated current mirror, the circuit operates more linearly.
**Inference:** Improved output swing and signal integrity.

#### Frequency Response:
- **Ckt without Current Mirror:** Dependent on device mismatches and unstable biasing.
- **Ckt with Current Mirror:** Current mirror ensures proper biasing, reducing parasitic effects.
**Inference:** Higher bandwidth and better high-frequency response in Ckt with Current Mirror.

---
