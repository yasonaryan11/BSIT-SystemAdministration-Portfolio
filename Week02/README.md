Week 02 — Enterprise IT Infrastructure Plan
Project Overview

This project presents an Enterprise IT Infrastructure Plan for Nexora Digital Solutions, Inc., a fictional software development startup with 20 employees operating from a single office floor.

The purpose of this project is to design the company's IT infrastructure from the ground up, including hardware, software, networking equipment, network topology, system administration roles, security recommendations, backup strategies, and future expansion plans.

The infrastructure was designed with emphasis on reliability, security, scalability, maintainability, and business requirements.

📄 Complete Infrastructure Plan:
EnterpriseInfrastructurePlan.pdf

Learning Objectives

Through this project, I learned how to:

Analyze the IT requirements of a small organization.
Identify appropriate hardware and software resources.
Prepare professional IT inventories.
Design an enterprise network topology.
Understand different system administration roles.
Develop infrastructure and security recommendations.
Plan backup and disaster recovery strategies.
Document technical decisions professionally using Markdown.
Consider scalability and future infrastructure requirements.
Company Scenario
Nexora Digital Solutions, Inc.

Nature of Business:
Nexora Digital Solutions, Inc. is a Philippine-based software development startup that develops web-based business management systems, cloud-enabled applications, and customized digital solutions for small and medium-sized businesses.

Organization
| Department             | Employees |
| ---------------------- | --------: |
| Information Technology |         5 |
| Human Resources        |         4 |
| Finance                |         5 |
| Sales                  |         6 |
| **Total**              |    **20** |

The company initially has no computers, servers, network infrastructure, Internet infrastructure, or formal security policies. The objective is to establish a complete and scalable IT environment before business operations begin.

Hardware Inventory Summary

The proposed hardware infrastructure includes:
| Hardware               | Quantity | Purpose                                   |
| ---------------------- | -------: | ----------------------------------------- |
| Desktop Computers      |       15 | Primary employee workstations             |
| Laptops                |        5 | Mobile workstations for IT and Sales      |
| Server                 |        1 | Hosts company services and applications   |
| Router                 |        1 | Network routing and Internet connectivity |
| Managed Switches       |        2 | Wired network connectivity and VLANs      |
| Printers               |        3 | Departmental printing and scanning        |
| UPS                    |        8 | Power protection                          |
| Wireless Access Points |        3 | Office-wide wireless connectivity         |
| NAS Storage            |        1 | Centralized storage and backup            |
| External Backup Drives |        2 | Offline backup copies                     |
| Monitors               |       20 | Employee workstation displays             |

Additional infrastructure equipment includes a network rack, patch panels, CAT6 cabling, RJ45 connectors, IP phones, CCTV equipment, and other supporting devices.

Software Inventory Summary

The software environment was selected according to the company's business and development requirements.

| Software           | Version             | Primary Use                |
| ------------------ | ------------------- | -------------------------- |
| Windows 11 Pro     | 25H2                | Employee workstations      |
| Ubuntu Server      | 26.04 LTS           | Server infrastructure      |
| Microsoft Office   | Office 2024         | Business productivity      |
| Visual Studio Code | 1.113.1             | Software development       |
| Git                | 2.51.0              | Version control            |
| GitHub Desktop     | 3.5.0               | Git repository management  |
| VirtualBox         | 7.2.2               | Virtualization and testing |
| Google Chrome      | 151.0.7922.137      | Web applications           |
| Microsoft Defender | Windows 11 built-in | Endpoint security          |
| AnyDesk            | 9.6.0               | Remote IT support          |
| 7-Zip              | 26.02               | File compression           |
| Python             | 3.14.6              | Programming and automation |
| PHP                | 8.3.32              | Web development            |
| Laravel            | 12.0.0              | Web application framework  |
| MySQL              | 8.4 LTS             | Database management        |


Embedded Network Diagram

