# FIR-FILTER-DESIGN
# EXP 4 A: Design-of-FIR-Digital-Filter-using-Rectangular-Window

# AIM 1:  
To perform Design-of-LOWPASS FIR-Digital-Filter-using-Rectangular-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
close;

M = input('Enter the Odd Filter Length = ');
Wc = input('Enter the Digital Cut off frequency = ');

alpha = (M - 1) / 2; // Center Value

for n = 1:M
    if (n == alpha + 1)
        hd(n) = Wc / %pi;
    else
        hd(n) = sin(Wc * ((n - 1) - alpha)) / (((n - 1) - alpha) * %pi);
    end
end

// Rectangular Window
for n = 1:M
    W(n) = 1;
end

// Windowing filter coefficients
h = hd .* W;

disp(h, 'Filter Coefficients are');

[hzm, fr] = frmag(h, 256);

// Magnitude Response
subplot(2, 1, 1);
plot(2 * fr, hzm);
xlabel('Normalized Digital Frequency w');
ylabel('Magnitude');
title('Frequency Response of FIR LPF using Rectangular Window');

// Magnitude Response in dB
hzm_dB = 20 * log10(hzm);

subplot(2, 1, 2);
plot(2 * fr, hzm_dB);
xlabel('Normalized Digital Frequency W');
ylabel('Magnitude in dB');
title('Frequency Response of FIR LPF using Rectangular Window');
```


# OUTPUT: 
<img width="750" height="697" alt="WhatsApp Image 2026-09-02 at 1 38 50 PM" src="https://github.com/user-attachments/assets/2bee8f16-3697-470d-8e4a-bd4646d570b0" />
<img width="521" height="650" alt="WhatsApp Image 2026-09-02 at 1 39 06 PM" src="https://github.com/user-attachments/assets/f2e3ca87-cf88-4ab5-9433-439af95454cf" />

# RESULT: 

Thus design of low pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.


# AIM 2:
To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2 // Center Value 
for n = 1:M 
if (n ==alpha+1) 
hd(n)=1-Wc/ %pi ; 
else 
hd(n) =-sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
end 
end 
// Rectangular Window 
for n = 1:M 
W(n) =1; 
end 
//Windowing filter coefficients 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of  FIR LPF using Rectangular Window ') 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR HPF using Rectangular Window');
```

# OUTPUT: 
<img width="802" height="718" alt="WhatsApp Image 2026-09-02 at 1 55 44 PM" src="https://github.com/user-attachments/assets/7310fab3-bb87-4c05-8bea-2274f5ac7f79" />
<img width="511" height="642" alt="WhatsApp Image 2026-09-02 at 1 55 57 PM" src="https://github.com/user-attachments/assets/ca2f9a10-515f-4320-bce0-2d2293bf53d6" />




# RESULT: 
Thus design of HIGH pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.



# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 


# OUTPUT: 


# RESULT: 
Thus design of BAND pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 


# OUTPUT: 


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.
