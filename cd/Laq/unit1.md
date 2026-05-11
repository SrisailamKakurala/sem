# 1. Explain the Instruction Formats and Addressing Modes of 8086 with Examples

## Introduction

The 8086 microprocessor executes instructions written in assembly language.
Each instruction contains information about:

* What operation should be performed
* On which data the operation should be performed

To execute instructions correctly, 8086 uses:

* Instruction formats
* Addressing modes

These help the processor understand the operation and locate data in memory or registers.

---

# Instruction Format of 8086

## What is an Instruction Format?

Instruction format is the structure or layout of an instruction in memory.

An instruction mainly contains:

* Opcode
* Operand
* Address information

---

## Parts of an Instruction

### 1. Opcode

Opcode tells the processor which operation to perform.

Examples:

* MOV → Move data
* ADD → Addition
* SUB → Subtraction

---

### 2. Operand

Operand represents the data or location on which operation is performed.

Example:

```asm
MOV AX, BX
```

* MOV → Opcode
* AX and BX → Operands

---

## Types of Instruction Formats

---

### 1. One-Byte Instruction

Contains only opcode.

Example:

```asm
CLC
```

Used for simple operations.

---

### 2. Two-Byte Instruction

Contains opcode and operand information.

Example:

```asm
MOV AL, BL
```

---

### 3. Multi-Byte Instruction

Contains opcode, addressing information, and data/address.

Example:

```asm
MOV AX, 1234H
```

---

# Addressing Modes of 8086

## What is an Addressing Mode?

Addressing mode is the method used to locate operands.

It tells the processor:

* Where data is stored
* How to access data

---

# Types of Addressing Modes

---

## 1. Immediate Addressing Mode

Data is directly given in instruction.

### Example

```asm
MOV AX, 1234H
```

Meaning:

* Load value 1234H directly into AX register.

### Advantages

* Fast execution
* Simple

---

## 2. Register Addressing Mode

Operand is stored in register.

### Example

```asm
MOV AX, BX
```

Meaning:

* Copy contents of BX into AX.

### Advantages

* Very fast
* No memory access needed

---

## 3. Direct Addressing Mode

Memory address is directly specified.

### Example

```asm
MOV AX, [2000H]
```

Meaning:

* Data from memory location 2000H is copied into AX.

---

## 4. Register Indirect Addressing Mode

Address of operand is stored in register.

### Example

```asm
MOV AX, [BX]
```

Meaning:

* BX contains memory address
* Data from that address moves into AX

---

## 5. Based Addressing Mode

Uses base register for memory access.

### Example

```asm
MOV AX, [BX+10H]
```

---

## 6. Indexed Addressing Mode

Uses index registers SI or DI.

### Example

```asm
MOV AX, [SI]
```

Used mainly in string operations.

---

## 7. Based Indexed Addressing Mode

Combines base and index registers.

### Example

```asm
MOV AX, [BX+SI]
```

Useful for array processing.

---

## Importance of Addressing Modes

* Efficient memory access
* Faster execution
* Supports arrays and strings
* Reduces instruction size

---

## Conclusion

Instruction formats define the structure of instructions, while addressing modes define how operands are accessed. These concepts are essential for programming and understanding 8086 microprocessor operations.

---

# 2. Explain the Instruction Set of 8086 Processor

## Introduction

Instruction set is the collection of commands that the 8086 processor can execute.

These instructions are used to:

* Transfer data
* Perform arithmetic operations
* Execute logical operations
* Control program flow

---

# Types of 8086 Instructions

---

# 1. Data Transfer Instructions

Used to transfer data between registers, memory, and I/O devices.

---

## Common Instructions

### MOV

Moves data from source to destination.

Example:

```asm
MOV AX, BX
```

---

### PUSH

Stores data into stack.

```asm
PUSH AX
```

---

### POP

Retrieves data from stack.

```asm
POP AX
```

---

### XCHG

Exchanges data.

```asm
XCHG AX, BX
```

---

# 2. Arithmetic Instructions

Used for mathematical operations.

---

## ADD

Adds data.

```asm
ADD AX, BX
```

---

## SUB

Subtracts data.

```asm
SUB AX, BX
```

---

## INC

Increments value by 1.

```asm
INC AX
```

---

## DEC

Decrements value by 1.

```asm
DEC AX
```

---

## MUL

Multiplies data.

---

## DIV

Divides data.

---

# 3. Logical Instructions

Used for logical operations.

---

## AND

Performs logical AND.

```asm
AND AX, BX
```

---

## OR

Performs logical OR.

---

## XOR

Performs exclusive OR.

---

## NOT

Inverts bits.

---

# 4. Branch Instructions

Used for decision making and looping.

---

## JMP

Unconditional jump.

```asm
JMP LABEL
```

---

## JZ

Jump if zero flag is set.

---

## JNZ

Jump if zero flag is not set.

---

## LOOP

Repeats instructions.

