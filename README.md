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

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |   1200       68          |
|                         |   1201       24          |

#### Manual Calculations

<img width="1280" height="855" alt="WhatsApp Image 2026-04-29 at 8 58 42 PM" src="https://github.com/user-attachments/assets/1e7796fa-5f45-44f2-a6b1-d144d24f6c52" />


## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="664" height="436" alt="WhatsApp Image 2026-04-22 at 1 57 36 PM" src="https://github.com/user-attachments/assets/adcae721-b97d-4462-9013-94102ca9fe1b" />


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
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,6543H
MOV BX,1234H
SUB AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV[SI],AX
MOV[SI+2],AX
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |    1200        0F        |             
|                         |    1201        53        |
 
#### Manual Calculations
<img width="1280" height="638" alt="WhatsApp Image 2026-04-29 at 8 58 20 PM" src="https://github.com/user-attachments/assets/29418080-3863-40cc-97c0-fe986313f021" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="641" height="437" alt="WhatsApp Image 2026-04-20 at 2 17 53 PM" src="https://github.com/user-attachments/assets/bf948181-c07a-47f7-8ba1-b23dc2c80b5e" />


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
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV DX,0000H
MOV AL,2CH
MOV BL,2FH
MUL BL
MOV SI,1200H
MOV[SI],AX
MOV[SI+02H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |    1200        11        |                      
|                         |    1201        02        |

#### Manual Calculations
<img width="1202" height="1040" alt="WhatsApp Image 2026-04-29 at 8 59 07 PM" src="https://github.com/user-attachments/assets/a83a17d1-4d0c-45ab-8021-9e45591e46f4" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="435" alt="WhatsApp Image 2026-04-20 at 2 40 45 PM" src="https://github.com/user-attachments/assets/8a7a1373-6a32-426c-80f3-8c43eeb1f15c" />


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
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV DX,0000H
MOV AX,123H
MOV CH,34H
MOV BL,CH
DIV BL
MOV SI,1200H
MOV[SI],AX
MOV[SI+02H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |    1200      05          |            
|                         |    1201      1F          |

#### Manual Calculations
<img width="1097" height="1040" alt="WhatsApp Image 2026-04-29 at 8 59 38 PM" src="https://github.com/user-attachments/assets/2ac3525b-77f8-4138-91f4-3308a135bb14" />


## OUTPUT FROM MASM SOFTWARE
<img width="653" height="443" alt="WhatsApp Image 2026-04-28 at 11 43 08 AM" src="https://github.com/user-attachments/assets/f3ed6e74-200f-4afb-bb3a-84c3721c453e" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
