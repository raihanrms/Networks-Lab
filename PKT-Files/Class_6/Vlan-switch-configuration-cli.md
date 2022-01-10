### Vlan Switch Configuration Cli commands
#### Go to
```text
Switch -> CLI
```
#### Commands
```text
Switch#show vlan brief
Switch(config)#vlan 2
Switch(config-vlan)#name accounts
Switch(config-vlan)#exit
Switch(config)#vlan 3
Switch(config-vlan)#name audit
Switch(config-vlan)#exit
Switch(config)#vlan 4
Switch(config-vlan)#name hr
Switch(config-vlan)#exit
Switch(config)#vlan 5
Switch(config-vlan)#name logistics
Switch(config-vlan)#exit
Switch(config)#exit
Switch#show vlan brief    
Switch#
Switch#enable
Switch#configure terminal 
Switch(config)#interface fastEthernet 0/2
Switch(config-if)#switchport mode access 
Switch(config-if)#switchport access vlan 2
Switch(config-if)#exit
Switch(config)#exit
Switch#enable
Switch#show vlan brief 
Switch#configure 
Switch(config)#interface fastEthernet 0/3
Switch(config-if)#switchport mode access 
Switch(config-if)#switchport access vlan 2
Switch(config-if)#exit
Switch(config)#exit
Switch#enable 
Switch(config)#interface fastEthernet 0/4
Switch(config-if)#switchport mode access 
Switch(config-if)#switchport access vlan 2
Switch(config-if)#exit
Switch(config)#exit
Switch#enable
Switch#configure 
Switch(config)#interface fastEthernet 0/6
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 3
Switch(config-if)#exit
Switch(config)#interface fastEthernet 0/7
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 3
Switch(config-if)#exit
Switch(config)#interface fastEthernet 0/8
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 3
Switch(config-if)#exit
Switch(config)#interface fastEthernet 0/10
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 5
Switch(config-if)#exit
Switch(config)#interface fastEthernet 0/11
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 5
Switch(config-if)#exi
Switch(config-if)#exit 
Switch(config)#interface fastEthernet 0/12
Switch(config-if)#switchport mode access
Switch(config-if)#switchport access vlan 5
Switch(config-if)#exit
Switch(config)#
Switch(config)#interface FastEthernet0/2
Switch(config-if)#
Switch(config-if)#exit
Switch(config)#interface FastEthernet0/10
Switch(config-if)#
Switch(config-if)#exit
Switch(config)#interface FastEthernet0/14
Switch(config-if)#
Switch(config-if)#
Switch(config-if)#switchport access vlan 4
Switch(config-if)#
Switch(config-if)#exit
Switch(config)#interface FastEthernet0/15
Switch(config-if)#
Switch(config-if)#exit
Switch(config)#interface FastEthernet0/15
Switch(config-if)#
Switch(config-if)#
Switch(config-if)#switchport access vlan 4
Switch(config-if)#
Switch(config-if)#exit
Switch(config)#interface FastEthernet0/16
Switch(config-if)#
Switch(config-if)#
Switch(config-if)#switchport access vlan 4
Switch(config-if)#exit
Switch(config)#exit
Switch#copy running-config startup-config 
Destination filename [startup-config]? 
Building configuration...
[OK]
Switch#
```
