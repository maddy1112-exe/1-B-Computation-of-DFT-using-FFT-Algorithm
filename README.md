# EXPT 1b: Computation-of-DFT-using-FFT-ALGORITHM

## AIM
To perform and verify DFT using FFT-ALGORITHM by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT FFT-ALGORITHM

clc;
clear;
clf;

xn = [1,2,3,4,4,3,2,1];

N = length(xn);
n = 0:N-1;
j = %i;

Xk = zeros(1, N);

// Direct DFT calculation
for k = 0:N-1
    for r = 0:N-1
        Xk(k+1) = Xk(k+1) + ...
            xn(r+1)*exp(-j*2*%pi*k*r/N);
    end
end

disp("DFT output:");
disp(Xk);

K = 0:N-1;
magnitude = abs(Xk);
phase = atan(imag(Xk), real(Xk));

subplot(3,1,1);
plot2d3(n, xn);
xtitle("Input Sequence", "n", "x(n)");

subplot(3,1,2);
plot2d3(K, magnitude);
xtitle("Magnitude Spectrum", "k", "|X(k)|");

subplot(3,1,3);
plot2d3(K, phase);
xtitle("Phase Spectrum", "k", "Phase (radians)")

### CALCULATIONS:
<br><img width="1280" height="1254" alt="image" src="https://github.com/user-attachments/assets/000ff9e3-f978-4373-93f4-026b1f8269f5" />

<br><img width="771" height="1280" alt="image" src="https://github.com/user-attachments/assets/a3b71471-c852-48af-9cb6-6f698197ea57" />

<br><img width="773" height="1280" alt="image" src="https://github.com/user-attachments/assets/ef5b03e3-e188-431a-9c64-0db36398d5d9" />

<br><img width="801" height="1280" alt="image" src="https://github.com/user-attachments/assets/f862f35a-c337-4fdd-addc-7b4a89693e99" />

<br>
### SAMPLE OUTPUT:
<br>
<br>
<br><img width="1599" height="1513" alt="image" src="https://github.com/user-attachments/assets/1034f445-c3ab-42f1-be3e-3c0e3a89235c" />

<br>



## RESULT:
Thus,  DFT using FFT-ALGORITHM for two given sequences were performed and its result was verified.

