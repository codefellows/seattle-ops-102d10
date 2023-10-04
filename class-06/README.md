# Class 06

## Class Outline

1. Ops 102 Overview
1. Review
1. Lecture
1. Demo
1. Lab 

## Overview

In this class, we'll be exploring how to setup a small network and working with some new tools.

## How does this topic fit?

**Where we've been**:
In the previous class we installed Virtualbox onto the lab PC.

**What are we focusing on today**:
Today, we'll be exploring networking on a deeper level from cabling and routers to software and basic security.

**Where we're headed**:
Next class will focus on virtualization with Ubuntu Linux.

## SOHO Networking

### Why
- A SOHO network allows you to share a single internet connection among multiple devices. This is especially crucial in homes or small offices where there are several computers, smartphones, tablets, and smart devices that need internet access. It ensures that all devices can connect to the internet without the need for separate connections for each device.
- With a SOHO network, you can easily share resources such as printers, scanners, and files among multiple devices. This promotes collaboration and efficiency in both home and office environments. 
- Setting up a network-attached storage (NAS) system allows you to centralize data storage. This means important files and documents can be stored in a central location that is accessible to all authorized users on the network. It solves the problem of scattered data and makes data management more efficient.
- A properly configured SOHO network can enhance security by implementing features like firewalls, encryption, and access controls. It enables you to monitor and control the devices that connect to your network, reducing the risk of unauthorized access and data breaches.
- Setting up your own SOHO network provides valuable learning experiences. You gain insights into network configurations, security practices, and troubleshooting. These skills are not only useful for personal or small business purposes but are also valuable in the job market, especially in IT-related fields. Setting up your own SOHO network is a great project to talk about during a job interview.

### What
- Router: A networking device that forwards data packets between computer networks. It is often used to connect multiple devices to the internet in a home or office environment.
- Modem: Short for modulator-demodulator, a device that modulates analog signals into digital signals for transmission over communication lines and demodulates incoming digital signals back into analog form.
- Ethernet: A popular networking technology that defines a set of wiring and signaling standards for the physical layer of wired local area networks (LANs).
- Wi-Fi: A technology that allows devices to connect to a LAN wirelessly, using radio waves, often via a router or access point.
- LAN (Local Area Network): A network that connects computers and devices in a limited geographical area, such as a home, office, or group of buildings.
- WAN (Wide Area Network): A network that covers a broad area, such as a city, country, or even intercontinental connections.
- IP Address: A unique numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication.
- DNS (Domain Name System): A system that translates human-friendly domain names (like www.example.com) into IP addresses that computers use to identify each other on the network.
- Firewall: A network security device or software that monitors and controls incoming and outgoing network traffic based on predetermined security rules.
- SSID (Service Set Identifier): A unique identifier for a wireless LAN, commonly known as the Wi-Fi network name.
- Encryption: The process of converting data into a secure code to prevent unauthorized access. In the context of Wi-Fi, it refers to securing wireless networks to prevent unauthorized users from accessing the network.
- Protocol: A set of rules that define how data is transmitted over a network. Common network protocols include TCP/IP (Transmission Control Protocol/Internet Protocol) and HTTP (Hypertext Transfer Protocol).
- Subnet Mask: A numerical label that defines a range of IP addresses within a network, indicating which part of the IP address represents the network and which part represents the specific device.
- Gateway: A device or software that connects two different networks, serving as a translator and a router between different protocols.
- Network Topology: The arrangement of various elements (links, nodes, etc.) of a computer network.
- DHCP (Dynamic Host Configuration Protocol): A network protocol that automatically assigns IP addresses and other network configuration information to devices on a network.
- Ethernet Cable: A common type of network cable used to connect devices in a wired network. It is also known as Cat5, Cat5e, Cat6, or Cat7 cable, depending on its category and performance specifications.
- Patch Cable: A short, usually straight cable used for making connections between network components. Patch cables are commonly used to connect computers to network outlets and to connect switches and routers.
- Coaxial Cable: A type of cable that consists of a central conductor, an insulating layer, a metallic shield, and an outer insulating layer. Coaxial cables are often used for cable television and broadband internet connections.
- RJ45 Connector: A standardized networking connector used for Ethernet connections. It has eight pins and is commonly used with Ethernet cables.
- Router Cable Ports: Different ports on a router for connecting various devices, including WAN (Wide Area Network) ports for internet connection and LAN (Local Area Network) ports for connecting computers and other devices.
- Switch: A network device with multiple Ethernet ports used to connect multiple devices within a LAN. It operates at the data link layer (Layer 2) of the OSI model and can forward data to specific devices within the network.
- Hub: A basic device that connects multiple Ethernet devices in a LAN.
- Access Point: A device that allows wireless devices to connect to a wired network using Wi-Fi. Access points are often used to extend the wireless coverage of an existing wired network.
- Network Splitter: A device that allows multiple devices to share a single Ethernet cable.It is commonly used to expand the number of available ports on a router or switch.
- Repeater: Device extending wireless network range or boosting wired signal strength.

