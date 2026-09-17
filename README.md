# BBQ20-RP2040 Custom QMK Firmware

This project is a custom QMK firmware for the BlackBerry BBQ20 keyboard, based on the Raspberry Pi RP2040 controller.
The project includes a BOM, schematics, compiled firmware, and source code.

It perfectly resolves legacy issues such as the original code failing to compile in the new QMK environment, dim backlighting, and incorrect touchpad orientation, and optimizes the top row of buttons for everyday use.

## 📍 Pin definition (Pinout Configuration)
The matrix mapping for this firmware is as follows (for a custom RP2040 driver board):

- **Rows (8)**: `GP1`, `GP2`, `GP3`, `GP4`, `GP5`, `GP6`, `GP7`, `GP20`
- **Cols (8)**: `GP8`, `GP9`, `GP14`, `GP13`, `GP12`, `GP11`, `GP10`, `GP19`
- **Backlight**: `GP25`

## ⌨️ Top button description (Top Row Keymap)

To better suit daily PC use, the physical buttons at the bottom of the screen have been remapped from left to right as follows:

- Dialer key (green) -> Tab key
- BlackBerry logo -> Win key / GUI key
- Touchpad pressed -> Left mouse button
- Back key -> Right mouse button
- Hang up key (red) -> Esc key

## 🚀 Compilation and Flashing Guide (Build Instructions)

**⚠️ Extremely Important:** You must use QMK version `0.22.0` to compile in order to avoid conflicts caused by underlying architecture changes in the latest version.

1. **Prepare the environment and switch to version 0.22.0:**

``bash
   cd qmk_firmware
   git fetch [https://github.com/qmk/qmk_firmware.git](https://github.com/qmk/qmk_firmware.git) --tags
   git checkout 0.22.0
   make git-submodule

## Place the code from this repository in the specified directory:
Place the bbq20 folder in the qmk_firmware/keyboards/ directory # BBQ20KBD_RP2040

