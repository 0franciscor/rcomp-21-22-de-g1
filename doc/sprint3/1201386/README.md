RCOMP 2021-2022 Project - Sprint 3 - Member 1201386 folder
===========================================


### Building 1

-------------------------------------------------------------------
#### OSPF (Open Shortest Path First)


  - **Router(config)#** router ospf 1
  - **Router(config)#** network 172.16.200.0 0.0.0.127 area 0
  - **Router(config)#** network 172.16.200.128 0.0.0.127 area 1
  - **Router(config)#** network 172.16.201.0 0.0.0.127 area 1
  - **Router(config)#** network 172.16.201.128 0.0.0.127 area 1
  - **Router(config)#** network 172.16.202.0  area 1
  - **Router(config)#** network 172.16.202.64  area 1
  
-------------------------------------------------------------------
#### HTTP Server

  
 

-------------------------------------------------------------------

#### DHCPv4 Service

* Floor 0:
    - **Router(config)#** ip dhcp pool b1groundfloor
    - **Router(config)#** network 172.16.202.0 255.255.255.192
    - **Router(config)#** default-router 172.16.202.1
    - **Router(config)#** dns-server 
    - **Router(config)#** domain-name rcomp-21-22-de-g1

* Floor 1:
    - **Router(config)#** ip dhcp pool b1floorone
    - **Router(config)#** network 172.16.200.128 255.255.255.128
    - **Router(config)#** default-router 172.16.200.129
    - **Router(config)#** dns-server
    - **Router(config)#** domain-name rcomp-21-22-de-g1

* WiFi:
    - **Router(config)#** ip dhcp pool b1wifi
    - **Router(config)#** network 172.16.201.0 255.255.255.128
    - **Router(config)#** default-router 172.16.201.1
    - **Router(config)#** dns-server
    - **Router(config)#** domain-name rcomp-21-22-de-g1
    
* VoIP:
    - **Router(config)#** ip dhcp pool b1voip
    - **Router(config)#** network 172.16.202.64 255.255.255.192
    - **Router(config)#** default-router 172.16.202.65
    - **Router(config)#** option 150 ip 172.16.202.65
    - **Router(config)#** dns-server 
    - **Router(config)#** domain-name rcomp-21-22-de-g1
    

* Gateway addresses have been deleted from the pool:
  
    - **Router(config)#** ip dhcp excluded-address 172.16.202.1
    - **Router(config)#** ip dhcp excluded-address 172.16.200.129
    - **Router(config)#** ip dhcp excluded-address 172.16.201.1
    - **Router(config)#** ip dhcp excluded-address 172.16.202.65

-------------------------------------------------------------------

#### VoIP Service


-------------------------------------------------------------------

#### DNS



-------------------------------------------------------------------

#### NAT


-------------------------------------------------------------------

#### ACLS

-------------------------------------------------------------------


