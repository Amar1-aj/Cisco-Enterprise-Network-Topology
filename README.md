Cisco Packet Tracer – IT, HR & Server Farm Network Topology

📌 Project Overview

This project demonstrates the design and configuration of a small enterprise network using Cisco Packet Tracer. The network consists of three departments: IT, HR, and Server Farm, connected through a Cisco 2911 router and three Cisco 2960 switches.
The project implements IPv4 and IPv6 addressing, DHCP services, DNS services, HTTP web hosting, wireless connectivity, and remote device management using SSH and Telnet.
The primary objective is to understand practical networking concepts, device configuration, IP addressing, DHCP relay, and network connectivity troubleshooting.

🖥️ Network Topology

Network Devices

Device	Model / Name	Quantity
Router	Cisco 2911 (R1)	1
Switch	Cisco 2960 (IT-Switch)	1
Switch	Cisco 2960 (HR-Switch)	1
Switch	Cisco 2960 (SERVER-FARM)	1
End Devices	PCs and Guest Phone	Multiple
Servers	DHCP, DNS, HTTP	3

Wireless Access Point	AP-Guest	1

🌐 Network Addressing Scheme

The network is divided into three separate IPv4 subnets.
Department	Network Address	Subnet Mask	Default Gateway
IT	192.168.1.0/25	255.255.255.128	192.168.1.1
HR	192.168.1.128/26	255.255.255.192	192.168.1.129
Server Farm	192.168.1.192/27	255.255.255.224	192.168.1.193
Router Interface Configuration
Router Interface	IPv4 Address	IPv6 Address
G0/0	192.168.1.1/25	2001:DB8:ACAD:1::1/64
G0/1	192.168.1.129/26	2001:DB8:ACAD:128::1/64
G0/2	192.168.1.193/27	2001:DB8:ACAD:192::1/64

🖥️ Server Configuration

Three dedicated servers are configured in the Server Farm network.
Server	IPv4 Address	Function
HTTP Server	192.168.1.221	Hosts a web page
DNS Server	192.168.1.222	Domain name resolution
DHCP Server	192.168.1.220	Automatic IP allocation
DHCP Configuration

The DHCP server automatically assigns IPv4 addresses to clients in the IT network.

•	DHCP Server IP: 192.168.1.220
•	Default Gateway: 192.168.1.1
•	DNS Server: 192.168.1.222
•	Starting IP Address: 192.168.1.100
•	Subnet Mask: 255.255.255.128
•	Maximum Users: 27

DHCP Relay Configuration:

The router uses the ip helper-address command to forward DHCP requests from the IT network to the DHCP server.
interface GigabitEthernet0/0
 ip helper-address 192.168.1.220
 
🔧 Technologies and Networking Concepts

The following networking concepts are implemented in this project:
•	IPv4 and IPv6 addressing
•	Subnetting and IP address planning
•	Cisco router configuration
•	Cisco Layer 2 switch configuration
•	DHCP server configuration
•	DHCP relay using IP Helper Address
•	DNS server configuration
•	HTTP server configuration
•	Wireless networking
•	WPA2-PSK wireless security
•	SSH remote device management
•	Telnet remote access
•	IPv6 unicast routing
•	Basic network connectivity troubleshooting

🔐 Security Configuration

Basic device security and remote management are configured on the router and switches.
•	Hostname configuration
•	Enable secret password
•	Console password protection
•	VTY line authentication
•	Password encryption
•	MOTD banner configuration
•	SSH version 2 configuration
•	RSA key generation
•	Local username authentication

📡 Wireless Network Configuration

A wireless access point is configured for guest connectivity.
Setting	Configuration
SSID	Guest
Security	WPA2-PSK
Authentication Key	Cisco123
IP Configuration	DHCP

🌍 DNS and HTTP Services

DNS Configuration
A DNS record is configured to resolve the domain name:
techacadipv4.com
The domain points to the HTTP server IPv4 address.
An additional DNS record is configured for IPv6 access.
HTTP Configuration
The HTTP server hosts a custom HTML page:
Project1 Using CISCO Packet Tracer
Welcome to TechAcad Project.
The web page can be accessed using the HTTP server's IPv4 or IPv6 address.

🧪 Network Testing and Verification

The following tests are performed to verify network functionality:
Test	Purpose
ping	Verify network connectivity
ipconfig	Check IPv4 configuration
ipconfig /renew	Request an IP address through DHCP
show ip interface brief	Check router interface status
show running-config	Verify device configuration
ssh -l admin IP_ADDRESS	Test secure remote access
telnet IP_ADDRESS	Test remote device access

Additional verification includes:
•	Testing communication between IT and HR networks.
•	Testing connectivity between PCs and servers.
•	Verifying automatic IP allocation through DHCP.
•	Accessing the HTTP web page using IPv4 and IPv6.
•	Testing DNS name resolution.
•	Testing wireless guest connectivity.

📚 Learning Outcomes

Through this project, I gained practical experience in:
1.	Designing a small enterprise network.
2.	Configuring Cisco routers and switches.
3.	Understanding IPv4 subnetting and IPv6 addressing.
4.	Configuring DHCP, DNS, and HTTP services.
5.	Implementing DHCP relay.
6.	Configuring SSH and Telnet remote access.
7.	Troubleshooting network connectivity and DHCP issues.
8.	Understanding basic wireless network security.

🛠️ Software Used
•	Cisco Packet Tracer

📁 Project Files
•	Cisco Packet Tracer topology file (.pkt)
•	Network topology screenshot (.png)



