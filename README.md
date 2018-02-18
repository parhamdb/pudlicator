# pudlicator
Parham's Monoprice Maker Select V2/Wanhao Duplicator i3 3D Printer.
The goal of my design and modifications to this printer was a very quiet printer (I use it in a shared office environment), remotely managed and reliability.

## firmware
I used Marlin 1.1.8 Firmware.
Three required files:
- Configuration.h
- Configuration_adv.h
- pin_RAMPS.h 
can be found under firmware/marlin-1.1.8 folder.
Simply Copy/Paste content of these files over or compare them line by line.

### Features enabled in this firmware
Make sure you disable features you don't need or have
- BLTouch with auto bed leveling
- TMC2130 Stepper Driver
  - SPI Configuration. Will require cable
  - Look at pins_RAMPS.h for SPI pin configuration
  - Endstop is NOT configured with Diag 1 of TMC2130
  - Only X and Y are connected to SPI interface, the rest are not configured with SPI
- NO DISPLAY Configured! I use MKS TFT28 display which works with serial port and through other interface. This does not need any display configured in the firmware. Make sure you enable this.
