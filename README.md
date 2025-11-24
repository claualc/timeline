

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

