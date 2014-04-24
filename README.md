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


This is the code used to program the FPGA
https://github.com/Austinbolinger/Lab5/blob/master/pinout.ucf

####Data Checked


#####Documentation

