#### J-K8 Chip
emulator of J-K8 (CPU/MCU) 
### Specification:
J-K8 CPU (HARVARD ARCHITECTURE):
## Memory:
*512 bytes program memory (FLASH)
*256 bytes  of RAM

**Memory Map**

 Special Registers  | General Propuse Registers| Video Buffer Registers
-------|---------|---------
0x00 to 0x02|    0x3 to 0x7D   | 0x7F to 0xFF
 (3 bytes)  |    (122 bytes)   | ( 128 bytes)
 
## Special registers:
InProcess...

##Output
*Video*
* 64 x 64 screen
* 8 bit color or *ASCII* character(in console mode)


## Input:
**8 key input**
* Personal Key Configuration

 KEY   | Hex code|   bit map
-------|---------|---------
 NULL  |   0X00  |   00000000
 UP    |   0X01  |   00000001
 DOWN  |   0X02  |   00000010
 LEFT  |   0X04  |   00000100
 RIGHT |   0X08  |   00001000
 A     |   0X10  |   00010000
 B     |   0X20  |   00100000
 C     |   0X40  |   01000000
 D     |   0X80  |   10000000



## CPU:
* 4 mhz (0.00025 mili seconds) (each 4 pulses[ Frec/4= pulse ] increase PC reg)
* #CPU registers:
* Working register               W  (acumulator)
* Program Counter register       PC
* Stack Pointer register         SP

## OP CODES :
**Info:**
* nnn or addr - A 12-bit value, the lowest 12 bits of the instruction
* n or nibble - A 4-bit value, the lowest 4 bits of the instruction
* x - A 4-bit value, the lower 4 bits of the high byte of the instruction
* y - A 4-bit value, the upper 4 bits of the low byte of the instruction
* kk or byte - An 8-bit value, the lowest 8 bits of the instruction
