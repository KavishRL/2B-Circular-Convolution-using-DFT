# EXPT 2B:CIRCULAR-CONVOLUTION-USING-DFT
## AIM
To perform and verify circular convolution operation of two given sequences using SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM:
```

clc;
clear;
close
x1 = [1 2 3 4];
x2 = [4 3 2 1];
N = max(length(x1), length(x2));
x1 = [x1 zeros(1, N-length(x1))];
x2 = [x2 zeros(1, N-length(x2))];
X1 = fft(x1, -1);
X2 = fft(x2, -1);
Y = X1 .* X2;
y = fft(Y, 1);
disp("Circular Convolution Result:");
disp(real(y));
```
## CIRCULAR CONVOLUTION

<img width="686" height="958" alt="image" src="https://github.com/user-attachments/assets/21da4d62-5463-4e3d-81b2-92639ed63254" />



### CALCULATIONS:
<img width="1080" height="1366" alt="image" src="https://github.com/user-attachments/assets/dbc1e901-c28e-4ca6-86d7-eaf926a82e0a" />

### SAMPLE OUTPUT:
<img width="1892" height="1022" alt="image" src="https://github.com/user-attachments/assets/944a528d-4780-4d7a-870b-5c98a3ab048b" />


## RESULT:
Thus, the circular convolution of the two given sequences were performed and its result was verified.
