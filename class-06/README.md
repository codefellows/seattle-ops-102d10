# Class 06

## Class Outline

1. Ops 102 Overview
1. Review
1. Lecture
1. Demo
1. Lab 

## Overview

In this class, we'll be exploring how to setup a small network and working with some new tools.

<!-- ## How does this topic fit?

**Where we've been**:
In the previous class ...

**What are we focusing on today**:
Today, we'll be doing ...

**Where we're headed**:
Next class will focus on ..

## SOHO Networking

### Why
- This topic is important because ...
- What problems are we facing that this concept will solve...

### What
- Concepts and Vocabulary listed here
- Be sure NOT to provide the definitions in this document, students can fill them in as note
- For example:
- REST: A modern way to transfer _____ between 2 systems using the _____ protocol.

### How
- What does the code we need to write have to do to solve these problems?
- What are some of the major concepts we have to tackle
- Briefly describe the type of work students will be seeing in demo and performing in lab

### Experimentation and Discovery Ideas
  - Provide some ideas here for how the instructor can be interactive with the students
  - Can this be built using the Socratic method?
  - Can we use breakout or small group sessions 
  - What is the difference between IPv4 and IPv6? -->

## Learning Objectives

### Students will be able to

#### Describe and Define

- SOHO Network Components
- Gateway
- Subnet
- Wi-Fi Configurations

#### Execute

- Setup a working SOHO Network

<!-- ## Helpful Resources

- [Cheat Sheet](){:target="blank"}
- etc. -->

## Notes
- List 1 new thing that you learned today.

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