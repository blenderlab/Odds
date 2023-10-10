![Sebsongs Modular Euclidean](https://modular.sebsongs.com/wp-content/uploads/2022/04/Odds_cropped-46x300.png)

# Odds
Alternative Firmware for the Sebsongs Modular **Odds** eurorack module sold on [Thonk](https://www.thonk.co.uk/shop/sebsongs-odds/).

## Background
This is fork of the original Sebsongs Modular firmware.

## V1.4 - Second TuringMachine Iteration
- Bugfix/Improve : initial Loop is still in EEPROM, and sometimes (according to the % knob) a new note is generated (but not stored in the EEPROM). It gives a little humanity to the sequence.


## V1.3 - First TuringMachine Iteration
- Loop button still loops, but slightly modify the notes according to the Probability pot.

## Prerequisites for uploading firmware to an Arduino Nano board
- Install [Arduino IDE 1.8.19](https://www.arduino.cc/en/software). It should work fine with the latest version 2.XX too, but has not been thorougly tested yet.
- For the Adafruit Pro Trinket 5V, a support package must be installed. Follow the instructions over at [Adafruits website](https://learn.adafruit.com/adafruit-arduino-ide-setup/arduino-1-dot-6-x-ide#add-the-adafruit-board-support-package-2103901).
- Connect the Adafruit Pro Trinket 5V board to an available USB port on your computer with a USB to USB micro cable.
- **Do not have the Pro Trinket connected to the module PCB while uploading code. Remove it from the module.**

## Uploading the firmware
- Open the .ino file in Arduino IDE.
- Make the following settings in the Tools menu:
  - Board: Pro Trinket 5V/16MHz (USB)
  - Programmer: USBtinyISP
- Compile the firmware by pressing CMD+R (mac) or CTRL+R (win). The Arduino compiler should say "Done compiling" and return no errors.
- Press the momentary switch once on the Pro Trinket. The onboard red onboard LED should now start fading in and out, indicating that the bootloader is enabled.
- While the LED is fading in and out, upload the firmware to the Nano board by pressing CMD+U (mac) or CTRL+U (win). If everything went well, the Arduino IDE will return "Done uploading" and return no errors.
- **Double check that the Pro Trinket is seated the right way on the module PCB before powering on!**
