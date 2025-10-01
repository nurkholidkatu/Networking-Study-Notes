# Cisco IOS — Interfaces Overview

---

## Example: Cisco 3745 Boot Output

```
Cisco 3745 (R7000) processor (revision 2.0) with 249856K/12288K bytes of memory.
Processor board ID FTX0945W0MY
R7000 CPU at 350MHz, Implementation 39, Rev 2.1, 256KB L2, 512KB L3 Cache
5 FastEthernet interfaces
DRAM configuration is 64 bits wide with parity enabled.
151K bytes of NVRAM.

Press RETURN to get started!
```

---

## What is an Interface?

In Cisco IOS, an **interface** refers to a physical port on a device (router or switch). You configure different settings depending on whether the interface is on a router or a switch.

---

## Cisco 1841 Rear View (Key Items)

<img width="800" height="300" alt="image" src="https://github.com/user-attachments/assets/064eb7e9-1add-48bc-b02b-31b5d2b1f2c8" />


- **Slot 1** – Network card expansion slot for additional interface cards.
- **Kensington slot** – Physical security lock point.
- **FastEthernet 0/1** – Ethernet port + status LED.
- **Console port** – Direct CLI access using a console cable.
- **Slot 0** – Another expansion slot (numbering right-to-left).
- **CompactFlash slot** – IOS image source.
- **USB port** – File transfer with a USB drive.
- **FastEthernet 0/0** – Ethernet port + status LED.
- **AUX port** – Legacy modem for out-of-band management.
- **Power & switch** – On/Off and power input socket.

---

## Quick Commands

Run these from **Privileged EXEC** (prompt ends with `#`).

- `show ip interface brief` — list interfaces, IPs and status
- `configure terminal` — enter global config mode
- `interface FastEthernet0/0` — enter interface sub-mode
- `no shutdown` — enable an interface (routers only)

---

## Configure Example

```
Router(config)# interface f0/0
Router(config-if)# ip address 192.168.0.1 255.255.255.0
Router(config-if)# no shutdown
%LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0, changed state to up
```

---

> 💡 **Tip:** On switches, ports are usually *up* by default. On routers, you must enable interfaces with `no shutdown`.

---

## Example: `show ip interface brief`

```
Interface              IP-Address      OK? Method Status                Protocol
FastEthernet0/0        192.168.0.1     YES manual administratively down down
FastEthernet0/1        unassigned      YES unset  administratively down down
Vlan1                  unassigned      YES unset  administratively down down
```

### Column Guide

| Column     | Meaning                                                         |
|------------|-----------------------------------------------------------------|
| Interface  | Port type and slot/port numbers (e.g., FastEthernet0/0)         |
| IP-Address | Configured IP or *unassigned*                                   |
| OK?        | Is IP valid? (YES/NO)                                           |
| Method     | How IP was set (manual/DHCP)                                    |
| Status     | Administrative state (up / administratively down)               |
| Protocol   | Operational state of line protocol (up / down)                  |

---

## Summary

Interfaces are physical ports. Use `show ip interface brief` to check status, and `no shutdown` to enable router ports.
