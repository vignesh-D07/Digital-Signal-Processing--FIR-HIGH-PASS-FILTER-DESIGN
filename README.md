# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Hamming Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
~~~
clc; % clear screen 
clear all; % clear screen 
close all; % close all figure windows 
wc=input('enter the value of cut off frequency');  
N=input('enter the value of filter');  
alpha=(N-1)/2;  
eps=0.001;  
%High Pass Filter Coefficient 
n=0:1:N-1;  
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc))./(pi*(n-alpha+eps)) 
%Hamming Window Sequence  
n=0:1:N-1;  
wh=0.54-0.46*cos((2*pi*n)/(N-1)) 
hn=hd.*wh  
% Plot the High Pass Filter with Hamming Window Technique 
w=0:0.01:pi;  
h=freqz(hn,1,w); 
plot(w/pi,abs(h),'blue');
title('High Pass FIR Filter using Hamming Window');
https://github.com/vignesh-D07/Digital-Signal-Processing--FIR-LOW-PASS-FILTER-DESIGN
~~~
## OUTPUT:
HIGH PASS FIR FILTER USING HAMMING WINDOW

<img width="700" height="516" alt="image" src="https://github.com/user-attachments/assets/bef48419-fe52-4e59-b24a-8d2c9b6fb7a8" />

## RESULT:

<img width="902" height="1600" alt="image" src="https://github.com/user-attachments/assets/943247dc-53be-4246-bdaa-9c9415f0aef7" />