### How
- Data Creation
  - Information is created on a device, like a computer or smartphone, in the form of binary data (0s and 1s).
- Data Encapsulation
  - Data is encapsulated into packets. Each packet contains the destination address, source address, and the actual data.
- Routing Decision
  - The device determines if the destination address is on the local network or a remote network.
    - Local Network
      - If the destination is on the same local network, the device sends the packet directly to the recipient using MAC addresses (on Ethernet networks) within the LAN.
    - Remote Network
      - If the destination is on a different network, the packet is sent to the default gateway (usually a router).
- Router Processing
  - At the router, the packet is received, and the router reads the destination IP address. It consults its routing table to determine the best path for the packet.
- Switching
  - Within local networks, switches are optional devices that use MAC addresses to forward packets only to the specific device on the network. This reduces unnecessary traffic.
- Internet Protocol (IP)
  - Routers use IP addresses to forward packets between different networks. They determine the best path using routing algorithms and protocols.
- Internet Backbone
  - For long-distance transmission, data travels through high-speed fiber-optic links known as the internet backbone, connecting various regions globally.
- Destination Network
  - The packet reaches the destination network and is received by the destination router.
- Local Delivery
  - If the destination is on the same local network, the packet is delivered directly to the device using MAC addresses.
- Data Extraction
  - The device receives the packet, extracts the data, and processes the information contained within.
- Response Generation
  - The destination device processes the received data and may generate a response.
- Acknowledgment
  - If necessary, an acknowledgment packet is sent back through the same process, confirming the receipt of data.
- Session Closure
  - Once the communication is complete, devices may exchange termination signals to close the connection gracefully.

### Experimentation and Discovery Ideas
- Considering the concept of data security in SOHO networks, what are the potential vulnerabilities? How can one experiment with encryption methods to enhance network security?
- In the context of SOHO networks, what is the significance of IP addressing and subnetting? How might experimenting with various IP configurations optimize network performance?
- Considering the evolution of networking technologies, such as IPv6 and IoT integration, what experiments can be devised to explore the compatibility and challenges these advancements pose in a SOHO environment?
- Investigating the impact of network congestion and bandwidth limitations in a SOHO network, what experiments can be conducted to optimize data traffic and prioritize critical applications? How might Quality of Service (QoS) protocols be explored in this context?

## Learning Objectives

### Students will be able to

#### Describe and Define

- SOHO Network Components
- Gateway
- Subnet
- Wi-Fi Configurations

#### Execute

- Setup a working SOHO Network

## Helpful Resources

- CrashCourse on YouTube
  - [Computer Networks](https://www.youtube.com/watch?v=3QhU9jd03a0&list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo&index=29&t=15s){:target="blank"}
  - [The Internet](https://www.youtube.com/watch?v=AEaKrq3SpW8&list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo&index=30){:target="blank"}
  - [The World Wide Web](https://www.youtube.com/watch?v=guvsH5OFizE&list=PL8dPuuaLjXtNlUrzyH5r6jN9ulIgZBpdo&index=31){:target="blank"}
- [Internet 101 | Computer Science | Khan Academy](https://www.youtube.com/playlist?list=PLSQl0a2vh4HD8wtmKZh0nKOsOvP1KYaNO){:target="blank"}
- [Professor Messer's CompTIA Network+ Course](https://www.professormesser.com/network-plus/n10-008/n10-008-video/n10-008-training-course/){:target="blank"}

## Notes
- What is the difference between IPv4 and IPv6? 

### `ip addr show` Output Cheatsheet
In the output of the `ip addr show` command in Linux, you can find the following information:
  - MAC address
    - The MAC address is displayed under the `link/ether` field for each network interface. 
    - It is a unique identifier assigned to the network interface card (NIC).
  - IP address
    - The IP address is shown under the `inet` field. 
    - It indicates the assigned IP address for each network interface. 
    - The IP address is often followed by a subnet mask and network prefix length.
  - Subnet Mask
    - The subnet mask is presented along with the IP address under the `inet` field. 
    - It indicates the network portion of the IP address and helps determine which part of the IP address represents the network and host.
  - Gateway address
    - The gateway address, also known as the default gateway, is not explicitly displayed in the `ip addr show` output. 
    - It is part of the routing configuration. 
    - To find the gateway address, you can use the `ip route` command or check the routing table with `ip route show` command.

### How do I find my router's IP address in Ubuntu?
- `ip route | grep default | awk '{print $3}'`
  - `ip route` displays the routing table, which includes information about network routes.
  - `grep` default filters the output to show only the line containing the default route.
  - `awk '{print $3}'` extracts and prints the third field, which represents the IP address of the default gateway (AKA the router).