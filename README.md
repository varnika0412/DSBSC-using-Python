# DSBSC-using-Python

## AIM:

To implement and analyze DSBSC using Python's NumPy and Matplotlib libraries. 

## EQUIPMENTS REQUIRED

1.	Software: Python with NumPy and Matplotlib libraries
2.	Hardware: Personal Computer


## Algorithm:


1.	Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and frequency deviation.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
5.	Generate DSBSC Signal: Apply the DSBSC formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.


## Program

```
import numpy as np
import matplotlib.pyplot as plt
AM=6.1
fm=363
fs=36300
AC=12.2
fc=3630
t=np.arange(0,2/fm,1/fs)
m=AM*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=AC*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1=(AC+m)*np.cos(2*3.14*fc*t)
s2=(AC-m)*np.cos(2*3.14*fc*t)
s =s1-s2# Define s as the sum of m and c
plt.subplot(3,1,3)
plt.plot(t,s)
plt.tight_layout()
plt.show()

```

## Output Graph
![WhatsApp Image 2025-09-11 at 18 55 16_fdd2eeec](https://github.com/user-attachments/assets/5d2021a3-4aa9-49f6-89f9-3ce5f124dee9)





## Tablular Column
![WhatsApp Image 2025-11-13 at 09 36 58_91941b53](https://github.com/user-attachments/assets/be44a0e9-bdf5-469c-a848-42841c850ff0)




## Result

Thus the DSB-SC-AM Modulation is generated using python.

