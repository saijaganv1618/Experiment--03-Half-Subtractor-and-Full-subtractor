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
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Jagan a
RegisterNumber:  212221230037
HALF SUBTRACTOR:
module halfsub(a,b,diff,borrow);
input a,b;
output diff,borrow;
wire x;
xor(diff,a,b);
not(x,a);
and(borrow,x,b);
endmodule

FULL SUBTRACTOR:
module fullsub(a,b,c,diff,borrow);
input a,b,c;
output borrow,diff;
wire an,q,r,s,t,cn,u;
not(an,a);
not(cn,c);
xor(q,a,b);
xor(diff,q,c);
and(s,a,b);
and(t,q,cn);
or(borrow,s,t);
endmodule 
*/

Half subtractor truth table:

![ha tt](https://user-images.githubusercontent.com/59290560/167336633-faa2a0a9-65d5-4c0a-a554-52554e848e12.png)



Full subtractor truth table:
![fs tt](https://user-images.githubusercontent.com/59290560/167336667-dc12d0f8-15e4-4594-a7ef-314da17df4f7.png)




RTL realization Output:

Half subtractor
![rtl ha](https://user-images.githubusercontent.com/59290560/167336680-d08b0a82-68c6-4574-8b81-5b304eb992d3.png)



Full subtractor:
![rtl fa](https://user-images.githubusercontent.com/59290560/167336690-c1de5449-4027-4f2b-80a0-41ad4c9509e7.png)
Timing Diagram

Half subtractor:
![tt ha](https://user-images.githubusercontent.com/59290560/167336715-06cded5e-c995-41bf-8d09-6ecf1677ebd3.png)



Full subtractor:
![fa tt](https://user-images.githubusercontent.com/59290560/167336734-26bbde42-2acd-408b-8f10-25372b7d5d6c.png)


Result: 
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
