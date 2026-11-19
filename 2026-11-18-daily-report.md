# INTERNSHIP DAILY PROGRESS REPORT

**Date:** 2026-11-18

## Activities Carried Out

1. Studied the fundamentals of IPv4 addressing, including how a 32-bit address is divided into four 8-bit octets.
2. Practiced converting IP addresses between binary, decimal, and hexadecimal formats (for example, 192.168.1.10 = C0.A8.01.0A).
3. Learned the concept of subnet masks and how to identify the network portion and host portion of an address using the Network ID (NID) and Host ID (HID).
4. Studied IP address classes A to E, their default subnet masks, and how to identify a class from the first octet.
5. Studied reserved IPv4 and IPv6 address ranges, including private ranges, loopback (127.0.0.0/8), 0.0.0.0, and link-local (169.254.x.x) addresses.
6. Carried out a practical loopback test by running `ping 127.5.5.5` in Command Prompt and interpreting the result (4 packets sent, 4 received, 0% loss).
7. Documented all notes in a structured GitHub repository under the networking section for future reference.

## Knowledge and Skills Acquired

- Gained a clear understanding of how IPv4 addresses are structured and written in different number systems.
- Learned that network and broadcast addresses (HID all 0s and all 1s) cannot be assigned to devices, and how to calculate usable hosts using 2^n - 2.
- Learned to tell private from public addresses, and that a 169.254.x.x address indicates a DHCP failure.
- Improved my ability to troubleshoot basic connectivity by using loopback testing and reading ping results (replies, TTL, and packet loss).
- Understood how changing a subnet mask splits a network into smaller subnets, which is the foundation of subnetting.
- Improved my technical documentation skills by organizing notes and practice questions in a GitHub repository.

## Related Notes
See [networking/fundamentals](../networking/fundamentals/README.md) for the full study notes.
