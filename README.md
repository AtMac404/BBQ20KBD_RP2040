# BBQ20-RP2040 Custom QMK Firmware

本项目是基于 Raspberry Pi RP2040 主控的 BlackBerry BBQ20 键盘客制化 QMK 固件。
项目包含bom，原理图，以编译的固件和源代码

完美解决了原版代码在新版 QMK 环境下无法编译、背光昏暗、触摸板方向错乱等历史遗留问题，并针对日常使用习惯优化了顶排按键。

## 📍 引脚定义 (Pinout Configuration)

本固件的矩阵映射如下（针对自定义 RP2040 驱动板）：
- **Rows (8)**: `GP1`, `GP2`, `GP3`, `GP4`, `GP5`, `GP6`, `GP7`, `GP20`
- **Cols (8)**: `GP8`, `GP9`, `GP14`, `GP13`, `GP12`, `GP11`, `GP10`, `GP19`
- **Backlight**: `GP25`

## ⌨️ 顶部按键说明 (Top Row Keymap)

为了适配 PC 日常操作，屏幕下方的实体按键功能已从左到右重映射为：
- `拨号键` (绿色) -> **Tab 键**
- `黑莓 Logo` -> **Win 键 / GUI**
- `触摸板按下` -> **鼠标左键**
- `返回键` -> **鼠标右键**
- `挂断键` (红色) -> **Esc 键**

## 🚀 编译与刷写指南 (Build Instructions)

**⚠️ 极其重要：** 必须使用 QMK `0.22.0` 版本进行编译，以避免最新版本底层的架构变动冲突。

1. **准备环境并切换到 0.22.0 版本**：
   ```bash
   cd qmk_firmware
   git fetch [https://github.com/qmk/qmk_firmware.git](https://github.com/qmk/qmk_firmware.git) --tags
   git checkout 0.22.0
   make git-submodule

## 将本仓库代码放入指定目录：
将 bbq20 文件夹放置在 qmk_firmware/keyboards/ 目录下# BBQ20KBD_RP2040

