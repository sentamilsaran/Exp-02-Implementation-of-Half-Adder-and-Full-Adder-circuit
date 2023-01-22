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
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: sentamilsaran S
RegisterNumber: 22008684 
*/
Half adder:

module add(a,b,sum,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule

Full adder:

module fulladd(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum = ((a^b)^c);

assign carry = ((a&b)|(b&c)|(c&a));

endmodule

Logic symbol & Truthtable
RTL realization
![image](https://user-images.githubusercontent.com/123304969/213918177-d49965d9-951b-4046-bb78-d4f3fb720db2.png)
![image](https://user-images.githubusercontent.com/123304969/213918187-2a93b2a7-da85-4577-b5aa-81612e13fed4.png)

### Output:
### RTL
### TIMING DIAGRAM
![image](https://user-images.githubusercontent.com/123304969/213918202-bde4f005-394c-4b09-8e3d-1cab25f866c1.png)
![image](https://user-images.githubusercontent.com/123304969/213918212-f5cad3f1-c9fe-4534-b031-fa4003075cf0.png)


### TRUTH TABLE 
![image](https://user-images.githubusercontent.com/123304969/213918220-04ad0eee-b3b3-4c36-93d2-0cca5b1dd16f.png)
![image](https://user-images.githubusercontent.com/123304969/213918228-4b99b39d-c3ad-4d5b-ad4a-4b0cde23bf17.png)

### Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
