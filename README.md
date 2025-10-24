# FM-using-Python

Aim


To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries. 

Apparatus Required

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer
  
Theory

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier wave is varied according to the instantaneous amplitude of the message signal. The general form of an FM signal is:



Algorithm


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

Program
```
import numpy as np
import matplotlib.pyplot as plt
Ac=3.18
fc=2740
Am=2.18
fm=274
fs=27400
B=3
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*3.14*fm*t) 
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
fm=Ac*np.cos(2*3.14*fc*t+B*np.sin(2*3.14*fm*t))
plt.subplot(3,1,3)
plt.plot(t,fm)
plt.tight_layout()
plt.show()
```
Output Waveform

<img width="640" height="916" alt="image" src="https://github.com/user-attachments/assets/1b687cb3-163b-4108-baf9-2815e98b2ba5" />

Tabular Column

<img width="630" height="954" alt="image" src="https://github.com/user-attachments/assets/1ea75f53-46e4-46eb-a848-7304e73e45fa" />


Calculation

<img width="640" height="954" alt="image" src="https://github.com/user-attachments/assets/143e831a-a97a-4da7-8a1f-e19de61ae182" />


Result


The message signal, carrier signal, and frequency modulated (FM) signal will be displayed in separate plots. The modulated signal will show frequency variations corresponding to the amplitude of the message signal.
