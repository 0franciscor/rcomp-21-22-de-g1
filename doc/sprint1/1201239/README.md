RCOMP 2021-2022 Project - Sprint 1 - Member 1201239 folder
===========================================

## These were the followed structured cabling standards:
- Minimum of 2 outlets per work area.
- Ratio of 2 outlets for every 10 square meters of area, with them being at less than 3 meters from the user's equipment.
- Each cable (whatever type) length should be less than 90 meters.
- The total area covered by a horizontal cross-connect should be less than 1000 m2.
- Straight line distance between the horizontal cross-connect and the outlet should be less than 80 meters.
- Cables connecting an intermediate cross-connect (IC) to a horizontal cross-connect (HC) are limited to 500 meters in length.
- The number of cables entering a telecommunications cabinet must always be less than 200.

### Important Remarks:

- So that the plants dimensions could be measured, the provided scale was used. Its real length of 5m
is equivalent to 2.7cm on an A4 printed sheet.


- Once the measurements were performed, the obtained measures 
were converted using the following formula:

![conversion_formula](resources/conv_formula.png)

- Each room and both floors are considered geometric rectangles. So, it's possible to obtain an area
by just multiplying a division's length by its width.

# Building 2 

## Ground Floor:

![floor0_plant](resources/Building2_Floor0.png)

> The floor itself is square, with a side of **19,07 m (10,3 cm)**, thus having an area of **363,67 m2**.

### Individual Rooms' Dimensions:

| Room  | Length (m) | Width (m) | Area (m2) | Number of outlets |
|-------|------------|-----------|-----------|-------------------|
| 2.0.1 | 2,96       | 3,51      | 10,39     | 0 (Storage Unit)  |
| 2.0.2 | 5,74       | 5,37      | 30,82     | 8                 |
| 2.0.3 | 9,91       | 8,52      | 84,43     | 18                |
| 2.0.4 | 8,52       | 3,33      | 28,37     | 6                 |
| 2.0.5 | 8,52       | 3,33      | 28,37     | 6                 |
| 2.0.6 | 8,52       | 3,33      | 28,37     | 6                 |

## Ground Floor with outlets:

![floor0_plant_outlets](resources/Building2_Floor0_Outlets.png)

### Justifications about the decisions made

*Thanks to the integrated underfloor raceway on the building, it is possible to route the needed cables to the several rooms.\
The mentioned cables include copper and fiber cabling.* 

> **Intermediate Cross-Connect**
>>  The intermediate cross-connect is responsible for receiving the optic fiber cable coming from the Main Cross-Connect located on Building 1.\
> It's located on room 2.0.1 and connected to the Horizontal Cross-Connect on the same floor and the floor above.

> **Horizontal Cross-Connect**
>> This floor contains a single HC, since its total area is inferior to 1000 m2 (based on the given standards).\
>  Being located on the same room as the IC (2.0.1), it allows for the needed cable to be a lesser amount than if mounted on other room.\
> It also allowed to copper connect to all the outlets on rooms 2.0.2 and 2.0.3

> **Consolidation Points**
>> There is only one consolidation point on this floor. It connects to the 2.0.4,5,6 rooms' 18 total outlets.

> **Outlets**
>> Having in consideration a real world outlet layout, the floor outlets were mostly placed on the rooms' walls.\
> Only in one room will the building owner be able to find outlets on the ground (which is on the biggest room).\
> The mapped placement was also defined respecting the rule which states that wherever a user may stand in a room, it should have an outlet located at a maximum of 3m, with a patch cord of 5m

### Important Note: The Outlet Order is defined clockwise

### Room 2.0.1

 - This room is responsible for housing the Building's IC and the floor's HC.
 - The Building's **IC** requires a Fiber Patch Panel, since it is fiber connected to both HC's (Ground and First Floor). Although the number of unused outlets is big, it allows for future expansibility. This Fiber Patch Panel is 1U sized.
 - The **HC** connects to a total of 26 Outlets, which requires a 48 Ports Copper Patch Panel, 2U sized. Since the CP's are also fiber connected, it is required for the HC to have a 1U sized fiber patch panel.
 - The total required space sits at 6U, however, a 50% increase in terms of capacity to futureproof the enclosure leads to a 9U sized enclosure.
 
### Room 2.0.2

| Outlet | CAT 7 needed cable length (m) |
|--------|-------------------------------|
| 1      | 4,44                          |
| 2      | 6,85                          |
| 3      | 9,81                          |
| 4      | 11,48                         |
| 5      | 13,15                         |
| 6      | 4,44                          |
| 7      | 6,67                          |
| 8      | 9,26                          |

