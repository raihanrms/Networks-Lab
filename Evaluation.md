## Written notes for network mid evaluation 

## Subnetting
### Steps:
- Add CFE connections to a router
- Keep one for outside network
- Make networks as required with Router-PT, Switch-PT, Connecttion: Copper-Straight-Through, and PC-PT
- Make the wire connection serial wise from router > switch > PC
- Divide the ip address (192.168.100.0/24) into the number of networks (8 Networks used here) 
- For example
   - *Switch 1 >*
     _Network: 192.168.100.0_
     _Start: 192.168.100.1_
     _Last: 192.168.100.30_
     _Broadcast: 192.168.100.31_

   -  *Switch 2 >*
     _Network: 192.168.100.32_
     _Start: 192.168.100.33_
     _Last: 192.168.100.62_
     _Broadcast: 192.168.100.63_

- Connection in routers:
    - Router 0: (FE 0/0)
        - Address: _192.168.100.1, Subnet: 255.255.255.224, Port Status: ON_
        - PC 0 - IP Configuration
            - _Address: 192.168.100.30, Subnet: 255.255.255.224, Default Gateway: 192.168.100.1_

        - PC 1 - IP Configuration
            - _Address: 192.168.100.15, Subnet: 255.255.255.224, Default Gateway: 192.168.100.1_

    - Router 1: (FE 1/0)
        - Address: _192.168.100.33, Subnet: _255.255.255.224, Port Status: ON_
        - PC 2 - IP Configuration
            - _Address: 192.168.100.51, Subnet: 255.255.255.224, Default Gateway: 192.168.100.33_

        - PC 3 - IP Configuration
            - _Address: 192.168.100.62, Subnet: 255.255.255.224, Default Gateway: 192.168.100.33_

    - Continue ...

- Test out by sending packets

#### DHCP (Dynamic Host Configuration Protocol)
