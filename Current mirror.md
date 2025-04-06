


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

## 🧮Calculation

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

Width of MOS:
M1: 3.37um, 
M2: 3.37um, 
M3: 3.37um 

#### ✏️DC Analysis
![dc analysis](https://github.com/user-attachments/assets/4f3a64a5-ce89-40f8-8cda-4c67547f1d8a)

- Measured drain current: **Id = 0.0002789A**
 ### **Analysis by Varying L while Maintaining the Ratio (W/L) constant**

| Length| Width | Current(ID<sub>M3</sub>) |
|------------|------------|---------|
| 180nm | 3.37um | 0.0002789A |
| 500nm | 9.361um | 0.0002819A |
|1000nm | 18.722um | 0.0002805A |

#### ✏️Transient Analysis
![transient](https://github.com/user-attachments/assets/1d9b00cf-60a3-49a3-a4ef-bc8c58363afb)

Obtained gain =12.729
#### ✏️AC Analysis
![Screenshot 2025-04-03 235849](https://github.com/user-attachments/assets/2170bfa3-5c24-4056-ab11-14da7c45f81c)
Obtained gain = 22.760 dB

## Ratio 1:2
🧮Current Calculation:
```math
I_{ref} = \frac{I_t}{3} = 0.185mA
```

W/L values:
```plaintext
M1: 2.9um / 180nm
M2: 5.8um / 180nm
M3: 5.8um / 180nm
```


### **✏️Transient Analysis**

Obtained gain: 12.1326V/V
![Screenshot 2025-04-04 002616](https://github.com/user-attachments/assets/f2a8ccb3-5cda-4365-8fde-702007e09fff)

### **✏️AC Response**

![Screenshot 2025-04-04 002719](https://github.com/user-attachments/assets/556a840c-2a33-46d9-a513-962d1fe76e2c)
Obtained gain (dB): 24.306 dB


## **📈Inference:**

✅ Consistent Current Replication:
The mirror circuit demonstrates excellent consistency in replicating the reference current, with only slight variation under simulation.

🔁 Effect of W/L Ratio Adjustment:
Modifying the transistor dimensions (W/L) leads to proportional scaling of the output current, reinforcing the mirror’s stability and reliability.

📈 Gain Deviations Explained:
Simulated gain values were marginally higher than the theoretical estimates, which can be attributed to secondary effects like parasitics or minor mismatches in transistor parameters.

⚖️ Gain vs Bandwidth Trade-Off:
While increasing the mirror ratio enhances the output current gain, it also introduces a reduction in bandwidth, indicating a typical trade-off encountered in analog design.

📐 Theoretical Alignment:
Overall, the circuit’s behavior closely matches theoretical predictions, supporting the effectiveness and accuracy of the current mirror design.



# 🧩 MOS Differential Amplifier With Current Mirror
## Aim

✅Design and analyze the MOS differential amplifier circuit for the given specifications:

- **V<sub>DD</sub>:** 3.3V
- **Power Consumption (P):** ≤ 3mW
- **V<sub>icm</sub>** 1.72V
- **V<sub>DCM</sub>:** 1.81V
- **Threshold Voltage (Vp):** 0.7V

## Theory

A current mirror is used to provide a constant bias current in a differential amplifier. This stable current helps the amplifier operate reliably and improves performance.

It enhances common-mode noise rejection by keeping the current balanced between the two transistors. For accurate current mirroring, the mirror transistors must be well-matched.

Proper design ensures enough voltage headroom and high output impedance, which supports better gain and frequency response.

In short, the current mirror improves stability, accuracy, and signal quality in differential amplifiers.


### ✨Significance of Current Mirror in Differential Amplifier
The current mirror plays a crucial role in enhancing the performance and reliability of a differential amplifier. It provides a constant tail current, which ensures stable biasing, improves common-mode rejection, and allows the amplifier to operate with greater precision and linearity.

By maintaining symmetry and a fixed operating point, the current mirror ensures consistent gain, better noise immunity, and improved high-frequency response. It's essential for achieving the core advantages of differential amplification in analog circuits.



## 🧮Calculation

- **Determine Iss (Source Current):**\
  Iss = Power / Vdd\
  Iss = 3mW / 3.3V = 0.909mA

## ⚡Circuit 

![2 1](https://github.com/user-attachments/assets/5227fdb3-a510-4c4d-bf44-e94e5c10b936)

## ✏️DC Analysis

![2 2](https://github.com/user-attachments/assets/c76d901c-b657-42cb-9b15-e93e5de8d2c9)


## ✏️Transient Analysis
![Screenshot 2025-03-24 234402](https://github.com/user-attachments/assets/2ea344f8-40b4-4a46-a28f-565a534f19aa)
Obtained Gain=14.93

## ✏️AC Analysis
![image](https://github.com/user-attachments/assets/42e0cb8e-dc0c-4529-9c81-caea25ffe597)

Gain=34.73db



## 📌 Inference :

Using a current mirror significantly enhances both **bias stability** and **gain predictability**. In basic circuits, the tail current is vulnerable to supply and temperature fluctuations, which in turn causes inconsistent transconductance and gain variation. By introducing a current mirror, the tail current becomes fixed and stable, ensuring a reliable operating point and consistent signal amplification across varying conditions.

The current mirror also improves **common-mode rejection** and overall **signal linearity**. Without it, mismatched transistors and unstable biasing lead to poor rejection of common-mode noise and limited output swing. With a current mirror in place, better matching and regulated current enable stronger differential performance and a more linear, wider output range.

Finally, **frequency response** benefits greatly from mirror-based biasing. Circuits without a current mirror suffer from parasitic effects due to unstable operation. The stable bias provided by the mirror minimizes these effects, leading to improved bandwidth and more reliable high-frequency behavior.



