RCOMP 2021-2022 Project - Sprint 3 - Member 1201386 folder
===========================================


### Building 1

-------------------------------------------------------------------
#### OSPF (Open Shortest Path First)

- Static routes between buildings were eliminated, except for the default route connecting to the ISP 
(since without this route there would be no internet distribution across the campus).
  
  
- All areas of the different buildings are connected to area 0, corresponding to the backbone.

  - **Router(config)#** router ospf 1
  - **Router(config)#** network 172.16.200.0 0.0.0.127 area 0
  - **Router(config)#** network 172.16.200.128 0.0.0.127 area 1
  - **Router(config)#** network 172.16.201.0 0.0.0.255 area 1
  - **Router(config)#** network 172.16.202.0 0.0.0.127 area 1
  
Falta fazer: inserir no protocolo de roteamento OSPF a rota padrão,
apontando para o roteador ISP (origem da informação padrão).

-------------------------------------------------------------------
#### HTTP Server

  
 

-------------------------------------------------------------------

#### DHCPv4 Service

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


-------------------------------------------------------------------

#### DNS



-------------------------------------------------------------------

#### NAT


-------------------------------------------------------------------

#### ACLS

-------------------------------------------------------------------


