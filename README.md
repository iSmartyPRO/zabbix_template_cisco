# Zabbix Template for monitoring CISCO

This template is tested for **CISCO 2960, CISCO C800**

**Name** Template Net Cisco IOS SNMPv2

**GROUP** Templates/Network Devices

**Additional Description**
Template Cisco IOS Software releases 12.2(3.5) or later version: 0.15
Known Issues:
description : no if(in|out)(Errors|Discards) are available for vlan ifType
version : IOS for example: 	12.1(22)EA11, 15.4(3)M2
device : C2911, C7600

## ITEMS
* Template Module Generic SNMPv2: Device contact details	
* Template Module Generic SNMPv2: Device description	
* Template Module Generic SNMPv2: Device location	
* Template Module Generic SNMPv2: Device name	
* Template Module Generic SNMPv2: Device uptime	
* Template Module Cisco Inventory SNMPv2: Hardware model name	
* Template Module Cisco Inventory SNMPv2: Hardware serial number	
* Template Module ICMP Ping: ICMP loss	
* Template Module ICMP Ping: ICMP ping	
* Template Module ICMP Ping: ICMP response time	
* Template Module Cisco Inventory SNMPv2: Operating system	
* Template Module Generic SNMPv2: SNMP availability	
* Template Module Generic SNMPv2: SNMP traps (fallback)	
* Template Module Generic SNMPv2: System object ID

## APPLICATIONS
* Template Module Cisco CISCO-PROCESS-MIB SNMPv2: CPU		
* Template Module Cisco CISCO-ENVMON-MIB SNMPv2: Fans		
* Template Module Generic SNMPv2: General	
* Template Module Cisco Inventory SNMPv2: Inventory	
* Template Module Cisco CISCO-MEMORY-POOL-MIB SNMPv2: Memory	
* Template Module EtherLike-MIB SNMPv2, Template Module Interfaces SNMPv2: Network interfaces	
* Template Module Cisco CISCO-ENVMON-MIB SNMPv2: Power Supply	
* Template Module Cisco CISCO-ENVMON-MIB SNMPv2: Power supply	
* Template Module ICMP Ping: Status	
* Template Module Cisco CISCO-ENVMON-MIB SNMPv2: Temperature	


## TRIGGERS
***
Template Module Generic SNMPv2: {HOST.NAME} has been restarted
Depends on:
Template Net Cisco IOS SNMPv2: No SNMP data collection
***
Template Module ICMP Ping: Unavailable by ICMP ping	
***
Template Module Generic SNMPv2: No SNMP data collection
Depends on:
Template Net Cisco IOS SNMPv2: Unavailable by ICMP ping
***
Template Module ICMP Ping: High ICMP ping response time
Depends on:
Template Net Cisco IOS SNMPv2: High ICMP ping loss
Template Net Cisco IOS SNMPv2: Unavailable by ICMP ping
***
Template Module ICMP Ping: High ICMP ping loss
Depends on:
Template Net Cisco IOS SNMPv2: Unavailable by ICMP ping
***
Template Module Cisco Inventory SNMPv2: Device has been replaced (new serial number received)	


## DISCOVERY
* Template Module Cisco CISCO-PROCESS-MIB SNMPv2: CPU Discovery	
* Template Module Cisco Inventory SNMPv2: Entity Serial Numbers Discovery	
* Template Module EtherLike-MIB SNMPv2: EtherLike-MIB Discovery	
* Template Module Cisco CISCO-ENVMON-MIB SNMPv2: FAN Discovery	
* Template Module Cisco CISCO-MEMORY-POOL-MIB SNMPv2: Memory Discovery	
* Template Module Interfaces SNMPv2: Network Interfaces Discovery	
* Template Module Cisco CISCO-ENVMON-MIB SNMPv2: PSU Discovery	
* Template Module Cisco CISCO-ENVMON-MIB SNMPv2: Temperature Discovery	
