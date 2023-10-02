# Lab: Virtualization of Windows OS

## Overview

Now that Virtualbox is loaded onto your Ubuntu-based lab PC, you'll be able to create a virtual machine (VM) of any operating system, assuming you can get your hands on the corresponding .iso installer or a premade .ova Virtualbox file. There are legal and ethical considerations to make when seeking out such files. For example, Apple forbids the virtualization of its macOS on non-Apple hardware. For this class, your first VM will be Windows 10, the most common enterprise business desktop used today.

## Objectives

- Create a Windows 10 VM in Virtualbox using the .iso installation method.
- Backup the working Windows 10 VM using Virtualbox's save state and .ova export features.
- Determine a consistent disk storage solution for .ova files.

## Resources

- [Windows 10 ISO Download](https://www.icloud.com/iclouddrive/01azgWsJOfzZaBbAj-G3sLWTg#Windows10){:target="_blank"}
- [Windows Media Creation Tool](https://www.microsoft.com/en-us/software-download/windows10){:target="_blank"}
  - Note that this is *not* required if you have downloaded Windows 10 ISO to your Ubuntu Linux lab kit PC.
- [How to set up Windows 10 with local account](https://www.windowscentral.com/how-set-windows-10-local-account){:target="_blank"}

> For our purposes in class, we will not be activating our installations of Windows. If you have access to activation keys for commercial systems we use in class, feel free to apply them at your discretion.

## Tasks

In this lab you'll be creating a Windows 10 VM in VirtualBox.

- Start a new Google Doc for your lab submission and document each step while working through this lab.
- Copy and paste the lab instructions into your Google Doc and record your experience under each task.
  - Be sure to take note of any errors, their solutions and all resources used.

### Part 1: VM Creation with ISO

Your Ubuntu Linux lab kit PC will need the [Windows 10 ISO](https://www.icloud.com/iclouddrive/01azgWsJOfzZaBbAj-G3sLWTg#Windows10){:target="_blank"} downloaded and accessible to VirtualBox Manager. You can either download it directly to your lab kit PC using the link above, or download it first to your personal computer then transfer it to your lab kit PC with WinSCP.

Alternatively, you can elect to create your own Windows 10 ISO using [Windows Media Creation Tool](https://www.microsoft.com/en-us/software-download/windows10){:target="_blank"}.

Once your VirtualBox Manager can see the Windows 10 ISO file, create a Windows 10 VM and insert the Windows 10 ISO into the (virtual) optical drive.

### Part 2: Configuring your VM

Now that your VM is created, you'll want to review its resource allocation. These resources are virtual representations of the physical components you cataloged in Class 1.

- Adjust various parameters to optimize performance of the VM.
  - Adjust RAM to 8 GB.
  - Adjust the CPU to utilize all four cores.
  - Allocate the maximum possible video memory.
  - Include screenshots of parameter adjustments.

- Set the network adapter to bridge mode.

### Part 3: Windows 10 Setup Wizard

Complete the setup wizard that runs the first time you launch the VM.
  - Do not sign in with a Microsoft account. Follow [this guide](https://www.windowscentral.com/how-set-windows-10-local-account) to set up Windows 10 with a local account instead.
    - DO NOT use a pre-existing personal account either.
  - Disable as many "features" and extras as seem reasonable for a minimalist installation.
  - When you have access to the Windows 10 desktop, this part is complete.

## Part 4: Virtualbox Snapshot, Save State, and Export/Import

Virtualbox includes a "save state" feature. We can use this to establish a "baseline" image of your Windows 10 VM.

Virtualbox has several features which are similar but which function very differently: Snapshots, Save Sate, and Export/Import

- Click the Close button on a VM and select "Save the machine state".
  - Restart the VM.
  - Describe what happened. Is this different than shutting down and restarting the VM? Is it faster or slower? When would you save the state and when would you shutdown the VM?
- Take a snapshot of the VM.
  - Make a change to the VM. For example, create a file on the desktop.
  - Restore the VM to the snapshot you took.
  - Describe whether the VM state was restored as expected. How might this be useful later on?
- Export a .ova file of your Windows 10 VM.
  - Make a copy of this file somewhere spacious and ideally separate from the SSD of the lab PC. If you have a second storage device on your lab machine, such as a large HDD, that is a perfect place for backups.
- Use Import Appliance to import a new VM from the .ova file you just exported.
  - How is this VM different from the original VM?
  - How do you imagine using this feature to save you time and effort?

## Stretch Goals (Optional Objectives)

Download the premade [Linux Mint 21 VirtualBox Image](https://www.linuxvmimages.com/images/linuxmint-21/){:target="_blank"}.
- Import the .ova into Virtualbox as a new VM.
- Document in your submission how this process differs from the .iso installation process you performed. What are the pros/cons of each method?
- Feel free to delete this VM and store the .ova file. We won't be using this one in class.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-102d33: Lab 04`
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can comment".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