---

# 5. CALL and RETURN Instructions

Used in subprograms.

---

## CALL

Transfers control to procedure.

```asm
CALL PROC1
```

---

## RET

Returns control to main program.

```asm
RET
```

---

# 6. String Instructions

Used for string and array processing.

---

## MOVS

Moves string data.

---

## LODS

Loads string data.

---

## STOS

Stores string data.

---

# Importance of Instruction Set

* Controls processor operations
* Helps in assembly language programming
* Supports mathematical and logical operations

---

## Conclusion

The instruction set of 8086 contains different categories of instructions used for data transfer, arithmetic, logic, branching, and string processing.

---

# 3. Explain Assembler Directives and Macros in 8086 Assembly Language Programming

## Introduction

Assembler directives and macros are special commands used in assembly language programming.

They help:

* Organize programs
* Simplify coding
* Improve readability

These are processed by assembler and not directly executed by processor.

---

# Assembler Directives

## What are Assembler Directives?

Assembler directives are instructions given to assembler for controlling assembly process.

They do not generate machine code.

---

# Common Assembler Directives

---

## 1. DB (Define Byte)

Used to define 8-bit data.

Example:

```asm
NUM DB 25H
```

---

## 2. DW (Define Word)

Defines 16-bit data.

```asm
NUM DW 1234H
```

---

## 3. SEGMENT

Defines memory segment.

---

## 4. ENDS

Ends segment definition.

---

## 5. ASSUME

Associates segment registers.

---

## 6. END

Marks end of program.

---

# Advantages of Directives

* Organize memory
* Define variables
* Simplify program structure

---

# Macros

## What is a Macro?

Macro is a group of instructions given a single name.

Whenever macro name is used, all instructions execute automatically.

---

# Structure of Macro

```asm
MACRO_NAME MACRO
instructions
ENDM
```

---

# Example

```asm
DISPLAY MACRO
MOV AH, 02H
INT 21H
ENDM
```

---

# Advantages of Macros

* Reduces repeated code
* Saves programming time
* Improves readability

---

# Difference Between Macro and Procedure

| Macro              | Procedure            |
| ------------------ | -------------------- |
| Expanded inline    | Called separately    |
| Faster execution   | Smaller memory usage |
| More memory needed | Less memory needed   |

---

## Conclusion

Assembler directives help control program organization, while macros simplify repeated instruction execution in 8086 programming.

---

# 4. Write and Explain 8086 Programs for Logical Operations, Branch Instructions, and CALL Instructions

## Introduction

8086 assembly language programs are written using instruction set commands to perform operations such as logical processing, branching, and subroutine calls.

---

# Program for Logical Operation

## Example: AND Operation

```asm
MOV AX, 1234H
MOV BX, 4321H
AND AX, BX
```

---

## Explanation

* First instruction loads AX
* Second loads BX
* AND performs bitwise logical AND
* Result stored in AX

---

# Program for Branch Instruction

## Example: Conditional Jump

```asm
MOV AX, 0000H
CMP AX, 0000H
JZ LABEL1

LABEL1:
MOV BX, 1111H
```

---

## Explanation

* CMP compares AX with zero
* JZ jumps if result is zero
* BX gets loaded

---

# Program Using CALL Instruction

## Example

```asm
CALL DISPLAY

DISPLAY:
MOV AX, 1234H
RET
```

---

## Explanation

* CALL transfers control to DISPLAY
* DISPLAY executes instructions
* RET returns control

---

# Importance

* Logical instructions help data processing
* Branching supports decision making
* CALL supports modular programming

---

## Conclusion

Logical, branch, and CALL instructions are essential for efficient assembly language programming in 8086.

---

# 5. Write and Explain 8086 Programs for Sorting and String Manipulation

## Introduction

8086 processor supports programs for sorting numbers and manipulating strings using loops and string instructions.

---

# Sorting Program

## Example: Ascending Order Sorting

```asm
MOV AX, 05H
MOV BX, 03H
CMP AX, BX
JBE SKIP
XCHG AX, BX

SKIP:
```

---

## Explanation

* AX and BX contain numbers
* CMP compares values
* If AX > BX, values exchange
* Numbers become sorted

---

# String Manipulation Program

## Example: String Copy

```asm
MOV SI, OFFSET SRC
MOV DI, OFFSET DEST
MOV CX, 05H
REP MOVSB
```

---

## Explanation

* SI points to source string
* DI points to destination
* CX stores count
* MOVSB copies bytes

---

# String Instructions Used

| Instruction | Function          |
| ----------- | ----------------- |
| MOVSB       | Move byte string  |
| CMPSB       | Compare strings   |
| LODSB       | Load string byte  |
| STOSB       | Store string byte |

---

# Applications

* Text processing
* Array handling
* Data organization

---

## Conclusion

Sorting and string manipulation programs demonstrate how 8086 handles data efficiently using loops, comparisons, and string instructions.
