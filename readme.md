# kei40

a diy handwired 40% ortholinear keyboard with a 4x10 layout.

### specifications

**layout:** 4x10 ortholinear (technically has 39 keys)  
**plate:** FR4 ortholinear plate  
**switches:** Feker Holy Panda (rails lubed with Krytox 205g0, springs with Krytox 105g0)  
**controller:** Raspberry Pi Pico (RP2040)  
**wiring:** 22 AWG and 8 AWG solid core copper wire  
**diodes:** 1N4148
**keycaps:** blank white xda profile keycaps

### firmware

this keyboard runs QMK firmware. configuration files can be found in the standard [QMK](https://qmk.fm/) directory structure.

### building

navigate to the QMK firmware directory and compile:
```bash
cd ~/qmk_firmware
qmk compile -kb handwired/kei40 -km default
```

### blashing

1. hold the BOOTSEL button on the Raspberry Pi Pico while plugging in the USB cable
2. the controller will mount as a drive named `RPI-RP2`
3. drag the compiled `handwired_{keyboard_name}_default.uf2` file to the drive
4. the drive will automatically unmount and the keyboard will be ready to use

### development

Edit keymap:
```bash
cd ~/qmk_firmware/keyboards/handwired/kei40
code keymaps/default/keymap.c
```

edit keyboard configuration:
```bash
code keyboard.json
```

---

personal project by [@rileriaaa](https://rileriaaa.vercel.app/)
