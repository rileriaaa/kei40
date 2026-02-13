# kei40

a diy/custom handwired 40% ortholinear keyboard with a 4x10 layout.

<p align="center">
  <img src="https://github.com/user-attachments/assets/b140ad96-b9a3-4d8d-b877-9a3faab7178d" width="49%">
  <img src="https://github.com/user-attachments/assets/0170b3a1-9312-4b20-b57d-9d033c36396c" width="49%">
</p>

*kei (軽) — light in weight; distilled to its essential form.*

## specifications

**layout:** 4x10 ortholinear (39 keys)  
**plate:** FR4 ortholinear plate  
**switches:** Feker Holy Panda (rails lubed with Krytox 205g0, springs with Krytox 105g0)  
**controller:** Raspberry Pi Pico (RP2040)  
**wiring:** 22 AWG solid core copper wire  
**diodes:** 1N4148<br>
**keycaps:** blank white xda profile keycaps


## firmware
this keyboard runs [QMK](https://qmk.fm/) firmware  with support for multiple layers and customizable keymaps.

### prerequisites

- QMK firmware environment set up
- QMK CLI tools installed

### building

navigate to the QMK firmware directory and compile:
```bash
cd ~/qmk_firmware
qmk compile -kb handwired/kei40 -km default
```

### flashing

1. hold the BOOTSEL button on the Raspberry Pi Pico while plugging in the USB cable
2. the controller will mount as a drive named `RPI-RP2`
3. drag the compiled `handwired_{keyboard_name}_default.uf2` file to the drive
4. the drive will automatically unmount and the keyboard will be ready to use

## development

Edit keymap:
```bash
cd ~/qmk_firmware/keyboards/handwired/kei40
code keymaps/default/keymap.c
```

edit keyboard configuration:
```bash
code keyboard.json
```

## project Structure
```
keyboards/handwired/kei40/
├── keyboard.json          # hardware configuration
├── keymaps/
│   └── default/
│       └── keymap.c      # default keymap definition
```

## features

- full QMK firmware support with all standard features
- three-layer keymap with base, symbol, and function layers
- momentary layer switching via MO(1) and MO(2)
- compact 39-key layout optimized for efficiency
- hot-swappable firmware via USB bootloader

---

#### a personal project by [@rileriaaa](https://rileriaaa.vercel.app/)
