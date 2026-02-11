# kei40 

### 40% 4x10 keyboard

fr4 ortholinear plate<br>
feker holy pandas - stems lubed with 205g0, springs with 105g0<br>
**raspberry pi pico** for the keeb controller<br>
22, 8 AWG solid core copper wires<br>
1N4148 diodes

keeb firmware and layout, written and configured with [qmk](https://qmk.fm/)

cd ~/qmk_firmware/keyboards/handwired/kei40<br>
code keymaps/default/keymap.c<br>
code info.json

#### compiling:<br>
cd ~/qmk_firmware<br>
qmk compile -kb handwired/kei40 -km default<br>
drag the new **handwired_kei40_default.uf2** file to the RPI-RP2 drive<br>

#### personal project [@rileriaaa](https://rileriaaa.vercel.app/)