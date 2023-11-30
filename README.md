# Name: POZHILAN V D
# Roll No: 23013442
# Experiment 03: Implementation of half subtractor and full subtractor circuit
# AIM
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.
#  Equipments Required
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
# Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor and Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)

Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

# Procedure
Connect the supply (+5V) to the circuit

Switch ON the main switch

If the output is 1, then the led glows.

# Program:
## Half Subtractor
module halfsubtractor(input x,y,output b,d);

assign d=x^y;

assign b=~x&y;

endmodule
## Full Subtractor
module fullsubtractor(input x,y,z, output d,b);

assign d=x^y^z;

assign b=~x&(y^z)|y&z;

endmodule



#  RTL realization
## Half Subtractor
![HALF RTL](https://github.com/POZHILANVD/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870498/c0526ddf-e5d2-4811-8276-2b7fc81eb3a7)


## Full Subtractor
![FULL RTL](https://github.com/POZHILANVD/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870498/fabc43db-3eab-4db6-b5a6-98764b3190ed)

# Truthtable
## Half Subtractor

![HALF TRUTH](https://github.com/POZHILANVD/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870498/5dc3d369-59c0-4dbb-a4bd-336630910cdc)

## Full Subtractor
![FULL TRUTH](https://github.com/POZHILANVD/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870498/dc12a6a5-bff3-4bba-aa1e-8d3863e49ce8)


# Timing diagram 
## Half Subtractor
![HALF TIME](https://github.com/POZHILANVD/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870498/f8abded1-a285-4fa1-9df0-b5fa901c5377)

## Full Subtractor
![FULL TIME](https://github.com/POZHILANVD/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/144870498/aa2342e2-126e-427b-8d31-9ad7c5ea3e84)


# Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
