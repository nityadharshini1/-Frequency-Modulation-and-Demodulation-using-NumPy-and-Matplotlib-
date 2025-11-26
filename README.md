# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

__Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

__Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
__Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

__Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Programme:__

clc; clear all; close all;

Am = 13.9;        % Message amplitude
Ac = 29.8;        % Carrier amplitude
fm = 420;         % Message frequency (Hz)
fc = 10000;       % Carrier frequency (choose a standard value)
kf = 100;         % Frequency sensitivity

Fs = 100000;      % Sampling frequency
T = 0.01;         % Duration
t = 0:1/Fs:T;

% Message signal
m = Am * sin(2*pi*fm*t);

% FM signal
y = Ac * cos(2*pi*fc*t + (kf/fm)*m);

% Plotting
figure;

subplot(3,1,1);
plot(t,m);
title('Message Signal');
xlabel('Time');
ylabel('Amplitude');

subplot(3,1,2);
plot(t, Ac*cos(2*pi*fc*t));
title('Carrier Signal');
xlabel('Time');
ylabel('Amplitude');

subplot(3,1,3);
plot(t,y);
title('FM Modulated Signal');
xlabel('Time');
ylabel('Amplitude');
__Output:__
![WhatsApp Image 2025-11-26 at 21 03 26_43eecca6](https://github.com/user-attachments/assets/a0b70ec8-5355-4ebb-a403-e31aeb1b2421)

__Result:__
![WhatsApp Image 2025-11-26 at 21 04 14_9ce57291](https://github.com/user-attachments/assets/98854888-2a57-498a-8da1-ee36af85af35)
