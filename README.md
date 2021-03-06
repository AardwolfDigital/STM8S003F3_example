# STM8S003F3 PCB Breakout and C examples
Breakout board and some lightweight C examples of the STM8S003F3 using the Small Device C Compiler (SDCC). Without the need for the STM8S/A Standard peripheral library.
Some examples are also compatable with the IAR compiler.

![Breakout Boards](https://user-images.githubusercontent.com/19818741/90937693-3b57d900-e3ff-11ea-88cc-298ae4a1f2fe.jpg)

Gerbers and design files for low cost breakout boards for the STM8S003F3 are available in the hardware folder.
The breakout boards are designed in EasyEDA and KiCAD are placed in the hardware folder. 
The EasyEDA gerbers and assembly files have been phyically tested with JLCPCB. KiCAD files have not been tested.

## Software Setup
To compile and run this SDCC will need to be installed.
On linux, this can be done with the `sudo apt update` and `sudo apt install sdcc`

## Flashing the STM8
The stm8flash utility is used to program the stm8 devices: https://github.com/vdudouyt/stm8flash 
Make sure you have an compatable ST-LINK programmer
This will need to be compiled. The directory for the executable was placed in:

>/home/*\<your username\>*/tools/stm8flash/

## Make Commands

Typing in the following commands in the development folder:
- `make blink` will compile the blink program to the *./bin/* folder.
- `make tim2` will compile the timer2 interrupt program to the *./bin/* folder.
- `make t2delay` will compile the timer2 delay program to the *./bin/* folder.
- `make burn` command will flash the device depending on the last build.
- `make clean` will clear the binary and the *./bin/* folder.

Depending on your programmer, the makefile may need to be edited.
