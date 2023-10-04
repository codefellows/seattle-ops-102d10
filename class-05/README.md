# Class 05

## Class Outline

1. Ops 102 Overview
1. Review
1. Lecture
1. Demo
1. Lab 

## Overview

In order to effectively utilize Ubuntu Linux as a virtualization server, you'll need to get comfortable using the Linux terminal. While many operations can be performed using the desktop graphical user interface (GUI), basic Linux terminal skills are generally expected of Ops professionals.

## How does this topic fit?

**Where we've been**:
In the previous class we installed the Ubuntu OS onto our lab computers.

**What are we focusing on today**:
Today, we'll be updating and installing packages and apps you will need throughout the upcoming courses.

**Where we're headed**:
Next class will focus on setting up our SOHO network using our lab router.

## Installing Virtualbox with Linux Terminal

### Why
- VirtualBox allows users to create virtual machines with different operating systems. This is important for computer engineers to ensure their applications work on various platforms without the need for multiple physical machines.
- Virtual machines created with VirtualBox are isolated from the host system. This isolation provides a secure environment for testing potentially harmful software, suspicious files, or websites. If anything goes wrong, it won't affect the host system.
- Some older software applications may not be compatible with the latest hardware or operating systems. VirtualBox allows running legacy software in virtual machines, ensuring that older applications can still be used and tested without the need for outdated hardware.
- Virtual machines can be configured to use specific amounts of CPU, memory, and disk space. This means you can run multiple virtual machines on a single physical host, optimizing hardware resources and reducing costs associated with maintaining multiple physical systems.
- VirtualBox provides a safe environment for learning about different operating systems. Users can experiment, break things, and learn without any risk to their main system. This is particularly useful for students and IT professionals who want to enhance their skills in a risk-free environment.
- VirtualBox can be utilized to create virtual server environments, such as instances running Ubuntu Server or Windows Server. This capability allows users to set up and manage multiple server systems within virtual machines, enabling efficient testing, development, and deployment of server-based applications and services.
- Virtual machines can be easily cloned, making it convenient to set up new instances for testing or development. Additionally, VirtualBox allows users to take snapshots of virtual machines, capturing their current state. This is invaluable for testing different configurations or software setups and reverting to a known state if something goes wrong.

### What
- Virtualization: The process of creating a virtual version of a resource, such as a server, storage device, network, or operating system, using software rather than a physical entity.
- Virtual Machine (VM): A software-based emulation of a computer system, which runs applications and programs as if they were running on a physical computer.
- Hypervisor: Software or hardware that enables the creation and management of virtual machines. Examples include VMware, Hyper-V, and VirtualBox.
- Host System: The physical computer or server on which the virtualization software is installed and runs virtual machines.
- Guest System: The virtual operating system running within a virtual machine.
- Snapshot: A saved state of a virtual machine at a specific point in time, allowing users to revert to that state if needed.
- Clone: A duplicate copy of a virtual machine, allowing users to create identical VMs for various purposes.
- Isolation: The separation of virtual machines from each other and from the host system to prevent interference and ensure security.
- Resource Allocation: The process of assigning specific resources, such as CPU, memory, and storage, to virtual machines.
- Server Consolidation: The practice of combining multiple servers into a single physical machine using virtualization technology.
- Sandboxing: Isolating an application or process within a secure environment to prevent it from affecting other parts of the system.
- Networking Modes: Different modes in which virtual machines can be connected to the network, such as NAT (Network Address Translation), Bridged, and Host-Only networking.
- Package Manager: A tool for installing, updating, and managing software packages on a Linux system.
- Update/Upgrade: Update downloads package information, while upgrade installs newer versions of packages.
- Dependency: A necessary software component required by another package to function properly.
- Terminal/Shell: The command-line interface for interacting with the operating system.
- Installation Command: A specific command used to install packages on Linux, such as `apt-get install`.
- Root/Superuser: The administrative user in Linux with elevated privileges, accessed using `sudo`.
- Guest Additions: Additional software enhancing performance and integration between VirtualBox host and guest systems.

### How
VirtualBox creates virtual machines by employing a technique called **hardware virtualization**. Here's a simplified explanation of how it works:
- Hypervisor:
  - VirtualBox acts as a hypervisor. A hypervisor is a software or hardware component that allows multiple operating systems to share a single hardware host. In the case of VirtualBox, it's a type 2 or hosted hypervisor, meaning it runs on top of an existing operating system (your Linux host system, for instance).
- Guest Operating System:
  - When you create a new virtual machine, you specify the guest operating system you want to install (such as Ubuntu, Windows, etc.). VirtualBox provides a virtual platform to this guest operating system, making it think it's running on real hardware.
