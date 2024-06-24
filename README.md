# Networking Fundamentals

![Logo](https://images2.alphacoders.com/816/81652.jpg)


## Overview

In these document we would know how do data flow through different devices & internet.




## Contents

 - [Network Devices](#Network-Devices)
    - [Hosts](#Hosts)
    - [IP-Address](#IP-Address)
        - [IPv4](#IPv4)
        - [IPv6](#IPv6)
    - [Network](#Network)
    - [Repeater](#Repeater)
    - [Hub](#Hub)
    - [Bridge](#Bridge)
    - [Switch](#Switch)
    - [Router](#Router)
- [OSI Model](#OSI-Model)
    - [Layer 1 Physical - Transporting Bits](Layer-1-Physical---Transporting-Bits)
    - [Layer 2 Data link - Hop to Hop](Layer-2-Data-link---Hop-to-Hop)
    - [Layer 3 Network - End to End](Layer-3-Network---End-to-End)
    - [Layer 4 Transport - Service to Service](Layer-4-Transport---Service-to-Service)
    - [Layer 5 Session](Layer-5-Session)
    - [Layer 6 Presentation](Layer-6-Presentation)
    - [Layer 7 Application](Layer-7-Application)
- [Everthing Hosts do to speak on the Internet](#Everthing-Hosts-do-to-speak-on-the-Internet)
    - [Hosts connected directly to each other](Hosts-connected-directly-to-each-other)
    - [Hosts connected through a Router](Hosts-connected-through-a-Router)
- [Everything switches do to facilitate communication](Everything-switches-do-to-facilitate-communication)
- [Everthing Routers do](Everthing-Routers-do)
- [Protocols](Protocols)

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

### Router
*facilitate communication between networks*
- Routers learn which networks they are attached to (mean they have a ip address in that network)
    - Known as Routes - Stored in a Routing table
- **Routing table** - all networks a router knows about
- When a device is unable to find the dst in its network it sends it to the default gateway
- ![router](https://i.ibb.co/JcDppmw/Screenshot-from-2024-06-19-11-25-47.png)

## OSI Model

**Its just a way of communication**
**Purpose of Networking**
- Allow two hosts to share data with one another

**OSI model divides rules of networking into 7 layers**
- Each layer servers a specific function. 
- ![osi_model](https://www.practicalnetworking.net/wp-content/uploads/2016/01/packtrav-osi-layers.png)


### Layer 1 Physical - Transporting Bits
- Computer data exists in the form of bits(1's and 0's).
- Something has to transport those bits between hosts.
- L1 Technologies : Cables,wifi,repeaters.
- Simply the devices which carry the data.

### Layer 2 Data link - Hop to Hop
- Interacts  with the wire.
    - Nic-Network interface cards/ wifi access cards
- Addressing Scheme - MAC addresses
    - 48 bits,represented as 12 hex digits
    - Every NIC has a unique MAC address
- Switchs are a example of layer 2 Technologies
as they help to transfer data from one NIC to another between two devices by knowing there mac addresses
- Often communication between hosts require multiple hops
- ![hop-hop](https://i.ibb.co/n0Z2PXX/Screenshot-from-2024-06-19-12-26-06.png)
**In these to transfer data from a1a1 mac to e8e8 first the data moves from a1a1 hop to b2b2 hope and for these L-2 is responsible**


### Layer 3 Network - End to End
- If layer 2 is responsible for hop to hop then what is responsible for end to end transmissoin of data .yes it's layer 3
- Address Scheme - IP address
- Anthing having a IP address is considered to be layer 3

**Layer 3 - IP address          - End to end delivery**

**Layer 2 - MAC address         - Hop to Hop delivery**

why do we need both of them ? 
lets see.

- ![](https://i.ibb.co/qpwhBDH/Screenshot-from-2024-06-19-13-16-09.png)

Over  data a layer 3 is added as we know the destination IP address and then the layer 2 is added to it which tell what is the next hop  then after reaching the hop the layer 2 changes and sets to b3b3 --> c4c4 then c5c5 --> d6d6 then d7d7 --> e8e8 then as the layer 3 IP matches to the computer then both layer are removed and the computer recieved the data


### Layer 4 Transport - Service to Service

**Lets assume a scenario . we are using a computer having a mac,ip address to serve browser and plaing game and attending a meeting at the same time, Each of these server send and recieve packets of data  and all the data will be recieved by the layer 3 header so how will it distinguish the packets between the different services , that where layer 4 comes into play.It makes sure that the right program recieve the right data**

- Address Scheme - Ports
    - 0-65535 - TCP -favour reliablity
    - 0-65535 -UDP - favour efficiency

- Servers listen for requests to pre-defined  Ports
- Clients select random port for each connection
    - ![ports](https://i.ibb.co/vPMvZXf/Screenshot-from-2024-06-19-14-39-21.png)
    - ![ports_2](https://i.ibb.co/yh3x43X/Screenshot-from-2024-06-19-14-44-07.png)

- what if we are using the same service on the same device on different windows ,why don't they merge?
    - because we use different ports for all different windows 
    - eg ![ports_3](https://i.ibb.co/qWbnkgG/Screenshot-from-2024-06-19-14-44-27.png)


### Layer 5 Session

**While surfing a website suppose we change our wifi network then how will the site know that its still us as the layer 3 is changed to solve these problem and  again & again login/logout problem cookies are used which are users local storage info which help site to DISTINGUISH between user independent of later 1,2,3,4**

- HTTP cookies are a type of layer 5 they are arbitary text strings that store user-specific information


### Layer 6 Presentation

**HTTP uses ASCII ecoding so each 8 bit binary  are converted into a ASCII character in these layer **
- Basically layer 6 tells how to interpredict 1's and 0's data 

### Layer 7 Application
**The real execution of request/response or data happens here**

- eg using a GET /simple.html HTTP/1.1  Host :site.com
### lets see the complete process at once 
![](https://i.ibb.co/Tcntcsr/Screenshot-from-2024-06-19-19-37-03.png)


 **So first the application generated data and these process of sending  data is know as Encapsulation and the process of recieving data is know as de-Encapsulation**

 - first data is generated by the application
 - then layer 4 port is added to it
 - then a ip is is stored in it (layer 3)
 - then a mac address (layer 2)
 - then finally data is converted into 1's & 0's and transmitted by layer 1


 - opposite for de-Encapsulation

 - ![](https://i.ibb.co/1JhsKTm/Screenshot-from-2024-06-19-19-45-32.png)

 Atlast OSI model is just a model not rigit rules.

 ## Everything Hosts do to speak on the Internet

### Hosts connected directly to each other
*In these we would discuss about the cases when both the hosts  are on the same network* 


![example](https://i.ibb.co/n88rkcJ/Screenshot-from-2024-06-20-11-06-25.png)
- **Host A and B are directly connected**
    - Both hosts have a NIC,and therefore a MAC address
    - Both hosts are configured with an IP address and a Subnet mask 
        - Subnet mask identifies the size of a IP network mean how many IP comes in it
        - We would discuss subnetting in detail in another [repo](link)

- Host A has some Data to send to Host B
- Host A knows the IP address of Host B 
    - As A have the subnet mask it knows that B is in its own network
- So A knows the IP of B so it can attach a layer 3 header
- we didn't provided the mac address of B to A so layer 2 can't be added but the computer will itself identify the MAC address of B and make the layer 2
    - These will be done with the help of ARP(Address Resolution Protocol)
    - Host A uses ARP to resolve target's MAC address
        - ARP Request asks for the MAC address associated with target IP
            - ARP Request includes sender's MAC address
            - ARP Request is a Broadcast - sent to everyone on the network
                - Destination MAC address: ffff.ffff.ffff
                - ffff.ffff.ffff is a Reserved MAC address to send a packet to everyone on the local network
                - ![](https://i.ibb.co/Y00JDjd/Screenshot-from-2024-06-20-11-30-41.png)

- ARP Mapping are stored in a ARP Cache
- As a reply to ARP B send its mac adderess to IP/MAC of A.
- ![](https://i.ibb.co/DWcFDpW/Screenshot-from-2024-06-20-11-42-02.png)
- When ARP packed is recieved by B then as it contains the IP/MAC of A then get added to the arp cache of B
- Next time when A or B  needs to send packet to B or A then by using its ARP cache 



**After all these A created layer 2 header and data is sent to B**
- L2,L3 header is discarded by B and data is processed by Application


**Now the steps are same regardless of if there are switches or hubs**
    - ARP links a L3 address to a L2 address


### Hosts connected through a Router
*In these we would discuss about the cases when the hosts  are in a  foreign network* 

- ![](https://i.ibb.co/rwZ7DYN/Screenshot-from-2024-06-21-09-38-33.png)

- Host A,Host C,and the router have MAC addresses
    - /24 is a subnet Mask - 255.255.255.0
    - Subnetting is not covered in this module will discuss it in another ripo
- Host A has some data to send to Host C
    - Host A knows Host C's IP address
        - Provided by the user or the Application 

    - Host A knows Host C's IP address is on a foreign network by help of its subnet and default gateway
    - So now to know the mac adderess of router for hop to hop it uses arp
    - then data is sent to router same thing repeates and data is sended
    
    
## Everything switches do to facilitate communication

- Switching is the process of moving data within networks 
    - Switches are devices whose primary purpose is Switching
    - Devices communicating through a switch belong to the same IP network
- Switches are L2 devices = They only use L2 header to make decisions
- ![](https://i.ibb.co/PM85fVQ/Screenshot-from-2024-06-21-11-04-03.png)
- Switches use and maintain MAC Address table
    - Mapping os switch Ports to MAC addresses
- Switches perform three actions:
    - **Learns** - Update MAC Address Table with mapping of switch port to sourse MAC 
    ![](https://i.ibb.co/8rHFd1L/Screenshot-from-2024-06-21-11-43-29.png)
    ![](https://i.ibb.co/DY9ywNK/Screenshot-from-2024-06-21-11-44-06.png)
    - **Flood** - duplicate and send frame out of all port expect receiving
    ![](https://i.ibb.co/TM6wCVk/Screenshot-from-2024-06-21-11-47-47.png)
    - **Forward** - Now Host D will send a response on the wire and by learning action its address will get added to the MAC TABLE of switch and these time direct forward will occur as the switch knows the address of A 
    ![](https://i.ibb.co/pj1k7WB/Screenshot-from-2024-06-21-11-52-05.png)
    ![](https://i.ibb.co/6sQPxKP/Screenshot-from-2024-06-21-11-52-28.png)


- Unicast frame - Destination MAC is another Host
    - **Switch will flood only if MAC address is not in the MAC address table**

- Broadcast frame - Destination MAC address of FFFF.FFFF.FFFF
    - Broadcast frames are always flooded


## Everthing Routers do

- Routers are connected to a network
    - Routers have an IP address and a MAC address

then what? the difference b/w a router and a Host?

![RFC2460](https://i.ibb.co/fNR8PzR/Screenshot-from-2024-06-21-13-07-00.png)

a host will reject a packet if it's not addressed to it 
whereas a router will help the packet reach its destination


- Routers maintain a map of all the networks they know about 
    - Routing table
    - ![](https://i.ibb.co/NNzp3t4/Screenshot-from-2024-06-21-13-10-47.png )

- Routing table can be populated via three methods:
    - Direct Connected - Routes for the networks which are attached 
    ![](https://i.ibb.co/5YD9432/Screenshot-from-2024-06-23-16-00-07.png)
    
    but what if a device in 10.0.66.x/24 want to talks with a device in 10.0.44.x/24
    there is no direct  route so we will see the second type

    - Static Routes - Routes manually provided by a Adminstrator

    it tells if it want to talk to a specific IP range then it can send the packet to a following router IP
    ![](https://i.ibb.co/99S0s43/Screenshot-from-2024-06-23-16-35-23.png)

    - Dyanmic Routes - Routes automatically learned form other routers. 
    although they are same as static but the only difference is they are added automatically

    ![](https://i.ibb.co/1XWK44f/Screenshot-from-2024-06-23-16-49-02.png)

- Routers also have ARP tables
    - Everything with a IP have a ARP table
![](https://i.ibb.co/1TTh25q/Screenshot-from-2024-06-23-16-54-54.png)


***Lets see how does thes arp table starts from empty***

*Supporse 10.0.44.9 wants to send a message to 10.0.66.7*

-   As the IP is not in its own network so it will send the data to the default gateway
-   But to sednd the data L2 header is not know mean the MAC of Default gateway
-   SO a ARP request will be broadcasted 
-   And router will add the IP and MAC of A in iys ARP table
-   now a arp request will be sent to know the address of router 2 by router 1 then for c and the packet will reach c 
- Now for sending a message from C to A no arp will be required as all required mac are in the respective arp table

## Protocals
**Set of rules and messages that form an Internet Standard**

- ARP - Address Resolution Protocal - RFC 826
    - Resolves IP to MAC mapping
    - ARP request/ARP responses

![RFC_826](https://i.ibb.co/yYGS1cw/Screenshot-from-2024-06-24-13-30-50.png)

- FTP - File Transfer Protocol
    - ![](https://i.ibb.co/QMZBVXW/Screenshot-from-2024-06-24-13-46-16.png)

- SMTP - Simple Mail Transfer Protocol
    - ![](https://i.ibb.co/fGV0hGT/Screenshot-from-2024-06-24-13-52-35.png)

- HTTP - Hyper Text Transfer Protocol
    - ![](https://i.ibb.co/B6pX1ZM/Screenshot-from-2024-06-24-13-56-12.png)

- SSL - Secure Sockets Layer

- TLS - Transport Layer Security

- HTTS - HTTP secured with SSL/TLS is know as HTTPS

![](https://i.ibb.co/Nsn7xrd/Screenshot-from-2024-06-24-13-56-28.png)


- DNS - Domain Name System
    - Converts Domain Names into IP addresses
    -  eg Site.com --> 35.176.92.19
    

Every  host needs four items for Internet connectivity
- IP Address  - Host's Identity on the internet
- Subnet Mask - Size of Host's Network
- Default Gateway - Router's IP address
- DNS Server IP(s) - Translate domain names to IPs


But everytime we connect to a new wifi we don't configure them so what controls it?

- DHCP - Dynamic Host Configuration Protocol
    - DHCP server provides IP/SM/DG/DNS for clients



------------------End------------------------------------------
