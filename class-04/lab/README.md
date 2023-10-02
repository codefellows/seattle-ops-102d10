# Lab: Installing Ubuntu Linux OS

## Overview

Your home Lab PC will be acting as a virtualization server for the duration of the Ops sequence. For this reason, we'll be using Ubuntu Linux as the computer's base operating system to capitalize on its lightweight, resource-efficient performance. We can later use the software application, Virtualbox, to "spin up" any other operating systems we may need, such as Windows 10.

Today you will install Ubuntu Linux 22.04 on the Lab PC using the bootable USB created previously. Once Linux is installed, you will then load Virtualbox and create your first VM (virtual machine) in the form of Windows 10. This configuration will make your home Lab PC highly versatile as a virtualization server. If you proceed to Ops Cybersecurity 401, this computer will ultimately become your "cyber range" system.

## Objectives

- Create a bootable USB flash drive of Ubuntu Linux Desktop 22.04
- Install Ubuntu Linux Desktop 22.04 on your Lab PC using the bootable USB flash drive

## Resources

- [Download Ubuntu Desktop](https://ubuntu.com/download/desktop){:target="_blank"}
- Windows/Linux OS: [Download Rufus](https://rufus.ie/en/){:target="_blank"}
- MacOS: [Balena Etcher](https://www.balena.io/etcher/).

## Tasks

- Start a new Google Doc for your lab submission and document each step while working through this lab.
- Copy and paste the lab instructions into your Google Doc and record your experience under each task.
  - Be sure to take note of any errors, their solutions and all resources used.

### Part 1: Creating a bootable Ubuntu USB flash drive

First, load Ubuntu Linux 22.04 into a bootable USB stick.

- Download [Ubuntu Desktop](https://ubuntu.com/download/desktop){:target="_blank"}.
- Download [Rufus](https://rufus.ie/en/){:target="_blank"} which is required for creating the bootable USB stick.
  - MacOS will use [Balena Etcher](https://www.balena.io/etcher/).
- Question: What is Rufus/Balena Etcher used for?
- Create the bootable Ubuntu USB stick by running Rufus or Balena and selecting the Ubuntu Desktop ISO.
  - Format the USB stick to FAT32 for optimal compatibility.
  - Include a photo of Rufus/Balena Etcher's successful completion in your submission.
- Safely eject it from your personal PC and remove it.

### Part 2: Installing Ubuntu

Now let's install Ubuntu onto the Lab PC.

- First, check that you've installed the provided solid state drive (SSD) to your lab kit PC. You'll be installing Ubuntu to the SSD for optimal performance.
- A network connection will allow Ubuntu to apply software updates, so connect an Ethernet cable from the PC to your network.
  > If you do not have immediate access to an ethernet port, use the provided USB Wi-Fi dongle instead. Beware the use of Wi-Fi on both personal computer and lab kit PC can negatively impact the responsiveness and "feel" of your remote connection later in the class. Connecting both computers to the same network via ethernet cabling is optimal and highly recommended.
- Confirm in BIOS that your system will boot into USB over HDD if a USB is detected.
  - Include a photo of this confirmation.
- Insert the USB into your lab kit PC with the system powered down.
- Power on the Lab PC. It should launch directly into your Ubuntu installer.
  - Include a photo of the Ubuntu installer during start up.
  - Installation options:
    - "Normal" installation is fine (as opposed to "Minimal").
    - It is recommended to uncheck the "Download updates while installing Ubuntu" option.
      - Why? This will make the installation process take longer. You will run the updates as part of the setup instructions in the next lab.
    - If your computer already has an OS installed (maybe it's already running Windows 10?):
      - Select the "Erase disk and install Ubuntu" option.
        - Note: This is NOT the default option.
      - Why? Installing both operating systems could leave too little space on your drive, and make future assignments harder.
    - **Do not** enable "Automatic Login" as that will make it tougher to connect remotely.
- Install Ubuntu, then remove the USB drive before booting into the HDD.

Once you're accessing the Ubuntu Desktop from a normal startup, you're all set. Describe the steps taken and your outcome in the submission doc for today.

Question: Turn your Lab PC off and back on one more time. Did you encounter any errors during/after start up? Explain your error and what you did/tried to solve it.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-102d33: Lab 04`
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can comment".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
