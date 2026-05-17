# SwiftMart-LTD-Network-Design-
Design Project: SwiftMart LTD Network design.

SwiftMart LTD is a fictional retail company.

Case Study intro:
SwiftMart Ltd is a medium-scale retail and distribution company involved in the supply of packaged food items, household products, and electronic accessories across multiple locations in Nigeria. The organization currently operates a Head Office located in Lagos and a branch warehouse office located in Ibadan.

As the company expanded its operations, the existing network infrastructure became insufficient to support secure communication, centralized management, departmental segmentation, and efficient inter-office connectivity. The absence of proper network segmentation exposed the organization to security risks, excessive broadcast traffic, poor scalability, and inefficient resource management.


The company wants:
1. Secure Communication between both sites
2. Internet access
3. Department separation using VLANs
4. Basic routing and network security
_______________

As a network engineer, solving this is not about 'I can configure OSPF or VLAN', but looking at what the challenges are and highlighting ways to resolve them.

Problems to be solved:
Broadcast congestion
Poor security
Risk of data interception
Slow business applications
IP conflicts

The Company wants:
Segmentation 
and Security
I added:
Scalability 
Security by design 
High Availability 
High Performance and Efficiency 

To curb broadcast congestions, I created separate vlans for each department to reduce broadcast domain size.
I implemented security at layer 2 using port security, whereby ports shuts down on violation, and unused ports are disabled to prevent unauthorized access.

I eliminated the risk of data interception by implementing HQ-Branch traffic encryption using IpSec tunnel over WAN network with aes encryption and isakmp policy.

To resolve IP conflicts due to inefficient manual IP assignment, I implemented DHCP to automatically assign IP address to host devices, which is more scalable.
To achieve high Availability, I implemented HSRP for redundancy easy failover. I also achieved higher performance and throughput by implementing redundant Etherchannel links between Distribution and Core layers.

In other to achieve true department segmentation, I implemented ACLS to restrict unauthorized access to other departments while still allowing access to core services and the internet. With ACLS I upheld security at layer 3.

Additionals:
BGP on WAN
OSPF for dynamic routing
Inter-site VoIP
NAT at exit
DNS
VMS
EMAIL
