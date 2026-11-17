# NID and HID

- **NID** (Network ID): the network part of the address
- **HID** (Host ID): the device part of the address

## Two HID values are never given to a device
- **HID all 0s** = network address (name of the network)
- **HID all 1s** = broadcast address (reaches every device on the network)

Example `192.168.1.x` with `255.255.255.0`:
```
192.168.1.0    HID all 0s  network address   (not assignable)
192.168.1.255  HID all 1s  broadcast address (not assignable)
192.168.1.1 to 192.168.1.254                 usable
```
That is the "minus 2" in: usable hosts = 2^n - 2.

## Class A network IDs
First octet starts with a 0 bit, so it ranges `00000000` (0) to `01111111` (127).
- 0 is reserved ("this network")
- 127 is reserved (loopback)
- Usable Class A network IDs: **1 to 126** (2^7 - 2 = 126)
- Hosts per Class A network: 2^24 - 2 = 16,777,214
