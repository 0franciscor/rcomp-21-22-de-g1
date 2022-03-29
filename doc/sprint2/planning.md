RCOMP 2021-2022 Project - Sprint 2 planning
===========================================
### Sprint master: 1201386 ###

# 1. Sprint's backlog #
| Task | Task Description                                                                                                                                                                                                 |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|T.2.1 | Development of a layer two and layer three Packet Tracer simulation for building one, encompassing the campus backbone. Integration of every member's Packet Tracer simulations into a single simulation.        |
|T.2.2 | Development of a layer two and layer three Packet Tracer simulation for building two, encompassing the campus backbone.                                                                                          |
|T.2.3 | Development of a layer two and layer three Packet Tracer simulation for building three, encompassing the campus backbone.                                                                                        |
|T.2.4 | Development of a layer two and layer three Packet Tracer simulation for building four, encompassing the campus backbone.                                                                                         |


# 2. Technical decisions and coordination #
* **Packet Tracer Version:** V 8.1.1

#### Devices naming
(ver melhor a nomenclatura atribuída)
* **Routers:** Router Number-Building Number (Example: Router3-B3), where the mc router is Router 0 
* **Switches:** Switch Number-Cross Connect Type-Building Number (Example: Switch0-CP-B1)
* **PCs or Laptops:** PC|Laptop Number-Building Number (Example: PC1-B1)
* **Wireless Access Points:** WAP Number-Building Number-Floor Number (Example: WAP1-B1-F1)
* **IP-phones:** IPphone number-Building Number (Example: ipPhone1-B2-2.1.4)

#### VLAN database
* **Range of VLAN IDs used:** 240 – 270

Campus range: 240 - 270

| Building    | Vlan Id Range |
| ----------- | -----------   |
| 1 + Backbone|  240 - 245    |
| 2           |  246 - 250	  |
| 3           |  251 - 255	  |
| 4           |  256 - 260	  |


####   VTP Domain
* **VTP Domain:** rc22deg1

#### IPv4 network

| Building    | Nodes  |IPv4 Networks    | 
|-------------|--------|-----------------|
|1 + Backbone | 520    |172.16.200.0/22  |
|2            | 219    |172.16.204.0/24  |
|3            | 188    |172.16.205.0/24  |
|4            | 175    |172.16.206.0/24  |


# 3. Subtasks assignment #
* 1200720 - Development of a layer two and layer three Packet Tracer simulation for building three, encompassing the campus backbone.
* 1201239 - Development of a layer two and layer three Packet Tracer simulation for building two, encompassing the campus backbone.
* 1201382 - Development of a layer two and layer three Packet Tracer simulation for building four, encompassing the campus backbone.
* 1201386 - Development of a layer two and layer three Packet Tracer simulation for building one, encompassing the campus backbone. Integration of every member's Packet Tracer simulations into a single simulation.
  

