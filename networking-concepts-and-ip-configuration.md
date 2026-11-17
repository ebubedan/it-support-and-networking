# Networking Concepts and IP Configuration

## Learning summary

I have been studying foundational networking concepts, including network topology, IP addressing, network IDs and host IDs, and basic IP configuration.

## Concepts

### Network topology

Network topology describes how devices and connections are arranged in a network. Common examples include:

- **Star:** devices connect through a central switch or hub.
- **Bus:** devices share a common communication line.
- **Ring:** devices form a closed loop.
- **Mesh:** devices have multiple interconnections.

### IP address

An IP address is a logical address used to identify an interface on an IP network so that data can be delivered to the right destination.

### Network ID and host ID

In IPv4 addressing, the network portion identifies the network, while the host portion identifies an interface within that network. The subnet mask determines which bits belong to each portion.

### Basic Windows IP check

The `ipconfig` command displays IP configuration information on Windows.

```powershell
ipconfig
ipconfig /all
```

These commands can help inspect an adapter's IPv4 address, subnet mask, default gateway and other configuration details.

## Further learning

I plan to practise subnet masks, CIDR notation, private and public IPv4 addresses, DHCP, DNS and subnetting in a lab.

## Skills

`TCP/IP` `IPv4` `Network Topology` `Windows Networking`
