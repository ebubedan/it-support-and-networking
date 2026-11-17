# Binary, Decimal and Hex

## Binary to decimal
Place values for 8 bits:

```
128  64  32  16   8   4   2   1
```
A 1 means add the value, a 0 means skip it.

`11001000` = 128 + 64 + 8 = **200**
`10101000` = 128 + 32 + 8 = **168**

Tip: write the place values above the bits and tick each 1 before adding.

## Hexadecimal
Digits: 0-9, then A=10, B=11, C=12, D=13, E=14, F=15.
One hex digit = 4 bits (a nibble), so one octet = **2 hex digits**.

Nibble place values: `8 4 2 1`

Example: `11001000`
- `1100` = 12 = C
- `1000` = 8 = 8
- Result: **C8**

Check: C8 = (12 x 16) + 8 = 200

## Worked example
`192.168.1.10`
| Octet | Binary | Hex |
|---|---|---|
| 192 | 11000000 | C0 |
| 168 | 10101000 | A8 |
| 1 | 00000001 | 01 |
| 10 | 00001010 | 0A |

Result: `C0.A8.01.0A` (keep leading zeros, always 2 digits per octet).
