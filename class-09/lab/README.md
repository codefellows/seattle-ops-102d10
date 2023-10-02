# Lab: Basic Windows Operations

## Overview

Now that we have installed Windows 10 as a virtual machine, let's take a look at some foundational operations that Ops professionals perform in supporting and administering the popular OS. Like the Linux terminal, an aspiring Ops professional will need a basic grounding in Windows terminal as well as desktop interfaces. You won't be an expert after this class, but you'll know enough to get some essential tasks completed on this common business platform.

## Objectives

- Setup a non-administrator user.
- Gather system information.
- View network adapter information and perform ping, trace route with Windows command line.
- Install Google Chrome and Sumatra, then associate them with their respective tasks.

## Resources

- [Command Prompt: 11 basic commands you should know](https://www.digitalcitizen.life/command-prompt-how-use-basic-commands/){:target="_blank"}

## Tasks

- Start a new Google Doc for your lab submission and document each step while working through this lab.
- Copy and paste the lab instructions into your Google Doc and record your experience under each task.
  - Be sure to take note of any errors, their solutions and all resources used.

### Part 1: User Setup

The first profile you created should be the admin. Check this is the case and in your Google Doc discuss where this setting is, and how you know it's an admin.
- Setup a non-admin user profile (local)
  - In your Google Doc describe the process used to create a non-admin user. Include a photo indicating there is one admin user and one non-admin user.
  - Log into the computer as the non-admin user. Attempt to perform an admin function, such as changing the computer name. Describe what happens when you do, and why this distinction between admin and user is important from an organizational security perspective.

### Part 2: System Info

There are many ways to view system information in Windows 10. Add some info to your Lab Report doc.
  - From the "Run" menu, run DXDIAG
    - Include a photo/screenshot of DXDIAG
    - Describe the graphics processor listed in DXDIAG
  - In the Windows SEARCH bar (magnifying glass next to the START button), search for and open 'About your PC'.
    - Include a photo/screenshot of the "Device specifications" and "Windows specifications" listing.
    - Rename the computer as you see fit. Reboot, then paste a screenshot of the new About your PC screen indicating the new name.

### Part 3: Command Line

Open the Terminal as Administrator and include screenshots of the below command line operations:
- Determine the IP address of this Virtual Machine.
- Ping your lab computer from this one.
- Run a `traceroute` to google.com.
- Navigate to the My Documents folder.
- In the My Documents folder, create a new folder called `mydir.`
- List the contents of My Documents in the Terminal.
- Delete `mydir`.

### Part 4: Software Administration

Basic operation of Windows includes installing applications and associated them with certain common tasks.
- Locate the Control Panel, and navigate to the Add/Remove Programs menu. Include a screenshot.
- Run Windows Update to check for OS updates. Download and install all of them. This will take some time, feel free to multitask. You'll need to reboot to apply updates.
  - If possible, include a photo/screenshot of the updater running.
  - Describe why the Version History menu might be useful for the administrator.
- Download and install Google Chrome.
- Download and install [Sumatra](https://www.sumatrapdfreader.org/free-pdf-reader){:target="_blank"}.
- Make Google Chrome your default web browser.
- Associate Sumatra with PDF (Portable Document Format) files as the default app. Verify this is the case by opening a [PDF file](http://www.orimi.com/pdf-test.pdf){:target="_blank"}.

If you've gotten this far, you've performed some basic Windows fundamental operations on your Windows 10 VM and have established a comfortable working home lab. This is the final lab assignment for Ops 102, so put together your notes and get ready for the final!

## Stretch Goals (Optional Objectives)

Third party software can often be more useful than native apps in revealing system information.

- Install [CPU-Z](https://www.cpuid.com/softwares/cpu-z.html){:target="_blank"} and run the app to view more information about your PC
  - Include a photo/screenshot of CPU-Z
  - Explain why this information would be useful for the administrator.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-102d33: Lab 04`
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can comment".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
