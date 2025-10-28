## ENSE 352 - Fundamentals of Computer Systems Architectures - Laboratory

# Lab 5: Introduction to C Projects with 384 Board

### University of Regina
### Faculty of Engineering and Applied Science - Software Systems Engineering

### Lab Instructor: Cameron Oehler

## Objective

The objective of this lab is to introduce the students to building a C project and interface to buttons and switches from their 384 hardware build (bread board).

## Background

General Purpose Input/Output (GPIO) refers to the use of logic level pins on the microcontroller device to connect to user input and output devices. It is often referred to as parallel I/O since multiple inputs or outputs appear in common registers inside the device. Reading a group of switches may be as simple as reading the value contained in one device register and driving outputs might be as simple as writing values to corresponding device registers.

Notice from the schematic that the LED’s and Switch are located on certain Port pins. In order to use these I/O lines you will need to first turn on the clocks for these ports.

Now that you are providing a clocking source to your I/O lines you must configure the lines to support what is connected to them. Remember that LED’s are outputs and switches or buttons are inputs. Notice that we need to configure outputs as max speed 50MHz, general purpose output push-pull. The input lines are configured as input mode, floating input.

## Procedure

### Phase 1
Last week you configured the onboard button to control the onboard LED. Repeat this but using a C project.

### Phase 2
If you have not done so already, use the parts from your electronics course to build the circuit from the schematic provided on URCourses. There is also a video for your resource on URCourses.

### Phase 3
Once the circuit is built, write the code such that each button will control a corresponding LED like a light switch.
