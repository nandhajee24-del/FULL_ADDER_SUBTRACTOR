## FULL_ADDER_SUBTRACTOR
## Developed By: NANDHA A
## Reg. No: 212225040271
Implementation-of-Full-Adder-and-Full-subtractor-circuit

## AIM:
To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Full Adder and Full Subtractor

## Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

## Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

**Figure -2 FULL SUBTRACTOR**

## Truthtable:
<img width="1166" height="678" alt="ex3 3 3" src="https://github.com/user-attachments/assets/e8b65d8f-be83-4d8b-b945-d051e407ecaf" />


## Procedure:

Write the detailed procedure here 1.Create a new project in Quartus II and open a Block Diagram/Schematic file. 2.Place logic symbols and connect inputs A, B, Cin and outputs Sum, Cout. 3.Implement logic: Sum = A ⊕ B ⊕ Cin, Cout = AB + Cin(A ⊕ B). 4.Compile and simulate to verify the output waveform.

## Program:
```
module full_add_sub(a,b,cin,sum,diff,carry,borrow);
input a,b,cin;
output sum,diff,carry,borrow;
assign sum = (a^b^cin);
assign carry = (a&b)|(a&cin)|(b&cin);
assign diff = (a^b^cin);
assign borrow = (~a&cin)|(~a&b)|(b&cin);
endmodule 
```

## RTL Schematic:
<img width="1920" height="1080" alt="ex3 3 1" src="https://github.com/user-attachments/assets/d57ebf46-b6d2-4ba3-b888-ab58fb7a61b9" />


## Output Timing Waveform:
<img width="1920" height="1080" alt="ex3 3 2" src="https://github.com/user-attachments/assets/510aa10d-a627-4195-9a4f-082f3853fd10" />


## Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
