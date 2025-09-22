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

## DIRECT ADDITION :

#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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
|     1200                |      12                  |
|     1201                |      34                  |
|     1202                |      12                  |
|     1203                |      34                  |
|     1204                |      24                  |
|     1205                |      68                  |
#### Manual Calculations :

(Add your calculation here)
![WhatsApp Image 2025-09-22 at 08 36 15_36855ab4](https://github.com/user-attachments/assets/e942b34e-8481-4e48-88bf-297ede2af795)


## OUTPUT IMAGE FROM MASM SOFTWARE :
![WhatsApp Image 2025-09-22 at 08 38 21_33c3153d](https://github.com/user-attachments/assets/8f89c774-2e12-42a5-970a-fc2bc71c13b5)

### INDIRECT ADDITION :

### PROGRAM : 
```
CODE SEGMENT 
ASSUME CS: CODE, DS:CODE 
ORG 1000H 
MOV SI,2000H 
MOV CL,00H 
MOV AX,[SI] 
MOV BX,[SI+02H] 
ADD AX,BX 
JNC L1 
INC CL 
L1:  MOV [SI+04H],AX 
MOV [SI+06H],CL 
MOV AH,4CH 
INT 21H 
CODE ENDS 
END

```
### OUTPUT TABLE :

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200                |      78                  |
|     1201                |      88                  |
|     1202                |      23                  |
|     1203                |      02                  |
|     1204                |      9C                  |
|     1205                |      8A                  |

### MANUAL CALCULATIONS :

![WhatsApp Image 2025-09-22 at 09 48 18_d281b87c](https://github.com/user-attachments/assets/468ba95d-c591-4f87-8167-bf7f8a4f714d)


### OUTPUT IMAGE FROM MASM SOFTWARE :
![WhatsApp Image 2025-09-22 at 08 38 30_3532c188](https://github.com/user-attachments/assets/3d1b9ca2-3ed9-4009-98c9-daa1f99e0d4c)

#### Manual Calculations
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
MOV AX,[SI]
MOV BX,[SI+02H]
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
|     1200                |      12                  |
|     1201                |      34                  |
|     1202                |      12                  |
|     1203                |      34                  |
|     1204                |      00                  |
|     1205                |      00                  |

#### Manual Calculations

(Add your calculation here)

![WhatsApp Image 2025-09-22 at 09 48 30_80377a55](https://github.com/user-attachments/assets/53a7b8f4-b30a-46e1-8206-bb3a13fd8841)

---


## OUTPUT SCREEN FROM MASM SOFTWARE :
![WhatsApp Image 2025-09-17 at 14 23 49_462c876e](https://github.com/user-attachments/assets/646153ff-3720-4e88-9f46-63875eb8170a)

### INDIRECT SUBTRACTION :

###PROGRAM :
```CODE SEGMENT 
ASSUME CS: CODE,DS:CODE 
ORG 1000H 
MOV SI,2000H 
MOV CL,00H 
MOV AX,[SI] 
MOV BX,[SI+02H] 
SUB AX, BX 
JNC DOWN 
INC CL 
DOWN: MOV [SI+04H],AX 
MOV [SI+06H],CL 
MOV AH,4CH 
INT 21H 
CODE ENDS 
END
```
### OUTPUT TABLE:
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200                |      12                  |
|     1201                |      34                  |
|     1202                |      12                  |
|     1203                |      34                  |
|     1204                |      00                  |
|     1205                |      00                  |

### MANUAL CALCULATION :

![WhatsApp Image 2025-09-22 at 09 48 31_0f7dce37](https://github.com/user-attachments/assets/53af2a4f-93c7-434e-b149-5fca828b09d5)

### OUTPUT SCREEN FROM MASM SOFTWARE :
![WhatsApp Image 2025-09-22 at 09 00 30_1160c9f9](https://github.com/user-attachments/assets/107cad3e-9cd3-4f05-8fb8-f48cfbac7b57)



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
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | -------------------------|
|     1200                |      12                  |
|     1201                |      34                  |
|     1202                |      12                  |
|     1203                |      34                  |
|     1204                |      09                  |
|     1205                |      5A                  |
#### Manual Calculations :

(Add your calculation here)


---![WhatsApp Image 2025-09-22 at 09 52 15_3d1590cd](https://github.com/user-attachments/assets/5aed5e86-8275-403f-9e06-f3fa41d547ba)


## OUTPUT SCREEN FROM MASM SOFTWARE :
![WhatsApp Image 2025-09-22 at 08 39 00_a8a5a6a7](https://github.com/user-attachments/assets/b432f057-84b9-4728-affa-d9e6fd38dda8)

### INDIRECT MULTIPLICATION :

### PROGRAM:
```CODE SEGMENT 
ASSUME CS: CODE,DS:CODE  
ORG 1000H 
MOV SI,2000H  
MOV DX,0000H 
 MOV AX,[SI] 
MOV BX,[SI+02H]  
MUL BX 
MOV [SI+04H],AX  
MOV [SI+06H],DX  
MOV AH,4CH 
INT 21H 
 CODE ENDS 
END
```

### OUTPUT TABLE :
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | -------------------------|
|     2000                |      12                  |
|     2001|               |      34                  |
|     2002                |      12                  |
|     2003                |      34                  |
|     2004                |      44                  |
|     2005                |      51                  |
|     2006                |      97                  |
|     2007                |      0A                  |

#### Manual Calculations :

![WhatsApp Image 2025-09-22 at 09 30 09_4193ebdf](https://github.com/user-attachments/assets/8e5cf855-2615-438c-b3e4-31b56d0acd8e)

### OUTPUT SCREEN FROM MASM SOFTWARE :
![WhatsApp Image 2025-09-22 at 09 11 38_3351edd6](https://github.com/user-attachments/assets/b7a61cc0-0988-4bcf-818d-fed1c849ef49)


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
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     2000                |      34                  |
|     2001|               |      12                  |
|     2002                |      34                  |
|     2003                |      12                  |
|     2004                |      01                  |
|     2005                |      00                  |

#### Manual Calculations :

![WhatsApp Image 2025-09-22 at 09 38 26_87524f85](https://github.com/user-attachments/assets/58d13f70-e545-46ea-9eef-66dfe306459a)


(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE :
![WhatsApp Image 2025-09-22 at 08 39 16_ac0336af](https://github.com/user-attachments/assets/44db926f-c50f-437d-b47d-d89fe445a644)

### INDIRECT DIVISION :

![IMG-20250922-WA0028 1](https://github.com/user-attachments/assets/9a5b5b2d-b715-4577-a7c0-5a6328b6dc72)

### PROGRAM :
```
CODE SEGMENT 
ASSUME CS: CODE,DS:CODE 
ORG 1000H 
MOV SI,2000H 
MOV DX,0000H 
MOV AX,[SI] 
MOV BX,[SI+02H] 
DIV BX 
MOV [SI+04H],AX 
MOV [SI+06H],DX 
MOV AH,4CH 
INT 21H 
CODE ENDS 
END
```
### OUTPUT TABLE :
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     2000                |      34                  |
|     2001|               |      12                  |
|     2002                |      34                  |
|     2003                |      12                  |
|     2004                |      01                  |
|     2005                |      00                  |
### MANUAL CALCULATIONS :

### OUTPUT FROM MASM SOFTWARE :
![WhatsApp Image 2025-09-22 at 09 27 18_30ecfa80](https://github.com/user-attachments/assets/85d47e9f-81ec-433f-a319-1c24cf95ebb9)





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

