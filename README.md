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


(i)FULL ADDER

![fatt](https://github.com/user-attachments/assets/ac37e8d4-0a10-47f3-a83a-a4aee31cd9c7)

(ii)FULL SUBTRACTOR

![fstt](https://github.com/user-attachments/assets/6f43b205-9187-4d76-a3c6-4094e6b291a4)


**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.



**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: A Praneya

RegisterNumber:24900343
*/
(i)FULL ADDER
```
module faexp(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
(ii)FULL SUBTRACTOR
```  
module fsexp(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```



**RTL Schematic**

(i)FULL ADDER

![fass](https://github.com/user-attachments/assets/28f2979d-10a1-4c33-903c-a83918388567)

(ii)FULL SUBTRACTOR

![fsss](https://github.com/user-attachments/assets/0beda55a-4e5b-43dc-8f9b-7667e0bb1ee1)

**Output Timing Waveform**

(i)FULL ADDER

![fawss](https://github.com/user-attachments/assets/4023f45e-a875-4d59-8e52-c58183c75592)

(ii)FULL SUBTRACTOR
![fswss](https://github.com/user-attachments/assets/8d1aad19-6ebc-41fa-8052-275da7aebcd4)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



