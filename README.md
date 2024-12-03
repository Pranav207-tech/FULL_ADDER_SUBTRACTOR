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

![WhatsApp Image 2024-12-03 at 13 46 07_621d657b](https://github.com/user-attachments/assets/42324503-630d-4d78-bf7d-0b48278b7c3c)

![WhatsApp Image 2024-12-03 at 13 47 15_1d417e92](https://github.com/user-attachments/assets/202d394f-7f12-40de-8e5d-c46052e4e62d)


**Procedure**

1. A combinational circuit that performs the addition of 2 bits is calledthe half adder
2. A half adder has 2 inputs and 2 outputs. The output variables producethe sum and carry
3. In full adder two input variables A and B represents the twosignificant bits to be added. The third input C represents the carry fromthe previous lower significant position
4. A half sub tractor is a combinational circuit that subtracts two bits. Ithas two inputs and two outputs. The output variables producedifference and borrow.
5. A full subtractor is a combinational circuit that performs subtraction between two bits taking into account one mayhave been borrowed by a lower significant stage

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
Developed by: Pranav K
RegisterNumber: 24900545
```
```
i)FULL ADDER

module fa(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
```
ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```
**RTL Schematic**

![LOGIC GATE](https://github.com/user-attachments/assets/baf33e95-ed89-481f-abd5-6c3e7c2d0d58)

![LOGIC GATE](https://github.com/user-attachments/assets/f60eacfa-7437-46e7-aa38-152ccb88185f)

**Output Timing Waveform**

![Screenshot (183)](https://github.com/user-attachments/assets/f56c2653-dee1-4fdf-ae58-5998329103ad)

![Screenshot (184)](https://github.com/user-attachments/assets/efa58bac-b580-4cb4-a89d-cb4a624e45d2)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



