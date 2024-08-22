# klipper for My 3d printer 

- ender3 custom direct drive with BIGTREETECH SKR Mini E3 V2.x
- Klipper backup script for manual or automated GitHub backups

main printer.cfg configuration file is at [printer_data/config/printer.cfg](https://github.com/bongiben/mainsail/blob/fd206d3a2f8caa8a670089263e1468404d171a7f/printer_data/config/printer.cfg)

macros macros.cfg file is at [printer_data/config/macros.cfg](https://github.com/bongiben/mainsail/blob/cdc041e903a571db4d9ad03abd3fa4af53cd5fa5/printer_data/config/macros.cfg)


## Equipment Used

- **Mainboard**: BIGTREETECH SKR Mini E3 V2.0
- **Stepper Drivers**: TMC2209
- **Display**: ST7920 LCD
- **Probing System**: BLTouch
- **Filament Runout Sensor**: Configured
- **Cooling Fans**: Heatbreak cooling fan and general cooling fan
- **Heated Bed**: Configured with PID control

## Features

### Stepper Configuration

The stepper motors for the X, Y, Z axes and the extruder are controlled by TMC2209 drivers, using UART communication. The microsteps are set to 16, with specified rotation distances for accurate movement control.

### Heater & Fan Configuration
Heated Bed: Controlled using a PID loop with specific Kp, Ki, and Kd values.
Cooling Fans: Configured for heatbreak cooling and general fan.
### BLTouch Configuration
The BLTouch is set up with an offset from the nozzle and configured for safe homing and bed mesh leveling.
### Bed Mesh Leveling
Mesh leveling is configured with a 5x5 grid for accurate bed leveling using a BLTouch sensor.
### Additional Features
- **Filament Runout Sensor**: Pauses the print on filament runout and includes custom `runout_gcode` for handling the event.
- **Input Shaper**: Configured with specific shaper types and frequencies for the X and Y axes to reduce vibrations.
- **Virtual SDCard**: Allows for G-code storage and retrieval from Klipper's virtual SD card.
- **External Configuration Files**: Additional configurations and macros included via external files.


# Klipper G-Code Macros

This repository provides a collection of G-Code macros for use with Klipper firmware. These macros can be copied into your `printer.cfg` file and customized as needed. Below is a summary of the key macros provided in this collection. **Currently work in progress as just needed to get working**


## Table of Contents

- [Start and End Print](#start-and-end-print)
- [Beeper](#beeper)
- [Filament Change](#filament-change)
- [Environmental Sensors](#environmental-sensors)
    - [BMP280/BME280/BME680](#bmp280bme280bme680-environmental-sensor)
    - [HTU21D](#htu21d-environmental-sensor)
- [Custom Commands](#custom-commands)
    - [Override M117](#override-m117)
    - [SDCard Looping (M808)](#sdcard-looping-m808)
    - [Cancel Object (M486)](#cancel-object-m486)
    - [Set Digital Potentiometer (G130)](#set-digital-potentiometer-g130)
- [YouMakeTech Macros](#youmaketech-macros)
