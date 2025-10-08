# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

FULL ADDDER

<img width="654" height="430" alt="image" src="https://github.com/user-attachments/assets/cf80cd7b-5c9a-4a76-ac0f-4618eb9242ea" />

FULL SUBTRACTOR 

<img width="438" height="393" alt="image" src="https://github.com/user-attachments/assets/4434a03c-27a2-4394-8066-8a552e4508fb" />



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**


Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

i)FULL ADDER

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule

**RTL Schematic**

FULL ADDDER :
<img width="1490" height="711" alt="Screenshot 2025-10-07 142141" src="https://github.com/user-attachments/assets/7dbb977d-80da-448f-a640-d03a7707d8b0" />


HALF SUBTRACTOR:
<img width="1471" height="558" alt="Screenshot 2025-10-07 143747" src="https://github.com/user-attachments/assets/5465297f-b738-48e3-b078-cfbaeb4950c0" />


**Output Timing Waveform**

FULL ADDER :

<img width="1919" height="453" alt="Screenshot 2025-10-07 143051" src="https://github.com/user-attachments/assets/4a80cb7b-3c4a-4819-9532-5a977eed4444" />


FULL SUBTRACTOR:

<img width="1910" height="416" alt="Screenshot 2025-10-07 144205" src="https://github.com/user-attachments/assets/f5112001-676b-4868-8e2a-b46048efa4af" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



