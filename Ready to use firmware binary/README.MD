firmware-20210225-105300.bin

Pre-compiled firmware file for Darren Noden

COPY THE firmware-20210225-105300.bin file to your SD CARD
- Power ON your Ender 3 Pro
- WAIT until firmware upgrade is complete
- Printer name post-install will be "Darren's Ender 3 Pro - Marlin v.2.0.7.2"

ADDED BY 3dpmarkr
=================

PID EDIT / AUTOTUNE - under "Advanced Settings"

Disable all Volumetric extrusion options e=mm3 (now always OFF)

Power-Loss Recovery:(ENABLED) / M413 Resume printing from SD Card in power loss situation.

NOTE : Once firmware update is completed - POWER OFF the Printer
- EJECT the SD CARD
- Put SD CARD back into your PC / Laptop and delete the firmware-20210225-105300.bin file
- Put the the SD CARD back into your printer

IMPORTANT NOTES ON CREALITY V.4.2.2 BOARD
- You cannot use the same filename for firmware updates - every time - the name should be UNIQUE
- As such - every time the firmware is re-compiled a new date / time stamp is added to create a unique name.

TMC2208 stepper drivers are running in STANDALONE mode
- Limitations
- NOT Compatible with Linear Advance (Disabled in this build of the firmware)
- VREF tuning needs to be done via the pots on the motherboard if steppers are getting hot. Use a multimeter to check VREF.

Enjoy !

3dpmarkr