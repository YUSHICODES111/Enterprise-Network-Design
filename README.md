# Enterprise Network Design and Implementation

## Project Overview

This project demonstrates the design and simulation of a basic enterprise network using Cisco Packet Tracer.

The network represents an organisation with three departments: HR, IT, and Finance. Each department has five computers connected through a central switch and router.

The main objective is to understand how organisations can manage departmental networks, separate network traffic, automate IP address allocation, and enable communication between different departments.

## Network Components

| Component | Quantity | Purpose |
|---|---:|---|
| Cisco 2911 Router | 1 | Routes traffic between different networks |
| Cisco 2960 Switch | 1 | Connects computers within the network |
| PCs | 15 | Represents users across three departments |
| VLANs | 3 | Separates departmental network traffic |

## Tools and Technologies Used

- **Cisco Packet Tracer:** Used to design, configure, and simulate the network.
- **VLAN (Virtual LAN):** Used to logically separate HR, IT, and Finance departments.
- **IPv4 Addressing:** Used to assign IP addresses to different departmental networks.
- **802.1Q Trunking:** Used to carry traffic from multiple VLANs through a single router-switch connection.
- **Router-on-a-Stick:** Used to enable communication between different VLANs through router subinterfaces.
- **DHCP (Dynamic Host Configuration Protocol):** Used to automatically assign IP addresses and network settings to computers.
- **Cisco IOS Commands:** Used to configure network devices and verify network connectivity.

## Network Configuration

Three VLANs were created to separate the departments.

| Department | VLAN ID | Network Address | Default Gateway |
|---|---:|---|---|
| HR | 10 | 192.168.10.0/24 | 192.168.10.1 |
| IT | 20 | 192.168.20.0/24 | 192.168.20.1 |
| Finance | 30 | 192.168.30.0/24 | 192.168.30.1 |

Each department contains five computers.

The router was configured with separate subinterfaces for each VLAN, enabling communication between the departmental networks.

DHCP pools were configured for all three departments to automate IP address allocation.

## Implementation Steps

1. Designed the network topology using Cisco Packet Tracer.
2. Connected 15 computers to a Cisco 2960 switch.
3. Created three VLANs for HR, IT, and Finance.
4. Assigned switch ports to their respective VLANs.
5. Configured trunking between the switch and router.
6. Configured router subinterfaces for inter-VLAN routing.
7. Configured DHCP pools for automatic IP address allocation.
8. Tested connectivity between computers and different VLANs.

## Testing and Verification

The network was tested using the following commands:

| Command | Purpose |
|---|---|
| `show vlan brief` | Verify VLAN creation and port assignments |
| `show interfaces trunk` | Check trunk configuration |
| `show ip interface brief` | Check router interface status |
| `show ip dhcp binding` | Verify assigned IP addresses |
| `ping` | Test connectivity between devices |

The simulation successfully demonstrated DHCP address allocation, communication with default gateways, and connectivity between different VLANs.

## How This Project Is Useful

This project demonstrates networking concepts commonly used in organisational IT environments.

- **Departmental Segmentation:** VLANs help separate departments and organise network traffic.
- **Simplified IP Management:** DHCP reduces the need to configure IP addresses manually on every computer.
- **Interdepartmental Communication:** Inter-VLAN routing allows authorised communication between separate departmental networks.
- **Network Troubleshooting:** Connectivity tests and Cisco IOS commands help identify basic network configuration issues.
- **Practical Learning:** The simulation provides hands-on experience with basic enterprise networking concepts without requiring physical networking equipment.

## Project Files

- `Enterprise_Network_Design.pkt` – Cisco Packet Tracer simulation file.
- `Screenshots/` – Network topology and configuration screenshots.

## Future Improvements

- Implement Access Control Lists (ACLs) to control communication between departments.
- Configure port security to restrict unauthorised device connections.
- Add additional switches to support network expansion.
- Explore network redundancy and dynamic routing.

## Author

**Ayushi Shukla**

B.Tech – Computer Science and Engineering (Data Analytics)

Areas of Interest: Computer Networking, Network Infrastructure, and IT Operations.
