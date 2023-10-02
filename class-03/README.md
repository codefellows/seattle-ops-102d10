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
- CMOS Battery: A small battery on the computer's motherboard that provides power to the CMOS memory, allowing it to retain configuration data when the computer is powered off.
- Firmware: Software that is permanently stored in a computer's memory and is responsible for basic hardware initialization during the booting process.
- POST (Power-On Self-Test): A diagnostic process performed by the BIOS during startup to check the computer's hardware components for errors.
- UEFI (Unified Extensible Firmware Interface): A modern replacement for traditional BIOS firmware, providing advanced features and security options for booting a computer.
- Boot Order: The sequence in which the computer checks different boot devices (such as hard drives, SSDs, optical drives, USB drives) to find the operating system to load.
- Boot Loader: A program or component that loads the operating system into the computer's memory during the boot process.
- Boot Menu: A menu that allows users to manually select a boot device or boot from different storage options.
- BIOS Updates: Software patches or updates provided by the motherboard manufacturer to improve system stability, compatibility, and security.
- Error Codes: Numeric or alphanumeric codes displayed during the POST process to indicate specific hardware issues.

### How
- CMOS, startup sequences, and BIOS are interconnected components that work together to ensure a computer system boots up correctly and operates smoothly. Here's how they work together:
  - Power On
    - When you power on the computer, the BIOS firmware is activated.
  - POST (Power-On Self-Test)
    - The BIOS performs a series of tests on the hardware components to ensure they are functioning correctly. It uses the configuration data stored in CMOS to initialize these components.
  - CMOS Configuration
    - The BIOS reads the CMOS settings to configure the hardware according to the user-defined parameters, such as CPU speed, RAM timings, and boot order.
  - Startup Sequence
    - Based on the boot order specified in CMOS, the BIOS attempts to load the operating system from the designated boot device. If successful, the operating system is loaded into the computer's memory, and the computer becomes operational.
- The work we do on our lab computers today will setup our cyber range for labs in the future courses.

### Experimentation and Discovery Ideas
- Imagine a scenario where a computer doesn’t follow its regular startup sequence. What factors could be at play, and how might understanding CMOS settings help diagnose the issue?
- In the context of experimentation, how could a deep understanding of CMOS configurations open avenues for innovative projects? Can you think of any experimental setups where tweaking these settings might yield intriguing results?
- Considering the role of CMOS in retaining system configurations, how might this feature influence long-term experiments? What challenges and opportunities arise when experiments span extended periods?
- Exploring the concept of boot order, how might experimenting with different boot devices impact the outcome of computational experiments? What creative possibilities emerge when we manipulate the sequence in unconventional ways?

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

- What connection does the BIOS have to the CMOS battery?
- Why is the CMOS battery necessary?
- Where can the CMOS battery be found?
- Create a flowchart that shows the startup sequence for a typical computer.
- What happens if the CMOS battery dies?
- How do you find out what key(s) to press to enter BIOS?
- What does a CMOS jumper do?
- What do all the different settings in BIOS do? Make a list and explain them.