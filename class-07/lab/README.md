# Lab: Network Connectivity

## Overview

To use the Ubuntu PC as a true dedicated virtualization server, we'll need to establish reliable network connectivity to it from our personal computer. To do this, we'll need to apply networking concepts such as IP addressing, ports, and MAC addressing. We'll also need to install some additional software on the Ubuntu box to facilitate these network protocols. After configuring and testing remote connectivity to your Ubuntu virtualization server, you'll no longer need to keep it around your desktop workspace and can relocate to a closet or garage with network access. Think of it as your "private cloud," but without the costs!

> The operations depicted in this lab are quite common in the world of networking and systems administration. Most servers are either reserved or static IPs, and in this cloud-driven market we're seeing heavy usage of remote desktop solutions such as Microsoft RDP (Remote Desktop Protocol).

## Objectives

- Establish SSH connectivity from your personal system to the Ubuntu PC.
- Establish GUI desktop remote connectivity from your personal system to the Ubuntu PC.
- Install and use a GUI SCP application.
- Perform a SCP file transfer via the GUI SCP application.

## Resources
- [DHCP Reservation](https://homenetworkadmin.com/dhcp-reservation/){:target="_blank"}
- Remote Desktop setup: [Ubuntu RDP access from Windows 10](https://linuxconfig.org/ubuntu-20-04-remote-desktop-access-from-windows-10){:target="_blank"}
- Alternative to RDP: [Ubuntu VNC access from macOS or Windows](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-vnc-on-ubuntu-20-04){:target="_blank"}

## Tasks

- Start a new Google Doc for your lab submission and document each step while working through this lab.
- Copy and paste the lab instructions into your Google Doc and record your experience under each task.
  - Be sure to take note of any errors, their solutions and all resources used.

### Part 1: Check IP Addresses
- Check the IP address of your lab computer and write it down. You probably did this in Lab05, go ahead and double check it anyway. Include the address here in your lab notes.
> If you're having trouble identifying your IP address on Ubuntu, follow [this guide](https://itsfoss.com/check-ip-address-ubuntu/){:target="_blank"} to look up the lab kit PC's IP address.
- Check your home computer's IP address and write it here as well.
- Compare these two addresses:
  - The first three 'sections' of the IP address should be the same (e.g. 192.168.1.161 and 192.168.1.12, or 10.0.1.43 and 10.0.1.77)
  - If the first three parts don't match, then your computers are not on the same network.

### Part 2: SSH Connectivity

SSH lets us access the command line of a remote computer by authenticating into it using a local user's password.
- On your lab computer, use the APT package manager to confirm that OpenSSH is installed.
- Create any necessary firewall exceptions to ensure port 22 is open.
> Hint: when you installed and configure `xrdp` in Lab05, one of those steps was creating new firewall rules to allow RDP traffic over port 3389. See if you can adapt that command to create a rule allowing SSH traffic over port 22.
- SSH into your lab computer from your personal computer's command line interface (Windows Command Line on Windows, or ZSH/Terminal if you are on MacOS). The first time you connect, you'll need to answer 'yes' to some permission questions. Take a screenshot of the successful (or unsuccessful) connection.
- Try issuing commands to the lab computer from your personal computer via SSH. Be sure to try these commands:
  - `whoami`
  - `ls`
  - `pwd`
  - `ip a`
- Take a screenshot of the output of these commands, and include a short explanation of what each command does.


### Part 3: Remote Desktop Connectivity

Windows 10 users, follow this instruction set.

- Before you make an RDP connection, **be sure to log out of your lab computer via the monitor and keyboard** attached to it.
- Open your RDP client software on your home computer:
  - Windows users will open Remote Desktop Connection, which is an RDP client that comes with Windows.
  - MacOS users will need to download and install [Microsoft Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466?mt=12){:target="_blank"} in order to use the RDP protocol to access Ubuntu remotely.
- Input the IP address and username of your lab computer into the RDP client on your home computer and establish an RDP connection to your lab computer

> If you're seeing a black screen as your RDP session, this is because XRDP does not allow a user profile to be logged in on Ubuntu itself while another computer is attempting to establish a RDP connection to it. Log out of your lab computer using its keyboard and monitor, then attempt RDP again.
> If you're still having trouble, check that the sharing switch and remote desktop switches are turned to ***ON***, instructions can be found here: [Ubuntu Turn on Sharing](https://help.ubuntu.com/stable/ubuntu-help/sharing-desktop.html){:target="_blank"}


Once you have established remote desktop connectivity, customize the interface to your liking by assigning common applications to favorites, such as Terminal and Files. Personalize this lab computer by adding a cool wallpaper and change the colors on your Terminal app while you're at it. Grab a screenshot of your customized home lab desktop.

### Part 4: Secure Copy Protocol (SCP)

Throughout your home lab journey, you'll have occasion to transfer files from your main personal computer to the lab system.

- Download/install a file transfer program:
  - Windows users can use [WinSCP](https://winscp.net/eng/index.php){:target="_blank"}.
  - MacOS users can use [Cyberduck](https://cyberduck.io/){:target="_blank"} to transfer files from the personal computer to the lab computer via SFTP protocol. Reference [this guide](https://kb.iu.edu/d/akom){:target="_blank"} for a step-by-step walkthrough.
- Include a screenshot of a successful file transfer.
- In as technical terms as you understand, explain how this file transfer works.

### Part 5: Prepare for Next Lab

Start downloading [Windows 10 ISO](https://www.icloud.com/iclouddrive/01azgWsJOfzZaBbAj-G3sLWTg#Windows10){:target="_blank"} to prepare for the next lab.
You will need this file on your lab computer, so you can either:
- Download it to your personal computer first, then use the file transfer program from Part 4 to transfer it to your lab kit PC
- Or simply download directly to your lab kit PC using its browser and enter the above link.


## Stretch Goals

At this point you've established remote connectivity to your lab kit PC, but what if its IP address gets reassigned during DHCP lease renewal? The stretch goal below addresses this issue. It's not absolutely essential to get it done right now, but it will save you the inconvenience of potentially losing track of the IP address.

### IP Address Reservation

In order to make sure your lab kit PC's IP address always stays the same every time you need it, you'll need to reserve a fixed IP address on your home DHCP server for the Ubuntu PC's network adapter. Be extra careful when manipulating the configuration of your network appliances (stretch goal), as this can affect your overall internet connectivity. If you're new to administering DHCP on your home modem/router appliance, pump the brakes and take it slow! If you neglect to properly do this step, the IP address of your Ubuntu PC may change, thus affecting our ability to connect to it.

- Identify the MAC address of the Ubuntu PC via terminal.
- Access your DHCP server's (router's) administrative interface and assign a reserved IP to the Ubuntu PC's network adapter MAC address.
- To update this new IP address on your lab computer, run the following commands in the Terminal:
```bash
sudo dhclient -r
```
```bash
sudo dhclient
```

> Ask your instructor for help if you're uncertain at this stage of the lab. Everyone's home network is different, and this is a very perilous stage of the lab to make a mistake.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-102d33: Lab 04`
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can comment".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
