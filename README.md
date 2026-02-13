# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
CMC
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP: CMP M
JNC NEXT
MOV A,M
NEXT: INX H
DCR C
JNZ LOOP
STA 4300H
HLT
```
## Output:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/67eacb82-848e-464b-8ebb-ecb9db7cf86e" />
<img width="292" height="365" alt="image" src="https://github.com/user-attachments/assets/e69b1102-f031-448b-9ac5-990a0af7cfde" />

## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
CMC
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP: CMP M
JC NEXT
MOV A,M
NEXT: INX H
DCR C
JNZ LOOP
STA 4301H
HLT
```

## Output:
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/33428c9e-ab7b-4d0c-9eaa-4e69f29927cb" />
<img width="298" height="364" alt="image" src="https://github.com/user-attachments/assets/137236ac-8061-442e-9e17-103fce93a2b5" />


## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
