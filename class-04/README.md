# Class 04

## Class Outline

1. Ops 102 Overview
1. Review
1. Lecture
1. Demo
1. Lab 

## Overview

Your home lab PC will be acting as a virtualization server for the duration of the Ops sequence. For this reason, we'll be using Ubuntu Linux as the computer's base operating system to capitalize on its lightweight, resource-efficient performance. We can later use the software application, Virtualbox, to "spin up" any other operating systems we may need, such as Windows 10.

## How does this topic fit?

**Where we've been**:
In the previous class we removed the CMOS battery to clear previous BIOS settings so that we could reconfigure them.

**What are we focusing on today**:
Today, we'll be installing the Ubuntu OS onto our lab computers.

**Where we're headed**:
Next class will focus on updating your OS and installing applications.

## Installing Ubuntu Linux OS

### Why
- When you need to install a new operating system on your computer, especially if your computer doesn't have an optical drive (CD/DVD drive), creating a bootable USB drive is essential. A bootable USB drive allows you to install or reinstall an operating system easily and efficiently.
- If your computer encounters issues and cannot boot normally, a bootable USB drive can provide access to various diagnostic and repair tools. Using a bootable USB drive, you can access tools like antivirus scanners, disk repair utilities, and recovery options to diagnose and fix problems.
- Proprietary software often restricts users in terms of usage, customization, and sharing knowledge. Ubuntu Linux is open source, promoting the free exchange of ideas and collaborative development. It allows users to view, modify, and distribute the source code, fostering a culture of innovation and community support.
- Proprietary operating systems and software can be costly, especially for businesses and individuals with limited budgets. Ubuntu Linux is free to use. It provides a powerful, stable, and secure operating system without the licensing fees, making it an excellent cost-effective alternative for businesses, educational institutions, and individuals.
- Security vulnerabilities and privacy concerns are prevalent in the digital age. Ubuntu Linux benefits from strong security measures, regular updates, and a robust permission system. It is less susceptible to malware and viruses commonly affecting other operating systems, enhancing user security and privacy.
- Engineers often need access to a wide array of programming languages, tools, and libraries, some of which might not be readily available on proprietary platforms. Ubuntu Linux provides robust support for software development, offering a vast repository of development tools, libraries, and compilers. It also supports a wide range of programming languages, fostering a thriving developer community.
- Many servers and cloud platforms are powered by Linux-based systems. Familiarity with Linux is crucial for server administrators and cloud professionals. Ubuntu Linux serves as a valuable introduction to server management and cloud computing. It prepares professionals for careers in IT infrastructure, cloud computing, and system administration.

### What
- Linux: The open-source Unix-like operating system kernel on which Ubuntu is based.
- Ubuntu: A popular, user-friendly Linux distribution based on Debian.
- Distribution (Distro): A specific version or variant of Linux, such as Ubuntu, Fedora, or Debian.
- Open Source: Software that is freely available for anyone to use, modify, and distribute.
- Kernel: The core component of an operating system that manages hardware resources and provides essential services for computer programs.
- GUI (Graphical User Interface): A visual way of interacting with the computer using windows, icons, buttons, and menus, as opposed to text-based interfaces.
- Driver: A software component that allows the operating system to communicate with hardware devices.
- Partition: A portion of a hard drive that functions as a separate unit, allowing the installation of different operating systems or organizing data.
- Dual Boot: A configuration that allows a computer to run two different operating systems, such as Ubuntu Linux and Windows, on the same machine.
- ISO Image: A file that contains an exact copy of a bootable CD or DVD. It is used to create bootable USB drives or burn installation discs.

### How 
- BIOS/UEFI Initialization:
  - On startup, the BIOS/UEFI firmware activates, initializing hardware like the processor, memory, and storage devices.
- Boot Sequence:
  - BIOS/UEFI checks boot devices based on defined order. A bootable USB is detected if it contains valid boot files.
- Loading Bootloader (GRUB):
  - Bootable USB triggers GRUB (Grand Unified Bootloader) to load Linux kernel and initial RAM disk (initrd).
- Loading Linux Kernel and Initrd:
  - Kernel, OS core, loads drivers for hardware and initrd mounts temporary file system for essential modules.
- Detecting Hardware and Drivers:
  - Kernel loads drivers for hardware components like hard drives, graphics, and network adapters.
- Mounting Root File System:
  - Kernel mounts root file system (usually Ext4) on the computer's hard drive or SSD.
- Starting Installation:
  - Ubuntu installation begins, guiding users through options, partition creation, and file copying from USB.
- Writing Bootloader (GRUB):
  - GRUB is installed on the computer, configured to offer Ubuntu or other OS options during boot.
- Finishing Installation and Reboot:
  - Installation completes, prompting USB removal. After reboot, GRUB menu appears.
- Post-Installation Setup:
  - Choose Ubuntu or other OS from GRUB, proceed with user setup, network configuration, and software installation.

### Experimentation and Discovery Ideas
- Why might someone choose to install Ubuntu Linux from a bootable USB drive rather than using traditional installation methods?
- When we talk about "bootable" USB drives, what fundamental principles of computer science are at play? How does the computer recognize and prioritize bootable devices?
- Reflect on the significance of choosing Ubuntu, an open-source operating system, for this installation method. How does the philosophy of open-source software align with the concept of experimentation and discovery? 
- During the installation process, various choices are presented, such as partitioning the hard drive. How might these choices impact the performance and usability of the Ubuntu system? What experimentation could one conduct to optimize these choices?
- Consider the role of GRUB (Grand Unified Bootloader) in this process. How does GRUB facilitate experimentation, allowing users to choose between different operating systems during boot? What happens if GRUB malfunctions, and how might one troubleshoot this?
- Reflect on the potential challenges users might face while installing Ubuntu from a USB drive. How might these challenges promote problem-solving skills and resilience? What resources could one explore when encountering difficulties? 

## Learning Objectives

### Students will be able to

#### Describe and Define

- OS
- Ubuntu Linux
- Bootable USB
- Distribution/distro
  - Mostly applies to Linux.
  - Examples: Ubuntu, Red Hat, Kali

#### Execute

- Install/uninstall the Ubuntu Linux OS using bootable physical media

## Helpful Resources

- [Download Ubuntu Desktop](https://ubuntu.com/download/desktop){:target="_blank"}
- Professor Messer:
  - [Linux Commands](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/linux-commands-220-1102/)
  - [Linux Features](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/linux-features-220-1102/)
  - [Installing Operating Systems](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/installing-operating-systems-comptia-a-220-1102-1-9/)
- [CompTIA Linux+ Certificate](https://www.comptia.org/certifications/linux){:target="_blank"}
- [Linux Journey](linuxjourney.com){:target="_blank"}
- [TryHackMe](https://tryhackme.com/hacktivities?tab=search&page=1&free=all&order=most-popular&difficulty=all&type=all&searchTxt=Linux){:target="_blank"}

## Notes

- What is the purpose of running Ubuntu on our lab computers?
- What is the software that creates the bootable Ubuntu USB drive called?
- What does "LTS" mean?
- Do you need to change the boot order after Ubuntu has been installed? Why or why not?
- Why do operating systems have versions?
- What are the differences between Windows Home and Windows Pro editions?