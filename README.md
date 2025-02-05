# COBOL REDEFINES Misuse Leading to Unexpected Data Overwrites
This example demonstrates a common error in COBOL programs involving the REDEFINES clause. The REDEFINES clause allows multiple data structures to share the same memory location.  However, careless use can lead to unexpected data overwrites and program errors.  The provided code showcases this potential pitfall and its solution.

## Bug Description:
The bug lies in the assumption that changes made to a redefined field (WS-SUB-AREA-1) will automatically update the original field (WS-AREA-1) and vice-versa.  This is not always the case. Modifying one field might unexpectedly change the others in ways not immediately apparent.

## Solution Description:
The solution demonstrates a more careful approach to managing redefined fields.  It highlights the need to either avoid overwriting data unintentionally or to account for those overwrites in the program logic. 

## How to Reproduce the Bug:
Compile and run the `bug.cob` program. Observe the output of WS-AREA-1 after changing WS-SUB-AREA-1. The unexpected result reveals the bug.

## How to Solve the Bug:
Refer to the `bugSolution.cob` program for a more robust solution, avoiding the potential for unintended data overwrites.