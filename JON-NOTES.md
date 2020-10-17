# 'Stock' Anet A8 configuration build

First build installed - 9da4cc1b458e0cd47ed8ef80aeef135f798ce93d

Advanced Memory Usage is available via "PlatformIO Home > Project Inspect"
RAM:   [==        ]  25.0% (used 4095 bytes from 16384 bytes)
Flash: [========  ]  83.4% (used 108490 bytes from 130048 bytes)


# Removed unused SD card reader

Mostly to stop the annoying status messages in OctoPrint

RAM:   [==        ]  18.0% (used 2947 bytes from 16384 bytes)
Flash: [=======   ]  70.8% (used 92014 bytes from 130048 bytes)

# Enabled the control buttons

Defined ADC_KEYPAD - found J3 / LCD pinouts in the anet pinout header

Advanced Memory Usage is available via "PlatformIO Home > Project Inspect"
RAM:   [==        ]  18.0% (used 2947 bytes from 16384 bytes)
Flash: [=======   ]  70.8% (used 92014 bytes from 130048 bytes)


# Resetting home position

M206 X-6 Y8  seemed good
can save with M500, load with M501 and reset with M502


# Thermal runaway on long prints

Trying to print the electronics case.
It failed at the same point in different layers.
Found it displaying thermal cutout warning.

hypotheis printing enough material the extruder couldn't keep up.

Trying baudrate: 115200
Send: N0 M110 N0*125
Recv: start
Changing monitoring state from "Detecting baudrate" to "Operational"
Send: N0 M110 N0*125
Recv: echo:Marlin 2.0.5.3
Recv: 
Recv: echo: Last Updated: 2020-03-31 | Author: (Bob Kuhn, Anet config)
Recv: echo:Compiled: Jun  9 2020
Recv: echo: Free Memory: 12245  PlannerBufferBytes: 1200
Recv: echo:V76 stored settings retrieved (640 bytes; crc 12275)
Recv: echo:  G21    ; Units in mm (mm)
Recv: echo:  M149 C ; Units in Celsius
Recv: 
Recv: echo:; Filament settings: Disabled
Recv: echo:  M200 D1.75
Recv: echo:  M200 D0
Recv: echo:; Steps per unit:
Recv: echo: M92 X100.00 Y100.00 Z400.00 E100.00
Recv: echo:; Maximum feedrates (units/s):
Recv: echo:  M203 X400.00 Y400.00 Z8.00 E50.00
Recv: echo:; Maximum Acceleration (units/s2):
Recv: echo:  M201 X2000.00 Y2000.00 Z100.00 E10000.00
Recv: echo:; Acceleration (units/s2): P<print_accel> R<retract_accel> T<travel_accel>
Recv: echo:  M204 P400.00 R1000.00 T1000.00
Recv: echo:; Advanced: B<min_segment_time_us> S<min_feedrate> T<min_travel_feedrate> J<junc_dev>
Recv: echo:  M205 B20000.00 S0.00 T0.00 J0.10
Recv: echo:; Home offset:
Recv: echo:  M206 X-6.00 Y8.00 Z0.00
Recv: echo:; Material heatup parameters:
Recv: echo:  M145 S0 H190 B60 F0
Recv: echo:  M145 S1 H240 B90 F0
Recv: echo:; PID settings:
Recv: echo:  M301 P21.00 I1.25 D86.00
Recv: echo:  M304 P295.00 I35.65 D610.21
Recv: echo:SD init fail
Recv: echo:SD init fail
Recv: ok
Send: N1 M115*39
Recv: FIRMWARE_NAME:Marlin 2.0.5.3 (GitHub) SOURCE_CODE_URL:https://github.com/MarlinFirmware/Marlin PROTOCOL_VERSION:1.0 MACHINE_TYPE:Anet A8 EXTRUDER_COUNT:1 UUID:cede2a2f-41a2-4748-9b12-c55c62f367ff
Recv: Cap:SERIAL_XON_XOFF:0
Recv: Cap:BINARY_FILE_TRANSFER:0
Recv: Cap:EEPROM:1
Recv: Cap:VOLUMETRIC:1
Recv: Cap:AUTOREPORT_TEMP:1
Recv: Cap:PROGRESS:0
Recv: Cap:PRINT_JOB:1
Recv: Cap:AUTOLEVEL:0
Recv: Cap:Z_PROBE:0
Recv: Cap:LEVELING_DATA:0
Recv: Cap:BUILD_PERCENT:0
Recv: Cap:SOFTWARE_POWER:0
Recv: Cap:TOGGLE_LIGHTS:0
Recv: Cap:CASE_LIGHT_BRIGHTNESS:0
Recv: Cap:EMERGENCY_PARSER:0
Recv: Cap:PROMPT_SUPPORT:0
Recv: Cap:AUTOREPORT_SD_STATUS:0
Recv: Cap:THERMAL_PROTECTION:1
Recv: Cap:MOTION_MODES:0
Recv: Cap:CHAMBER_TEMPERATURE:0
Recv: ok
Send: M21
Recv: echo:SD init fail
Recv: ok
Send: M117 Connected to Octoprint.
Recv: ok
Send: M500
Recv: echo:Settings Stored (640 bytes; crc 12275)
Recv: ok
Send: M105
Recv: ok T:41.70 /0.00 B:18.66 /0.00 @:0 B@:0
Send: M155 S2
Recv: ok

Send: M503
Recv: echo:  G21    ; Units in mm (mm)
Recv: echo:  M149 C ; Units in Celsius
Recv: 
Recv: echo:; Filament settings: Disabled
Recv: echo:  M200 D1.75
Recv: echo:  M200 D0
Recv: echo:; Steps per unit:
Recv: echo: M92 X100.00 Y100.00 Z400.00 E100.00
Recv: echo:; Maximum feedrates (units/s):
Recv: echo:  M203 X400.00 Y400.00 Z8.00 E50.00
Recv: echo:; Maximum Acceleration (units/s2):
Recv: echo:  M201 X2000.00 Y2000.00 Z100.00 E10000.00
Recv: echo:; Acceleration (units/s2): P<print_accel> R<retract_accel> T<travel_accel>
Recv: echo:  M204 P400.00 R1000.00 T1000.00
Recv: echo:; Advanced: B<min_segment_time_us> S<min_feedrate> T<min_travel_feedrate> J<junc_dev>
Recv: echo:  M205 B20000.00 S0.00 T0.00 J0.10
Recv: echo:; Home offset:
Recv: echo:  M206 X-6.00 Y8.00 Z0.00
Recv: echo:; Material heatup parameters:
Recv: echo:  M145 S0 H190 B60 F0
Recv: echo:  M145 S1 H240 B90 F0
Recv: echo:; PID settings:
Recv: echo:  M301 P21.00 I1.25 D86.00
Recv: echo:  M304 P295.00 I35.65 D610.21
Recv: ok


Ran M303 S200

Recv: PID Autotune finished! Put the last Kp, Ki and Kd constants from below into Configuration.h
Recv: #define DEFAULT_Kp 32.09
Recv: #define DEFAULT_Ki 2.33
Recv: #define DEFAULT_Kd 110.42

And again with the fan on 
  // With fan - M303 E0 S210
  #define DEFAULT_Kp 40.95
  #define DEFAULT_Ki 3.94
  #define DEFAULT_Kd 106.50

Setting temporarily and retrying case print

M301 P40.95 I3.94 D106.50
M304 P269.41 I53.04 D912.21