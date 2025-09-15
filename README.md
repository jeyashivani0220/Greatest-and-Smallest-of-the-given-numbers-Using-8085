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
LDA 4200H ;
MOV C,A ;
LXI H, 4201H ;
MOV A,M ;
INX H ;
DCR C ;
LOOP: CMP M ;
JNC NEXT ;
MOV A,M;
NEXT:INX H;
DCR C ;
JNZ LOOP ;
STA 4300H ;
HLT ;


```
## Output:
![WhatsApp Image 2025-09-15 at 13 06 37_68c4b66c](https://github.com/user-attachments/assets/673f3cb7-d246-4524-a832-ccb45313c074)
![WhatsApp Image 2025-09-15 at 13 07 03_040816d0](https://github.com/user-attachments/assets/b0d30ce3-0ade-43fc-a740-8d653896cc1e)




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


LDA 4200H ;
MOV C,A ;
LXI H, 4201H ;
MOV A,M ;
INX H ;
DCR C ;
LOOP: CMP M ;
JC NEXT ;
MOV A,M;
NEXT:INX H;
DCR C ;
JNZ LOOP ;
STA 4301H ;
HLT ;


```

## Output:
![WhatsApp Image 2025-09-15 at 13 07 43_8a26f9dc](https://github.com/user-attachments/assets/71e98973-673a-422d-9524-bb704f169a9b)
![WhatsApp Image 2025-09-15 at 13 11 32_5401fe68](https://github.com/user-attachments/assets/2f4876d2-4d87-42ab-a6b7-f2db17640833)




## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
