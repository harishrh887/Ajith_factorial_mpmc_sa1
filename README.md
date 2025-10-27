

## AIM
To 

---

## APPARATUS REQUIRED
- Personal computer with dosbox software

---

## ALGORITHM



---

## PROGRAM
```asm
ORG 0000H
 ARRAY:  DB 25H, 12H, 45H, 78H, 56H, 9AH, 3CH, 5EH  
N       EQU 08H                                    
TARGET  EQU 30H                                  
MAIN:
        MOV  R0, #ARRAY       
        MOV  R1, #N           
        MOV  A, #TARGET
 SEARCH_LOOP:
        MOV  B, @R0           
        CJNE A, B, NEXT       
        SJMP FOUND            
        INC  R0               
        DJNZ R1, SEARCH_LOOP
		NOT_FOUND:
        MOV  P1, #00H        
        SJMP END_PROGRAM     
FOUND:
        MOV  P1, #0FFH      
END_PROGRAM:
        SJMP END_PROGRAM
		
END

```
OUTPUT



---


RESULT

Thus, the factorial of a number was calculated and executed successfully using 8086.

---


