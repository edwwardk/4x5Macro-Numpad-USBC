## 4x5Macro-Numpad-USBC
This fork of tobychui's 4x5Macro-Numpad modifies the original design to use usbc instead of microusb as well as using a through hole reinforced port for a stronger hold on the board. Additionally, it also moves the user led to the front of the board and adds a button for resetting the mcu. Pins are identical to the 4x5Macro-Numpad to allow for using the same firmwares.

## v1.0 Known Issues
- resistor/capacitor/led designators/value missing from silkscreen in gerbers
- switch indices missing from silkscreen in gerbers
- size is larger than 100x100mm which causes upcharge (at least from jlcpcb)

### Bill of materials
(LCSC manufacturer part numbers in brackets)
- 1x CH552G (CH552G)
- 1x USBC (GT-USB-7010ASV)
- 20x switches for 4x5 layout, 17x switches for numpad layout
- 2x 0.1u 0805 capacitors (0805B104J250CT)
- 2x 0805 LEDs (17-215SURC/S530-A3/4T and BL-HJC35A-AV-TRB)
- 8x 10k 0805 resistors (SCR0805F10K)
- 2x 5.1k 0805 resistors (CR0805J80512G)
- 2x smd momentary buttons (TS5216A 250gf 025)

### Fabrication instructions
- in the "4x5Macro-Numpad-USBC/fabrication" folder there is a zip file called fabrication.zip. these are the set of gerbers required to order from JLCPCB and should work as is.




### Build Instruction

1. Send the PCB to print (See /PCB)

2. Purchase all the required materials (See BOM list)

3. 3D print the base plate (See /3D Model)

4. Install the required Arduino library for CH552G and drivers

5. Visit [4-key Macropad | imuslab](https://tobychui.github.io/4xMacropad/) (4xMacropad only) or modify the sketch in /firmware folder

6. Flash the CH552G with the sketch

### Program Flashing Instructions

As all the keyboard designs share the same MCU and programming button design, this instruction should be suitable for all the macropads / numpad in this repo.

1. Hold and press the PROG button on the PCB

2. While the button has been held, insert the USB cable into the mini USB port

3. Release the button when the Arduino code has finished compiling and ready to upload (Timing is important)

4. Wait for the upload to complete

### License

Software: MIT License

Hardware: CC BY-NC-SA
