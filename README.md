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
![WhatsApp Image 2026-02-07 at 9 41 48 AM](https://github.com/user-attachments/assets/a0e0326b-6c1c-4b9d-86c6-1a0c5fcf12e6)

#### Manual Calculations
![WhatsApp Image 2026-02-07 at 10 03 30 AM](https://github.com/user-attachments/assets/557dd8b2-ea68-4afb-a005-6be1e51830ad)

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="655" height="447" alt="546487466-120cde55-9af9-4d1d-9f58-80f39f279438" src="https://github.com/user-attachments/assets/e9af0301-8af0-4a6d-b2da-b8dd70d07a11" />

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
![WhatsApp Image 2026-02-07 at 8 33 59 AM](https://github.com/user-attachments/assets/e0700703-d1ab-48cc-8ce8-bc4ddcbcde21)

#### Manual Calculations
![WhatsApp Image 2026-02-07 at 10 05 27 AM](https://github.com/user-attachments/assets/ffc27a69-2fbb-4996-a09c-0357b20ee2b4)

## OUTPUT SCREEN FROM MASM SOFTWARE
 <img width="638" height="431" alt="546490890-8e385997-b435-4123-8aaa-4d7cac8d25d6" src="https://github.com/user-attachments/assets/4e24951b-2925-40b0-b402-d1306649d7fb" />

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
![WhatsApp Image 2026-02-07 at 10 06 43 AM](https://github.com/user-attachments/assets/d3806b74-d601-4f71-845a-71b79018faf1)

#### Manual Calculations
<img width="1599" height="606" alt="546489594-635c2480-ec46-416e-8da0-a0d073625fac" src="https://github.com/user-attachments/assets/624716d0-75c0-4a1a-94da-658576153b54" />

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="642" height="424" alt="546488340-b84231e0-f979-4d7e-bd6e-1f417827eebe" src="https://github.com/user-attachments/assets/e6a4f179-cdd6-4d3c-8e7f-d3a4ba092538" />

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
![WhatsApp Image 2026-02-07 at 10 08 18 AM](https://github.com/user-attachments/assets/14a92be7-6b28-4518-8a8a-25961059c5ab)

#### Manual Calculations
![WhatsApp Image 2026-02-07 at 10 09 14 AM](https://github.com/user-attachments/assets/a4cc8bf5-dc6f-4518-8b85-0cf09a34b3e3)

## OUTPUT FROM MASM SOFTWARE
<img width="638" height="431" alt="546489095-348a598b-5463-4042-8b5e-1bae679eb0cc" src="https://github.com/user-attachments/assets/847579a6-caf8-4cec-8b67-dd29133d9503" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

