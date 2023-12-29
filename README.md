# Developed by: Shaik Samreen
# RegisterNumber: 23013412

# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


 
## Theory
 A combinational circuit is a circuit in which the output depends on the present combination of inputs. Combinational circuits are made up of logic gates. The output of each logic gate is determined by its logic function. Combinational circuits can be made using various logic gates, such as AND gates, OR gates, and NOT gates.
## Procedure
1.reate a New Project: Open Quartus and create a new project by selecting "File" > "New Project Wizard." Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2.Create a New Design File: Once the project is created, right-click on the project name in the Project Navigator and select "Add New File." Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3.Write the Combinational Logic Code: Open the newly created Verilog or VHDL file and write the code for your combinational logic.

4.Compile the Project: To compile the project, click on "Processing" > "Start Compilation" in the menu. Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5.Analyze and Fix Errors:* If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window. Review and fix any issues in your code if necessary. View the RTL diagram.

6.Verification: Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF". Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All. Give the Input Combinations according to the Truth Table amd then simulate the Output waveform
## Program:
```
module exp2de(A,B,C,D,F1);
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
## RTL realization
![285508978-117e5d3b-33bb-4f4b-b712-1f1b7d0e0a64](https://github.com/samreen-sk/Experiment--02-Implementation-of-combinational-logic-/assets/149347632/a79759f2-540c-4af1-a4a7-5516da83611e)

## Truth Table
![285499286-82d469bc-98e8-45f5-a969-42fa063b435c](https://github.com/samreen-sk/Experiment--02-Implementation-of-combinational-logic-/assets/149347632/6baaf27a-7364-49ee-a843-1f233a3f1c94)

## Timing Diagram
![285510363-b3cee5d5-b46a-4324-aa30-46766f306eb1](https://github.com/samreen-sk/Experiment--02-Implementation-of-combinational-logic-/assets/149347632/40c5994d-fc61-4f37-b341-515391b113bb)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
