#### J-K8-Chip
emulator of J-K8 (CPU/MCU) 
### Specification:
J-K8 CPU (HARVARD ARCHITECTURE):
## Memory:
512 bytes program memory (FLASH)
256 bytes  of RAM

**Memory Map**




## Special registers:
#InProcess...

## Input:
8 key input
Personal Key Configuration

 KEY   | Hex code
-------|---------
 UP    |   0X00  
 DOWN  |   0X01  
 LEFT  |   0X02  
 RIGHT |   0X03  
 A     |   0X04  
 B     |   0X05  
 C     |   0X06  
 D     |   0X07  



## CPU:
4 mhz (0.00025 mili seconds) (each 4 pulses[ Frec/4= pulse ] increase PC reg)
*Working register               W
*Program Counter register       PC
*Stack Pointer register         SP

## OP CODES :
**Info:**
nnn or addr - A 12-bit value, the lowest 12 bits of the instruction
n or nibble - A 4-bit value, the lowest 4 bits of the instruction
x - A 4-bit value, the lower 4 bits of the high byte of the instruction
y - A 4-bit value, the upper 4 bits of the low byte of the instruction
kk or byte - An 8-bit value, the lowest 8 bits of the instruction
