*This project has been created as part of the 42 curriculum by nchairun*

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/8d/42_Logo.svg" width="120"/>
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


### Submission requirements
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

- **Subnet masks and CIDR notation**

  how networks are divided into smaller subnetworks.
  
- **Default gateways and routing basics**

  how packets are sent between different networks.

- **Routers and switches**

  how devices and networks are connected together.

- **Network and broadcast addresses**

  reserved addresses used to identify and manage networks.

- **OSI layer basics**
  
  introduction to the different layers involved in network communication.

### Useful References
**CIDR and Subnet Mask Reference**
| Mask          | CIDR | Network Portion     |
| ------------- | ---- | ------------------- |
| 255.0.0.0     | /8   | first number        |
| 255.255.0.0   | /16  | first two numbers   |
| 255.255.255.0 | /24  | first three numbers |

**Special IP Ranges**

The following IP ranges are reserved for special purposes and should generally not be used as normal host addresses.
| Range           | Purpose                  |
| --------------- | ------------------------ |
| 127.X.X.X       | localhost / loopback     |
| 0.0.0.0         | default route            |
| 255.255.255.255 | broadcast address        |
