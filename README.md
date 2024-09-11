# Pulchowk Campus Network Project

## Overview
This project models the network topology of Pulchowk Campus, implemented using **Cisco Packet Tracer**. The network is divided into five areas with 16 routers, 16 switches, and PCs connected via switches. The network supports different departments and services, featuring DNS and Web servers for domain resolution and hosting internal and external websites.
![image](https://github.com/user-attachments/assets/3459f26a-8f9d-49c1-8570-d9c9523c7b00)
## Network Address Block
- **192.168.0.0/20**

## Areas and Subnet Allocation

### Area 1: Civil, Aerospace, Mechanical, and Chemical Departments
| Department  | Hosts Required | Subnet        | Subnet Mask       | Available IP Range           |
|-------------|----------------|---------------|-------------------|------------------------------|
| Civil       | 500            | 192.168.0.0/23 | 255.255.254.0      | 192.168.0.1 - 192.168.1.254   |
| Mechanical  | 200            | 192.168.2.0/24 | 255.255.255.0      | 192.168.2.1 - 192.168.2.254   |
| Aerospace   | 150            | 192.168.3.0/24 | 255.255.255.0      | 192.168.3.1 - 192.168.3.254   |
| Chemical    | 150            | 192.168.4.0/24 | 255.255.255.0      | 192.168.4.1 - 192.168.4.254   |

### Area 2: Computer, Electronics, Electrical Departments
| Department     | Hosts Required | Subnet        | Subnet Mask       | Available IP Range           |
|----------------|----------------|---------------|-------------------|------------------------------|
| Computer       | 400            | 192.168.5.0/23 | 255.255.254.0      | 192.168.5.1 - 192.168.6.254   |
| Electronics    | 200            | 192.168.7.0/24 | 255.255.255.0      | 192.168.7.1 - 192.168.7.254   |
| Electrical     | 200            | 192.168.8.0/24 | 255.255.255.0      | 192.168.8.1 - 192.168.8.254   |

### Area 3: Dean Office, Architecture, and Library
| Department     | Hosts Required | Subnet        | Subnet Mask       | Available IP Range           |
|----------------|----------------|---------------|-------------------|------------------------------|
| Dean Office    | 150            | 192.168.9.0/24 | 255.255.255.0      | 192.168.9.1 - 192.168.9.254   |
| Architecture   | 150            | 192.168.10.0/24| 255.255.255.0      | 192.168.10.1 - 192.168.10.254 |
| Library        | 200            | 192.168.11.0/24| 255.255.255.0      | 192.168.11.1 - 192.168.11.254 |

- **Dean Office VLANs**:
  - VLAN10 (Account): 192.168.9.64/27
  - VLAN20 (Administration): 192.168.9.32/27
  - VLAN30 (Management): 192.168.9.96/27

### Area 4: Boys and Girls Hostels
| Department     | Hosts Required | Subnet        | Subnet Mask       | Available IP Range           |
|----------------|----------------|---------------|-------------------|------------------------------|
| Boys Hostel    | 150            | 192.168.12.0/24| 255.255.255.0      | 192.168.12.1 - 192.168.12.254 |
| Girls Hostel   | 50             | 192.168.13.0/26| 255.255.255.192    | 192.168.13.1 - 192.168.13.62  |

### Area 0: Backbone Network (CIT)
- **CIT Server**: 
  - Subnet: 192.168.14.160/30
  - IP Range: 192.168.14.161 - 192.168.14.167
- **ISP Connection**: 
  - Subnet: 192.168.15.0/24
  - IP Range: 192.168.15.1 - 192.168.15.254
                   |

> **Note**: Static routing is used to forward internet traffic to the ISP through CIT in Area 0.

## IP Addresses for Servers
| Server            | IP Address        | Domain               |
|-------------------|-------------------|----------------------|
| Web Server (Computer Dept.) | 192.168.5.5 | www.locus.com        |
| Web Server (CIT)  | 192.168.14.162     | www.pcampus.com       |
| Web Server (ISP)  | 150.168.15.3       | www.google.com        |
| DNS Server (Computer Dept.) | 192.168.5.4 | Resolves `locus.com` |
| DNS Server (CIT)  | 192.168.14.163     | Resolves `pcampus.com`|
| DNS Server (ISP)  | 150.168.15.2       | Resolves `google.com` |

## Connectivity 
- Ping from PC0 to PC18
![Ping](https://github.com/user-attachments/assets/c43d2056-44c2-440a-9e33-2113740d8e59)

- Telnet:
From PC20 to Subash3
![Telnet](https://github.com/user-attachments/assets/8e41775a-6fe8-44f4-8438-921a26131173)

DNS Resolution:
For www.locus.com:
![locus](https://github.com/user-attachments/assets/f9e60ebb-0050-44fd-a517-df9b4b565fa6)

For www.pcampus.com:
![pcampus](https://github.com/user-attachments/assets/6a952cc0-6fc1-482f-84ee-9f7b3cfbae45)

For google.com:
![image](https://github.com/user-attachments/assets/47769fdf-a644-4db5-8984-7a8900dd49d6)

## Technologies Used
- **Cisco Packet Tracer**: For network simulation and configuration.
- **DNS and Web Servers**: Used for resolving domain names and hosting web applications.
- **VLANs**: To segment the network for administrative purposes (e.g., Dean Office).

## How to Run the Project
1. Open **Cisco Packet Tracer**.
2. Load the provided `project.pkt` file.
3. Simulate network traffic by sending requests from PCs in different areas.


