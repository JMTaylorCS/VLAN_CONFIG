# VLAN_CONFIG
## Overview
Small business design and configuration of a network using cisco packet tracer. Separating office devices into their own logical networks using VLANs.

## Network Design
- 1 router
- 1 switch
- 3 PCs
- 1 Network printer\
\
see topology.png

## IP Addressing and VLANs
- VLAN 10 Admin: '192.168.10.0/24' default: 192.168.10.1
- VLAN 20 Ops: '192.168.20.0/24' default: 192.168.20.1
- Vlan 30 Guest: '192.168.30.0/24' default: 192.168.30.1
- Printer : static '192.168.10.10'

## Configuration
### Switch
- Created VLANs 10, 20 and 30
- Assigned end device switch ports to their VLANs
- Configured the router facing switch port as 802.1Q trunk

### Router
- Configured router subinterfaces for each VLAN
- Assigned a gateway address to each subinterface
- enabled inter VLAN routing
  
### DHCP
- Created separate DHCP pool for each VLAN
- Configured correct subnet and default gateway in each pool
  
### Access Control
- Created Extended ACLs to deny guest traffic on unauthorised subnets
- applied the ACL inbound on guest router subinterface
- Verified ACL
  
## Testing 
- verified each pc through pings both allowed traffic and blocked
- Verified ACL was in place and denied guest traffic
- Checked VLAN routing tables

## Skills Demonstrated
- VLAN configuration
- Access and trunk ports
- 802.1Q Tagging
- Router-on-a-stick
- IPv4 addressing and DHCP
- Inter VLAN routing
- ACLs
- Network verification and troubleshooting 
