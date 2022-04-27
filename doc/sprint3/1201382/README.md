RCOMP 2021-2022 Project - Sprint 3 - Member 1201382 folder
===========================================


### Building 4

-------------------------------------------------------------------
#### OSPF (Open Shortest Path First)

-Static routes between buildings were eliminated, except for the default route connecting to the ISP
  (since without this route there would be no internet distribution across the campus).


- R1_B4 router configuration
    - **Router(config)#** router ospf 4
    - **Router(config)#** network 172.16.200.0 0.0.0.127 area 0
    - **Router(config)#** network 172.16.206.0 0.0.0.255 area 4
    

-------------------------------------------------------------------
#### HTTP Server

- A server was placed in the DMZ VLAN to take over the HTTP service.
- Added a building identifier to an HTML page.

![HTML.PNG](resources/webpage1.0.png)

![HTML.PNG](resources/webpage2.0.png)

-------------------------------------------------------------------

#### DHCPv4 Service

- The router in each building must be configured to provide a DHCPv4 service to all local networks excluding
  the DMZ networks and the backbone.

* Floor 0:
  - **Router(config)#** ip dhcp pool b4groundfloor
  - **Router(dhcp-config)#** network 172.16.206.192 255.255.255.224
  - **Router(dhcp-config)#** default-router 172.16.206.193
  - **Router(dhcp-config)#** dns-server 172.16.206.226
  - **Router(config)#** domain-name rcomp-21-22-de-g1

*Floor 1:
  - **Router(config)#** ip dhcp pool b4floorone
  - **Router(dhcp-config)#** network 172.16.206.128 255.255.255.192
  - **Router(dhcp-config)#** default-router 172.16.200.129
  - **Router(dhcp-config)#** dns-server 172.16.206.226
  - **Router(dhcp-config)#** domain-name rcomp-21-22-de-g1
  
* WiFi:
  - **Router(config)#** ip dhcp pool b4wifi
  - **Router(dhcp-config)#** network 172.16.206.0 255.255.255.128
  - **Router(dhcp-config)#** default-router 172.16.206.1
  - **Router(dhcp-config)#** dns-server 172.16.206.226
  - **Router(dhcp-config)#** domain-name rcomp-21-22-de-g1

*VoIP:
  - **Router(config)#** ip dhcp pool b4voip
  - **Router(dhcp-config)#** network 172.16.206.240 255.255.255.240
  - **Router(dhcp-config)#** default-router 172.16.206.241
  - **Router(dhcp-config)#** option 150 ip 172.16.206.241
  - **Router(dhcp-config)#** dns-server 172.16.206.226 
  - **Router(dhcp-config)#** domain-name rcomp-21-22-de-g1


-------------------------------------------------------------------

#### VoIP Service

Building 4 prefix: 4...


-------------------------------------------------------------------

#### DNS


-------------------------------------------------------------------

#### NAT

-------------------------------------------------------------------

#### ACLS

-------------------------------------------------------------------
