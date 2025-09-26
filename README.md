# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
Developed by: Sandhiya M
RegisterNumber: 212224220086

Half Adder:
module halfadd(a,b,s,c);
input a,b;
output s,c;
xor G1(s,a,b);
and G2(c,a,b);
endmodule

Half Subractor:
module halfsubtractor(x,y,d,b);
input x,y;
output d,b;
wire w1;
xor g1(d,x,y);
not g2(w1,x);
and g3(b,w1,y);
endmodule

```

**RTL Schematic**

Hald Adder:

<img width="798" height="443" alt="half add img" src="https://github.com/user-attachments/assets/51f87156-5eab-4328-8908-6f04cf11388d" />

Half Subractor:

<img width="911" height="437" alt="halfsub" src="https://github.com/user-attachments/assets/9e9f346d-4bda-4943-8ab1-f7c38ff7fe8c" />


**Output/TIMING Waveform**

Half Adder:

<img width="1910" height="522" alt="half add waveform" src="https://github.com/user-attachments/assets/cdb0288e-3919-4f75-8eb8-7d20288e220b" />

Half Subractor:

<img width="1906" height="598" alt="halfsub img" src="https://github.com/user-attachments/assets/1b2bae11-b521-4eb4-a7b5-65c42be881f5" />


**Result:**

Implementation-of-Half-Adder-and-Half Subtractor-circuit was successfully done.
