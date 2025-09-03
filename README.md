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

| MEMORY LOCATION (INPUT)       | MEMORY LOCATION (OUTPUT) |
| -----------------------       | ------------------------ |
|          1200:  12            | 1204: 24                 |
|          1201:  34            | 1205: 68                 |
|          1202:  12            | 1206: 00                 |
|          1203:  34            |                          |
____________________________________________________________

#### Manual Calculations

(Add your calculation here)
![Manual Calculations  (ADD)](https://github.com/user-attachments/assets/3da749e9-06d9-4187-a1be-6ffbb12a2aad)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="637" height="422" alt="Add" src="https://github.com/user-attachments/assets/38464a22-2874-49ec-b9a3-185f360c5b0a" />
<img width="640" height="480" alt="vetriadd" src="https://github.com/user-attachments/assets/fb5fc8a7-c01b-4e5e-950f-cb9c6b1428ec" />




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



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|        1200:12          | 1204:00                  |
|        1201:34          | 1205:00                  |
|        1202:12          | 1206:00                  |
|        1203:34          |                          | 
______________________________________________________

#### Manual Calculations

(Add your calculation here)
![Manual Calculations (SUM)](https://github.com/user-attachments/assets/36bbe80d-ba21-4df2-ae1d-f91cae7ffd7b)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="634" height="426" alt="Sum" src="https://github.com/user-attachments/assets/ffc06152-04db-4bb2-bf13-2a44e6998f48" />
<img width="640" height="480" alt="vetrisum" src="https://github.com/user-attachments/assets/9957ccf4-2b5e-4b03-877c-9a7bd4729fab" />



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
| ----------------------- | ------------------------ |
|  1200:12                | 1204:44                  |
|  1201:34                | 1205:51                  |
|  1202:12                | 1206:97                  |
|  1203:34                |                          |
______________________________________________________

#### Manual Calculations

(Add your calculation here)
![Manual Calculations (MULTI)](https://github.com/user-attachments/assets/b8c73afd-a5d7-48d3-9615-b668d44c8917)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="636" height="427" alt="Multi" src="https://github.com/user-attachments/assets/7bba912c-6857-489e-9f87-3b432db3b63f" />
<img width="640" height="480" alt="vetrimulti" src="https://github.com/user-attachments/assets/88e6079a-9e94-43e4-bc88-eb29ae158184" />



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
| 1200:12                 | 1204: 01                 |
| 1201:34                 | 1205: 00                 |
| 1202:12                 | 1206: 00                 |
| 1203:34                 |                          |
______________________________________________________
#### Manual Calculations

(Add your calculation here)
![Manual Calculations(DIV)](https://github.com/user-attachments/assets/f575b5e4-3a0f-4fdd-acbd-8e0c9c303f01)


---
## OUTPUT FROM MASM SOFTWARE
<img width="639" height="427" alt="div" src="https://github.com/user-attachments/assets/fdec2040-1d7b-48d1-8e94-bde70af94758" />
<img width="640" height="480" alt="vetridiv" src="https://github.com/user-attachments/assets/f3894549-cbb6-49a5-ab16-941a6e478851" />





## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
