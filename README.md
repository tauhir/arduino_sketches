arduino_sketches
================

This code was forked from NickGammons' Arduino Sketches in order to revive bricked AVRs due to dodgy clock fuses. This was built specifally for the ATmega64 which has a different algorithm to get into High Voltage Parallel Programming to change fuses however it will work for any similar device (see the parallel programming section of the ATmega64 datasheet to see the algorithm).

Rather than using an uno and having RESET come from a circuit built from VCC, I've adapted the code to have a seperate reset pin.

Wiring
------

| Arduino Pin | Target device Pin |
|-------------|-------------------|
| A0          | RDY               |
| A1          | OE                |
| A2          | WR                |
| A3          | BS1               |
| A4          | XTAL1             |
| A5          | XA0               |
| 2           | XA1               |
| 3           | PAGEL             |
| 4           | BS2               |
| 5           | VCC               |
| 6           | Data Bit 0        |
| 7           | Data Bit 1        |
| 8           | Data Bit 2        |
| 9           | Data Bit 3        |
| 10          | Data Bit 4        |
| 11          | Data Bit 5        |
| 12          | Data Bit 6        |
| 13          | Data Bit 7        |
| 14          | RESET (to circuit)|

RESET Circuit:
