# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime
## Theory:
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor and Full Subtractor:
## Half Subtractor:
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor:
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure:
1. Use module projname(input,output) to start the Verilog programmming.
2. Assign inputs and outputs using the word input and output respectively.
3. Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
4. Use each output to represnt onre for differnce and the other for borrow.
5. End the verilog program using keyword endmodule.
## Program:

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: S Adithya Chowdary.
RegisterNumber: 212221230100.
## Half-Subtractor:
~~~
module sam(A,B,Difference,Borrow);
input A,B;
output Difference, Borrow;
wire x;
xor (Difference,A,B);
not (x,A);
and (Borrow,x,B);
endmodule
~~~
## Full-Subtractor:
~~~
module sam2(A,B,C,Diff,Borrow);
input A,B,C;
output Diff,Borrow;
wire p;
assign Diff = ((A^B)^C);
not(p,A);
assign Borrow = ((p&B)|(p&C)|(B&C));
endmodule
~~~
## Output:
## Half Subtractor:
## Truthtable:
![image](https://user-images.githubusercontent.com/93427248/196045175-b1393cbd-db1b-4535-b9db-f82c223289cf.png)
##  RTL realization:
![image](https://user-images.githubusercontent.com/93427248/196045192-47275229-5c46-455f-9d77-4a361b64ba0a.png)
## Timing diagram:
![image](https://user-images.githubusercontent.com/93427248/196045209-add29db5-f830-4b2e-b28a-f867f858a715.png)
## Full Subtractor:
## Truthtable:
![image](https://user-images.githubusercontent.com/93427248/196045256-1e33c7d5-269f-4cef-b5d6-0acc6d391740.png)
##  RTL realization:
![image](https://user-images.githubusercontent.com/93427248/196045282-c3d8d042-7f3e-4506-9a71-c96f5b91957c.png)
## Timing diagram:
![image](https://user-images.githubusercontent.com/93427248/196045306-1b806a0e-5d98-4f53-a076-abbd34cb4ba9.png)
## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
