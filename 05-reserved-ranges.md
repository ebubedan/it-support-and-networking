# Reserved IPv4 and IPv6 Ranges

## IPv4
| Range | Purpose |
|---|---|
| `0.0.0.0/8` | "This network" / no address yet |
| `10.0.0.0/8` | Private |
| `172.16.0.0/12` | Private (172.16 to 172.31) |
| `192.168.0.0/16` | Private |
| `127.0.0.0/8` | Loopback |
| `169.254.0.0/16` | Link-local (APIPA, self-assigned when DHCP fails) |
| `100.64.0.0/10` | Carrier-grade NAT |
| `224.0.0.0/4` | Multicast (Class D) |
| `240.0.0.0/4` | Experimental (Class E) |
| `255.255.255.255` | Limited broadcast |
| `192.0.2.0/24` + 2 similar blocks | Documentation |

## Loopback (127.x.x.x)
Traffic never leaves the device. Used for loopback testing (`ping 127.0.0.1`), self connectivity (localhost) and interprocess communication (programs on the same machine talking to each other). Host part can be anything.

`01111111` = 127 (a 0 followed by seven 1s).

## 0.0.0.0 vs 169.254.x.x
| | 0.0.0.0 | 169.254.x.x |
|---|---|---|
| Meaning | No address yet | Self-assigned address |
| Can communicate? | No | Only on the local link |
| Appears when | Starting up or disconnected | DHCP failed |

0.0.0.0 also means the default route (`0.0.0.0/0`): "send everything else to the gateway".

## Private vs public, DHCP vs static
- `10.0.0.1` is private. That says nothing about how it was assigned.
- DHCP = automatic assignment by a server (usually the router). Static = typed manually.
- `.1` is often the router/gateway, which usually has a static address.
- Windows check: `ipconfig /all`, look at "DHCP Enabled".

## Fixing 169.254.x.x
1. Restart the router and reconnect
2. `ipconfig /release` then `ipconfig /renew`
3. Check cable / Wi-Fi

## IPv6 (128 bits, hex)
| Range | Purpose |
|---|---|
| `::/128` | Unspecified (like 0.0.0.0) |
| `::1/128` | Loopback (like 127.0.0.1) |
| `fe80::/10` | Link-local |
| `fc00::/7` | Unique local (private-like) |
| `ff00::/8` | Multicast |
| `2000::/3` | Global unicast (public) |
| `2001:db8::/32` | Documentation |

Differences: IPv6 has no broadcast (uses multicast), loopback is a single address, and every device has an `fe80::` address automatically.
