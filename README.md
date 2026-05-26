# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB
AIM: To write a program for mean, variance and cross correlation in SCILAB and verify the output.

COMPONENTS REQUIRED:

• Computer with i3 Processor 
• SCI LAB

ALGORITHM:

1)Define the Function: Specify the function you want to simulate. For example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2)Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3)Evaluate the Function: Compute the function values at each of these sample points.
4)Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5)Display Results: Output the computed mean variance and Cross Correlation PROCEDURE
• Refer Algorithms and write code for the experiment. 
• Open SCILAB in System • Type your code in New Editor 
• Save the file
• Execute the code 
• If any Error, correct it in code and execute again
• Verify the generated results

Program :
Mean -
```
clear;
clc;
function z = f(x)
    z = x * 4 * (1 - x)^2;
endfunction
function z = g(y)
    z = y * 4 * (1 - y)^2;
endfunction
a = 0;
b = 1;
EX = intg(a, b, f);
EY = intg(a, b, g);
disp(EX, "i) Mean of X =");
disp(EY, "Mean of Y =");

```
Variance - 
```
clear;
clc;
function z = f(x)
    z = x * 4 * (1 - x)^2;
endfunction
function z = g(x)
    z = x^2 * 4 * (1 - x)^2;
endfunction
function z = h(y)
    z = y * 4 * (1 - y)^2;
endfunction
function z = k(y)
    z = y^2 * 4 * (1 - y)^2;
endfunction
a = 0;
b = 1;
EX = intg(a, b, f);
EX2 = intg(a, b, g);
VX = EX2 - (EX)^2;
EY = intg(a, b, h);
EY2 = intg(a, b, k);
VY = EY2 - (EY)^2;
disp(VX, "ii) Variance of X =");
disp(VY, "Variance of Y =");

```

Cross Correlation -
```
clear;
clc;
x = input("Type in the reference sequence = ");
y = input("Type in the second sequence = ");
n1 = max(size(y)) - 1;
n2 = max(size(x)) - 1;
r = corr(x, y, n1);
disp(r, "Cross Correlation Sequence = ");
plot2d3('gnn', r);
xtitle("Cross Correlation", "Lag", "Amplitude");

```

Output:
i) Mean of X =  Mean of Y = 

ii) Variance of X = Variance of Y =

Cross Correlation Type in the reference sequence = [1 2 3 4 5 6 7 8]

Type in the second sequence = [2 1 3 5 6 3 5 9]

Calculation:

Result:
