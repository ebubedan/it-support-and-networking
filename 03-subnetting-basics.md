# Subnetting Basics

Subnetting = splitting one network into smaller networks. It works with IPv4 and IPv6 (it is not "IPv6").

## Analogy
- Whole complex = network
- Building = subnet
- Apartment = device

An address has a **network part** (which building) and a **host part** (which apartment). The **subnet mask** shows where the split is.

## Subnet mask
`255.255.255.0` in binary = `11111111.11111111.11111111.00000000`
- 1s = network bits, 0s = host bits
- Written in **CIDR** shorthand as `/24` (24 network bits)

Note: it is **255**, the max value of an octet (`11111111`).

## Finding the network address (bitwise AND)
```
IP:    11000000.10101000.00000001.00001010  (192.168.1.10)
Mask:  11111111.11111111.11111111.00000000  (255.255.255.0)
AND:   11000000.10101000.00000001.00000000  (192.168.1.0)
```
Shortcut for masks made of 255s and 0s: where the mask is 255, copy the address number; where it is 0, write 0.

`192.168.5.77` with `255.255.255.0` -> network `192.168.5.0`

## Same network?
Devices with the same network address talk directly. Different networks need a router.
- `192.168.5.77` and `192.168.5.90` -> same network
- `192.168.5.77` and `192.168.6.10` -> different networks

## Why subnet?
- Split a big network (staff, guests, cameras)
- Use addresses efficiently
- Better security and less traffic

## Hosts per network
Host bits = 32 - prefix length. Usable hosts = 2^(host bits) - 2.
| Mask | CIDR | Usable hosts |
|---|---|---|
| 255.0.0.0 | /8 | 16,777,214 |
| 255.255.0.0 | /16 | 65,534 |
| 255.255.255.0 | /24 | 254 |
