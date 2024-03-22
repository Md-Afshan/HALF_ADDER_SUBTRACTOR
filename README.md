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


![315920317-f054018f-219b-4b58-85b2-be728594c318](https://github.com/Md-Afshan/HALF_ADDER_SUBTRACTOR/assets/147140059/fcf53ce2-7b1d-4c26-b5e8-2e41d98b3608)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

**Half_adder**
```
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
 assign sum = a^b;
 assign carry = a & b;
endmodule
```

**Half_subtractor**
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule
```

Developed by: Muhammad Afshan A
RegisterNumber: 212223100035
*/

**RTL Schematic**
![315919812-b8fcda97-0438-4190-852b-a0028ff5adbe](https://github.com/Md-Afshan/HALF_ADDER_SUBTRACTOR/assets/147140059/c32ff23c-cfde-45e8-a032-9f18799998b6)

**Output/TIMING Waveform**

Half_adder
![315919606-18b3bcfe-6a65-4d24-8874-4420091953fa](https://github.com/Md-Afshan/HALF_ADDER_SUBTRACTOR/assets/147140059/cfe3b38b-962e-4ed6-b57c-599a6b32013e)

Half_subtractor
![315919503-fb1a88d1-5862-480f-983c-18c6c2639d66](https://github.com/Md-Afshan/HALF_ADDER_SUBTRACTOR/assets/147140059/da1e194f-de57-4cf9-90f2-8f187e3aa1bb)

**Result:**
The code is excecuted successfully.
