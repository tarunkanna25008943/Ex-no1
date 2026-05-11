# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

```#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                                 68
                                  24
```

#### Manual Calculations


<img width="1280" height="1023" alt="WhatsApp Image 2026-04-27 at 2 45 39 PM" src="https://github.com/user-attachments/assets/e14e5ebd-f8a5-4106-85b2-6197eb6a042f" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="643" height="421" alt="image" src="https://github.com/user-attachments/assets/e159e6ee-f0a8-4752-a3c1-ede1349a2883" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |      00                  |
|                         |      00                  |
#### Manual Calculations


<img width="1280" height="860" alt="WhatsApp Image 2026-04-27 at 3 42 38 PM" src="https://github.com/user-attachments/assets/3ba76f9f-e1a4-487e-ac4c-336edf7df145" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="637" height="420" alt="image" src="https://github.com/user-attachments/assets/29bc242e-ce39-4814-b1ff-edf63d5d445c" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV DX,0000H
MOV AX,1234H
MOV BX,1234H
MUL BX
MOV SI,1200H
MOV [SI],AX
MOV [SI+02H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

```#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |       90                 |
|                         |       5A                 |
```

#### Manual Calculations

<img width="1280" height="987" alt="image" src="https://github.com/user-attachments/assets/3029ad22-fcbd-4fbe-8474-89112e9afd13" />

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="622" height="276" alt="image" src="https://github.com/user-attachments/assets/70435644-4209-45f2-9f81-6f8d7483a72a" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,1234H
MOV BX,1234H
DIV BX
MOV SI,1200H
MOV [SI],AX
MOV [SI+02H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

```#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |         01               |
|                         |         00               |
```
#### Manual Calculations

<img width="1280" height="957" alt="WhatsApp Image 2026-04-27 at 9 33 00 PM" src="https://github.com/user-attachments/assets/d58efd4d-4ecb-4741-943a-7cfdaca73a0e" />


---
## OUTPUT FROM MASM SOFTWARE

<img width="640" height="427" alt="image" src="https://github.com/user-attachments/assets/55f7f42a-910c-485b-8e8d-493d027d8165" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
