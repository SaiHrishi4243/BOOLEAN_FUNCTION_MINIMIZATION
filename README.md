# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: Sai Hrishi M   RegisterNumber: 24900846  */

```
module Bool(a,b,c,d,w,x,y,z,o1,o2,o3,o4,o5,o6,o7,o8,o9,o10,f1,f2);
input a,b,c,d,w,x,y,z;
output o1,o2,o3,o4,o5,o6,o7,o8,o9,o10,f1,f2;
assign o1=~(a&b&c&d);
assign o2=a&~(c&d);
assign o3=c&~(b&d);
assign o4=(a&b&c)&~a;
assign o5=(b&d)&~c;
assign o6=(x&z)&~y;
assign o7=z&~(x&y);
assign o8=(x&y)&~w;
assign o9=(w&y)&~x;
assign o10=w&x&y;
assign f1=o1|o2|o3|o4|o5;
assign f2=o6|o7|o8|o9|o10;
endmodule
```

**RTL realization**

![RTL REALIZATION](https://github.com/user-attachments/assets/4b8110e0-cfbc-4b0e-babb-86048cd2df91)

**Output:**

![Truth table 3](https://github.com/user-attachments/assets/e241dfc6-c8b8-4282-a591-544ad0fd0f48)

**RTL**

![rtl (2)](https://github.com/user-attachments/assets/7b218dcf-a128-44c6-bf51-6480dbf25daf)

**Timing Diagram**

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

