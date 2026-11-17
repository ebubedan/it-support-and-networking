# Practice Questions

Try first, then check the answers at the bottom.

1. Convert `11000000.10101000.00000001.00001010` to decimal.
2. Convert `10100101` to hex.
3. Convert `01111110` to hex.
4. Convert `192.168.1.10` to hex.
5. What is the network address of `192.168.5.77` with mask `255.255.255.0`?
6. What is the network address of `10.20.30.40` with mask `255.255.0.0`?
7. Are `192.168.1.20` and `192.168.2.20` on the same network with `255.255.255.0`?
8. What is the broadcast address of `10.0.0.0` with mask `255.0.0.0`?
9. Why can't `192.168.1.0` or `192.168.1.255` be given to a device on a /24 network?
10. How many usable hosts does a /24 have, and why not 256?
11. What does `169.254.12.8` tell you?

## Answers
1. `192.168.1.10`
2. `A5`
3. `7E`
4. `C0.A8.01.0A`
5. `192.168.5.0`
6. `10.20.0.0`
7. No (`192.168.1.0` vs `192.168.2.0`)
8. `10.255.255.255`
9. They are the network address (HID all 0s) and broadcast address (HID all 1s)
10. 254, because 2^8 = 256 minus the network and broadcast addresses
11. DHCP failed and the device self-assigned an address (APIPA); no internet access
