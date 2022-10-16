# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: G Jayanth.
RegisterNumber: 212221230030.
```
```
## HALF ADDER:

module Adder (a,b,sum,carry);
input a,b;
output sum,carry;
xor (sum,a,b);
and (carry,a,b);
endmodule

## FULL ADDER:

module FullAdder (a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
Logic symbol & Truthtable
RTL realization

## Output:
### Logic symbol & Truthtable:
#### HALF ADDER :
![1a](https://user-images.githubusercontent.com/93427345/196041504-3b0b47e8-8461-4ecb-b408-1ca2db78d568.png)

#### FULL ADDER :
![1b](https://user-images.githubusercontent.com/93427345/196041513-426a78fd-ffe7-4e7c-a131-f4ebc9f4ee68.png)

### RTL
#### HALF ADDER :
![1c](https://user-images.githubusercontent.com/93427345/196041580-ab421444-134c-40d2-8762-d3621f9a21ae.png)

#### FULL ADDER :
![1d](https://user-images.githubusercontent.com/93427345/196041587-c1f5a504-442a-420a-b19b-29fea1da5c60.png)

### TIMING DIAGRAM
#### HALF ADDER :
![1e](https://user-images.githubusercontent.com/93427345/196041703-1602328b-ce28-4d0b-b68b-10d2093bedee.png)

#### FULL ADDER :
![1](https://user-images.githubusercontent.com/93427345/196041707-fabe4697-8f78-49f9-bc26-edd29305c3c0.png)

#### TRUTH TABLE 
![1f](https://user-images.githubusercontent.com/93427345/196041715-4798d643-240a-4f42-beff-ba28418d8501.png)

## Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
