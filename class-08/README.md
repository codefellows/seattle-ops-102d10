# Class 08

## Class Outline

1. Ops Overview
1. Review
1. Lecture
1. Demo
1. Lab 


## Overview

Now that Virtualbox is loaded onto your Ubuntu lab PC, you'll be able to create a virtual machine (VM) of any operating system, assuming you can get your hands on the corresponding .iso installer or a premade .ova Virtualbox file. There are legal and ethical considerations to make when seeking out such files. For example, Apple forbids the virtualization of its macOS on non-Apple hardware. For this class, your first VM will be Windows 10, the most common enterprise business desktop used today.

## How does this topic fit?

**Where we've been**:
In the previous class we setup remote connectivity from our personal computer to the lab kit PC.

**What are we focusing on today**:
Today, we'll be be creating a virtual machine with Windows 10.

**Where we're headed**:
Next class will focus on getting familiar with the command line, terminals and core OS.

## Virtualization of Windows OS

<!-- ### Why
- This topic is important because ...
- What problems are we facing that this concept will solve... -->

<!-- ### What
- Concepts and Vocabulary listed here
- Be sure NOT to provide the definitions in this document, students can fill them in as note
- For example:
- REST: A modern way to transfer _____ between 2 systems using the _____ protocol. -->

<!-- ### How
- What does the code we need to write have to do to solve these problems?
- What are some of the major concepts we have to tackle
- Briefly describe the type of work students will be seeing in demo and performing in lab -->

### Experimentation and Discovery Ideas
- Check out the [PCJS Museum](https://www.pcjs.org/software/pcx86/)!
  - PCJS Museum refers to the "PCjs Project," an online museum and emulator platform that allows users to experience vintage computer systems and software in a web browser. 
  - The PCjs Project is a collaborative effort by a group of computer enthusiasts and historians to preserve and provide access to historical computer systems and software.

## Learning Objectives

### Students will be able to

#### Describe and Define

- .iso file
- .ova file
- Virtualbox save state feature
- Virtualbox export/import .ova feature

#### Execute

- Install Windows 10 from a .iso file.
- Allocate resources to a Virtualbox VM.
- Perform snapshot and save state operations on a Virtualbox VM.
- Export a .ova file in Virtualbox, then import a new VM from the .ova file.

## Helpful Resources

- How to deploy your own virtual machine in VirtualBox (ref. [Walkthrough](https://askubuntu.com/questions/142549/how-to-install-ubuntu-on-virtualbox)){:target="_blank"}
- [Windows Media Creation Tool](https://www.microsoft.com/en-us/software-download/windows10){:target="_blank"}
    > For our purposes in class, we will not be activating our installations of Windows. If you have access to activation keys for commercial systems we use in class, feel free to apply them at your discretion.

## Notes

### Windows 10 VM Hardware Allocation Guide

- Memory (RAM)
  - Windows 10 typically requires a minimum of 2 GB of RAM to run smoothly, but for a better experience, it is recommended to allocate at least 4 GB or more to the VM, depending on your available system resources and the workload you plan to run. 
  - If you have a significant amount of RAM on your host machine (e.g., 8 GB or more), allocating 6 GB to 8 GB to the VM would provide a good balance between performance and resource usage.

- CPU
  - The number of virtual CPUs (vCPUs) to allocate depends on the number of physical CPU cores available on your host machine and the workload you intend to run. 
  - It is generally recommended to allocate 1-2 vCPUs to a Windows 10 VM, especially if you have a dual-core or quad-core CPU on your host machine. 
  - If your host machine has a higher core count (e.g., 8 cores or more) and you plan to run CPU-intensive tasks on the VM, you can allocate additional vCPUs to improve performance.

- Hard Disk Space
  - Allocate enough hard disk space to accommodate the Windows 10 installation, along with the applications and data you expect to use on the VM. 
  - Microsoft recommends a minimum of 32 GB of disk space for a Windows 10 installation, but this may not be sufficient if you plan to install additional software or store a significant amount of data. 
  - Allocate at least 50-100 GB of disk space to ensure you have enough room for the VM's needs.

- Graphics
  - For basic usage and everyday tasks, the default virtual graphics adapter provided by VirtualBox should be sufficient. 
  - However, if you plan to run graphics-intensive applications or games, you may want to allocate more video memory to the VM. 
  - In VirtualBox, you can adjust the video memory by going to the VM's settings, selecting "Display," and modifying the "Video Memory" slider. 
  - Allocating 128 MB to 256 MB of video memory should be adequate for most needs.

### VirtualBox Guest Additions

- To achieve fullscreen resolution in a VirtualBox virtual machine, you can install VirtualBox Guest Additions, which provides additional features and drivers for improved integration between the host and guest systems.

Here's how you can install it:
  1. Start the virtual machine in VirtualBox.
  2. From the VirtualBox menu, go to Devices > Insert Guest Additions CD image. This will mount the Guest Additions ISO file to the virtual machine.
  3. Within the virtual machine, open a terminal or command prompt.
  4. Navigate to the mounted CD image directory. You can usually find it at `/media/cdrom` or a similar location.
  5. Run the Guest Additions installer by executing the command `./autorun.sh` (on Linux) or `autorun.exe` (on Windows). This will start the installation process.
  6. Follow the on-screen instructions to complete the installation of Guest Additions.
  7. Once the installation is finished, restart the virtual machine.

- Google also says that you can run: 
  - `sudo apt install virtualbox-guest-additions-iso`

- After installing Guest Additions, you should be able to achieve fullscreen resolution by adjusting the display settings within the virtual machine. This will allow the virtual machine's desktop to match the resolution of your host system, providing a more seamless user experience.