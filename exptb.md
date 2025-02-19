## CS Amplifier with current source load
### 1. CIRCUIT DIAGRAM

 ### 2. COMPONENTS USED
 | Components | Value/Model | Purpose |
 |------------|-------------|---------|
 |MOSFET (M1) | CMOSN | Main active element |
 | MOSFET (M2) | CMOSP | Main active element (replacing resistor (R1) |
 | Voltage source (V1) | 1.8V | Supply voltage |
 | Voltage source (V2) | SINE(0.9 50m 1k) | AC input signal(1kHz, 50mV AC + 0.9V DC) |
 | Voltage source (V3) | -2 | Gate voltage for CMOSP |
 | MOSFET model library | .lib "tsmc018.lib"| Defines MOSFET characteristics |   

 ### 3. SIMULATION PROCEDURE
 The whole procedure and analysis is done by replacing the resistor with CMOSP.
  We provide the same working conditions for the CMOSP and do the DC, Transient and AC analysis.
 ### 3.1 DC operating point analysis
Set the gate voltage of PMOS so as to make sure that the PMOS is always ON. As we did in Expt1a, by trial and error method, we find the Length and Width of the MOSFET and find  the DC Operating Point of the circuit.

According to the power budget given, the current value is 27µA. The operating analysis makes sure that the PMOS is working in saturation region.

 ###  Transient Response
An alternating(sine) signal is given to the input source of 0.9v with 50m amplitude and 1k frequency.



Here we see a 180 degree phase shift between the input and output wavefprms.

### AC Analysis
Small signal analysis is appiled to observe the frequency response of the circuit.


### 4. OBSERVATION
- The PMOS regulates the drain current of M1, leading to more stable operating conditions.
- It helps to keep the NMOS in saturation region of operation.

### 5. CONCLUSION
- The CMOS circuit simulated using LTSpice is a saturated amplifier with stable gain, phase shift, and transient response.
- The output characteristics and voltage gain measured validate its appropriateness for low-power amplification use.
- More analysis, such as cut-off frequency and bandwidth determination, will assist in designing the circuit to meet particular design needs.
