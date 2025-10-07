## ENSE 352 - Fundamentals of Computer Systems Architectures - Laboratory

# Lab 3: Nested Subroutines 

### University of Regina
### Faculty of Engineering and Applied Science - Software Systems Engineering

### Lab Instructor: Cameron Oehler

## Objective

The objective of this lab is to introduce the students to nested subroutines and bit manipulations using the ARM assembly instruction set.


## Background

We know how to call a subroutine and how to return from a subroutine with the following:
- BL  Branch with Link (Call a subroutine) and store the return address in the LR.
- BX LR Branch pack to where the LR is pointing.
What happens if we are in a subroutine and need to call another subroutine whithin this one?  What will happen to the Link Register.  There is an example in this repository to download and run to see how to handle this situation.
 
## Procedure

### Phase 1
Write a subroutine that supports the following features.
- Create a nested subroutine that uses R0 as the input and R1 as the register that will contain the return information (the answer). The function of the subroutine is to determine if bit 11 is a 1 or a 0.  R1 will contain the answer (1 for true and 0 for false).
- Create a nested subroutine that uses R0 as the input.  This subroutine will be responsible for setting bit 3 and clearing bit 7.  All other bits shall be left undisturbed.
- Create a nested subroutine that uses R0 as the input register and R1 as the register that will contain the return information (the answer).  The function of the subroutine shall be to count the number of 1's that are resident in R0 (the input).  Count the 1's and put the answer in R1.


### Phase 2
Write a subroutine that meets the following requirements:
- rot_left_right1 that takes a general purpose register as an input.
- Rotates Left or Right the lower 16 bits(without touching the upper 16 bits). 
- The amount to rotate is given in a second  input register, bits 3:0.
- The direction to rotate is given in bit 5 of this second input register.  {1} means rotate left, {0} means rotate right. 
- The result shall be returned in a register of your choice and the original contents
of the input register shall be unchanged by the function.
- For example, if you call your function with an input register =0x12345678 and the rotate amount in the second register =1 in bits 3:0 and the bit 5 = 1, the result in the original register will be rotated left by 1 bit: input register is =0x1234ACF0.
If the user provides a rotate value of 0, then the function should return the original
integer unchanged.


## Submission
Submit your *.s code to URCourses and be prepared to demonstrate your solution.