The diagram below illustrates the logical enterprise network topology of Nexora Digital Solutions, Inc., showing the connection from the Internet and ISP modem through the firewall, router, and core network before reaching the company's servers, wireless access points, printer, and departmental LAN segments.

Network Topology

Network Flow:
Internet
   ↓
ISP Modem / ONT
   ↓
Firewall
   ↓
Router
   ↓
Core Managed Switch
   ├── Server
   ├── NAS
   ├── Network Printer
   ├── Wireless Access Points
   └── Departmental Networks

VLAN Structure
|    VLAN | Department / Function | Network         |
| ------: | --------------------- | --------------- |
| VLAN 10 | IT                    | 192.168.10.0/24 |
| VLAN 20 | HR                    | 192.168.20.0/24 |
| VLAN 30 | Finance               | 192.168.30.0/24 |
| VLAN 40 | Sales                 | 192.168.40.0/24 |
| VLAN 50 | Servers               | 192.168.50.0/24 |
| VLAN 60 | Guest Wi-Fi           | 192.168.60.0/24 |
| VLAN 70 | Network Management    | 192.168.70.0/24 |

Technologies Used
Infrastructure
Windows 11 Pro
Ubuntu Server 26.04 LTS
Managed Ethernet Switches
Enterprise Firewall
Business Router
Wireless Access Points
CAT6 Ethernet
NAS Storage
UPS
Software Development
Visual Studio Code
Git
GitHub Desktop
Python
PHP
Laravel
MySQL
VirtualBox
Documentation & Design
Markdown
GitHub
Draw.io / diagrams.net
Microsoft Word / PDF
Network topology diagrams
Challenges Encountered

One of the main challenges encountered during the project was determining how the different infrastructure components should work together. Selecting hardware was not simply a matter of choosing devices based on quantity; each device had to support the company's departments and future requirements.

Another challenging task was designing the network topology. I had to determine the correct relationship between the ISP modem, firewall, router, switches, servers, wireless access points, and departmental networks while also considering VLAN segmentation.

Maintaining consistency between the hardware inventory, software inventory, network design, and infrastructure recommendations was also important throughout the project.

Reflection

This project helped me understand that system administration involves much more than maintaining computers and solving technical problems. A System Administrator must first understand an organization's requirements and carefully plan its infrastructure before deployment.

I learned how hardware, software, networking, security, backup, and scalability are interconnected. The project also improved my ability to document technical decisions and explain why particular technologies are appropriate for a business environment.

The network diagram was the most challenging part because it required me to visualize how the different infrastructure components communicate with each other. Overall, the project helped me develop a more organized and practical approach to infrastructure planning and strengthened my understanding of the responsibilities of a System Administrator.

References

The following resources were consulted for technical information and software documentation:

1. [Microsoft Windows Documentation](https://learn.microsoft.com/en-us/windows/)
2. [Microsoft Office Documentation](https://learn.microsoft.com/en-us/office/)
3. [Ubuntu Server Documentation](https://documentation.ubuntu.com/server/)
4. [Visual Studio Code Documentation](https://code.visualstudio.com/docs)
5. [Git Documentation](https://git-scm.com/doc)
6. [GitHub Desktop Documentation](https://docs.github.com/en/desktop)
7. [Oracle VirtualBox Documentation](https://www.virtualbox.org/wiki/Documentation)
8. [Google Chrome Documentation](https://developer.chrome.com/docs/)
9. [Microsoft Defender Documentation](https://learn.microsoft.com/en-us/defender/)
10. [AnyDesk Documentation](https://support.anydesk.com/)
11. [7-Zip Official Website](https://www.7-zip.org/)
12. [Python Documentation](https://docs.python.org/)
13. [PHP Documentation](https://www.php.net/docs.php)
14. [Laravel Documentation](https://laravel.com/docs)
15. [MySQL Documentation](https://dev.mysql.com/doc/)

