firmware-20210226-184703.bin

Pre-compiled firmware file for Darren Noden
(Revised 26th February 2021) @ 18:47hrs

NEW PID values for Hotend and Bed (PID Tuned) added to build
============================================================

PID settings based on PLA @ 210 hotend / 55 bed
Hotend : M301
P24.89 I2.07 D74.82

Bed :  M304
P136.37 I26.59 D466.36

NEW FEATURES ADDED
==================
MMBL - Manual Mesh Bed Levelling (9 points - 3 by 3)
- Level Bed Corners (step 1) followed by Level Bed (step 2)
- - Use the ROTARY KNOB to adjust the 9 points up or down and CLICK to store / move to next point
- - When complete - remember to "Store Settings"
- For a good video guide on HOW TO USE : Chep - https://youtu.be/fSNqJuVdQHw
--- (Ignore the references to the BTT SKR Mini E3 board)
- Restore levelling after G28 has also been enabled (to prevent G28 HOME all axis erasing the mesh data)

AS - ARC Support (for use with Arc Welder - CURA Plugin)

Z Probe Offset Wizard (requires ABL)

UPDATE INSTRUCTIONS
===================
COPY THE firmware-20210226-184703.bin file to your SD CARD
- Power ON your Ender 3 Pro
- WAIT until firmware upgrade is complete
- Printer name post-install will be "Darren's Ender 3 Pro - Marlin v.2.0.7.2 - MMBL AS" (Shows extra features added)

ADDED BY 3dpmarkr
=================

PID EDIT / AUTOTUNE - under "Advanced Settings"

Disable all Volumetric extrusion options e=mm3 (now always OFF)

Power-Loss Recovery:(ENABLED) / M413 Resume printing from SD Card in power loss situation.

NOTE : Once firmware update is completed - POWER OFF the Printer
- EJECT the SD CARD
- Put SD CARD back into your PC / Laptop and delete the firmware-xxxxxxxx-xxxxxx.bin file
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