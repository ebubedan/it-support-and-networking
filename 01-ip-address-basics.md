# IP Address Basics

- **IP address**: a number that identifies a device on a network.
- **IPv4** = **32 bits**, split into **4 octets** of **8 bits** each (octet = group of 8).
- Each octet ranges from **0 to 255**.

## Three ways to write the same address
| Format | Example |
|---|---|
| Binary | `11001000.11111100.00111111.11110111` |
| Decimal | `200.252.63.247` |
| Hexadecimal | `C8.FC.3F.F7` |

## Classes (old system)
| Class | First bits | Share of all addresses |
|---|---|---|
| A | 0 | 50% |
| B | 10 | 25% |
| C | 110 | 12.5% |
| D | 1110 | 6.25% |
| E | 1111 | 6.25% |

Classes A, B, C were the rigid way of splitting network and host parts. Subnetting replaced this with flexible splits.

## IP and location
An IP address has no built-in location. ISPs get blocks from regional registries (e.g. AFRINIC for Africa), and geolocation databases map blocks to places. This usually gives country/city/ISP, not a street address. VPNs, proxies and mobile networks can make it wrong. Private addresses (e.g. `192.168.1.10`) are not on the public internet at all.
