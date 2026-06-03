*This project has been created as part of the 42 curriculum by nchairun*

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/8d/42_Logo.svg" width="100"/>
</p>

<h1 align="center">
  NetPractice
</h1>

## Description
**NetPractice** is a 42 networking project designed to introduce the fundamentals of **TCP/IP networking** and **small network configuration**.

The goal of the project is to understand how devices communicate through **IP addressing, subnet masks, CIDR notation, switches, routers, routing tables, and default gateways**.

The project consists of 10 levels where incorrect network configurations must be analyzed and fixed so devices can communicate successfully across the network.


---

## Instructions
### Compilation
- No complation is required for this project.

### Installation
- Download the file attached to the project page.
- Extract the files into a folder of your choice.

### Execution
#### How To Run Training Interface
- In the folder, run te run.sh file
    ```bash
    ./run.sh
    ```
  This script launches a local web server and opens the NetPractice interface in web browser.

- If the script does not work properly, run the server manually: 
  ```bash
  python3 -m http.server 49242
  ```
- Then open this in web browser:
  ```bash
  http://localhost:49242
  ```

### How To Export Configuration
After completing a level:
- Click the **[Get my config]** button.
- Download the exported configuration file.
- Save the file in the root of the repository.


### Submission Requirements
The repository must contain:
- 10 exported configuration files.
- one configuration file for each level.
- all files placed at the repository root.

The project requires completing all 10 levels.

---

## Resources
### Documentation
- 42 NetPractice subject.
- TCP/IP and IPv4 addressing documentation.
- CIDR and subnet mask references.

### Articles and Tutorials
The following resources were used to study networking fundamentals such as **TCP/IP addressing, subnet masks, CIDR notation, default gateways, routers, switches, and basic OSI layer** concepts:
  - https://www.youtube.com/watch?v=s_Ntt6eTn94&t=669s 
  - https://www.youtube.com/watch?v=jgwWFKryrOw

  - https://github.com/lpaube/NetPractice

### AI Usage
AI tools were used as learning assistance during the project to:
- understand subnet masks and CIDR notation.
- explain networking concepts in beginner-friendly terms.
- practice subnet calculations and routing logic.
- review and improve the README structure and formatting.

---

## Networking Concepts Learned
- **TCP/IP addressing**
  
  how devices identify and communicate with each other on a network.

  - **TCP** stands for Transmission Control Protocol
    
    It is a communications standard that enables devices to exchange messages over a network. It is used to send packets across the internet.

  - **IP** is part of an internet protocol suite
    
    which also includes the transmission control protocol. Together, these two are known as TCP/IP. 
    
    The internet protocol suite governs rules for packetizing, addressing, transmitting, routing, and receiving data over networks.

- **Subnet masks and CIDR notation**

  how networks are divided into smaller subnetworks.

  - **Subnet Mask** 
    
    is a 32 bits (4 bytes) address used to distinguish between a network address and a host address in the IP address. 

    It defines the range of IP addresses that can be used within a network or a subnet.

  - **Classless Inter-Domain Routing (CIDR)**
    
    This form represents the SUBNET mask as a slash "/",
    
    followed by the number of bits that serve as the network address.
  
- **Default Gateways and Routing Basics**

  how packets are sent between different networks.

  - **Default Gateway**
 
    is the router interface used to leave the local subnet.
    
    A computer can directly communicate only with devices inside its own subnet.

    When the destination is outside the local network, packets are sent to the default gateway, which is usually a router.

    When PC1 wants to communicate with another network:
    ```bash
    PC1 -> Gateway(router) -> Destination network
    ```
    The gateway must belong to the same subnet as the host.
  

    simplest packet flow model

      same subnet
      - -> direct communication

      different subnet
      
      - -> send to gateway
      - -> router forwards packet
      - -> destination receives

  - **Router Interfaces**
  
    Routers connect multiple networks together.

    Example:

        Router left  = 192.168.1.1/24
        Router right = 192.168.2.1/24

      The router belongs to both networks and forwards packets between them.

  - **Routing Basics**

    Routers use routes to decide where packets should be forwarded.

    A route is essentially:

    ```bash
    destination network -> next hop
    ```

    Example:
    ```bash
      192.168.2.0/24 -> 10.0.0.2
    ```

    Meaning:
  
    To reach the 192.168.2.0/24 network, send packets to the router at 10.0.0.2.

