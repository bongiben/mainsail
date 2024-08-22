# klipper for My 3d printer 

- ender3 custom direct drive with BIGTREETECH SKR Mini E3 V2.x
- Klipper backup script for manual or automated GitHub backups

main printer.cfg configuration file is at [printer_data/config/printer.cfg](https://github.com/bongiben/mainsail/blob/fd206d3a2f8caa8a670089263e1468404d171a7f/printer_data/config/printer.cfg)

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
