# Baikal Handwired Split Corne Keyboard

<p align="center">
  <img src="media/Home.png" alt="Baikal Keyboard" width="700"/>
</p>

An affordable, beginner-friendly handwired split keyboard build (~€20) using a Pro Micro NRF52840 (Nice!nano V2 clone). Wireless via ZMK (BLE) with USB wired mode fallback.

---

## Why This Project?

**The goal of this project is to create a simple, cheap, and easy-to-build handwired Corne keyboard with step-by-step instructions.**

When I got into building keyboards, I wished something like this existed: a detailed guide that walks you through the entire process. This project is designed so anyone who wants to build their own handwired Corne can do it with confidence.

### Key Features

- **Budget-friendly**: Total build cost around ~€20 (excluding keycaps and tools)
- **Beginner-friendly**: Ready-to-flash firmware included so no coding required if you follow the wiring diagram
- **Wireless**: Bluetooth Low Energy (BLE) via ZMK firmware
- **Flexible switch support**: Works with both **Kailh Choc low-profile** switches AND **standard MX** switches
- **ZMK Studio compatible**: Edit your keymap visually without reflashing
- **Customizable**: If you wire differently or want to tweak the firmware, the source repo is available

---

## Gallery

### Real Build

<p align="center">
  <img src="media/real pic.jpg" alt="Real keyboard photo" width="700"/>
</p>

### Renders

<p align="center">
  <img src="media/front.png" alt="Front view render" width="600"/>
</p>

<p align="center">
  <img src="media/top.png" alt="Top view render" width="700"/>
</p>

<p align="center">
  <img src="media/exploded view.png" alt="Exploded view" width="500"/>
</p>

---

## Keymap Layers

The firmware comes with 3 layers preconfigured:

### Base Layer (QWERTY)

<p align="center">
  <img src="media/base layer.png" alt="Base layer" width="700"/>
</p>

### Lower Layer (Numbers + Bluetooth)

<p align="center">
  <img src="media/lower layer.png" alt="Lower layer" width="700"/>
</p>



### Raise Layer (Symbols)

<p align="center">
  <img src="media/raise layer.png" alt="Raise layer" width="700"/>
</p>

---

## Bill of Materials (BOM)

This is a handwired build, assuming you have solder, soldering iron, and some [wires](https://www.aliexpress.com/item/1005005048098404.html).

| Item | Qty | Link |
|:-----|:----|:-----|
| Mechanical Cherry MX switches **OR** Kailh Choc switches | 42 | [MX switches](https://www.aliexpress.com/item/1005007345651159.html) / [Choc switches](https://www.aliexpress.com/item/1005008883418065.html) |
| Pro Micro NRF52840 controller (Nice!Nano V2 clone) | 2 | [Link](https://www.aliexpress.com/item/1005006995289476.html) |
| Controller feet pins | 4 | Comes with controller |
| Diodes 1N4148 | 42 | [Link](https://www.aliexpress.com/item/1005006245109375.html) |
| M2 6mm screws | 10 | [Link](https://www.aliexpress.com/item/1005005070119421.html) |
| M2 6mm stand-offs | 6 | [Link](https://www.aliexpress.com/item/1005006049595637.html) |
| M2 (OD 3.2mm) 3mm heat-set inserts | 4 | [Link](https://www.aliexpress.com/item/1005003582355741.html) |
| Kapton tape | 1 | [Link](https://www.aliexpress.com/item/1005007518587827.html) |
| Copper wire | 1 | [Link](https://www.aliexpress.com/item/1005009078359338.html) |
| 801350 3.7V Li-Po batteries | 2 | [Link](https://www.aliexpress.com/item/1005007117105334.html) |
| Keycaps | 42 | 3D print or buy online |

### Notes

- **Switches**: Case supports both Kailh Choc (low-profile) and MX-style switches. Choose based on your preference.
- **Keycaps**: Can be bought or 3D printed. Plenty of good options online depending on your budget.


---

## Wiring Diagram

<p align="center">
  <img src="media/wiring diagram.jpg" alt="Wiring diagram" width="700"/>
</p>

The diagram shows GPIO pin numbers for both halves. **Follow this exactly if you want to use the prebuilt firmware.**

- Numbers correspond to NRF52840 GPIO pins

---

## Build Instructions

Full step-by-step instructions are included in the PDF:

📄 **[Baikal Build Instructions (PDF)](media/Baikal%20build%20instructions.pdf)**

Please read the build guide before starting. It includes:
- Wiring details and assembly sequence
- Tips for handwiring
- Notes specific to this design

---

## Firmware

### Ready-to-Flash Firmware

If you wire according to the provided diagram, you can flash the prebuilt firmware directly:

| Half | File |
|------|------|
| Left | [corne_hw_left-nice_nano_v2-zmk.uf2](Ready%20to%20flash%20Firmware/corne_hw_left-nice_nano_v2-zmk.uf2) |
| Right | [corne_hw_right-nice_nano_v2-zmk.uf2](Ready%20to%20flash%20Firmware/corne_hw_right-nice_nano_v2-zmk.uf2) |
| Reset (troubleshooting) | [settings_reset_nice_nano.uf2](Ready%20to%20flash%20Firmware/settings_reset_nice_nano.uf2) |

### Flashing Instructions (UF2)

1. Put the Nice!nano into bootloader mode (short GND and the reset pins  quickly to simulate double-tap)
2. A USB drive named `NICENANO` should appear
3. Drag-and-drop the appropriate `.uf2` file onto the drive
4. The board will automatically reboot with new firmware
5. Repeat for the other half

### Custom Firmware

If you wire differently or use a different controller, you'll need to build your own ZMK firmware:

- **My ZMK config repo**: [github.com/vostoklabs/zmk-config-hw](https://github.com/vostoklabs/zmk-config-hw)  Fork this and modify for your needs
- **ZMK User Setup Guide**: [zmk.dev/docs/user-setup](https://zmk.dev/docs/user-setup)
- **ZMK Documentation**: [zmk.dev/docs](https://zmk.dev/docs)

### ZMK Studio

This build supports [ZMK Studio](https://zmk.dev/docs/features/studio) for convenient keymap adjustments without reflashing. Connect via USB or Bluetooth and edit your layout visually.

---

## 3D Print Files

The printable case files (Step/3MF) are available on MakerWorld:

 **[Baikal Keyboard on MakerWorld](https://makerworld.com/en/@Vostok_Labs)**

---

## License

This project is open source. Feel free to use, modify, and share.

---

## Credits

Designed by [Vostok Labs](https://github.com/vostoklabs)

Inspired by the [Corne keyboard](https://github.com/foostan/crkbd) by foostan.