### Room 2.0.3

| Outlet | CAT 7 needed cable length (m) |
|--------|-------------------------------|
| 1      | 10,74                         |
| 2      | 13,89                         |
| 3      | 17,04                         |
| 4      | 20,56                         |
| 5      | 22,96                         |
| 6      | 25,37                         |
| 7      | 28,51                         |
| 8      | 31,67                         |
| 9      | 34,63                         |
| 10     | 36,67                         |
| 11     | 14,26                         |
| 12     | 10,93                         |
| 13     | 15,74                         |
| 14     | 18,89                         |
| 15     | 22,22                         |
| 16     | 19,26                         |
| 17     | 22,22                         |
| 18     | 18,89                         |

### Room 2.0.4

| Outlet | CAT 7 needed cable length (m) |
|--------|-------------------------------|
| 1      | 12,96                         |
| 2      | 10,56                         |
| 3      | 8,15                          |
| 4      | 11,48                         |
| 5      | 13,70                         |
| 6      | 16,30                         |

### Room 2.0.5

 - This room is responsible for housing the Consolidation Point which makes the Outlets on rooms 2.0.4,5,6 possible.
 - The CP requires a 24 Port Cat7 Copper Patch Panel, which has a size of 1U.
 - Futureproofing the enclosure makes the total at 1.5*2U = 3U.

| Outlet | CAT 7 needed cable length (m) |
|--------|-------------------------------|
| 1      | 9,81                          |
| 2      | 7,22                          |
| 3      | 5                             |
| 4      | 1,67                          |
| 5      | 2,97                          |
| 6      | 6,48                          |

### Room 2.0.6

| Outlet | CAT 7 needed cable length (m) |
|--------|-------------------------------|
| 1      | 13,33                         |
| 2      | 10,93                         |
| 3      | 8,52                          |
| 4      | 5,37                          |
| 5      | 7,78                          |
| 6      | 10,37                         |

### Floor inventory:

| Room | Total CAT7A Cable (m) |
|------|-----------------------|
| 2    | 66,1                  |
| 3    | 384,45                |
| 4    | 73,15                 |
| 5    | 33,15                 |
| 6    | 56,3                  |

| Equipment      | Quantity |
|----------------|----------|
| Outlets        | 40       |
| Copper Cable   | 613,15m  |
| Fiber Cable    | 35,56m   |


## Floor Nº1:

![floor1_plant](resources/Building2_Floor1.png)

> Like the floor beneath, it has a side of **19,07 m (10,3 cm)**, thus having an area of **363,67 m2**.

### Individual Rooms' Dimensions:

| Room   | Length (m) | Width (m) | Area (m2) | Number of outlets                           |
|--------|------------|-----------|-----------|---------------------------------------------|
| 2.1.1  | 2,96       | 3,51      | 10,39     | 0 (Storage Unit)                            |
| 2.1.2  | 2,96       | 5,19      | 15,36     | 4                                           |
| 2.1.3  | 2,96       | 5,19      | 15,36     | 4                                           |
| 2.1.4  | 2,78       | 5,19      | 14,43     | 4                                           |
| 2.1.5  | 2,96       | 5,19      | 15,36     | 4                                           |
| 2.1.6  | 3,33       | 5,19      | 17,28     | 4                                           |
| 2.1.7  | 6,30       | 3,33      | 20,98     | 7 (+1 required because of the access point) |
| 2.1.8  | 6,30       | 3,33      | 20,98     | 6                                           |
| 2.1.9  | 2,96       | 5,19      | 15,36     | 4                                           |
| 2.1.10 | 2,96       | 5,19      | 15,36     | 4                                           |
| 2.1.11 | 2,96       | 5,19      | 15,36     | 4                                           |
| 2.1.12 | 3,52       | 5,19      | 18,27     | 4                                           |

## First Floor with outlets:

![floor1_plant_outlets](resources/Building2_Floor1_Outlets.png)

### Floor inventory:

| Equipment    | Quantity |
|--------------|----------|
| Outlets      | 49       |
| Copper Cable | -        |
| Fiber Cable  | -        |


===========================================

## Building Inventory:

- After performing the building planning, this is the total Inventory:

| Equipment    | Quantity |
|--------------|----------|
| Outlets      | 89       |
| Copper Cable | -        |
| Fiber Cable  | -        |