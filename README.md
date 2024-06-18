# Networking Fundamentals

![Logo](https://images2.alphacoders.com/816/81652.jpg)


## Overview

In these document we would know how do data flow through different devices & internet.




## Contents

 - [Network Devices](#Network-Devices)
    - [Hosts](#Hosts)
    - [IP-Address](#IP-Address)
    - [Network](#Network)
    - [Repeater](#Repeater)
    - [Hub](#Hub)
    - [Bridge](#Bridge)
    - [Switch](#Switch)
    - [Router](#Router)

## Network Devices


**Network devices are critical components in any networking setup, facilitating communication and resource sharing between different devices. This document provides an overview of some common network devices.**

### Hosts
*Any device which sends or receive data*

![host_exaples](https://i.ibb.co/kBKWw9x/Screenshot-from-2024-06-18-17-09-30.png)


eg:-  Client initate requests,Server(servers are simply computers with software instaled which responds to specific requests) responds  so both are hosts.

### IP Address 
*An IP address is the identity of each host*

![IP_example](https://i.ibb.co/864gqsS/Screenshot-from-2024-06-18-17-22-48.png)


eg whenever a computer sends a request to the server it attaches the src(source IP address) and DST(destination IP address) same follows for server. every ping send on the internet will contain the src and dst
#### Number conversions
- Please refer the following repo if you want to know about it [link](https://google.com)
#### IPv4
- It is of 32 bits.
- These 32 bits are divides into 4 octet(mean each ocetet contain 8 bits)
- An IPv4 normaly looks like a decimal numbers combination
- As 8 bits can represent numbers between 0-255 so out of all 4 block can have a value only between them
- So a total of 256*256*256*256 = 4294967296 many IPv4 are possible but these is becoming a problem with time as more device are getting added to the internet so to solve these problem IPv6 are introduced
    ![ip_converter](https://i.ibb.co/BqxFFw1/Screenshot-from-2024-06-18-18-57-57.png)
- Try playing with the ip converter [link](https://github.com/AJ-17/c/tree/master/ip-converter)


#### IPv6
- It is 128 bit long.
- These 128 bit are divided into 8 parts each part 16 bit long or 4 hexadecimal digit. referred to as "hextet" or "quartet" 
- An IPv6 normaly looks like a hexamdecimal number combination.
- So we have total 2^128=340,282,366,920,938,463,463,374,607,431,768,211,456  ipv6 address

### Network
*A Network is what transports traffic between hosts*
    anytime two hosts are connected,you have a network.
    It is logical grouping of hosts which require similar connectivity.
    Networks can contain other networks like a school network have classes network,
        sometimes called sub-networks or subnets
### Repeater
*Data crossing a wire decays as it travels to overcome these problem repeaters are used they simply regenerated the signal coming in it  which allow greater transmission of data/signals*
![repeater](https://media.geeksforgeeks.org/wp-content/uploads/20230828190552/IMG-20230828-WA0013.jpg)

### Hub
*When we make a direct cable network between more than 2 devices by a Mesh topology the method doesn't scale so to resolve these devices like hub,bridge,switch,router which are used convert it into star topology *

![topology](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQQLhYGLxiU0lVTeELWssV0_rgJ2cp1VGzM5w&s)

Hub are simply multi-port repeater mean they send the recieving packet to all the other devices connected to it.
![Hub](https://azizozbek.ch/wp-content/uploads/2018/01/bus.gif)

### Bridge
*Bridges sit between Hub connected hosts*
- Bridges only have two ports
- Bridges learn which hosts are on each side
- ![Bridge](https://i.ibb.co/J2sFxYW/Screenshot-from-2024-06-18-21-34-48.png)
- The bridge only allow signals to travel through it if they are sended to the different hub connection

### Switch
*They are a combination of hubs and bridges*
- Multiple ports,
- Learns which hosts are on each port,
- Signal is transmited only between desired devices.
- ![](https://azizozbek.ch/wp-content/uploads/2018/02/Work-Principl-of-Switch.gif)

- Switches facilitate communication within a network
    - Host on a network share the same IP address space
    - ![switch_2](https://i.ibb.co/tpshZL6/Screenshot-from-2024-06-18-22-00-47.png)
    
