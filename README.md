# Experiment--04-Implementation-of-combinational-logic-using-universal-gates-
 ## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.
F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate


## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
 
 
 
 


## Procedure
1.Create a project with required entities.
2.Create a module along with respective file name.
3.Run the respective programs for the given boolean equations.
4.Run the module and get the respective RTL outputs.
5.Create university program(VWF) for getting timing diagram.
6.Give the respective inputs for timing diagram and obtain the result
## Program:
Program to design a Implementation of combinational logic using universal gates-  and verify its truth table in quartus using Verilog programming.
Developed by: kathirveL.A
RegisterNumber:  212221230047

-> F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' USING NAND GATE

module ex04(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P = C&(~B)&(~A);
assign Q = D&(~C)&(~A);
assign R = (~C)&B&(~A);
assign F = (~P&~Q&~R);
endmodule

-> F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' USING NOR GATE

module ex41(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = C&(~B)&A;
assign Q = D&(~C)&A;
assign R = C&(~B)&A;
assign S = ~(P|Q|R);
not(F,S);
endmodule
*/

## Output:

IMPLEMENTATION OF GIVEN LOGIC FUNCTION USING NAND GATE:


## Truthtable

![image](https://user-images.githubusercontent.com/94911373/167337013-9226cbf0-c208-4458-8f0f-0a09ae7707a2.png)




##  RTL realization

![image](https://user-images.githubusercontent.com/94911373/167337043-4ad38faa-bbe9-4fef-a413-93ea0096b0d7.png)



## Timing diagram 

![image](https://user-images.githubusercontent.com/94911373/167337084-2882f3ca-5067-4d71-9e7f-3427ac4bcdbf.png)


## Result:

The given logic function is implemented using NAND and NOR gates and it is verified successfully in Quartus using Verilog programming.


 
