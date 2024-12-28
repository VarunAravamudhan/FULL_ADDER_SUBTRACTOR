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

**Truth Table**

![image](https://github.com/user-attachments/assets/52815c22-b6e7-4c1c-81b7-5ab2b16e6396)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin

Borrow out = A'Bin + A'B + BBin

**Truth Table**

![image](https://github.com/user-attachments/assets/4af36354-b86a-43ef-9e91-75eb18871645)

**Procedure**

  1. Type the program in Quartus software.

  2. Compile and run the program.

  3. Generate the RTL schematic and save the logic diagram.

  4. Create nodes for inputs and outputs to generate the timing diagram.

  5. For different input combinations generate the timing diagram.

**Program:**

Designed By: Varun A

Register Number : 24900420

Full Adder

```
module Lab4Fa (A, B, Cin, sum, car) ;
input A,B,Cin;
output sum, car;
assign sum = A ^ B ^ Cin;
assign car = ( (A & B) | ( (A ^ B) &Cin) ) ;
endmodule
```

Full Subtractor

```
module Lab4Fs (A, B, Bin, diff, bor) ;
input A, B, Bin;
output diff, bor;
assign diff = A ^ B ^ Bin;
assign bor = ((~A & B) | (~ (A ^ B) & Bin) ) ;
endmodule
```

**RTL Schematic**

Full Adder

![Screenshot (57)](https://github.com/user-attachments/assets/404070cb-586b-4a9f-8689-4af56b974804)

Full Subtractor

![Screenshot (60)](https://github.com/user-attachments/assets/2a666866-8c75-4ab0-9384-f92f44b9caf8)


**Output Timing Waveform**

Full Adder

![Screenshot (58)](https://github.com/user-attachments/assets/6d9e7146-410d-45b2-aa9c-2fc345d5feed)

Full Subtractor

![Screenshot (61)](https://github.com/user-attachments/assets/83e45b6b-2f84-432a-a36b-fc718dc0ef25)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



