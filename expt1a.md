# LIC Simulation-4NI23EC114
## LTSpice simulation of a CMOS circuits.
### Design of CS amplifer #ciruit-01
### Question:
Perform DC,transient and AC analysis of the CS Amplifier with the following specification using LTspice.
a)VDD=1.8V
b)Vg=0.9V
c) Technology=180nm
d)Power=50 micro watt.

# 1) INTRODUCTION:
   In this experiment using LTspice software we are going to design a CS amplifier circuit  which is a CMOS based circuit. In this we are going to find the DC operating point, Transisent analysis
   along with AC analysis using LTspice. The circit parameter are NMOS4, resistor, voltage source. The DC operating region helps to determine the steady state behaviour of a circuit by finding the
   biasing conditions, which are crucial for ensuring proper operation of active devives like transistors. Transisent analysis examines how a circuit responds to time varying inputs, allowing
    to know about the behavior during switching, startup or other dynamic condtitons. This is parituclary importat for circuits with capacitors, inductors, or feedback loops. AC analysis on the
   other hand , focuses on the frequency rsponse of a circuit by analyzing how it reacts to small-signal sinusoidal inputs, which is vital in applications like amplifier design and signal processing.

### 2) CIRCUIT DIAGRAM:

![Screenshot 2025-02-17 211753](https://github.com/user-attachments/assets/67fd7f55-8762-4121-a34b-fff1c72f9bf5)

### 3) SIMULATION PROCEDURE :

### 3.1 DC OPERATING POINT ANALYSIS:
 In this simulation a DC supply voltage(VDD) of 1.8V is given and 1k ohm resistor is used . Here as the power rating is 50 micro watt. We have considered drain current(iD)=27.77micro ampere from the 
 equation (P=VDD*I) by setting L=700nm and W=690nm.The gate terminal of the MOSFET is biased at 0.9V DC, while the source terminal is grounded(0V). The drain volatge(Vd) is determined by the circuit 
 components and the MOSFETS's characteristics. Since the threshold voltage (Vth) is 0.37V , the applied Vgs = 0.9V ensures that the MOSFET is turned ON.After running the .op simulation , the DC volatges 
 at key nodes are observed. The MOSFET's drain current(Id) and the volatge drop across R1 are also obtained. Based on these values, we determine whether the MOSFET operates in Saturation(for amplification),
 Triode( for switching) or Cutoff( if OFF). If the drain volatge is significantly lower than VDD, the MOSFET is conducting and likely in saturation mode, which essential for amplification purposes.

### 3.2 TRANSISENT ANALYSIS:
An AC signal is apllied to the circuit using sine wave input volatge source parameters:

a)Amplitude: 50mV(peak)
b)Frequency: 1kHz
c)DC offset: 0.9V The simulation runs for 3 milliseconds(.trans 3m), capturing multiple cycles of the input waveform. The output waveform is observed at the drain of the MOSFET.
If there's a phase shift than the circuit is functioning as an amplifier.

### 3.3 AC ANALYSIS:
An AC signal sweep is applied to the circuit over a wide range of frequencies, from 0.1 Hz to 1T Hz, using a logarithmic scale. The AC input is a small signal sine wave, and the gain is measured
as the ratio of output peak voltage to input peak voltage in decibels. The simulation uses the following command:
(.ac dec 20 0.1 1T)

Here,

dec 20: Takes 20 data points per decade for a smooth response curve.
0.1 Hz to 1T Hz: Defines the frequency sweep range.

### 4) OBSERVATION:
### 4.1 DC OPERATING POINT ANALYSIS:
 ![Screenshot 2025-02-17 212054](https://github.com/user-attachments/assets/01a88d40-15c0-410e-b1c1-6e51ca44b8af)
 ![Screenshot 2025-02-17 212110](https://github.com/user-attachments/assets/586f23d7-7b5a-4009-8453-0f7e6c8274d3)
HERE,
  VDD=1.8V
  Gate voltage= 0.9V
  source voltage=0
  drain current=27.77micro ampere.
  This confirms that the MOSFET is in the saturation region, which is necessary for proper amplification.

### 4.2 TRANSISENT ANALYSIS:  
![Screenshot 2025-02-17 213209](https://github.com/user-attachments/assets/457bcab4-094d-4966-b484-291619b7da34)
Input signal charcteristics: A 1kHz sine wave and 50mV peak amplitude and 0.9V DC offset was applied.
Observed Output voltage(Vout): The output peak voltage was measured as V of the sine wave, indicating a successful amplification.
Waveform integrity: 
 The amplified signal retainsits shape without significant distortion, confirming proper circuit operation.

### 4.3 AC ANALYSIS:
![Screenshot 2025-02-17 213354](https://github.com/user-attachments/assets/322a5d87-0f43-4138-85fa-965e6984ea7b)
Voltage Gain: The circuit shows a gain of -30.88dB, which corresponds to a linear gain of -35.02. This indicates significant amplification of the input signal.
Phase shift: At 1k Hz, the output waveform lags the input by approximately 120 degree, as calculated from the transient response graph. This suggests a frequency-dependent phase delay.
Frequency: 200.699G Hz.

### 5) INFERENCE:
The LTSpice simulation of the CMOS circuit provides insights into its operational behaviour in different domains:

DC operating point analysis cofirmed that the MOSFET operates in saturation region. The observed drain voltage (1.799V) and the drain current(55uA) align with theoretical values.
Transient analysis verified that the circuit amplifies the input 1k Hz sine wave with minimal distortion. The output peak voltage of 1.751V suggests successful signal amplification.
A phase shift in output indicates that the circuit introduces delay, which is typical in amplifiers.
The transient response graph shows how the circuit behaves over time. The response is smooth, with no unexpected delays or distortions. The circuit reacts well to changes, confirming its stability.
AC analysis showed a voltage gain of -17dB indicating strong signal amplification. There is a significant difference between the gain calculated from the AC analysis and the transient analysis.
However, the AC analysis(-17dB) is likely the correct small-signal gain at the given frequency. The transient analysis(-30.88dB) is overestimated due to phase shift and peak misalignment 
that effects the calculation. The phase shift of ~120 degree at 1k Hz suggests that the frequency-dependent behaviour must be considered for applications requiring precise phase alignment.



