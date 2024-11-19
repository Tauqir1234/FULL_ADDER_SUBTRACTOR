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

**Full Adder:**

![Screenshot 2024-11-19 184246](https://github.com/user-attachments/assets/f55aa561-95f8-4b3e-a873-6657c399f3f5)

**Full Subtractor:**

![Screenshot 2024-11-19 184950](https://github.com/user-attachments/assets/95504035-2296-46c8-bdf9-55840398de5b)

**Procedure**

1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.


**Program:**
***
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: TAUQIR AHMED S

RegisterNumber:24013512
***
***
**Full Adder:**

module Full_Adder(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule
***
***
**Full Subtractor:**

module Full_Subtractor(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~ a & b)| ( bin & (~ (a ^ b ))));

endmodule
***
**RTL Schematic**

**Full Adder:**

![Screenshot 2024-11-17 182616](https://github.com/user-attachments/assets/49022992-7e5f-4092-b482-58f909d67096)

**Full Subtractor:**

![Screenshot 2024-11-17 183729](https://github.com/user-attachments/assets/f267ed43-400c-4838-8c74-50dee969d387)


**Output Timing Waveform**

**Full Adder:**

![Screenshot 2024-11-17 183012](https://github.com/user-attachments/assets/df01ac60-d159-4494-bdc3-ddfab0185b69)

**Full Subtractor:**

![Screenshot 2024-11-17 184020](https://github.com/user-attachments/assets/e2cc62c9-5820-4e05-8f5d-ce1ffa31e59b)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



