### Vlan Switch Trunking Configuration Cli commands
#### Go to
```text
Switch -> CLI
```
#### Commands
```text
Switch>enable 
Switch#conf t
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#interface range fastEthernet 0/1-3
Switch(config-if-range)#switchport mode access 
Switch(config-if-range)#switchport access vlan 2
Switch(config-if-range)#do wr
Building configuration...
[OK]
Switch(config-if-range)#exit
Switch(config)#interface range fastEthernet 0/6-8
Switch(config-if-range)#switchport mode access 
Switch(config-if-range)#switchport access vlan 3
Switch(config-if-range)#do wr
Building configuration...
[OK]
Switch(config-if-range)#exit
Switch(config)#interface range fastEthernet 0/10-12
Switch(config-if-range)#switchport mode access 
Switch(config-if-range)#switchport access vlan 5
Switch(config-if-range)#do wr
Building configuration...
[OK]
Switch(config-if-range)#exit
Switch(config-if-range)#interface range fastEthernet 0/14-16
Switch(config-if-range)#switchport mode access 
Switch(config-if-range)#switchport access vlan 4
Switch(config-if-range)#do wr
Building configuration...
[OK]
Switch(config-if-range)#exit
Switch(config)#exit
Switch#
```

#### Configure switch for trunking
```text
Switch>enable 
Switch#conf t
Switch(config)#interface gigabitEthernet 0/1
Switch(config-if)#switchport mode trunk 
Switch(config-if)#do wr
Building configuration...
[OK]
Switch(config-if)#exit
Switch(config)#
```

#### Configure Router
```text
Router>enable 
Router#configure terminal 
Enter configuration commands, one per line.  End with CNTL/Z.
Router(config)#interface gigabitEthernet 0/1.2
Router(config-subif)#encapsulation dot1q 2
Router(config-subif)#ip address 192.168.10.1 255.255.255.0
Router(config-subif)#no shutdown 
Router(config-subif)#exit
Router(config)#interface gigabitEthernet 0/1.3
Router(config-subif)#encapsulation dot1q 3
Router(config-subif)#ip address 192.168.20.1 255.255.255.0
Router(config-subif)#no shutdown 
Router(config-subif)#exit
Router(config)#interface gigabitEthernet 0/1.4
Router(config-subif)#encapsulation dot1q 4
Router(config-subif)#ip address 192.168.30.1 255.255.255.0
Router(config-subif)#no shutdown 
Router(config-subif)#exit
Router(config)#interface gigabitEthernet 0/1.5
Router(config-subif)#encapsulation dot1q 5
Router(config-subif)#ip address 192.168.40.1 255.255.255.0
Router(config-subif)#no shutdown 
Router(config-subif)#exit
Router(config)#
Router#
```

#### Manually add the ip address and default gate way to each pc
```text
Accounts: Vlan 2
PC1:
	ip: 192.168.10.2
	subnet: 255.255.255.0
	def-gate: 192.168.10.1

	.
	.
	.

Logistics: Vlan 5
PC3:
	ip: 192.168.40.4
	subnet: 255.255.255.0
	def-gate: 192.168.40.1
```