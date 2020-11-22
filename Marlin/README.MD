Configuration files for Ender 3 - 3dpmarkr (22nd November 2020)
====================================================================

Marlin 2.0.7.2.

Configuration.h

Configuration_adv.h

HARDWARE
========
Creality Ender 3 printer

with BTT SKR v.1.2 board (STM32F103RC_btt_512K)

and BTT TFT35 display (running in Marlin mode - 12864-LCD / emulator mode)

Stock Hotend / Satsana (Modular) FAN Assembly

Filament Runout Sensor (based on my Thingiverse model - https://www.thingiverse.com/thing:4576651
- The FRO I use is the "surplus to requirements" Z Axis Limit Switch which is no longer required after installing the BL Touch V.3.1.

FRO Sensor case / mount
DOWNLOAD my FRO Box / Mount & Lid from Thingiverse - https://www.thingiverse.com/thing:4576651

Connects to E0-STOP header port on the BTT SKR Mini E3. V.1.2.
-The Sensor is wired up for G and S only (3 pin connector / 2 pins used)
- the other end of the cable is a 2 pin connector (GND and PC15) on e0-STOP header / port on SKR mini board

FRO SENSOR STATE
After Installation - use a gCode Terminal to check 
- M119 should show FRO sensor as "Open" with no filament loaded
- M119 will show "Triggered" with filament inserted (as switch is depressed / triggered when filament is present!)

BL Touch v.3.1 mount with spacer (Satsana Modular)

- MUST be wired to SERVO Port, and Z-Min endstop port (NOT Probe)


TMC2209 stepper drivers - configured for StealthChop x 4

Using physical endstops (NOT SENSORLESS HOMING)

MARLIN 2.0.7.2. Features Enabled
================================
Thermal Runaway Protection - Hotend and Bed ONLY (Not Chamber!)

ABL - G29 - BILINEAR AUTO_BED_LEVELING_BILINEAR x 4 Probe Points (16 total)

PID AutoTune Hotend & Bed *enabled*

*NEW FEATURE* - Z Probe Offset Wizard *enabled*

Printer Info Screen

Software Endstops Menu on LCD

S Curve Acceleration *enabled* 

Probe Z Offset / Babystepping Z COMBINED MODE - double-click LCD knob while printing to access.

NEW - Arc Support *enabled* - for use with the Octoprint Arc Welder "plug-in"


BUG's Fixed
===========

NOTE : All changes to Marlin are noted with comments line of //3dpmarkr

POST-INSTALLATION NOTES
=======================
After you have installed the firmware.bin

A)- Perform an EEPROM reset

B)- Get current PID settings using M503

- PID Tune the hotend for your desired material temperatures (use the built-in Menu on the LCD "Advanced Settings", or the following gCode via a terminal)

>HOTEND

>m303 c5 e0 s205 u1

>(c=5 iterations e=0 hotend s=target temp {205}) u1 store / use settings immediately

>m500

>(save to eeprom)

- PID Tune the BED for your printing adhesion temperatures (60) (use the built-in Menu on the LCD, or the following gCode via a terminal)

>BED

>m303 c5 e-1 s60 u1

>(c=5 iterations e=-1 bed s=target temp {60}) u1 store / use settings immediately

>m500

>(save to eeprom)

C) Level your bed
- Pre-heat your machine to an appropriate temperature - i.e. 200 nozzle / 60 bed
- From the "Motion" menu, choose "Level Corners"
- - Follow the procedure for levelling your bed corners / centre

- once complete, select "Level Bed" from the menu
- - Your bed levelling procedure will now measure n/25 points 
- - Once complete, choose "STORE SETTINGS" to store the G34 / Mesh Data from the bed levelling procedures.

D) AUTO-HOME your printer

E) Under "Temperature" - lower the temperature of your hot-end to 150 degrees C (it needs to be WARM, but not oozing filament!)
- Wait until the Hotend reaches the new lower temperature
- Clean your NOZZLE (a dirty nozzle can interfere with Z Probe offset measurements in next step)

F) If required - run the "Probe Offset Wizard" from the LCD menu - "Probe Offsets" menu - to correctly set your Z Probe Offset
- Follow the on-screen instructions.
- Remember to "Store Settings" once complete.

G) From the "Temperature" menu, select "Cooldown"


H) FINALLY - load up, and print a bed tramming / 1st layer test gCode - to ensure your printer is dialled in (especially your Z Offset)
- While it is printing - you can DOUBLE-CLICK the knob / selector wheel to access the Probe Z Offset values, and rotate left / right to "fine-tune" the value (includes Babystepping Z)

CONGRATULATIONS - YOUR ENDER 3 IS NOW READY TO USE.
========================================================

Don't forget to "tune" your printer.