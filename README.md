**NAME:T.SANJAI
REG NUMBER:24900899**

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

![image](https://github.com/user-attachments/assets/18d04ce4-3910-42f9-9d49-d2660d3b56e0)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

**HALF ADDER**

module half_adder_structural (

  input a,    // Input ‘a’

  input b,    // Input ‘b’

  output s,   // Output ‘s’ (Sum)

  output c    // Output ‘c’ (Carry)

);

xor gate_xor (s, a, b);  // XOR gate for sum

 and gate_and (c, a, b);  // AND gate for carry

endmodule

**HALF SUBTRACTOR**

module fullsub(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
wire w1,w2,w3,w4,w5,w6;
xor g1(diff,a,b,bin);
and g2(w4,w2,b);
and g3(w5,w1,b);
and g4(w6,b,bin);
or g5(borr,w4,w5,w6);
endmodule




**RTL Schematic**

**HALF ADDER**

![image](https://github.com/user-attachments/assets/6b5a7a81-5d04-4421-9862-0c671c22d06a)

**HALF SUBTRACTOR**

![image](https://github.com/user-attachments/assets/a6ca9520-19cd-44e9-a874-6fc1f9479364)


**Output/TIMING Waveform**


**HALF ADDER**

![Screenshot 2024-11-21 113052](https://github.com/user-attachments/assets/9ad0ff90-08a0-4e35-96ad-5af6297e8439)

**HALF SUBTRACTOR**

![image](https://github.com/user-attachments/assets/c19040fa-ec6a-4140-ae60-9eaff846831d)



**Result:**
Thus we learned to design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

