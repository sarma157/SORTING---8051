
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**
![WhatsApp Image 2025-10-24 at 09 44 31_6b2c9b38](https://github.com/user-attachments/assets/96aba8b1-3eb1-458a-8a27-73dff74c586c)

**MEMORY WINDOW:**

Before execution: D:0x40H:
<img width="1917" height="986" alt="descending before" src="https://github.com/user-attachments/assets/ebf3939b-6aca-4415-9b91-a7a1885b26ac" />

After execution: D:0x40H:
<img width="1918" height="982" alt="descending after" src="https://github.com/user-attachments/assets/86b9b865-215d-4ed1-8815-5eb72416ed42" />



**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**
![WhatsApp Image 2025-10-24 at 09 44 31_299e17b2](https://github.com/user-attachments/assets/f3e192d9-fc80-4b14-a73d-a066ce16f5ef)

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<img width="1917" height="987" alt="assending before" src="https://github.com/user-attachments/assets/8233c0e8-ada2-4c24-8493-5a2cf000d4bf" />

After execution:
D:0x40H:
<img width="1917" height="987" alt="asss  after" src="https://github.com/user-attachments/assets/882b8b6f-2fcc-45be-ae5d-a0309075f06a" />

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

