#  LINEAR INTEGRATED CIRCUTIS
### EXPERMINENT 02:
DIFFERENTIAL AMPLIFIER.
## INTRODUCIION:

#### DEFINIATION:
A MOS differential amplifier is an electronic circuit that amplifies the difference between two input signals while rejecting common-mode signals. It consists of two MOSFET transistors operating in a differential configuration, typically biased by a constant current source to ensure balanced operation. This type of amplifier is widely used in analog circuits, including operational amplifiers and signal processing systems.

#### WORKING:
The MOS differential amplifier operates based on the principle of differential signal amplification. When two input voltages are applied to the gates of the MOSFETs, the transistor with the higher gate voltage conducts more current, while the other conducts less. This imbalance creates a differential output voltage. The circuit's tail current source ensures that the total current remains constant, allowing the amplifier to focus only on the difference between the inputs. If both inputs receive the same voltage (common-mode signal), the circuit ideally produces no output, thus effectively rejecting noise and interference. Enhancements such as active loads or current mirrors improve gain and performance.


![WhatsApp Image 2025-03-09 at 17 01 48_06c11091](https://github.com/user-attachments/assets/d7559099-5727-45ac-9c5b-2643623405c1)

# DESIGN:
Design and Analyze the Differential Amplifier for the following specs: VDD=3.2v, P<=2.8mW, Vicm=1.6v, Vocm=1.7V with node voltage Vp=0.6v. Perform DC Analysis, Transient Analysis and Frequency response and extract the parameters

Observing the above circuit, to calculate the required parameters, we need to calculate the values of Rd and RSS to help the MOSFET function properly. Given:- VDD=2.2v, P<=2.2mW, Vicm=1.2v, Vocm=1.25v, Vp=0.4v. We know that P=VI. Using this, we can calculate the total current flowing in the circuit. I=P/VDD => I=2.8m/3.2 => I=0.875mA. Since ID1=ID2=I/2, I/2=0.4375A=ID1=ID2. 
Calculating the total and branch current we can calculate the resistor values. Rd=VDD-Vocm/ID1 => (3.2-1.7)/0.4375 => Rd=3.428kΩ. RSS=Vp/ISS => RSS=0.6/0.875mA => RSS=685.714Ω.

![Screenshot 2025-03-08 220521](https://github.com/user-attachments/assets/399d7296-db86-4d6f-b071-1f73cbd20a4e)

# DC ANAYSIS:
 To find the DC characteristics of the circuit. As we have calculated the values of Rd and RSS and total current of the circuit. Design the ciruit in LTspice and assign the all set of values . Now taking Length (L) and Width(W) for the both  NMOS transistors . By taking L=180nm and W=2.53222um for both NMOS tranisstors we will get the acurrate dc operating point. 

 
![Screenshot 2025-03-09 174043](https://github.com/user-attachments/assets/e8ca774c-03c6-4780-9e83-47253478366d)
![Screenshot 2025-03-09 174059](https://github.com/user-attachments/assets/2ba81318-80a8-4604-8b90-b90d311375ff)
![Screenshot 2025-03-08 230612](https://github.com/user-attachments/assets/bee64765-9a91-43b7-8d48-e8f3e081835c)

 From the above dc analysis  bothe the MOSFET are working under saturation region. The current flowing in each tranistor perfectly matches given design specification and also the source voltage and output voltage (i.e Vocm).( Power rating should be 2.8mW or below).

 # TRANSISENT ANALYSIS:
 To perform the transisent analysis we have aapply the sine input dc offset voltage for both the NMOS transistors.
 The  sine input dc offset voltage for the bothe the transistor is 1.6V and amplitude is 50m and the frequency is 1khz. 
 The graph is observied between the output Vocm and the input gate voltage to analyse the circuit.
 Conduct the taransiset analysis by giving the stop timme about 5m.

 ![Screenshot 2025-03-09 175834](https://github.com/user-attachments/assets/bdb7a7ed-9954-4126-93fd-6b05ae53de6c)

 From the graph the green sine wave  graph indicates the output signal and blue sine wave  graph indicates the input signal. We can observe that the amplifier circuit produces output with 180 phsase shifs wtih input signal. Let us find the Gain pf the circuit 
 we know that  Av=Vout/Vin
              Av=(1.864-1.536)/(1.649-1.550)
              Av=3.31 
              The db conversion of the gain is 
              db=20log(AV)
              db=20*log(3.31)
              db=10.404db. This can be varified by conducting the frequency response.
 This analysis helps evaluate the amplifier’s dynamic behavior, including signal amplification, response time, and transient distortions. By adjusting design parameters like the tail current, load resistance, and transistor dimensions, the performance can be optimized for higher gain, faster response, and improved linearity.             


# AC ANALYSIS:
 This is done to verify the overall gain of the circuit and the gain calculated inn transisent anlysis and atlast to find -3db gain of the given circuit.
 To perform the frequency respose we have apply the sinusoidal signal to the gate terminals and apply the  AC amplitude about as 1. Apply start frequency=0.1 and stop frequency=0.1t
 

![Screenshot 2025-03-08 223541](https://github.com/user-attachments/assets/d53c7c9a-591c-41dd-989f-62ab61dc35ad)

From the graph we can say that the gain what we have find in the transisent analysis is almost equal to what we find in the frequency response graph.
The gain what we find in frequency response graph is about 10.45db and the gain what we find in transisent analysis is about  10.404db.
The -3db gain of the ciruit is somewhere around 7.45db which is near to 33.80Ghz.
The simulation provides key parameters like differential gain, -3dB bandwidth, phase response, and common-mode rejection. By analyzing the magnitude and phase plots, designers can optimize the circuit for high gain and stable operation across the desired frequency range.

Now let us try to analyse a variation of differential amplifier circuit by applying a current source and mosfet in place of RSS.


# REPLACING RESISTOR WITH A CURRENT SOURCE:
In an NOS differential amplifier, replacing the resitive tail(RSS) with an activ current source significantly improves performance. The primary effect is increased gain and better common-mode rejection. A resistive tail limits the differential gain due to voltage drops and variations, whereas a current source provides a high output resistance, ensuring a nearly constant tail current. This forces the differential pair to operate more efficiently, improving linearity and reducing distortion. Additionally, an active current source enhances the common-mode rejection ratio (CMRR), minimizing noise and interference from power supply fluctuations. Overall, the amplifier becomes more stable, with improved gain and better differential-mode performance.

![Screenshot 2025-03-08 230141](https://github.com/user-attachments/assets/c2e5a902-05a4-4657-af80-fb82bb9caff4)
![Screenshot 2025-03-08 230612](https://github.com/user-attachments/assets/ebd505a7-b30c-4405-be8f-14a2415bbbfa)

there is not much change in the components of the circuit other than the current source, there is not much change in the DC Output. Since the Current source stabilizes the current through the MOSFETs, the overall stability increases. The current and the voltage across Vp remain the same. The power budget will be within the limit of 2.8 mW. 

#TRANSISENT ANALYSIS:
![Screenshot 2025-03-09 220140](https://github.com/user-attachments/assets/cc54a3c6-db06-41a9-8621-c04e2e9d5900)

In the above transisent analysis the green sine wave graph indicates the output signal and blue sine wave graph indicates the input signal. We can observe that the amplifier circuit produces output with 180 phsase shifs wtih input signal. Let us find the Gain of the circuit 
 we know that 
               Av=Vout/Vin
               Av=(1.865-1.536)/(1.649-1550)
               Av=3.32
               The db conversion of the gain is 
               db=20*log(Av)
               db=20*log(3.32)
               db=10.42. This can be varyified by conducting the frequency response. As we can observe that there is not much more difference in the gain of the circuit but  slightly greater than when replaced with current source. This can be varified by ac analysis.

# AC ANALYSIS:

![Screenshot 2025-03-08 230537](https://github.com/user-attachments/assets/ef9fb464-51d3-4579-9805-79e52aa8d249) 
To analyse the ac analyse , we have to apply the sinusoidal wave signal to the gate voltage and apply the ac amplitude about 1. As we can seee that their is a negligible change in the gain of the circuit when we applied a current source . The gain of the circuit is 10.42.  At 118.697 degree the -3db gain is 7.42 with a frequence of 34.21Ghz.

# REPLACING RESISTOR WITH NMOS:
Let us move to the final circuit. Replace the current source with an NMOS. The theory explanation for this is that the MOSFET acts as a CONSTANT CURRENT SOURCE when voltage is given to the gate terminal to make it work in the saturation region. After adjusting the W and L values to make sure that the MOSFET is conducting 0.875mA through it. After calculating, we found the W and L values to be L=180n and W=2529n. Now let us conduct a DC Analysis.


# DC ANALYSIS:

![Screenshot 2025-03-09 224951](https://github.com/user-attachments/assets/a6c1d82f-35e9-414a-ad03-4abfbf674502)

![Screenshot 2025-03-09 225012](https://github.com/user-attachments/assets/08d53521-bc07-4b8f-b117-bccac7eef03f)

According to the definition of MOSFET, we need to provide voltage to the gate terminal so that it drives the MOSFET to work in saturation region. To consider the value of Vg, let us consider overdrive voltage. We know that Vd should be greater than Vov. The formula is Vds>Vov. We know that Vov=Vgs-Vt. Substituting that, we get Vds>Vgs-Vt. Rearranging that we get the formula Vgs>Vds+Vt. We know the value of Vds(Vd-Vs => Vp-0 => 0.4) which is 0.4 and the given value of Vt for the MOSFET is 0.366. Using this, we get Vgs>0.6+0.366 => Vgs>0.966. The approximate value to be give to Vg should be greater than 0.966. So let us provide voltage of 1.43v to Vg. After setting the value of Vg, we find thecan observe that the sum of both the branch current of 0.875mA is available through the MOSFET M3 which makes it to act like a current source. According the value, we can calculate the POWER RATING of the circuit which will come out to be 2.8mW which is the prescribed and preferred value. After confirming the values, we can now proceed to so Transient Analysis to calculate the gain of the circuit.

![Screenshot 2025-03-09 225711](https://github.com/user-attachments/assets/f6b21e57-2498-4c94-85d2-3f74573f9b51)

# TRANSISENT ANALYSIS:

Like before, we apply a sinusoidal input to the MOSFET M1 and M2 with offset 1.6v, amplitude 50m and frequency of 1k to calculate the gain. Let us study the graph.

![Screenshot 2025-03-09 224825](https://github.com/user-attachments/assets/e38c4275-edb1-4ee7-aeea-3f64c760b7c5)
The gain of the circuit is 
               Av=Vout/Vin
               Av=(1.866-1.536)/(1.649-1.550)
               Av=3.33
               The db conversion of the gain is
               db=20*log(Av)
               db=20*log(3.33)
               db=10.45
We can observe that the output is amplified with the output with just a slight variation. Calculating gain we get Av 3.33 which converted to dB is 10.45dB. We can verify the results by conducting AC Analysis.

# AC ANALYSIS:

After calculating the dB gain of 10.45dB from the graph obtained from Transient analysis, let us confirm the finding by analysing the AC component of the circuit. Provide AC AMPLITUDE of 1 to the MOSFETs M1 and M2 and conduct the analysis.

![Screenshot 2025-03-09 224417](https://github.com/user-attachments/assets/20167321-6eb1-4fd8-8132-d141d3832b61)
We can observe that the calculated value of gain corresponds with the gain plotted from the graph of AC Analysis.

# COMPARISION OF REPLACEING THE RSS WITH CURRENT SOURCE AND A NMOSET:
| Replacement type | Advantages | Disadvantages|
|------------------| -----------| -------------|
| Current Source   | - Provides higher gain due to increased impedance. - 111 |...|
| Resistor| ...| ... |
| MOSFET | ... | ,, |






# INFERENCE:
The choice of replacing RSS (Resistor Source Degeneration) with a Current Source or a MOSFET in a MOS differential amplifier significantly impacts the amplifier's performance in terms of gain, stability, complexity, and power consumption.

### RSS (Resistor Source Degeneration)
Using a resistor (RSS) in the source of the MOS differential amplifier provides a simple and stable design. The resistor introduces local negative feedback, which helps improve linearity and reduces variations due to process and temperature changes. Additionally, an RSS-based design consumes less power compared to active current sources. However, this approach limits the amplifier's gain since the resistance reduces the effective transconductance. Moreover, RSS results in lower Common-Mode Rejection Ratio (CMRR) compared to an active current source, and in IC designs, large resistors occupy significant chip area, making them less desirable for compact designs.

### Current Source (Active Load)
Replacing RSS with a current source significantly improves the gain of the differential amplifier since the current source has a much higher impedance compared to a resistor. This also enhances the CMRR, allowing better rejection of common-mode signals. Furthermore, a current source provides more predictable biasing, as it is less sensitive to temperature and process variations compared to MOSFET-based sources. However, this method introduces additional circuit complexity, requiring components like current mirrors, which increase power consumption. Another drawback is reduced voltage headroom, meaning that the available signal swing is limited due to the voltage drop across the active current source.

### MOSFET (Diode-Connected or Current Source)
Replacing RSS with a MOSFET offers advantages, especially in integrated circuit (IC) designs where space is a concern. MOSFETs can act as active loads or current sources, providing a higher output impedance that boosts the amplifier's gain. Additionally, MOSFETs offer better matching compared to resistors, which is beneficial in IC fabrication for ensuring uniform performance. However, MOSFET-based current sources are highly sensitive to temperature and process variations, requiring compensation techniques to maintain stability. Moreover, biasing a MOSFET-based current source is more complex than using a simple resistor, as it requires additional circuitry to ensure the correct operating point.

# CONCLUSION:

Each approach has its advantages and trade-offs. RSS is simple, power-efficient, and stable, but it limits gain and consumes more space in IC designs. A current source significantly improves gain and CMRR but adds complexity and power consumption while reducing voltage headroom. Using a MOSFET provides a compact and high-gain solution but is more sensitive to process and temperature variations and requires careful biasing. Therefore, the selection between these approaches depends on the application requirements, design constraints, and performance priorities in the MOS differential amplifier.



                   



