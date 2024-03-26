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


## *Program:*
```Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
Developed by: K SANTHAN KUMAR
RegisterNumber: 212223240065
```

```
module experiment(
    input a, b, c, d, w, x, y, z,
    output f1, f2
);

wire adash, bdash, cdash, ddash, ydash, zdash, wdash;
not(adash, a);
not(bdash, b);
not(cdash, c);
not(ddash, d);
not(ydash, y);
not(zdash, z);
not(wdash, w);

wire p, q, r, s, t, u, term1, term2, term3;

and(p, bdash, ddash);
and(q, adash, b, d);
and(r, a, b, cdash);
and(term1, ydash, z);
and(term2, x, y);
and(term3, w, y);

or(f1, p, q, r);
or(f2, term1, term2, term3);

endmodule
```

<img width="960" alt="image" src="https://github.com/SANTHAN-2006/BOOLEAN_FUNCTION_MINIMIZATION/assets/80164014/ac5e312c-e7be-4f99-a24f-2e4d7d67977d">

## RTL Realization :
![image](https://github.com/SANTHAN-2006/BOOLEAN_FUNCTION_MINIMIZATION/assets/80164014/974a7ddc-71c0-401b-829e-9e318ff0f71f)

## *Output:*
<img width="639" alt="image" src="https://github.com/SANTHAN-2006/BOOLEAN_FUNCTION_MINIMIZATION/assets/80164014/f19332b1-d26d-4375-9245-5c88df091248">

## TRUTH TABLE :
![image](https://github.com/SANTHAN-2006/BOOLEAN_FUNCTION_MINIMIZATION/assets/80164014/c84edbd0-feb7-4900-95f8-e1545ee77b8f)

## *Result:*

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

