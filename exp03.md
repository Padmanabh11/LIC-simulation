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

