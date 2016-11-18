# J-K8 Chip
emulator of J-K8 ( 8 bit CPU/MCU) (TEORIC MODEL)
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
0x00   | RESET VECTOR|*|*|*|*|*|*|*|*
0x01   | STATUS |x|x|x|x|Mode|Digit Carry|Carry|Zero
0x02   | INPUT  |Key 7|Key 6|Key 5|Key 4|Key 3|Key 2|Key 1|key 0
0x03   | PROGRAM COUNTER | | | | | | | |  
0x04   | STACK POINTER | | | | | | | |  
0x05   | W(WORKING REG OR ACUMULATOR) | | | | | | | |  
0x06   | NONE | | | | | | | |  
0x07   | NONE | | | | | | | |  
##Output
*Video*
* 64 x 64 @60Hz screen
* 8 bit **COLOR** or **ASCII** character (mode 1 = color , mode 0 = ascci, only for PC emualtor)


## Input:
**8 key input**
* Personal Key Configuration,also can be keyboard scheme with 256 keys :)

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
**Frequency**
*CPU FREC = 24mhz* </br>
*CPU FREC IN SECONDS 1/CPUFREC=0.04155 Mili seconds= 1 MACHINE CYCLE, increments PC by 2 each machine cycle* </br>
*Each execution block needs 0.01385 ms ( CPU_FREC_IN_SECONDS/3)* </br>
*P1 = fetch instruction; P2 = decode instruction ; P3 = execute instruction </br>*
### CPU REGS:
**Stack Pointer,stack frame and program counter**
*16 addresses(16 bit) stack depth(allocated in the last position of the general propouse regs-0X7D)*</br>
*16(2 bytes) bit porgram counter lenght *</br>
*16 bit program counter*</br>

it might we have too large values for the addressing, but is a theorical model.

## Instruction Set :
*Compiler goes here lol*</br>
**Info:**
* **kk**   =  8 bit Address 
* **[kk]**  = 8 bit constant  
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

