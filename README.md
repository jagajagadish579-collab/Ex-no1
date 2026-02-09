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
<img width="607" height="924" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1000 = 1234H        |    1200 =  58            |
|     1001 = 0123H        |    1201 =  13            |

#### Manual Calculations

![WhatsApp Image 2026-02-09 at 10 07 26 AM](https://github.com/user-attachments/assets/b8381cc1-dbff-420b-92ec-c6f298ced15e)



---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="533" height="391" alt="Screenshot 2026-01-28 112650" src="https://github.com/user-attachments/assets/6cb79d2d-a373-4cf3-8069-361a66b803e8" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="378" height="697" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
SUB AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1000 = 1234H        |      1200 = 10           |
|     1001 = 0123H        |      1201 = 11           |

#### Manual Calculations
![WhatsApp Image 2026-02-09 at 10 07 25 AM](https://github.com/user-attachments/assets/4162d363-578d-4019-84c5-0832d12e5c2b)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="569" height="289" alt="Screenshot 2026-01-28 112426" src="https://github.com/user-attachments/assets/74648cd4-30cc-44fc-88be-9edb7f8a5523" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="806" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,124H
MUL AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1000 =  1234        |      1200 = 58           |
|     1001 =  124         |      1201 = 13           |
|                         |      1202 = 00           |
|                         |      1203 = E8           |
 
#### Manual Calculations


---![WhatsApp Image 2026-02-09 at 10 33 17 AM](https://github.com/user-attachments/assets/1bfb2a6c-ca95-4443-be19-5034f640abf2)



## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2026-02-09 at 10 36 07 AM](https://github.com/user-attachments/assets/dfaf5eba-9cd1-45dd-b5fb-090825fa90e2)



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
MOV CL,00H
MOV AX,1234H
MOV BX,124H
DIV AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|    1000 = 1234H         |         1200 = 01        |
|    1001 = 124 H         |         1201 = 00        |
|                         |         1202 = 00        |
|                         |         1203 = E8        |

#### Manual Calculations
![WhatsApp Image 2026-02-09 at 10 30 17 AM](https://github.com/user-attachments/assets/95d04403-4b55-4357-b184-5831624d6e97)



---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2026-02-09 at 10 43 46 AM](https://github.com/user-attachments/assets/0fe1bc4e-8022-4012-a84c-d39b8c46183c)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
