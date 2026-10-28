# CAPSTONE FINAL ASSESSMENT

Created for Leep Talent’s Level 3 Cybersecurity Bootcamp.


#### PROJECT OVERVIEW

This project was completed as part of Leep Talent’s Level 3 Cybersecurity Bootcamp. It involves expanding an existing business network to accommodate additional staff and an additional office, while improving network security and connectivity for a fictional organisation called Capstone. The assessment covers network design, IP addressing, DHCP, email services, wireless configuration, device hardening, and connectivity testing using Cisco Packet Tracer.

---

#### PROJECT FILES

##### Network Design:

##### Evidence Sheet:

---

#### LEARNING OBJECTIVES

- Configure wired and wireless networks
- Configure DHCP services
- Apply basic cybersecurity protections
- Configure basic routing
- Implement secure device management
- Configure Email
- Test and troubleshoot connectivity
- Document evidence professionally

---

#### ASSESSMENT BRIEF / SCENARIO

You are a junior network engineer working for a growing company called TechSolutions Ltd.

- The company currently employs 8 people.
- 4 staff members are permanently based in the office using the 4 client PCs.
- 2 PCs have static IP addresses assigned. 1 Printer has a static IP address assigned. All
other PCs, Laptops and mobile phones use DHCP.
- 4 staff members regularly visit customers and use Laptops.
- All Staff members have mobile phones.
- There are 2 printers in the office. 1 wired and 1 wireless.
- There is 1 Wi-Fi router serving the entire office.
- There is 1 server providing DHCP leases.

The company is expanding operations and is looking to hire 4 more staff. The office next door has
been purchased in preparation. Physical wired communication devices have been installed between the two offices in the form of a router and cable. The Gigabit ports on the Router are configured with IP addresses. Management is also aware that security needs to be improved and has tasked you with strengthening the level of security across the entire infrastructure.

**Your task is to deploy, configure, secure, and test the network using Cisco Packet Tracer.**

---

#### SPECIFICATION

###### Network Requirements:

- Additional network devices.
- Secure wireless connectivity.
- Secure router and switch configuration.
- Additional DHCP services.
- Static addressing for infrastructure devices.
- Printer connectivity.
- Email configuration.
- Secure router and switches.


###### Addressing Table:

| Network | Purpose | Address Range | Network Class |
|---|---|---|---|
| Office 1 | Main office | 192.168.1.1 – 192.168.1.254 | Class C |
| Office 2 | Second office | 192.168.2.1 – 192.168.2.254  | Class C |

---

#### TASKS

##### Task 1 - Basic Network Topology

###### Second Office Requirements:
- 1 switch – Wired to the Router Gigabit port 0/1.
- 4 wired PCs and 1 wired Printer with the following configurations.

###### Second Office Configuration Settings:
| Name | IP Configuration | Subnet Mask | Gateway |
|---|---|---|---|
| Client 5 | DHCP | 255.255.255.0 | 192.168.1.10 |
| Client 6 | DHCP | 255.255.255.0 | 192.168.1.10 |
| Client 7 | DHCP | 255.255.255.0 | 192.168.1.10 |
| Client 8 | DHCP | 255.255.255.0 | 192.168.1.10 |
| Printer 3 |192.168.2.3 | 255.255.255.0 | 192.168.1.10 |

###### Evidence Required:
- Full logical topology, correct cabling, and device labels.
- IP configuration of any PC in Main Office.
- IP configuration of Printer 3.


##### Task 2 - DHCP Configuration

###### Second Office Requirements:
- Configure DHCP services for OFFICE 2:
- Add a server in Office 2 and change its name to DHCP 2.
- Wire it to the switch with the appropriate cabling.
- Enable DHCP on the server.
- Set Clients 5, 6, 7, and 8 to use DHCP.

###### Second Office Configuration Settings:
| Setting | Value |
|---|---|
| Server IP | 192.168.2.1 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.1.10 |
| DNS Server | 192.168.1.10 |
| Starting Address | 192.168.2.50 |
| Maximum Users | 100 |

###### Testing:
- Verify clients can ping devices in other offices.

###### Evidence Required:
- DHCP pool configuration.
- Any PC in Second Office IP configuration.
- Any PC in Second Office to Main Office.
- Any PC in Main Office to Second Office.


##### Task 3 - Email Configuration

###### Requirements:
- Deploy a new Email server in Main Office (add server from menu – do not use the existing
server).
- Use appropriate wiring to cable it into the switch.
- Rename the server “EMAIL”.
- Configure the server with the Server settings below.
- Configure Email from the services tab with the Email Settings and User settings below.
- Configure any PC in Main Office with Setup Client 1 Email settings.
- Configure any PC in Other Office with Setup Client 8 Email settings.

###### Server Settings:
| Setting | Value |
|---|---|
| Server IP | 192.168.1.2 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.2.10 |
| DNS Server | 192.168.2.10 |
| Display name | EMAIL |

###### Email Settings:
| Setting | Value |
|---|---|
| SMTP | ON |
| POP3 | ON |
| Domain name | ts.com (remember to SET) |

###### User Setup:
| Username | Password |
|---|---|
| Client1 | Password1 |
| Client8 | Password8 |

###### Setup Client 1 email:
| Setting | Value |
|---|---|
| Your Name | Client1 |
| Email Address | Client1@ts.com |
| Incoming Mail | Server 192.168.1.2 |
| Outgoing Mail | Server 192.168.1.2 |
| User Name | Client1 |
| Password | Password1 |

###### Setup Client 8 email:
| Setting | Value |
|---|---|
| Your Name | Client8 |
| Email Address | Client8@ts.com |
| Incoming Mail Server | 192.168.1.2 |
| Outgoing Mail Server | 192.168.1.2 |
| User Name | Client8 | 
| Password | Password8 |

###### Testing and Evidence Required:
- Screenshots of EMAIL server configuration.
- Screenshot of Client 1 email configuration.
- Send an email from Client 1 to Client 8 & Screenshot of received email on Client 8.


##### Task 4 - Wireless Security Configuration

###### Main Office Requirements:
- Configure secure wireless access for Main Office:
- Configure the Wireless router with the settings in “Staff Wireless Settings”.
- Connect all Laptops and mobile phones to the Wi-Fi network securely. (some physical
hardware changes may be required on the laptops).
- Verify all devices receive IP addresses.
- Test connectivity to local gateway with ping from any laptop.

###### Staff Wireless Settings:
| Setting | Value |
|---|---|
| SSID | MainOffice |
| Security | WPA2-PSK |
| Password | Passcode123! |

###### Evidence Required:
- Basic Wireless settings.
- Wireless Security.
- All connected wireless devices in Logical view.
- Successful ping test from any wirelessly connected laptop to gateway.


##### Task 5 - Cybersecurity Hardening (secure the router and the two switches)

###### Requirements: 
Configure Hostnames:
| Device | Name |
|---|---|
| Router | R1 |
| Main office | Switch S1 |
| Second office | Switch S2 |

###### R1, S1, and S2 Settings:
- Secure user EXEC mode with password & Secure Console port with password Cisco123.
- Secure privileged EXEC mode with password Cisco123.
- Encrypt passwords.
- Set Message Of The Day e.g. Authorised Access Only.
- Configure SSH on R1.

###### Testing and Evidence Required:
- Test SSH login to R1 from any Client 8.
- Connect Client 8 to R1 with Console cable – Test connection.
- Show the full running configuration of R1.
- Reload R1 to the login screen asking for password.
