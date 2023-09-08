# NAME: KANCHARLA NARMADHA
# REGISTER NUMBER: 212222110016

# Experiment 04 Half Subtractor and Full subtractor
## Implementation of Half subtractor and Full subtractor circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
# Half Subtractor:
```
module exp4(A,B,diff,borrow);
input A,B; output diff,borrow;
wire X;
xor(diff,A,B);
not(X,A);
and(borrow,X,B);
endmodule
```
# Full Subtractor:
```
module fullsub(A,B,Bin,diff,borrow);
input A,B,Bin;
output diff,borrow;
assign diff = A ^ B ^ Bin;
assign borrow = (~A&B)|(~(A^B))&Bin;
endmodule
```

##  RTL Diagram:
# Half Subtrator:

![exp4 rtl](https://github.com/kancharlaNarmadha/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559316/b5635804-bc30-42a3-af08-cdec435c822f)

# Full Subtractor:


![exp 4 rtl fllsub](https://github.com/kancharlaNarmadha/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559316/e826b312-38c1-4059-887c-890f4325ec8c)

# TRUTH TABLE:
# HAFL SUBTRACTOR:
![213157495-55fe7372-034a-4deb-a57a-c7808e35f670](https://github.com/kancharlaNarmadha/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559316/bb77e32f-1b5b-4118-a932-5ba12385502e)

# FULL SUBTRACTOR:

![213157894-a8d50f39-7ebd-4939-a458-b86dda3fd8c5](https://github.com/kancharlaNarmadha/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559316/3d7abca0-e92d-493d-b7c7-736731a0418d)


## OUTPUT WAVEFORM:
# HALF SUBTRACTOR:
![exp4 waveform](https://github.com/kancharlaNarmadha/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559316/5a12dd2f-d00e-457a-ac5e-9ca7a756735c)

# FULL SUBTRACTOR:

![WhatsApp Image 2023-09-08 at 09 24 50](https://github.com/kancharlaNarmadha/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119559316/fe558929-672c-467c-8894-33a06c62c5ac)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
