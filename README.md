# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

## **AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## **Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## **Full Adder and Full Subtractor**

## **Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

## **Figure -1 FULL ADDER**

## **Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## **Truthtable**
### ![fa (2)](https://github.com/user-attachments/assets/2c6012a2-78e0-4e3f-9006-d81c4b921d03)
### ![fs (2)](https://github.com/user-attachments/assets/48d0d8a0-a6d2-4985-80ff-d8380d45e9dc)
 
## **Procedure**
1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.



## **Program:**
## Full Adder:
```
module fa(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule
```
## Full Subtractor:
```
module fs(df,bo,a,b,bin);
input a,b,bin;
output df,bo;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
``` 
### Developed by:Mahajanani.R
### RegisterNumber:24003555


## **RTL Schematic**
### ![full adder](https://github.com/user-attachments/assets/d658d474-dfb5-4b17-8c88-8c813cbeb154)
### ![full subtractor](https://github.com/user-attachments/assets/ba471ddd-7062-40c7-99f2-bab60f29df15)

## **Waveform**
### ![fa](https://github.com/user-attachments/assets/f00e5a63-200e-4c39-8a14-26dc73aa8d15)
### ![fs](https://github.com/user-attachments/assets/ac3d259b-9732-42c4-8b81-81b15edb003d)

## **Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
