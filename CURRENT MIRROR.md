### EXPERIMENT-04 
### CURRENT MIRROR AS A ACTIVE LOAD IN AMPLIFIER CIRCUIT.

![Screenshot 2025-03-24 213555](https://github.com/user-attachments/assets/73bce1d6-fc37-4a40-ab03-2e8547a3c5bf)# **Current Mirroring Experiment**

Given :

V<sub>dd</sub>=1.8 V.\
P <=1 mW.\
A<sub>v</sub>>-10 V/V.
Circuit diagram : ![Screenshot 2025-03-22 215639](https://github.com/user-attachments/assets/4c266142-5e04-4fc7-8ee4-efe180e88590)

# FOR L = 180 nm
# **1:1 Ratio :**
# **DC Analysis:**
I<sub>Total</sub> = P/V<sub>DD</sub>\
Since the ratio is 1:1 I<sub>ref</sub> = I<sub>x</sub>\
I<sub>ref</sub> = I<sub>Total</sub>/2\
I<sub>Total</sub> = 1 mW/1.8 V\
I<sub>Total</sub> = 0.555 mA\
I<sub>ref</sub> = 0.555 m/2\
I<sub>ref</sub> = 0.2778 mA.\
The W/L values for M1, M2, and M3 are 10	µm/180nm, 10	µm/180nm, and 10	µm/180nm, respectively.
![Screenshot 2025-03-24 211655](https://github.com/user-attachments/assets/b6d2b872-84ed-4b95-9124-edb063432780)
![Screenshot 2025-03-24 211707](https://github.com/user-attachments/assets/d8900953-5cd3-4f31-94c4-75e52687187a)

# **Transient Analysis :**
- Change the input voltage to sine and change the amplitude to 50 mV , frequency to 1 kHz and offset voltage to 0.6275 V.
![Screenshot 2025-03-24 211741](https://github.com/user-attachments/assets/dd64b9fa-0ba8-4c8c-8972-5bc95e5717b3)

# **AC Analysis :**
![Screenshot 2025-03-24 211801](https://github.com/user-attachments/assets/474f2285-76b7-4c80-b847-47635bc3f62b)
 The Expected gain in dB is 20 and the obtained gain is 26.23 dB.


 # **1:2 Ratio :**
 # **DC Analysis :**
 ![Screenshot 2025-03-24 212420](https://github.com/user-attachments/assets/ccaed9cb-e42a-4dd2-8676-7bf4c010240b)
I<sub>ref</sub> = 0.185 mA.
In order to determine the current value based on the specified ratio, the W/L values for  M2 and M3 are 6	µm/180nm and 6	µm/180nm, nd M1 is 3	µm/180nm respectively. 

# **Transient Analysis :**
![Screenshot 2025-03-24 212428](https://github.com/user-attachments/assets/0d0dd2d6-4cb1-43ad-8017-7ed3ef188885)
 The expected gain was greater than or equal to 10 V/V and the obtained gain is 12.11 V/V.

 # **AC Analysis :**
![Screenshot 2025-03-24 212440](https://github.com/user-attachments/assets/f147b316-9ceb-4b09-b395-8db7773acb7c)


# **2:1 Ratio :**

## **DC Analysis :**
![Screenshot 2025-03-24 212932](https://github.com/user-attachments/assets/34e958df-0fb1-4095-9645-0b8d3d0003de)
I<sub>ref</sub> = 0.555 mA.
In order to determine the current value based on the specified ratio, the W/L values for  M2 and M3 are 6	µm/180nm and 6	µm/180nm, nd M1 is 3	µm/180nm respectively.

## **Transient Analysis :**
![Screenshot 2025-03-24 212941](https://github.com/user-attachments/assets/49a98c6b-4680-4c37-b70a-af9759818ef6)
 The expected gain was greater than or equal to 10 V/V and the obtained gain is 9.86 V/V.\

## **AC Analysis :**
![Screenshot 2025-03-24 212948](https://github.com/user-attachments/assets/96509b2e-1020-414f-a908-1ea3d490c074)


# FOR L = 1 	µm

|Ratio|  Av(in dB)    | Av(in V/V) | 
|-----|---------------|------------|
|1:1  |12.60          |15.3        |    
|1:2  |9.55           |15.98       |   
|2:1  |12.56          |16.87       |

## Variation observed when current mirror is in certain ratios:
# 1:1 Ratio
This is the standard configuration, where both transistors in the mirror have the same size.

The mirrored current equals the reference current:

I 
OUT
​
 =I 
REF
​
​
 
The amplifier maintains a balanced operation with maximum symmetry in a differential pair.

Provides standard gain and balanced voltage swing.

# 1:2 Ratio 
(Output transistor is twice the size of the reference)
The mirrored current is doubled:

I 
OUT
​
 =2⋅I 
REF
​
 
This increases the load current, which can reduce the output impedance of the mirror.

In an amplifier, this results in:

Lower gain, because Rout is reduced due to increased current.

Possible clipping or reduced headroom, depending on biasing.

Higher power consumption.

#  2:1 Ratio 
(Output transistor is half the size of the reference)
The mirrored current is halved:

I 
OUT
​
 =0.5⋅I 
REF
​



 
This reduces the load current, which can:

Increase the output impedance, potentially increasing the gain.

Improve power efficiency.

Possibly degrade bandwidth, due to slower operation at lower currents.







# **Inference :**
- The current mirror circuit accurately copies the reference current with very little variation, ensuring reliable current mirroring across different W/L ratios.
- Even when the W/L ratio changes while keeping the same proportion, the drain current (I<sub>D</sub>) stays nearly the same, confirming the circuit's effectiveness.
- The amplifier gain is slightly higher than expected due to small differences in transistor properties or minor simulation effects.
- When the mirror ratio increases (from 1:1 to 1:2), the gain also increases as expected.
- Overall, the results closely match theoretical predictions, proving that the simulation and circuit design are working correctly.
- When a current mirror is used as an active load in an amplifier circuit, it significantly enhances the circuit's performance by providing a high output resistance and stable current.
- Unlike a passive resistor, the current mirror behaves like a constant current source, which leads to a more stable biasing condition and improves the amplifier’s linearity.
- The high output impedance of the current mirror increases the overall voltage gain of the amplifier, since the gain is directly proportional to the load resistance.
- In differential amplifier configurations, using a current mirror as the load also improves the common-mode rejection ratio (CMRR), allowing the circuit to better suppress unwanted common-mode signals and amplify only the differential input.
- This behavior is especially advantageous in integrated circuit (IC) design, where space is limited and precision is critical.
- Current mirrors are more area-efficient than large resistors and provide better matching characteristics, making them ideal for high-performance analog designs.



# *PART-B*
**Aim :**
Design the differential amplifier using the same design specification as Experiment-3. Perform DC analysis,trasient and AC analysis.
![Screenshot 2025-03-24 213555](https://github.com/user-attachments/assets/3858fa0a-db90-4255-964d-2c8b17277d62)

# **DC Analysis :**
1.Case 1: 180nm
![Screenshot 2025-03-24 223314](https://github.com/user-attachments/assets/bebb9514-dc08-4ec4-815e-07b78ac66e05)
PMOSFET 1,2 = width is 70um \
M3, M4  = width is 238.7um\
M5 = width is 70um\
M6 = width is 140um\
V<sub>out</sub>=  1.4V\
I<sub>ref</sub> = 0.277mA\

2.Case 2: 500nm
![Screenshot 2025-03-24 223332](https://github.com/user-attachments/assets/a78dd2b1-9634-4b68-aa02-8e3b12743399)
PMOSFET 1,2 = width is 70um \
M3, M4  = width is 693.6um\
M5 = width is 70um\
M6 = width is 140um\
V<sub>out</sub>=  1.41V\
I<sub>ref</sub> = 0.277mA\

### Transient analysis:
1.Case 1: 180nm
![Screenshot 2025-03-24 223417](https://github.com/user-attachments/assets/b8fb9a39-181e-4696-b98f-4ef9ffa3d31f)

2.Case 2: 500nm
![Screenshot 2025-03-24 223426](https://github.com/user-attachments/assets/02546256-4a7d-4fbc-8b46-a05f13b33764)


# **Inference :**
- The circuit operates as a differential amplifier based on a current mirror, with the output (Vout) being controlled by the difference between V2 and V3.
- Stable current replication is guaranteed by the PMOS current mirror (M1-M2).
- This circuit is helpful for signal processing and amplification in analog designs because it uses the NMOS differential pair (M3-M4) for amplification.

  #  Conclusion:
  The use of a current mirror as an active load in an amplifier circuit offers several advantages that make it a fundamental building block in modern analog design, particularly in integrated circuits. When implemented as an active load, the current mirror provides a high output impedance, which directly translates into increased voltage gain for the amplifier. Unlike passive resistors, current mirrors maintain a constant current over a wide range of output voltages, ensuring a more stable and predictable operating point. This is especially beneficial in differential amplifier configurations, where the current mirror enhances the common-mode rejection ratio (CMRR), allowing the circuit to effectively reject common-mode noise and focus on amplifying the differential signal. Additionally, by adjusting the ratio of the current mirror—such as 1:1, 1:2, or 2:1—designers can fine-tune the output current, which in turn affects gain, bandwidth, and power consumption. A 1:1 ratio maintains balance and symmetry, a 1:2 ratio increases current and bandwidth at the cost of gain, and a 2:1 ratio lowers current and power usage while boosting gain. These scaling capabilities add flexibility to the design, allowing trade-offs between performance parameters such as speed, gain, and power efficiency. Furthermore, current mirrors are compact and match well in integrated designs, making them more area- and process-efficient than passive components. Overall, current mirrors as active loads greatly improve the performance, stability, and design scalability of amplifier circuits, and their role is essential in achieving high-gain, low-power, and high-precision analog systems.








