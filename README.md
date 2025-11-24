

## Ethernet 
![headers](./eth_frame.png)

```
PREAMBLE: 7 bits
SFD: Start Frame Delimiter 1
------------------------- not considered
MAC DEST: 6 
MAC SRC: 6
TYPE: 2
*VLAN_TAG 2x2
PAYLOAD
FCS: Frame check Sum 4
```
- Multiple Vlans: 802.1q with VLAN tagging
    - headers: 18 bytes
    - payload: 42 to 1500 bytes
    - MIN: 64 bytes and 1518 max
- Eth: 802.3
    - headers: 22 bytes
    - payload: 42 to 1500 bytes
    - MIN: 64 bytes and 1522 max

## ARP

- <u>Gratuitous ARP</u>: to update caches without an ARP REQUEST. E/g change of router ip 
- <u>Prove ARP</u>: SRC.IP empty so it doesn't update the caches
- <u>Proxy ARP</u>: NAT


show arp -> L3 devices with ARP cache
   - includes local interfaces
   - swL3 Vs router : NAT & tunneling
sh mac-address-table -> L2 devices with CAM MAc-IP map
   - local interfaces do not have IP
clear arp cache -> in L3 (?)

## VLAN

-  Broadcast domain (vlan) != collision domain (link)
- L3 devices might not support vlan


## Ath

- secret Vs password: 
    - secret is encrypted
    - enable secret first option, then fallback to password if present
- enable Vs vty:
    - vty ssh/telnet enable for exec mode


## Startup config

- Management setup Vs normal setup: the managment is for the network adm.
## OBS
- Config L3 switch 


## Configs

Router:
 - Set up ips on each interface (already up)
Switch
 - Configure Vlan1 (basic)
    - No need to configure all the interfaces (?)