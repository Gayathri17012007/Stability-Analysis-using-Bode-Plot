# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
~~~
num=[1];
den=[0.05 0.6 1 0];
sys=tf(num,den)
bode(sys)
grid on;
[gm pm wpc wgc]=margin(sys)
gmindB=20*log10(gm)
if (wpc>wgc)
    disp('stable')
elseif (wpc==wgc)
    disp('marginally stable')
else
    disp('unstable')
end
~~~

## Output:
<img width="1747" height="887" alt="Screenshot 2025-11-16 135010" src="https://github.com/user-attachments/assets/97598207-116e-459b-85c7-5d6fd8649d15" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12 dB.<br>
Phase Margin = 60 degree.<br>
Gain crossover frequency =  0.9070 rad/s.<br>
Phase crossover frequency =  4.4721 rad/s.<br>
The system is  Stable.<br>
