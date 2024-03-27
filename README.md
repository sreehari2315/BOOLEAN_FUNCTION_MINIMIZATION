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

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: SREE HARI K

RegisterNumber: 212223230212
~~~

//Program to compute the function f1=a'b'c'd'+ac'd'+b'cd'+a'bcd+bc'd
//f2=xy'z+x'y'z+w'xy+wx'y+wxy
// simplify the logic using Boolean minimization/k map 
//compute f2 and write verilog code for f2 as like f1
module BMf1f2(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
//type code for f2 as like f1
not(ydash,y);
and(s,x,y);
and(t,ydash,z);
and(u,w,y);
or(f2,s,t,u);
endmodule

~~~
![316274720-6d15f315-f552-4271-84cc-c88ea2047317](https://github.com/sreehari2315/BOOLEAN_FUNCTION_MINIMIZATION/assets/139331590/bac7ebc6-448c-4f30-875a-8b0033449fe3)


**RTL realization**
![316248152-de44cdf3-076c-42a4-aa29-a6ac23ee33b3](https://github.com/sreehari2315/BOOLEAN_FUNCTION_MINIMIZATION/assets/139331590/fb55e87b-8882-4039-89d7-5f593ddd39e3)



**Output:**
![316248169-8d171afc-ba93-4ca8-a618-7a115f25cbe4](https://github.com/sreehari2315/BOOLEAN_FUNCTION_MINIMIZATION/assets/139331590/95647006-c469-4f5e-ac26-3320325d2526)


**Result:**

Thus,the given logic functions are implemented using and their operations are verified using Verilog programming.

