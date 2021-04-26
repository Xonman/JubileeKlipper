# JubileeKlipper
Klipper configuration for Jubilee3d toolchanger using Duet2 &amp; Duex5 hardware.

Heavily inspired by [SteveJWallace's config](https://github.com/SteveJWallace/JubileeKlipper) but using Duet2 & Duex pins.

The exact Jubilee3d setup this config is maintained for is:
- LDO geared stepper motor (LDO-28STH32-0674APG14)
- Standard LDO motors (42STH60-2004MAC for X/Y, 3x 42STH47-1684MAC for Z)
- X/Y plugged into X/Y, REL geared stepper plugged into Z, ZZZ plugged into E2/3/5
- 3x extruders plugged into E0/1/6, though Extruder2 (E6) is using the E3 heater on the duex
- Thermostatic fans on all extruders using Fan0/1/3 and an MCU fan on Fan2 limited to 40%
- A single part fun on FAN7 - this is to use a single Berd air pump for all tools - if you use individual tool fans check out [Steve's modified fan setup](https://github.com/SteveJWallace/JubileeKlipper/blob/master/configs/fans.cfg#L3) - the fan file is included but commented out as it's not needed.

Included are lightly modified versions of Steve's tool management macros adjusted to match the LDO stepper distances.
