### EXPERIMENT-07  
### INSTRUMENTATION AMPLIFIER:
## INTRODUCITON:
An instrumentation amplifier using three operational amplifiers (3-op-amp instrumentation amplifier) is a widely used analog circuit designed to amplify small differential signals while rejecting large common-mode voltages, making it ideal for precision measurement applications. This type of amplifier is particularly known for its high input impedance, low output impedance, excellent linearity, and high common-mode rejection ratio (CMRR
A key feature of the 3-op-amp instrumentation amplifier is the ability to set and control gain using a single resistor connected between the inverting inputs of the two input-stage op-amps. This makes gain adjustment simple and precise, often without affecting the input impedance. The final stage (difference amplifier) typically uses a resistor network to further refine the differential gain and to eliminate common-mode signals effectively.
 ## CIRCUIT DIAGRAM:
 ### a) DIFFERENTIAL MODE AMPLIFITER:
 ![Screenshot 2025-04-20 154600](https://github.com/user-attachments/assets/c7ecbfd8-6615-4ef0-8769-ec68d7a54dcb)

### b) COMMON MODE AMPLIFIER:
![Screenshot 2025-04-20 154832](https://github.com/user-attachments/assets/e65ce5c9-4be2-4c84-a249-1a093bbc8339)

### DESIGN QUESTION:
Design an instrumentation maplifier usin 3op-amp configuration with the following constraints.
R1=R3=10K ,R2=R4=20K ,R5=R6=10K. find the gain for Rg values for 20k and 10k resistors values.
### Calculation: 
### FOR Rg=20k:
### DIFFERENTIAL MODE:
### TABULAR COLUMN:
| V1(volts) | V2(volts) | Vout(theortical) | Vout(pratical) | Ad=Vout/V2-V1) |
|-----------|-----------|------------------|----------------|----------------|
| 0 | 0.5 |  1.5 | 1.5001 | 3.00004 |
| 1.5 | 0.8 | -2.1| -2.10003 | 3.00004 |
| 2 | 2.6 | 1.8 | 1.80001 | 3.00001 |
| 2.2 | 2.55 | 1.0 5 | 1.05 | 3 |
| 5.4 | 4.4 | -3 | -3.00006 | 3.0006 |
| 6.4 | 7.4 | 3  | 2.9999 | 2.9999 |
| 4.6 | 6.8 | 6.6 | 6.60004 | 3.00001 |
 ### AVG Ad= 3.0001

 
### a) V1=5.4V and V2=4.4V
### =Rf/R1*(1+2*(R4/Rg))(V2-V1)
### Vout=-3V

### FOR V1=5.4V and V2=4.4V
![Screenshot 2025-04-20 154509](https://github.com/user-attachments/assets/954cba5e-3c7e-484d-9c73-e068dff33b86)

![Screenshot 2025-04-20 154522](https://github.com/user-attachments/assets/cbec4d26-e633-4e3b-a756-547dca5e37f2)

 ### COMMON MODE:
 ### TABULAR COLUMN:
 | Vin (volts) | Vout (volts) | Ac=Vout/Vin |
 |-------------|--------------|-------------|
 | 2 | 1.899n | 0.9495n |
 | 3 | 2.847n  | 0.949n | 
 | 5.6 | 5.308n | 0.947n |
 | 12 | 11.282n | 0.94n |
 ### AVG Ac=0.9463n

 ### FOR Vin=2V
 
![Screenshot 2025-04-20 154900](https://github.com/user-attachments/assets/3dedef86-925c-4abf-a0cd-f7e5671e7b70)

![Screenshot 2025-04-20 154910](https://github.com/user-attachments/assets/eff1cfac-4775-4b55-9ad9-9bbd9b8ee60e)

### CMRR= 20*log(Ad/Ac)
### CMRR= 20*log(3/0.9463n)
### CMRR= 190.021 db

### 2) For Rg=10k:
### DIFFERENTIAL MODE:
### TABULAR COLUMN:
| V1(volts) | V2(volts) | Vout(theortical) | Vout(pratical) | Ad=Vout/V2-V1) |
|-----------|-----------|------------------|----------------|----------------|
| 0 | 0.5 |  2.5 | 2.5 | 5 |
| 1.5 | 0.8 | -3.5 | -3.5 | 5 |
| 2 | 2.6 | 3 | 3 | 5 |
| 2.2 | 2.55 | 1.75 | 1.75 | 5 |
| 5.4 | 4.4 | -5 | -5 | -5 |
| 6.4 | 7.4 | 5 | 5 | 5 |
| 4.6 | 6.8 | 11 | 11 | 5 |
 ### AVG Ad= 5

 ### a) V1=6.4V and V2=7.4V
### =Rf/R1*(1+2*(R4/Rg))(V2-V1)
### Vout=5V

### FOR V1=6.4V and V2=7.4V
![Screenshot 2025-04-20 154734](https://github.com/user-attachments/assets/4ae19222-0ed2-4ea9-b281-3d7124f4c78e)

![Screenshot 2025-04-20 154747](https://github.com/user-attachments/assets/0b08f8b0-ef5a-4233-ae2a-e961d2412904)
 
 ### COMMON MODE:
 ### TABULAR COLUMN:
 | Vin (volts) | Vout (volts) | Ac=Vout/Vin |
 |-------------|--------------|-------------|
 | 2 | 1.899n | 0.949n |
 | 3 | 2.8477n  | 0.949n | 
 | 5.6 | 5.303n | 0.946n |
 | 12 | 11.28n | 0.94n |
 ### AVG Ac=0.946n
 
  ### FOR Vin=2V:
 
 ![Screenshot 2025-04-20 154936](https://github.com/user-attachments/assets/c081c61e-9a52-46a0-8a14-eb012f964798)
 ![Screenshot 2025-04-20 154946](https://github.com/user-attachments/assets/26ffcc4b-8161-4c25-9c91-e2304625e722)
 

 ### CMRR= 20*log(Ad/Ac)
### CMRR= 20*log(5/0.946n)
### CMRR= 194.46 db

### EFFECT OF Rg VALUES ON INSTRUMENTATION AMPLIFIER:

###  i)Gain Increases

The amplifier amplifies the input signal more.

###  ii)Bandwidth Reduces

The frequency range over which the amplifier works effectively becomes narrower.

### iii)Higher Risk of Saturation

The output can reach maximum/minimum limits quickly if input signals are not small.

### iv)Offset and Drift Effects Become More Prominent

Small errors like offset voltage or temperature drift get amplified more.

###  v)Noise Amplification Increases

Any noise present at the input also gets boosted, possibly affecting signal quality.

### vi)Why the output voltage remains constant when Rg values is decreased:
As the value of Rg decreases in a 3-op-amp instrumentation amplifier, the gain of the amplifier increases significantly, since gain is inversely proportional to Rg. This means that even a very small differential input voltage gets amplified much more. However, operational amplifiers have a limited output voltage range, typically constrained by their power supply rails (for example, ±15V or 0 to 5V in single-supply systems). When the amplified output exceeds this limit, the op-amp output can no longer increase linearly and instead saturates at its maximum (or minimum) possible voltage. This results in the output voltage becoming constant, even though the theoretical gain continues to increase with decreasing Rg. Additionally, at very high gains, small offsets, noise, or common-mode signals present at the input may also get amplified enough to push the output into saturation. Therefore, despite increasing the gain by lowering Rg, the output voltage appears constant because the amplifier has reached its output limit and cannot represent any further increase.

### INFERENCE:
From the observed behavior of the instrumentation amplifier as Rg decreases, we can infer that while reducing Rg increases the gain of the amplifier, there is a practical limit to how much the output can respond. As gain rises, the amplifier becomes highly sensitive to even the smallest input differences. However, once the amplified output approaches the supply voltage limits of the op-amps, the amplifier enters saturation, and the output voltage remains constant regardless of further increases in gain. This indicates that although theoretical gain increases with decreasing Rg, the usable output range is constrained by the amplifier's power supply and internal limitations. Therefore, careful selection of Rg is essential to ensure accurate signal amplification without pushing the amplifier into saturation.









 
