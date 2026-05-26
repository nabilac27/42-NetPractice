*This project has been created as part of the 42 curriculum by nchairun*

# <center>NetPractice</center>

## Description
**NetPractice** is a networking training project from the 42 curriculum focused on understanding IP addressing and small network configuration.

The goal of the project is to learn basic networking concepts such as:
- IP addresses
- subnet masks
- CIDR notation
- switches
- routers
- routing tables
- default gateways

The project consists of 10 levels where network configurations must be corrected so devices can communicate successfully.


---

## Instructions
- Compilation*
- Installaton*
- Execution*

### How to run the training interfaces:
- Download the file attached to the project’s page.
- Extract the files into a folder
- In his folder, run te run.sh file
    ```bash
    ./run.sh
    ```
- The shell script will launch a web server and oben preferred web browser to the dedicated page

### How to export configuration
- to-do*
  
### Submission requirements
- to-do*
- 10 exported configuration files (one per level)
must be placed at the repository root

---

## Resources

- documentation*
- articles*
- tutorial*
- How AI was used* (which tasks and which parts of the project)

- To learn subnet mask
  - https://www.youtube.com/watch?v=s_Ntt6eTn94&t=669s 
  - https://www.youtube.com/watch?v=jgwWFKryrOw


### Networking Concepts
- TCP/IP Adressing
- Subnet Mask
- Default Gateways
- Routers and Switches
- OSI Layers

- ---



| Mask          | CIDR | Network Part        |
| ------------- | ---- | ------------------- |
| 255.0.0.0     | /8   | first number        |
| 255.255.0.0   | /16  | first two numbers   |
| 255.255.255.0 | /24  | first three numbers |

----

SUPER IMPORTANT

Avoid these special ranges in NetPractice unless explicitly needed:
| Range           | Meaning               |
| --------------- | --------------------- |
| 127.X.X.X       | localhost/loopback    |
| 0.0.0.0         | default route/special |
| 255.255.255.255 | broadcast             |
