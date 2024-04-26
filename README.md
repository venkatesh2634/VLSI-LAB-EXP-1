# VLSI-LAB-EXPERIMENTS

# AIM:

To simulate and synthesis Logic Gates,Adders and Subtractor using vivado 2023.2.

# APPARATUS REQUIRED:

vivado 2023.2

# PROCEDURE:

STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the run simulation adn then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table. Logic Diagram :

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/69e44845-a84e-4f34-a203-71efa1542e8c)

# Half Adder:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/42e25186-a65a-48e3-93cc-1475fd0b2b82)

# Full adder:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/efbe3ae5-fb02-456a-80c4-a056faa981cf)

# Half Subtractor:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/333bd2d7-e5c3-4ed5-9a51-4d0c06ad992a)

# Full Subtractor:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/a9f30837-eaa9-4e32-a097-f0ca22fc343c)

# 8 Bit Ripple Carry Adder:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/ee910397-df7c-40cf-9ab7-f017dfc8fe33)

# VERILOG CODE:

LOGIC GATES: module logic(a,b,andgate,orgate,xorgate,nandgate,norgate,xnorgate,notgate );

input a,b;

output andgate,orgate,xorgate,nandgate,norgate,xnorgate,notgate;

and(andgate,a,b);

or(orgate,a,b);

xor(xorgate,a,b);

nand(nandgate,a,b);

nor(norgate,a,b);

xnor(xnorgate,a,b);

not(notgate,a);

endmodule

# HALF ADDER:
module HalfAdder(a,b,sum,carry);

input a,b;

output sum,carry;

xor (sum,a,b);

and (carry,a,b);

endmodule

# FULL ADDER:
module FA(a,b,cin,sum,cout);

input a,b,cin;

output sum,cout;

wire w1,w2,w3;

xor g1(w1,a,b);

and g2(w2,w1,cin);

and g3(w3,a,b);

xor g4(sum,w1,cin);

or g5(cout,w2,w3);

endmodule

# FULL SUBTRACTOR:
module full_sub(a,b,bin,diff,borrow);

input a,b,bin;

output diff,borrow;

wire w1,w2,w3;

xor g1(w1,a,bin);

and g2(w2,~a,b);

xor g3(diff,w1,bin);

or g4(borrow,w2,w3);

and g5(w3,~w1,bin);

endmodule

# HALF SUBTRACTOR:
module halfsubtractor(a,b,diff,borrow);

input a,b;

output diff,borrow;

xor g1(diff,a,b);

and g2(borrow,~a,b);

endmodule

# 8 BIT RIPPLE CARRY ADDER:
module fa(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum = a^b^c;

assign carry=(a&b)|(b&c)|(c&a);

endmodule

module rca(a,b,cin,sum,cout);

input [7:0]a,b; input cin;

output [7:0]sum;

output cout;

wire c1,c2,c3,c4,c5,c6,c7;

fa fa1(a[0],b[0],cin,sum[0],c1);

fa fa2(a[1],b[1],c1,sum[1],c2);

fa fa3(a[2],b[2],c2,sum[2],c3);

fa fa4(a[3],b[3],c3,sum[3],c4);

fa fa5(a[4],b[4],c4,sum[4],c5);

fa fa6(a[5],b[5],c5,sum[5],c6);

fa fa7(a[6],b[6],c6,sum[6],c7);

fa fa8(a[7],b[7],c7,sum[7],cout);

endmodule

# OUTPUT:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/b73ee1b3-5f0c-46f4-93f7-03e4acd796d9)

# HALF ADDER:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/03aa578e-627f-4b54-b278-d44659658099)

# FULL ADDER:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/b86834cc-7903-403a-957d-095f99aad69d)

# HALF SUBTRACTOR:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/f138f93e-fded-4f93-86ff-669313c66efe)

# FULL SUBTRACTOR:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/b4c0bfaf-1d92-49e0-bc58-064e28a5b91d)

# 8 BIT RIPPLE CARRY ADDER:

![image](https://github.com/venkatesh2634/VLSI-LAB-EXP-1/assets/168212451/6a3fefc8-43b6-4c0c-a3dc-3382672640ac)

# RESULT:
Thus the simulation and synthesis of Logic Gates,Adders and Subtractors using vivado has been sucessfully executed and verified .




















