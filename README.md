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

**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

**FULL ADDER**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
 
```
module EXP4FULLADDER(A,B,Cin,Sum,Carry);
input A,B,Cin;
output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=A&B|B&Cin|A&Cin;
endmodule
```
**FULL SUBTRACTOR**
```
module EXP4FULLSUBTRACTOR(A,B,Cin,Difference,Borrow);
input A,B,Cin;
output Difference,Borrow;
assign Difference=A^B^Cin;
assign Borrow=~A&B|B&Cin|~A&Cin;
endmodule
```

Developed by: Kruthika R 
RegisterNumber: 212225240075


**RTL Schematic**
**FULL ADDER**
<img width="1451" height="733" alt="image" src="https://github.com/user-attachments/assets/409c8784-c021-4a98-9e2c-819efde4ce10" />
**FULL SUBTRACTOR**
<img width="1399" height="703" alt="image" src="https://github.com/user-attachments/assets/72615894-2c36-4f10-953d-407fcf52f420" />


**Output Timing Waveform**
**FULL ADDER**
<img width="1347" height="687" alt="image" src="https://github.com/user-attachments/assets/589d790a-2f62-4f8f-9606-eb08ffa2500e" />
**FULL SUBTRACTOR**
<img width="1347" height="704" alt="image" src="https://github.com/user-attachments/assets/3c9ced3d-1a72-4d06-8ffc-8b1543ed8eb7" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



