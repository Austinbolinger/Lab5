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
1. When the controller's current state is "FETCH," what is the status of the following control lines: a) PCLd - 1. b) IRLd - 1. c) ACCLd 0.

2. The current state is LoAddr and the IR contains “OUT.”  What are the control signals are asserted, and what will the next state be?
MarLoLd, MemSel, R/W, and PCLd are asserted while the next state is Direct IO Execute.

3. What are the three status signals sent from the PRISM datapath to the PRISM controller?
IR, Add, Data

4. Why is it important that ACCLd signal be active during the execute state for the ADDI instruction?
So that the Accumulator can be loaded and the add function can use it. Otherwise it ######will ######not ######change
what is on the accumulator and the add function will have been useless. 

5. What changes are necessary to the PRISM datapath to add another instruction (SUBI, which would subtract an immediate value from the accumulator) to the instruction set?
You would have to change the number of bits in the OpSel so that it could handle more than 8 options, or you could make some changes to the add funtion. If you added some sort of flip flop mux to the that function with a SubiLd you could choose to add normal or add the opposite of what you would subtract. For example, if you wanted to subtract one, you could add F. 

This is the code used to program the FPGA for part 1
https://github.com/Austinbolinger/Lab5/blob/master/part1.bit

This is the code used to program the FPGA for part 2
https://github.com/Austinbolinger/Lab5/blob/master/part2.bit
Here is the code for the PRISM program
https://github.com/Austinbolinger/Lab5/blob/master/part2.b.psm

####Data Checked
24 APR 14 - Part 1 checked in class: full functionality
25 APR 14 - Part 2 checked : full functionality

#####Documentation
C3C Pluger helped me understand how fetch and the others work based on the state diagram from the lab handout.
