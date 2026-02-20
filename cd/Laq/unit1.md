Got it Sri 👍 no images, no extra stuff — just simple, clean, easy-to-remember notes for exam writing.


---

1️⃣ Architecture of 8086 Microprocessor

The 8086 is a 16-bit microprocessor divided into two main parts:

1. Bus Interface Unit (BIU)

Fetches instructions from memory

Handles communication with memory and I/O

Contains segment registers and instruction pointer

Has 6-byte instruction queue (for faster processing)


2. Execution Unit (EU)

Executes instructions

Contains ALU (Arithmetic Logic Unit)

Contains general registers and flag register


👉 BIU fetches, EU executes → this improves speed (pipelining).


---

2️⃣ Minimum Mode Pin Configuration of 8086

8086 works in two modes: Minimum and Maximum.

Minimum Mode:

Used when only one processor is present.

Control signals are generated internally.


Important Pins:

AD0–AD15 → Address/Data lines

ALE → Separates address from data

RD → Read signal

WR → Write signal

M/IO → Select memory or I/O

INTR, NMI → Interrupt signals


Minimum mode is simpler and used in small systems.


---

3️⃣ Register Organization in 8086

Registers are 16-bit and grouped into types:

1. General Purpose Registers

AX (Accumulator)

BX (Base)

CX (Count)

DX (Data)


Each can be divided into two 8-bit parts (AH/AL etc.)

2. Segment Registers

CS → Code Segment

DS → Data Segment

SS → Stack Segment

ES → Extra Segment


3. Pointer & Index Registers

SP → Stack Pointer

BP → Base Pointer

SI → Source Index

DI → Destination Index


4. Instruction Pointer (IP)

Points to next instruction.

5. Flag Register

Stores status like Zero, Carry, Sign, Overflow.


---

4️⃣ Arithmetic and Logical Instructions

Arithmetic Instructions

ADD AX, BX → Adds BX to AX

SUB AX, BX → Subtracts BX from AX

INC AX → Increases AX by 1

DEC AX → Decreases AX by 1

MUL BX → Multiplies AX with BX



---

Logical Instructions

AND AX, BX → Bitwise AND

OR AX, BX → Bitwise OR

XOR AX, AX → Clears AX

NOT AX → Inverts bits


Arithmetic changes numbers.
Logical works on bits (0 and 1).


---

5️⃣ Addressing Modes of 8086

Addressing mode tells how operand is accessed.

1. Immediate → MOV AX, 1234H (value given directly)


2. Register → MOV AX, BX


3. Direct → MOV AX, [1234H]


4. Register Indirect → MOV AX, [BX]


5. Indexed → MOV AX, [SI]


6. Based Indexed → MOV AX, [BX+SI]




---

6️⃣ Data Transfer Instructions

MOV AX, BX → Copies data

PUSH AX → Stores data in stack

POP AX → Retrieves from stack

XCHG AX, BX → Swaps values

IN AL, 60H → Reads from I/O port

OUT 60H, AL → Sends data to I/O port


These instructions only move data, not modify it.


---

🔥 Quick Memory Trick for Exam

Architecture → BIU + EU
Registers → General + Segment + Pointer + Flag
Modes → Minimum = Single processor
Instructions → Arithmetic / Logical / Data
Addressing → How operand is accessed


---

If you want, I can now give:

Very short 2-mark answers

Differences between microprocessor & microcontroller

8051 notes

Important viva questions


Tell me what your exam is focusing on Sri 💪


Good Sri 💪🔥 these are important interfacing questions. I’ll explain them in simple, easy-to-remember notes, exam-friendly.


---

13️⃣ Interfacing of Stepper Motor with 8086

✅ What is a Stepper Motor?

A stepper motor rotates in fixed steps (not continuous like DC motor).
Each input pulse → one step rotation.


---

✅ Why Interface with 8086?

8086 cannot directly drive motor (low current).
So we use:

8255 Programmable Peripheral Interface (PPI)

Driver circuit (like ULN2003)



---

✅ Basic Connection

8086 → 8255 → Driver → Stepper Motor

Port of 8255 gives binary sequence

Driver amplifies current

Motor rotates step by step



---

✅ Working Principle

Example sequence for 4-phase motor:

Step	A	B	C	D

1	1	0	0	0
2	0	1	0	0
3	0	0	1	0
4	0	0	0	1


Changing sequence direction → motor reverses.


---

✅ Applications

Robotics

CNC machines

Printers



---

14️⃣ Modes of 8255

✅ What is 8255?

8255 is a Programmable Peripheral Interface (PPI) used to connect input/output devices.

It has:

Port A (8-bit)

Port B (8-bit)

Port C (8-bit)



---

✅ Modes of Operation

🔹 Mode 0 – Basic I/O Mode

Simple input/output

No handshaking

Used for LEDs, switches



---

🔹 Mode 1 – Strobed I/O Mode

Input/output with handshaking signals

Ensures data transfer control

Uses Port C bits for control



---

🔹 Mode 2 – Bi-directional Mode

Only for Port A

Data can flow both ways

Used for advanced communication



---

🔹 BSR Mode (Bit Set Reset)

Controls individual bits of Port C

Used for control signals



---

15️⃣ Short Notes on External Communication Interface

External communication interface allows microprocessor to communicate with:

Keyboard

Display

Printer

Serial devices

Other microprocessors



---

Types:

🔹 Parallel Communication

Multiple bits sent at once

Faster

Example: 8255


🔹 Serial Communication

One bit at a time

Slower but long distance

Example: 8251 USART



---

Purpose:

Data exchange

Device control

System expansion



---

16️⃣ Pins of 8255 (Important Pins)

8255 has 40 pins.


---

🔹 Data Bus (D0–D7)

Transfers data between CPU and 8255.


---

🔹 Port A (PA0–PA7)

8-bit input/output port.


---

🔹 Port B (PB0–PB7)

8-bit input/output port.


---

🔹 Port C (PC0–PC7)

Used as I/O or control signals.


---

🔹 Control Pins

RD → Read

WR → Write

CS → Chip Select

A0, A1 → Select port

RESET → Reset device



---

17️⃣ Interfacing 4×4 Keyboard with 8051

✅ What is 4×4 Keyboard?

16 keys arranged in matrix

4 rows and 4 columns



---

✅ Why Matrix?

Reduces number of pins needed.


---

✅ Connection

Rows → Output pins of 8051

Columns → Input pins of 8051



---

✅ Working Principle (Scanning Method)

1. Make one row LOW at a time.


2. Check which column becomes LOW.


3. Detect key number based on row-column match.



Example: Row 1 + Column 2 active → Key 2 pressed.


---

✅ Key Detection Formula

Key number = (Row × 4) + Column


---

✅ Applications

Calculators

ATM keypad

Embedded systems



---

🔥 Quick Revision Table

Device	Used With	Purpose

Stepper Motor	8086 + 8255	Control rotation
8255	8086	I/O interface
4×4 Keyboard	8051	Key detection
Serial Interface	8251	Serial communication



---

If you want next:

8051 architecture notes

Difference between 8086 and 8051

Important 10-mark long answers

Viva questions


You’re covering full syllabus now Sri 😄🔥