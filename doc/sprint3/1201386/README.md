RCOMP 2021-2022 Project - Sprint 3 - Member 1201386 folder
===========================================


### Building 1

-------------------------------------------------------------------
#### OSPF (Open Shortest Path First)

- Static routes between buildings were eliminated, except for the default route connecting to the ISP 
(since without this route there would be no internet distribution across the campus).
  
  
- All areas of the different buildings are connected to area 0, corresponding to the backbone.
  
- R1_B1 router configuration
  - **Router(config)#** router ospf 1
  - **Router(config)#** network 172.16.200.0 0.0.0.127 area 0
  - **Router(config)#** network 172.16.200.128 0.0.0.127 area 1
  - **Router(config)#** network 172.16.201.0 0.0.0.255 area 1
  - **Router(config)#** network 172.16.202.0 0.0.0.127 area 1

- R0_B1 router configuration
  - **Router(config)#** router ospf 5
  - **Router(config)#** network 172.16.200.0 0.0.0.127 area 0
  
- Default route definition
  - **Router(config)#** ip route 0.0.0.0 0.0.0.0 15.203.47.93
  - **Router(config)#** router ospf 5
  - **Router(config-router)#** default-information originate

  

-------------------------------------------------------------------
#### HTTP Server

- A server was placed in the DMZ VLAN to take over the HTTP service.
- Added a building identifier to an HTML page.

![HTML.PNG](./webPage.jpg)

![HTML_2.PNG](./webPage2.jpg)
  
 

-------------------------------------------------------------------

#### DHCPv4 Service

- The router in each building must be configured to provide a DHCPv4 service to all local networks excluding 
  the DMZ networks and the backbone.

* Floor 0:
    - **Router(config)#** ip dhcp pool b1groundfloor
    - **Router(dhcp-config)#** network 172.16.202.0 255.255.255.192
    - **Router(dhcp-config)#** default-router 172.16.202.1
    - **Router(dhcp-config)#** dns-server 172.16.201.130
    - **Router(config)#** domain-name rcomp-21-22-de-g1

* Floor 1:
    - **Router(config)#** ip dhcp pool b1floorone
    - **Router(dhcp-config)#** network 172.16.200.128 255.255.255.128
    - **Router(dhcp-config)#** default-router 172.16.200.129
    - **Router(dhcp-config)#** dns-server 172.16.201.130
    - **Router(dhcp-config)#** domain-name rcomp-21-22-de-g1

* WiFi:
    - **Router(config)#** ip dhcp pool b1wifi
    - **Router(dhcp-config)#** network 172.16.201.0 255.255.255.128
    - **Router(dhcp-config)#** default-router 172.16.201.1
    - **Router(dhcp-config)#** dns-server 172.16.201.130
    - **Router(dhcp-config)#** domain-name rcomp-21-22-de-g1
    
* VoIP:
    - **Router(config)#** ip dhcp pool b1voip
    - **Router(dhcp-config)#** network 172.16.202.64 255.255.255.192
    - **Router(dhcp-config)#** default-router 172.16.202.65
    - **Router(dhcp-config)#** option 150 ip 172.16.202.65
    - **Router(dhcp-config)#** dns-server 172.16.201.130
    - **Router(dhcp-config)#** domain-name rcomp-21-22-de-g1
    

* Gateway addresses have been deleted from the pool:
  
    - **Router(config)#** ip dhcp excluded-address 172.16.202.1
    - **Router(config)#** ip dhcp excluded-address 172.16.200.129
    - **Router(config)#** ip dhcp excluded-address 172.16.201.1
    - **Router(config)#** ip dhcp excluded-address 172.16.202.65

-------------------------------------------------------------------

#### VoIP Service

- On the ports of the switches connected to the phones, the respective voice vlan was 
  activated, and the access vlan deactivated.
  
  
- Automatic phone registration and directory number assignment
  - **Router(config)#** telephony-service
  - **Router(config-telephony)#** auto-reg-ephone
  - **Router(config-telephony)#** ip source-address 172.16.202.65 port 2000
  - **Router(config-telephony)#** max-ephones 40
  - **Router(config-telephony)#** max-dn 40
  - **Router(config-telephony)#** auto assign 11 to 12
  - **Router(config)#** ephone-dn 11
  - **Router(config-ephone-dn)#** number 1000
  - **Router(config)#** ephone-dn 12
  - **Router(config-ephone-dn)#** number 1001
  
  
- Calls forwarding

  - dial-peer voice 2 voip
  - destination-pattern 2…
  - session target ipv4:172.16.200.2

  - dial-peer voice 3 voip
  - destination-pattern 3…
  - session target ipv4:172.16.200.3

  - dial-peer voice 4 voip
  - destination-pattern 4…
  - session target ipv4:172.16.200.4
  
  
- The image below shows mobile 1000 communicating with telephone 1001.

![VoIPService.jpg](./VoIPService.jpg)

-------------------------------------------------------------------

#### DNS



-------------------------------------------------------------------

#### NAT


-------------------------------------------------------------------

#### ACLS

-------------------------------------------------------------------


