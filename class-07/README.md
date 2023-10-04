# Class 07

## Class Outline

1. Ops 102 Overview
1. Review
1. Lecture
1. Demo
1. Lab 

## Overview

To use the Ubuntu PC as a true dedicated virtualization server, we'll need to next establish reliable network connectivity to it from our personal computer. To do this, we'll need to apply networking concepts such as IP addressing, ports, and MAC addressing. After configuring and testing remote connectivity to your Ubuntu virtualization server, you'll no longer need to keep it around your desktop workspace and can relocate to a closet or garage with network access. Think of it as your "private cloud," but without the costs!

> The operations depicted in this lab are quite common in the world of networking and systems administration. Most servers are reserved or static IPs, and in this cloud-driven market we're seeing heavy usage of remote desktop solutions such as Microsoft RDP (Remote Desktop Protocol).

## How does this topic fit?

**Where we've been**:
In the previous class we setup a basic LAN using the provided router in the lab kit.

**What are we focusing on today**:
Today, we'll explore network connectivity protocols.

**Where we're headed**:
Next class we'll be deploying our first virtual machine on the lab PC.

## Remote Connectivity 

### Why
- Running VMs, simulations, or complex computations can be resource-intensive. Utilizing a powerful remote server, like our lab PC, ensures that these tasks do not overwhelm your personal machine, leading to better performance.
- Servers, like our lab PC, often have specialized hardware configurations optimized for tasks like virtualization, providing better performance and stability.
- Remote connections provide flexibility in terms of work arrangements. Employees can work from home or any location, improving work-life balance and job satisfaction. This flexibility also enables businesses to hire talent from anywhere in the world, expanding their pool of potential employees.
- IT professionals can troubleshoot, update, and maintain systems without being physically present, saving time and resources.
- Remote connections reduce the need for on-site visits, minimizing travel costs and downtime associated with commuting.
- IT support can assist users remotely, resolving issues without the need for physical presence.
- Remote connections enable IT professionals to manage backups and perform system restores remotely, aiding in disaster recovery efforts.
- Users can choose different types of remote connections based on their specific needs, providing flexibility in accessing resources.

### What
- Remote Connection: The ability to access a computer or network from a different location using various technologies.
- Client: The computer or device that initiates a connection to a remote server or system.
- Server: A computer or system that responds to requests from clients, providing services or resources over a network.
- Host: A computer or device connected to a network, which can be a server or a client depending on the context.
- Protocol: A set of rules defining how data is transmitted and received over a network. (e.g., TCP/IP, UDP)
- Authentication: The process of verifying the identity of users, devices, or systems trying to establish a connection.
- RDP (Remote Desktop Protocol): A proprietary protocol developed by Microsoft, allowing users to control a remote computer over a network connection.
- SSH (Secure Shell): A cryptographic network protocol used for secure remote login, command execution, and other secure network services over an insecure network.
- VPN (Virtual Private Network): A technology that allows secure and encrypted communication over an untrusted network, providing privacy and anonymity.
- Firewall: A network security device or software that monitors and controls incoming and outgoing network traffic, based on predetermined security rules.
- Bandwidth: The maximum data transfer rate of a network or internet connection, often measured in bits per second (bps) or megabits per second (Mbps).

### How
SSH (Secure Shell) and RDP (Remote Desktop Protocol) are both protocols used for remote access and management of systems. Here's how they work:
**SSH (Secure Shell):**
  - Initialization:
    - The client initiates a connection request to the server.
    - The server responds with its identification, including the public key.
  - Key Exchange:
    - The client and server perform a key exchange to agree on encryption algorithms and generate shared secret keys.
    - The Diffie-Hellman key exchange algorithm is commonly used in SSH for this purpose.
  - User Authentication:
    - The client provides user credentials (username and password) or presents a public key for authentication.
    - If key-based authentication is used, the server checks the client's public key against the authorized keys list.
  - Encryption and Authentication:
    - A symmetric encryption session is established using the shared secret keys.
    - All further communication, including user authentication, commands, and data exchange, is encrypted using these keys.
    - HMAC (Hash-based Message Authentication Code) is used for message integrity.
  - Session Establishment:
    - Once authenticated, the client and server can establish a shell session or execute specific commands securely.
    - The encrypted channel is used for all communication, ensuring confidentiality and integrity of the data exchanged.
**RDP (Remote Desktop Protocol):**
  - Connection Initialization:
    - The client initiates a connection request to the server hosting the remote desktop session.
  - Security Negotiation:
    - The client and server negotiate security settings, including encryption algorithms and methods for user authentication.
    - RDP supports various encryption levels and authentication mechanisms, including Network Level Authentication (NLA).
  - User Authentication:
    - The client provides user credentials (username and password) for authentication.
    - If Network Level Authentication (NLA) is enabled, the user is authenticated before the remote desktop session is established.
  - Graphics and Input Redirection:
    - Graphics and input data (keyboard, mouse) are redirected from the client to the server over the encrypted connection.
    - RDP uses its own compression and encoding techniques to optimize the transmission of graphical data, ensuring efficient use of network resources.
  - Session Establishment:
    - Once authenticated, the remote desktop session is established, allowing the client to interact with the server's desktop environment as if they were physically present.
    - All user actions, screen updates, and input are transmitted over the encrypted RDP connection. 

### Experimentation and Discovery Ideas
- Why is the process of key exchange crucial in SSH? How does it enhance security in remote connections?
- What are the ethical considerations surrounding the use of RDP? Can you think of potential misuse scenarios and their implications?
- Reflecting on SSH and RDP, what similarities and differences can you identify in their underlying principles? How do these technologies contribute to the broader landscape of remote communication and access?

## Learning Objectives

### Students will be able to

#### Describe and Define

- Network Protocol
- IP
- TCP 
- UDP
- DHCP
- XRDP
- SSH
- SCP
- RDP

#### Execute

- Perform a DHCP reservation on a DHCP server.
- Use XRDP or VNC to remotely access a Ubuntu Linux computer.
- Install an OpenSSH Server in Ubuntu Linux and remotely SSH in.
- Transfer a file to a remote computer using WinSCP.

## Helpful Resources

- Professor Messer:
  - [Remote Access](https://www.professormesser.com/free-a-plus-training/220-1102/220-1102-video/remote-access-220-1102/){:target="_blank"}
  - [Common Network Ports](https://www.professormesser.com/free-a-plus-training/220-1101/220-1101-video/common-network-ports-220-1101/){:target="_blank"}
  - [Networking Protocols](https://www.professormesser.com/network-plus/n10-005/networking-protocols/){:target="_blank"}
  - [DHCP Addressing Overview](https://www.professormesser.com/professor-messer-archives/n10-007/dhcp-addressing-overview-3/){:target="_blank"}

## Notes

- What are “ports” and why are they numbered?
- What are protocols?
- What does a DHCP server do?
- What is the diffence between static IP, dynamic IP and reserved IP addresses?
- How do I exit my SSH connection in the terminal?

### How to check OpenSSH status in Linux
- `sudo systemctl status ssh.service`
  - Get the current status of the SSH server.
- `sudo systemctl start ssh.service`
  - Start the SSH server.
- `sudo systemctl stop ssh.service`
  - Stop the SSH server.
- `sudo systemctl restart ssh.service`
  - Restart the SSH server.

# Lab Topology

![Lab 07 Topology](./assets/lab07-topology.png)