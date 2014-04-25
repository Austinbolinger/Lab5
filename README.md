Lab5
==============

#Design
When tested, my program did match the program given below.

![Program 1](https://github.com/Austinbolinger/Lab5/blob/master/program1.JPG?raw=true "Program 1")

A step by step is as follows:

1) Loads value 8 into the accumulator

2) Adds 1 to 8

3) Outputs the answer to port 3

4) Now, if the value in the accumulator is negative, the next step is to jump back up to the add 1 protion in step 2

5) Otherwise, the program jumps to the jump locator which is pointing at its own self and just stays at the value it is currently.

This just loads the input and than repeatedly adds one to the number and starts back over at 0 when it passes F. This just cycles through the memory.

![instructions from 000-100ns](https://github.com/Austinbolinger/Lab5/blob/master/instructions0-100ns.JPG?raw=true "instructions from 000-100ns")

![instructions from 100-200ns](https://github.com/Austinbolinger/Lab5/blob/master/instructions100-200ns.JPG?raw=true "instructions from 100-200ns")


##Questions
1. When the controller's current state is "FETCH," what is the status of the following control lines: a) PCLd - . b) IRLd - . c) ACCLd .

2. The current state is LoAddr and the IR contains “OUT.”  What are the control signals are asserted, and what will the next state be?

3. What are the three status signals sent from the PRISM datapath to the PRISM controller?

4. Why is it important that ACCLd signal be active during the execute state for the ADDI instruction?

5. What changes are necessary to the PRISM datapath to add another instruction (SUBI, which would subtract an immediate value from the accumulator) to the instruction set?


This is the code used to program the FPGA
https://github.com/Austinbolinger/Lab5/blob/master/part1.bit

####Data Checked
24 APR 14 - Part 1 checked in class: full functionality

#####Documentation
C3C Pluger helped me understand how fetch and the others work based on the state diagram from the lab handout.
