# Lab: Startup Sequences and BIOS

## Overview

Before a computer even launches into its OS (operating system), it performs a sequence of activities behind the scenes immediately after you press the power button. These activities include selecting a boot device based on a prescribed boot sequence. These low-level computing activities take place in the computer's BIOS. Settings such as motherboard or component voltage allocation, overclocking, boot sequence, system time, and more can be found in the BIOS menu system. Because virtualized computers can have multiple bootable drives and accept external media in the form of .iso disk images, it will be valuable for you to gain experience manipulating a physical computer's BIOS and boot sequence within it.

## Objectives

Today you will be performing the following operations on your lab computer's Basic Input/Output System (BIOS):
- Document detailed system information using BIOS.
- Clear the CMOS using BIOS.
- Change boot sequence using BIOS.
- Secure BIOS with an administrator password.
- Access the event log in BIOS.

## Tasks

- Start a new Google Doc for your lab submission and document each step while working through this lab.
- Copy and paste the lab instructions into your Google Doc and record your experience under each task.
  - Be sure to take note of any errors, their solutions and all resources used.

### Part 1: System Information

Create a new Google Doc for this lab per Submission Instructions below.
- Log into your lab computer’s BIOS.
  > Changes made to BIOS do not apply until you select "Exit Saving Changes."
- In the BIOS, look up the following system spec information. Provide a screenshot of the information and describe where in the BIOS you found it:
  - Motherboard
  - CPU
  - Amount of RAM installed
  - BIOS firmware version
- Lookup the BIOS menu that allows you to disable USB ports. Include a photo.

    _**Note:** this is different than the settings which enable booting from usb._

### Part 2: Clearing the CMOS

In this part of the lab, you will attempt to clear the CMOS. **Clearing the CMOS will revert BIOS back to its factory default settings.** It may also take some time for the CMOS to discharge electrically. Take care to perform Part 2 before Part 3-4 in this lab assignment, to avoid inadvertently clearing your desired settings.
- Note the System Date and System Time on the Main menu. Shut down the computer.
- As always, don't touch PC internals until you've confirmed the power cable is disconnected, PSU set to 0, and your body is free of static charge.
- Carefully remove the CR2032 battery from the motherboard. Wait five minutes.
- Reinsert the CR2032 battery. Plug in power, switch power to 1, and boot the PC. Go back into BIOS.
- Include a photo of the warning message and altered time setting.
- Describe the process you used to clear the CMOS. Describe what all changed, and explain why it changed.
- Adjust System Date and Time to correct values.

### Part 3: Boot Sequence

Change boot order to prioritize USB over HDD.
- What boot mode is your BIOS currently set to use, UEFI or Legacy? Include a photo.
- Configure USB flash drive to take priority over the hard drive. We'll need this to install Ubuntu via USB later.
- Include a photo of the boot order/priority menu.
- Describe the steps you took and any issues you encountered.

> If you do not get into the BIOS (by hitting the right key in time), you might receive an error that looks something like: "PXE-E61 Media test failure, check cable PXE-M0F: Exiting PXE ROM. No Boot Device Found. Press any key to reboot the machine." With no operating system installed, this message is expected. Simply reboot the computer and be ready to hit the key to get to the BIOS screen.

> Typically, external media like DVD-ROM and USB will take precedence over the internal hard disk in order to facilitate smooth installation of operating systems using external media. When the installation process is complete and you're about to reboot into the HDD, you'll typically remove the external media at that stage so the boot sequence doesn't re-launch the installer off the external media.

### Part 4: Securing BIOS

If you're distributing physical computers to a workforce as company-administered property, consider securing the BIOS with an administrator password.
- Once configured, include a photo of the BIOS prompting you for a password.
- Describe the procedure you used to configure a password.
- Remove the password requirement.

### Part 5: Enabling Virtualization

These settings vary depending on the make and model of your lab kit PC, so refer to your motherboard instruction manual for exact directions.  **Failure to complete this step means virtualization will be impossible until you do.**
- In the BIOS, find the Virtualization settings.
- Make sure Intel Virtualization Technology is ENABLED and Intel VT for Directed I/O (VT-d or VT-x) is ENABLED.
- Capture a photo of your virtualization settings.

### Part 6: Prepare for Next Lab

Start downloading the latest [Ubuntu Desktop LTS](https://ubuntu.com/download/desktop) and [Rufus](https://rufus.ie/en/) (if you are running Windows) or [Balena Etcher](https://www.balena.io/etcher/) (if you are on a Mac) to your personal computer to be prepared for the next lab.

## Stretch Goals (Optional Objectives):

Pursue these optional objectives if you are an advanced user or have remaining lab time.

### Additional System Information

- Lookup and provide the CPU Fan Speed in RPM and the Processor Temperature in Celsius. Describe where you found this information.
- Lookup and provide the configuration setting of the Integrated Graphics Device. Explain what this means.
- Navigate to the SATA Drives menu and include a photo showing all devices attached via SATA.

### Flash the BIOS Firmware

If you're feeling confident thus far, check to see if there is a new version of your BIOS firmware and download it. Update the firmware via BIOS or whatever method is prescribed by the motherboard vendor.

- There are many ways to update BIOS. Choose one method and proceed.
- Include photos of all the steps you took. Describe any challenges or problems you encountered.

> Note that if a firmware upgrade goes wrong, such as a power interruption during the upgrade process, you run the risk of "bricking" the device (rendering the hardware permanently inoperable). This makes firmware upgrades inherently riskier than software application or OS upgrades.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-102d33: Lab 04`
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can comment".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
