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

1. Connect the supply (+5V) to the circuit
2. Switch ON the main switch
3. If the output is 1, then the led glows.
### Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Evangelin.S
RegisterNumber:  212221230025
*/
HALF ADDER

module Adder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 

FULL ADDER

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule

### Output:
## Half Adder :
### Logic Symbol:
![image](https://user-images.githubusercontent.com/94219798/166143129-491db209-acc1-48d4-8749-8acdf418b735.png)

### RTL Realization:
![image](https://user-images.githubusercontent.com/94219798/166143157-50f7143d-8842-4301-b2c2-071deafde956.png)

### TRUTH TABLE 
![image](https://user-images.githubusercontent.com/94219798/166143172-63ab4593-681f-49b9-b981-6e1dbca9d554.png)

### TIMING DIAGRAM
![image](https://user-images.githubusercontent.com/94219798/166143263-d21f1d06-e36d-40e9-bb51-2dc9b3ca417e.png)

## Full Adder :
### Logic Symbol:
![image](https://user-images.githubusercontent.com/94219798/166143311-61697e35-50cc-44c7-a04d-1e8bb2974ff4.png)
### RTL Realization:
![image](https://user-images.githubusercontent.com/94219798/166143316-992c165a-2291-487f-8aac-5b20cce32386.png)
### Truthtable:
![image](https://user-images.githubusercontent.com/94219798/166143326-336a0dfd-604e-498a-98a2-5bde6076dc20.png)
### Timing Diagram:
![image](https://user-images.githubusercontent.com/94219798/166143336-e51cccbc-d332-4868-a056-15adef5c84d7.png)


### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
