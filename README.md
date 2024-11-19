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

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Full Adder:**

![Screenshot 2024-11-19 184246](https://github.com/user-attachments/assets/59a65d7b-8a9e-4d57-bb55-ce0b3b128c78)

**Full Subtractor:**

![Screenshot 2024-11-19 184950](https://github.com/user-attachments/assets/5bf13873-e5c8-48f7-a694-c45df82802e4)

**Procedure**

1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

**Developed by: TAUQIR AHMED S**

**RegisterNumber: 24013512**

**Full Adder:**

module full_adder(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

**Full Subtractor:**

module full_subtractor(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~ a & b)| ( bin & (~ (a ^ b ))));

endmodule

**RTL Schematic**

**Full Adder:**

![Screenshot 2024-11-17 182616](https://github.com/user-attachments/assets/eb1af7fd-ec3e-40e3-b795-f8f91410ca06)

**Full Subtractor:**

![Screenshot 2024-11-17 183729](https://github.com/user-attachments/assets/074f3e27-b769-4928-8ea2-302b5df32ea3)


**Output Timing Waveform**

**Full Adder:**

![Screenshot 2024-11-17 183012](https://github.com/user-attachments/assets/b79c5a3a-8dea-41a4-8c4b-c934e866684d)

**Full Subtractor:**

![Screenshot 2024-11-17 184020](https://github.com/user-attachments/assets/9633bce6-7f63-4a80-ade0-24bce578a50d)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