- **Routers and switches**

  how devices and networks are connected together.
  
  - switch connects multiple devices together in a single network.

  - router connects multiple networks together.

  - routing table
    
    routing table is a data table stored in a router.
    It consits of
    - Destination
      
      specifies a network address on which a host is the end target of the packets. The route of default or 0.0.0.0/0, is the route that takes effect when no other route is available for an IP destination address. 
      
      The default route will use the next-hop address to send the packets on their way without giving a specific destination. The default route will match any network.

    - Next hop
    
      The next hop refers to the next closest router a packet can go through. It is the IP address of the next router on the packet's way. 

- **Network and broadcast addresses**

  reserved addresses used to identify and manage networks.

  - **Network Address** 
    
    identifies the subnet itself. 
    
    It is always the first address in the subnet.

  - **Broadcast Address**
    
    is used to send packets to all devices inside the subnet.
    
    It is always the last address in the subnet.

- **OSI layer basics**
  
  introduction to the different layers involved in network communication.

  - **OSI (Open Systems Interconnection) model** 
    
    describes how data travels through a network
  
  - **7 OSI Layers**
  
    | Layer | Name         | Main Purpose                        |
    | ----- | ------------ | ----------------------------------- |
    | 7     | Application  | User-facing network services        |
    | 6     | Presentation | Data formatting and encryption      |
    | 5     | Session      | Connection management               |
    | 4     | Transport    | Reliable data transport             |
    | 3     | Network      | Routing and IP addressing           |
    | 2     | Data Link    | MAC addresses and local delivery    |
    | 1     | Physical     | Electrical or physical transmission |

- **Summary**
  - Same subnet → direct communication
  - Different subnet → send packet to default gateway
  - Default gateway → router used to leave local network
  - Routers forward packets between networks
  - Routes tell routers where packets should go next

---

### Useful References
**CIDR and Subnet Mask Reference**
| Subnet Mask     | CIDR | Block Size | Network Portion                   |
| --------------- | ---- | ---------- | --------------------------------- |
| 255.0.0.0       | /8   | 16,777,216 | first number                      |
| 255.255.0.0     | /16  | 65,536     | first two numbers                 |
| 255.255.255.0   | /24  | 256        | first three numbers               |
| 255.255.255.128 | /25  | 128        | first 3 numbers + half of last    |
| 255.255.255.192 | /26  | 64         | first 3 numbers + quarter of last |
| 255.255.255.224 | /27  | 32         | subnet jumps by 32                |
| 255.255.255.240 | /28  | 16         | subnet jumps by 16                |
| 255.255.255.248 | /29  | 8          | subnet jumps by 8                 |
| 255.255.255.252 | /30  | 4          | subnet jumps by 4                 |

**Block size formula**
```bash
256 - last subnet mask octet = block size
```

**Special IP Ranges**

The following IP ranges are reserved for special purposes and should generally not be used as normal host addresses.
| Range                   | Purpose                                  | Example Use                                     |
| ----------------------- | ---------------------------------------- | ----------------------------------------------- |
| 127.X.X.X               | localhost / loopback                     | testing local machine using `127.0.0.1`         |
| 0.0.0.0                 | default route / unspecified address      | router sends unknown traffic to default gateway |
| 255.255.255.255         | local network broadcast                  | DHCP discovery packets                          |


**Private IP Ranges**

The internet behaves like a router. However, if an interface is connected directly or indirectly to the internet, it cannot have an IP address in the following reserved private IP ranges:

| Private IP Range      | Start Address | End Address     | Number of IP Addresses |
| --------------------- | ------------- | --------------- | ---------------------- |
| Class C Private Range | 192.168.0.0   | 192.168.255.255 | 65,536                 |
| Class B Private Range | 172.16.0.0    | 172.31.255.255  | 1,048,576              |
| Class A Private Range | 10.0.0.0      | 10.255.255.255  | 16,777,216             |


---
