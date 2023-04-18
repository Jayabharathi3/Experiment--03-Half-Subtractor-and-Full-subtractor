# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
```
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: JAYABHARATHI.S
RegisterNumber:  212222100013

HALF SUBTRACTOR  

module HS(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=(~a&b);
endmodule  


FULL SUBTRACTOR  

module FS(a,b,c,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b^c);
assign borr=(~a&(b^c)|(b&c));
endmodule  
*/
```

## Output:

## Truthtable

HALF SUBTRACTOR 

![image](https://user-images.githubusercontent.com/120367796/232836275-92dd9f57-eff3-47f5-9582-130af885bce1.png)

FULL SUBTRACTOR


![image](https://user-images.githubusercontent.com/120367796/232836580-f225c66b-96e6-415f-b0ce-975cde621b25.png)


##  RTL realization

HALF SUBTRACTOR 

![image](https://user-images.githubusercontent.com/120367796/232836847-95636ea9-46e9-4e49-ba71-3bc6c6277d2f.png)

FULL SUBTRACTOR


![image](https://user-images.githubusercontent.com/120367796/232837093-ad72dcac-99ab-49c4-9ed5-5e8a91337c06.png)


## Timing diagram 

HALF SUBTRACTOR 

![image](https://user-images.githubusercontent.com/120367796/232837183-c8c754e3-d019-4866-8290-efb9be0118de.png)


FULL SUBTRACTOR

![image](https://user-images.githubusercontent.com/120367796/232837293-e9b471ac-8e6a-47a0-a05c-61347992ad26.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
