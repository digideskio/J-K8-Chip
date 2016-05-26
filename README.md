# J-K8 Chip
emulator of J-K8 ( 8 bit CPU/MCU) 
# Specification:
## Memory:
* 512 bytes program memory (FLASH)
* 256 bytes  of RAM/VRAM shared 

**Memory Map**

 Special Registers  | General Propuse Registers| Video Buffer Registers
-------|---------|---------
0x00 to 0x07|    0x8 to 0x7D   | 0x7F to 0xFF
 (7 bytes)  |    (118 bytes)   | ( 128 bytes)
 
## Special registers:
Address| Description |Bit 7|Bit 6|Bit 5|Bit 4|Bit 3|Bit 3|Bit 2|Bit 0
-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
0x00   | NOTHING|*|*|*|*|*|*|*|*
0x01   | STATUS |x|x|x|x|x|Mode|Carry|Zero
0x02   | INPUT[1 pressed;0 clear] |Key 7|Key 6|Key 5|Key 4|Key 3|Key 2|Key 1|key 0
0x03   | NONE | | | | | | | |  
0x04   | NONE | | | | | | | |  
0x05   | NONE | | | | | | | |  
0x06   | NONE | | | | | | | |  
0x07  | NONE | | | | | | | |  
##Output
*Video*
* 64 x 64 @60Hz screen
* 8 bit **COLOR** or **ASCII** character (in console mode)


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



## CPU :
**4 mhz (0.00025 mili seconds);(each 4 pulses[ Frec/4= pulse ] increase PC reg)** </br>
*P1 = fetch instruction; P2 = decode instruction ; P3 = execute instruction </br>*
**8 bit CPU registers**
* Working register -> W (acumulator)
* Program Counter register->PC


## Instruction Set :

**Info:**
* kk   ->  8 bit Address 
* [kk] -> 8 bit constant  
*Example:* </br>
**MOV 0X05,0X04 // copy value from 0x04 to 0x05** </br>
**MOV 0X6,[52]  // copy the value '52 decimal/ or hex equivalent' to address 0x06** </br>


###Op codes(v1.0).

 hex     | bin     | mnemonic    |Description
---------|---------|---------|---------|
 ||| 
 ||| 
 ||| 
 ||| 
 ||| 
 ||| 
 ||| 
 ||| 
 ||| 
 |||
 |||
 ||| 
 ||| 
 ||| 

