## CS Amplifier with current source load
### 1. CIRCUIT DIAGRAM
![WhatsApp Image 2025-02-19 at 22 49 43_2e811cc2](https://github.com/user-attachments/assets/127f08af-71f9-472c-a393-bbfc0467f816)
![WhatsApp Image 2025-02-19 at 22 50 16_0796ba05](https://github.com/user-attachments/assets/7d29ad43-06f4-45b6-82a1-29b61aa201f9)
![WhatsApp Image 2025-02-19 at 22 50 05_8e0c5985](https://github.com/user-attachments/assets/31378c58-8958-406d-a34c-706c4d503039)

 ### 2. COMPONENTS USED
 | Components | Value/Model | Purpose |
 |------------|-------------|---------|
 |MOSFET (M1) | CMOSN | Main active element |
 | MOSFET (M2) | CMOSP | Main active element (replacing resistor (R1) |
 | Voltage source (V1) | 1.8V | Supply voltage |
 | Voltage source (V2) | SINE(0.9 50m 1k) | AC input signal(1kHz, 50mV AC + 0.9V DC) |
 | Voltage source (V3) | -2 | Gate voltage for CMOSP |
 | MOSFET model library | .lib "tsmc018.lib"| Defines MOSFET characteristics |   

 ###3.THEORY
- A diode-connected CMOS transistor is a MOSFEt with gate and drain terminals shorted together so that it acts like a diode with voltage-dependent resistance.
- This loop is usually employed in current mirrors to provide a reference voltage.
- This behaves as a diode in certain analog signal-processing functions.

 ### 4. SIMULATION PROCEDURE
 The whole procedure and analysis is done by replacing the resistor with CMOSP.
  We provide the same working conditions for the CMOSP and do the DC, Transient and AC analysis.
 ### 3.1 DC operating point analysis
Set the gate voltage of PMOS so as to make sure that the PMOS is always ON. As we did in Expt1a, by trial and error method, we find the Length and Width of the MOSFET and find  the DC Operating Point of the circuit.
![WhatsApp Image 2025-02-19 at 22 50 29_d9d62e98](https://github.com/user-attachments/assets/732dca0b-e6e1-4f69-8d81-ecee7e0d2f2c)
According to the power budget given, the current value is 27µA. The operating analysis makes sure that the PMOS is working in saturation region.

 ###  Transient Response
An alternating(sine) signal is given to the input source of 0.9v with 50m amplitude and 1k frequency.
![WhatsApp Image 2025-02-19 at 22 50 47_03beac1d](https://github.com/user-attachments/assets/a0aa0217-feb5-4bfe-b6d8-2865226822a9)
Here we see a 180 degree phase shift between the input and output waveforms.
The gain of the circuit= 1.804 

### AC Analysis
Small signal analysis is appiled to observe the frequency response of the circuit.
![WhatsApp Image 2025-02-19 at 22 51 15_12bd8274](https://github.com/user-attachments/assets/25ecdb27-9ca6-415f-a3c2-2cc6984b6ad5)

### 5. OBSERVATION
- The PMOS regulates the drain current of M1, leading to more stable operating conditions.
- It helps to keep the NMOS in saturation region of operation.

### 6. CONCLUSION
- The CMOS circuit simulated using LTSpice is a saturated amplifier with stable gain, phase shift, and transient response.
- The output characteristics and voltage gain measured validate its appropriateness for low-power amplification use.
- More analysis, such as cut-off frequency and bandwidth determination, will assist in designing the circuit to meet particular design needs.
