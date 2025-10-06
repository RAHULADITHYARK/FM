# FM

EXP NO: 4	GENERATION AND DETECTION OF FM


AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.


EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

THEORY:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.
FREQUENCY DEVIATION f and MODULATION INDEX m f :
The frequency deviation f represents the maximum shift between the  modulatedsignal
frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency
m= f / fm


FREQUENCY MODULATION GENERATION:
The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.
Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the modulating signal.
•	Beta: Modulation index, which controls the extent of frequency deviation.
2.	Generate Signals:
•	Modulating signal: Sinusoidal signal used for modulation.
•	Carrier signal: The high-frequency carrier signal.
•	Modulated signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.
3.	FM Modulation:
•	Modulated signal is obtained by modulating the carrier signal with the modulating signal.
 
4.	FM Demodulation:
•	Differentiation: Computes the derivative of the modulated signal to extract frequency variations.
•	Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.
•	Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.
5.	Visualization:
•	Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.



PROCEDURE


•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
Verify the generated waveform using Tabulation and Model Waveform

MODEL GRAPH:

<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />


Program
```scilab
Am=5.7;
Fm=452;
Fs=45200;
t=0:1/Fs:2/Fm;
m1=Am*cos(2*3.14*Fm*t);
subplot(3,1,1);
plot(t,m1);
Ac=11.4;
Fc=4520;
c1=Ac*cos(2*3.14*Fc*t);
subplot(3,1,2);
plot(t,c1);
Bt=4.75;
FM=Ac*cos((2*3.14*Fc*t)+(Bt*sin(2*3.14*Fm*t)));
subplot(3,1,3);
plot(t,FM);
```
Output Waveform

<img width="1366" height="616" alt="image" src="https://github.com/user-attachments/assets/b3f66ee0-10e2-416c-bede-ce00a199345a" />

Tabulation

![fm](https://github.com/user-attachments/assets/2f9e09da-b4c4-4b87-8af0-90edd5439849)

Calculation

![fmcal](https://github.com/user-attachments/assets/390c2dfe-71a4-4bd0-8308-917d9c9a14d1)

Frequency Deviation Practical = 2121.15

Modulation Index Practical	= 5.84

Modulation Index Theoretical	= 5.8



RESULT:

Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.