- Emulated Hardware:
  - VirtualBox emulates a complete set of hardware devices to the guest operating system. This emulated hardware includes a virtual CPU (central processing unit), virtual RAM (memory), virtual storage controllers (hard drives), virtual network interfaces, and more. These virtual components are presented to the guest OS as if they were physical hardware.
- Binary Translation:
  - When the guest operating system sends instructions to the CPU, VirtualBox intercepts these instructions. If the instructions are privileged (i.e., they access hardware directly), VirtualBox translates these instructions into instructions that can be executed on the host system. This process is binary translation. It ensures that the guest OS can run without modifying its code, making it compatible with the virtual environment.
- Resource Management:
  - VirtualBox also manages the allocation of host system resources such as CPU cycles, memory, and disk space to the virtual machine. It ensures that these resources are shared efficiently among all running virtual machines.
- I/O Handling:
  - VirtualBox intercepts input/output (I/O) operations from the guest OS. For example, when the guest OS wants to write data to the virtual hard drive, VirtualBox handles this operation and writes the data to the actual physical hard drive of the host system.
- Display and User Interaction:
  - VirtualBox provides a virtual display for the guest OS. It captures graphical output from the guest OS and renders it on the host system's display. Users interact with the virtual machine through this interface, and VirtualBox translates user input (keyboard, mouse, etc.) back to the guest OS.

### Experimentation and Discovery Ideas
- In the spirit of experimentation, how might the use of VirtualBox on Linux contribute to environmental sustainability and resource conservation? Can virtualization technologies play a role in reducing the need for physical hardware, and what impact could this have globally?
- Reflecting on the principles of open-source software, how does the availability of VirtualBox as open-source technology align with the ethos of the Linux community? In what ways might this influence collaborative experimentation and knowledge sharing?
- In the context of lifelong learning, how might experimenting with VirtualBox on Linux serve as a foundation for continuous exploration and skill development? Can you envision this knowledge leading to future discoveries in related fields?
- How does the process of discovery in experimenting with VirtualBox on Linux parallel the scientific method? What similarities can you identify in terms of hypothesis formulation, experimentation, observation, and drawing conclusions?
- Virtualization often involves the concept of 'snapshotting,' allowing users to save a virtual machine's state at a particular moment. Why might this feature be crucial in software development and system administration? Can you think of real-world scenarios where this could prevent significant issues or enhance efficiency?
- Imagine a future where virtualization technology continues to advance. How might virtualization shape our interactions with computers and digital environments in the next decade? What ethical dilemmas or societal changes could arise from these potential advancements?

## Learning Objectives

### Students will be able to

#### Describe and Define

- Virtualization
- Containers
- Docker
- Kubernetes
- Virtual box
- Terminal
- CLI
- APT

#### Execute

- Perform basic navigation in terminal.
- Manage software packages using the APT package manager.
- Use APT to install Virtualbox and its Extension pack.
- View system specs in terminal.

## Helpful Resources

- [Professor Messer - Linux Commands](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/linux-commands-220-1102/)
- [Linux Command Line for Beginners](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview){:target="_blank"}
- [Linux Commands for Linux Beginners](https://www.howtouselinux.com/post/linux-commands-for-linux-beginners-cheat-sheet){:target="_blank"}
- [Advanced Package Tool for Linux](https://www.poftut.com/what-is-apt-advanced-package-tool-for-linux/){:target="_blank"}
- [How to Install Virtualbox on Ubuntu](https://itsfoss.com/install-virtualbox-ubuntu/){:target="_blank"}

## Notes

### Linux Commands
- `CTRL+C`
  - Press and hold the `CTRL` key on your keyboard, then press the `C` key while still holding the `CTRL` key down.
    - Macs `CTRL` key says `control` on it.
  - Used to break out of a running process or terminate a command.
  - Provides a quick and convenient way to stop a process that might be taking longer than expected.

- `pwd`
  - Stands for "print working directory" and displays the current location in your file system.
  - Helpful for knowing where you are within the directory structure.

- `ls`
  - Lists the files and directories contained in the current directory.

- `ls -al`
  - Provides more detailed information about the files, such as permissions, ownership, and file sizes.

- `cd [path]`
  - Used to change the directory you are currently in.
  - By specifying the desired path, you can navigate to different directories within the file system.

- `mkdir [dirname]`
  - Used to create a new directory.
  - By specifying a directory name after the command, you can quickly create a new folder.

- `touch [file name]`
  - Used to create a new file.
  - By specifying a file name after the command, you can create an empty file with that name.

- `sudo [command]`
  - Used to elevate your command to root or superuser privileges.
  - After entering the sudo command, you will be prompted to enter the root password to execute the command with elevated privileges.

- `[command name] -[modifier/flag parameter] [target/action parameter]`
  - This is the general syntax for performing an action with a command in the Linux terminal.
  - You can use various commands with specific flags or modifiers to perform different actions on specific targets.
