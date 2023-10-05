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

### Why
- Windows OS is one of the most widely used operating systems globally. Many businesses, educational institutions, and government organizations use Windows-based computers. Learning how to navigate Windows ensures you can use computers in various settings.
- Many software applications and games are developed for Windows. By being proficient in using Windows, you can access and use a wide range of software without compatibility issues.
- Windows OS provides a user-friendly interface and a variety of productivity tools such as Microsoft Office suite, which includes Word, Excel, and PowerPoint. Proficiency in these tools is often a requirement in many job positions.
- There is a vast amount of online resources, tutorials, and support available for Windows users. Knowing how to use Windows means you can access these resources to troubleshoot issues and learn new skills.
- Windows OS offers built-in networking features that make it easier to connect computers to the internet, share files and printers, and set up home networks.
- Many job roles require proficiency in using Windows-based applications. Having Windows skills can enhance your employability and open up various career opportunities in fields such as IT support, software development, data analysis, and more.

### What
- Graphical User Interface (GUI): A visual way of interacting with the computer using graphical elements such as windows, icons, buttons, and menus.
- Desktop: The primary screen area that you see after logging into Windows, where you can place icons for applications, files, and shortcuts.
- Start Menu: A menu in Windows that provides access to various programs, settings, and features.
- Taskbar: The bar usually located at the bottom of the screen in Windows, displaying open applications and providing quick access to certain features.
- File Explorer: A file management application in Windows used to browse files, folders, and drives on your computer.
- Shortcut: An icon or link that points to a file, folder, application, or website, providing quick access to the target resource.
- Control Panel: A centralized configuration area in Windows where users can modify system settings and install or uninstall software.
- Windows Update: A feature that allows Windows users to download and install security updates, patches, and feature enhancements from Microsoft.
- Task Manager: A system monitor and management tool in Windows that provides information about running applications and processes, and allows users to terminate them if necessary.
- User Account: A user's personal space on a computer, containing settings, files, and preferences specific to that user.
- File Extension: A suffix at the end of a filename, indicating the format or type of a file (e.g., .docx for Microsoft Word documents, .jpg for image files).
- Driver: Software that allows the operating system to communicate with hardware devices such as printers, graphics cards, and network adapters.
- Registry: A hierarchical database used to store configuration data in Windows operating systems.
- Firewall: A security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules.
- Antivirus: Software designed to detect, prevent, and remove malicious software (malware) from a computer system.
- Backup: Creating a copy of important files and data to prevent loss in case of hardware failure, data corruption, or accidental deletion.
- System Restore: A feature in Windows that allows users to revert their computer's state (system files, programs, and registry settings) to a previous point in time.

### How
The Windows operating system consists of several layers, each serving specific functions and interacting with one another to provide a complete computing environment. Here are the fundamental layers of the Windows OS, starting from the lowest level (closest to the hardware) to the highest level (user interface and applications):
- Hardware Layer:
  - This layer comprises the physical hardware components of the computer, including the CPU, memory (RAM), storage devices (hard drives, SSDs), input/output devices (keyboard, mouse, monitor), and network interfaces.
- Kernel:
  - The kernel is the core component of the operating system. It acts as an intermediary between hardware and software, managing system resources, providing essential services (such as process management, memory management, device drivers, and file system access), and ensuring security and stability.
- Device Drivers:
  - Device drivers are specialized programs that allow the operating system to communicate with specific hardware devices. These drivers act as translators, enabling the kernel and the hardware to understand each other. Windows includes a vast library of built-in drivers and can also install additional drivers for new hardware components.
- Executive Services Layer:
  - The executive services layer provides higher-level system services, such as input/output management, process and thread management, security, and error handling. It extends the functionalities of the kernel and supports the operating system's core operations.
- Win32 Subsystem:
  - The Win32 subsystem provides the Win32 API (Application Programming Interface), which is a set of programming instructions and standards for creating Windows applications. It includes graphical components and functions for creating windows, menus, buttons, and other graphical elements. Most Windows applications are built using the Win32 API.
- User Mode Applications:
  - User mode applications are the programs that users interact with directly. These include word processors, web browsers, games, and other software applications. User mode applications make use of the services provided by the underlying layers through system calls, accessing resources and functionalities while being isolated from the kernel for security and stability reasons.
- User Interface:
  - The user interface layer encompasses the graphical elements users interact with, such as the desktop, Start menu, taskbar, windows, icons, buttons, and other visual components. This layer provides the user experience, allowing users to interact with applications and the operating system intuitively.

### Experimentation and Discovery Ideas
- Reflecting on the concept of user experience in Windows, how do you think the balance between customization and standardization affects the way users interact with the OS? Can you think of any real-world examples where too much customization might lead to confusion or inefficiency for users?
- Considering the rapid advancements in technology, what potential future innovations do you foresee in the Windows operating system or any operating system in general? How might these innovations open new avenues for experimentation and discovery in the realms of artificial intelligence, cybersecurity, or human-computer interaction?

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

- Professor Messer:
  - [An Overview of Windows](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/an-overview-of-windows-220-1102/){:target="_blank"}
  - [Windows Features](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/windows-features-220-1102/){:target="_blank"}
  - [Windows Upgrades](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/windows-upgrades-220-1102/){:target="_blank"}
  - [Troubleshooting Windows](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/troubleshooting-windows-220-1102/){:target="_blank"}
- How to deploy your own virtual machine in VirtualBox (ref. [Walkthrough](https://askubuntu.com/questions/142549/how-to-install-ubuntu-on-virtualbox)){:target="_blank"}
- [Windows Media Creation Tool](https://www.microsoft.com/en-us/software-download/windows10){:target="_blank"}
    > For our purposes in class, we will not be activating our installations of Windows. If you have access to activation keys for commercial systems we use in class, feel free to apply them at your discretion.
- Check out the [PCJS Museum](https://www.pcjs.org/software/pcx86/)!
  - PCJS Museum refers to the "PCjs Project," an online museum and emulator platform that allows users to experience vintage computer systems and software in a web browser. 
  - The PCjs Project is a collaborative effort by a group of computer enthusiasts and historians to preserve and provide access to historical computer systems and software.

## Notes

### VirtualBox Guest Additions
To achieve fullscreen resolution in a VirtualBox virtual machine, you can install VirtualBox Guest Additions, which provides additional features and drivers for improved integration between the host and guest systems.

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