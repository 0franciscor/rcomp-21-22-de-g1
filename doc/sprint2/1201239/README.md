RCOMP 2021-2022 Project - Sprint 1 - Member 2222222 folder
===========================================

# Building 2

### VLAN Database and IPv4 Network

![network_diagram](resources/network_diagram.png)

## VLAN Database and IPv4 Network Table ##

|                | VLAN ID | VLAN Name     | TOTAL NODES | IP                | FIRST IP          | LAST IP           | BROADCAST         |
|----------------|---------|---------------|-------------|-------------------|-------------------|-------------------|-------------------|
|Wi-Fi           | 248     | b2wifi        | 120         | 172.16.204.0/25   | 172.16.204.1/25   | 172.16.204.126/25 | 172.16.204.127/25 |
|First Floor     | 247     | b2floorone    | 50          | 172.16.204.128/25 | 172.16.204.129/25 | 172.16.204.190/25 | 172.16.204.191/2  |
|Ground Floor    | 246     | b2groundfloor | 25          | 172.16.204.192/25 | 172.16.204.193/25 | 172.16.204.224/25 | 172.16.204.223/2  |
|DMZ             | 249     | b2dmz         | 12          | 172.16.204.224/25 | 172.16.204.225/25 | 172.16.204.238/25 | 172.16.204.239/25 |
|VoIP            | 250     | b2voip        | 12          | 172.16.204.240/25 | 172.16.204.241/25 | 172.16.205.0/25   | 172.16.205.1/25   |

> According to the presented diagram, there are still 37 nodes which have available unused IP's, allowing for future expansion.

### Routing Tables ##