# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
 Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. ###Using NAND gates NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
## Logic Diagram
## Procedure:
1.Create a project with required entities.
2.Create a module along with respective file name.
3.Run the respective programs for the given boolean equations.
4.Run the module and get the respective RTL outputs.
5.Create university program(VWF) for getting timing diagram.
6.Give the respective inputs for timing diagram and obtain the results.
## Program:

Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: KOWSALYA M
RegisterNumber:  212222230069
```
module ex02(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign F1=x1|x2|x3|x4|x5;
endmodule
```
## Output:
## RTL realization:
![image](https://github.com/Kowsalyasathya/Experiment--02-Implementation-of-combinational-logic-/assets/118671457/921fee7e-c452-49db-a034-3b5731ac6666)
## Truth table:
![R2](https://github.com/Kowsalyasathya/Experiment--02-Implementation-of-combinational-logic-/assets/118671457/7c1a0e81-4a43-4395-9949-53d8ef02e61b)
## Waveform:
![d2](https://github.com/Kowsalyasathya/Experiment--02-Implementation-of-combinational-logic-/assets/118671457/96d90011-ab1e-4539-af2d-4020c9c21a41)
## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
