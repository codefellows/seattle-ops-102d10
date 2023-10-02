# Class 03

## Class Outline

1. Ops 102 Overview
1. Review
1. Lecture
1. Demo
1. Lab 

## Overview

Today we’re taking a closer look at the startup sequence of a computer. Familiarity with the “lower level” operations of a computer will be very relevant to a support technician who encounters various issues with computers and must isolate problems, and who also may be reconfiguring hardware components such as hard drives. This lab will be very much sandbox learning; students will likely encounter all sorts of problems.

## How does this topic fit?

**Where we've been**:
In the previous class we upgraded and reassembled our lab computers.

**What are we focusing on today**:
Today, we'll be configuring the boot order sequence in the BIOS.

**Where we're headed**:
Next class will focus on installing Ubuntu OS to your lab computer.

## CMOS, Startup Sequences and BIOS

### Why
- CMOS, startup sequences, and BIOS are important topics to learn because they are essential for understanding how a computer boots up and how the BIOS settings control the basic functions of the motherboard. By understanding these concepts, you can troubleshoot problems with your computer and make informed decisions about how to configure your BIOS settings.
- If your computer is booting into the wrong device, you can change the boot order in BIOS. This can be helpful if you have multiple storage devices connected to your computer and you want to boot from a specific one.
- If a feature is not configured on your motherboard, such as virtualization support, you can enable it in BIOS. This can be helpful if you want to use a feature that is not enabled by default.
- If you want to overclock your CPU, you can do so in BIOS. Overclocking is the process of increasing the clock speed of your CPU. This can improve the performance of your computer, but it can also increase the heat output and instability of your system.
- If you make a change in BIOS that causes your computer to not boot up properly, you can reset the CMOS to restore the BIOS settings to their default values. This can be helpful if you are not sure what caused the problem and you want to start over.

### What
- What connection does the BIOS have to the CMOS battery?
- Why is the CMOS battery necessary?
- Where can the CMOS battery be found?

### How
- Continuing to work in the lowest level of abstraction, we will work hands-on with our CMOS battery in an effort to reset the BIOS settings.
- The work we do on our lab computers today will setup our cyber range for labs in the future courses.

### Experimentation and Discovery Ideas
- Create a flowchart that shows the startup sequence for a typical computer.
- What happens if the CMOS battery dies?
- How do you find out what key(s) to press to enter BIOS?
- What does a CMOS jumper do?
- What do all the different settings in BIOS do? Make a list and explain them.

## Learning Objectives

### Students will be able to

#### Describe and Define

- ROM
- BIOS
- CMOS Battery
- Startup Sequence
- POST

#### Execute

- Operate BIOS
- Choose boot options BIOS vs Legacy
- Assign device priority chain

## Helpful Resources

- [Future Learn](https://www.futurelearn.com/courses/computer-systems/0/steps/53497){:target="_blank"}
- [What happens when I turn on the computer?](https://www.geeksforgeeks.org/what-happens-when-we-turn-on-computer/){:target="_blank"}
- [Prowler Boot Sector Virus](https://www.youtube.com/watch?v=fSL4J0zhMcY){:target="_blank"}
- [Lenovo BIOS Simulator](https://support.lenovo.com/us/en/solutions/HT502745)
  - Try out the IdeaCentre 310-15ASR (90G5).

## Notes

- List 1 new thing that you learned today.