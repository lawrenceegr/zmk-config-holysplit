# HolySplit Keyboard User Manual

## Table of Contents
1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Keyboard Layout](#keyboard-layout)
4. [Layers Explained](#layers-explained)
5. [RGB Lighting Control](#rgb-lighting-control)
6. [Bluetooth Pairing](#bluetooth-pairing)
7. [Battery and Charging](#battery-and-charging)
8. [Firmware Flashing](#firmware-flashing)
9. [Troubleshooting](#troubleshooting)
10. [Technical Specifications](#technical-specifications)

---

## Introduction

The HolySplit is a wireless ergonomic split keyboard featuring:

- **True wireless split design** - No cable between keyboard halves
- **Bluetooth connectivity** - Connect to up to 5 devices
- **USB-C charging and wired mode** - Works while charging
- **Per-key RGB lighting** - Customizable underglow effects
- **6 programmable layers** - Maximum efficiency
- **ZMK firmware** - Modern, open-source keyboard firmware
- **Long battery life** - Weeks of use on a single charge

---

## Getting Started

### First-Time Setup

1. **Charge both keyboard halves**
   - Connect USB-C cables to both halves
   - Charge for at least 2 hours before first use
   - Full charge takes approximately 2-3 hours

2. **Power on both halves**
   - Press the power switch on each half to ON position
   - Both halves will automatically pair with each other via Bluetooth
   - This pairing happens automatically and only needs to be done once

3. **Connect to your computer**
   
   **Option A: Wireless (Bluetooth)**
   - The left keyboard half enters pairing mode automatically on first power-on
   - On your computer, go to Bluetooth settings
   - Look for "HolySplit" in the list of available devices
   - Click to pair
   
   **Option B: Wired (USB)**
   - Plug a USB-C cable from the left half to your computer
   - The keyboard works immediately
   - Automatically switches to wired mode for lower latency

4. **Start typing**
   - Both halves communicate wirelessly with each other
   - Only the left half connects to your computer

---

## Keyboard Layout

### Physical Layout

The HolySplit features an ergonomic column-staggered layout with:
- Alphanumeric keys arranged in a split QWERTY layout
- Function keys (F13-F20) on the outer edges
- Thumb clusters for frequently used modifiers and layer access
- Arrow keys on the right side

### Default Layer (Layer 0)



Standard typing layer with:
- Standard QWERTY letter arrangement
- Number row (1-0)
- Common symbols accessible with Shift
- Function keys on edges (F13-F20)
- Arrow keys in bottom right

---

## Layers Explained

The HolySplit has 6 layers accessed by holding layer keys in the thumb clusters.

### Layer 0 - Default (Base Layer)

![Layer 0](/docs/images/layer-0.png)

Standard QWERTY layout for everyday typing.

---

### Layer 1 - Function Keys & Navigation
**Access:** Hold "Layer1" key (left thumb cluster)

![Layer 1](/docs/images/layer-1.png)

**Features:**
- F1-F12 on the number row
- Navigation keys: Home, End, PgUp, PgDn on arrow cluster

---

### Layer 2 - Symbols
**Access:** Hold "Layer2" key (right thumb cluster)

![Layer 2](/docs/images/layer-2.png)

**Features:**
- Special symbols: !, @, #, $, %, ^, &, *, (, )
- Programming symbols: ~, _, +, {, }, <, >, ?, :

---

### Layer 3 - Bluetooth Control
**Access:** Hold "Layer3" key (thumb cluster)

![Layer 3](/docs/images/layer-3.png)

**Features:**
- **BT CLR:** Clear current Bluetooth profile
- **BT 0-4:** Switch between 5 saved Bluetooth profiles

**Usage:**
1. To pair new device: Press BT 0-4 to select slot, then pair from device
2. To switch devices: Press BT 0-4 for the device you want
3. To clear profile: Select profile, then press BT CLR

---

### Layer 4 - RGB Lighting
**Access:** Hold "Layer4" key (left thumb cluster)

![Layer 4](/docs/images/layer-4.png)

**Features:**
- **RGB TOG:** Toggle RGB on/off
- **RGB BRI+:** Increase brightness
- **RGB BRI-:** Decrease brightness
- **RGB EFF:** Next lighting effect
- **RGB EFF-:** Previous lighting effect

---

### Layer 5 - Custom
**Access:** Hold "Layer5" key (right thumb cluster)

![Layer 5](/docs/images/layer-5.png)

Reserved for future customization via firmware updates.

---

## RGB Lighting Control

### Basic Controls

- **Toggle on/off:** Layer 4 → RGB TOG
- **Adjust brightness:** Layer 4 → RGB BRI+ / RGB BRI-
- **Change effects:** Layer 4 → RGB EFF / RGB EFF-

### Available Effects

- Solid color
- Breathing
- Rainbow wave
- Color cycle

### Power Impact

RGB lighting affects battery life:
- **RGB Off:** Several weeks
- **RGB Low brightness:** Several days
- **RGB High brightness:** 1-2 days

**Tip:** Disable RGB when on battery for maximum runtime.

---

## Bluetooth Pairing

### Pairing Your First Device

The keyboard enters pairing mode automatically on first power-on:
1. Open Bluetooth settings on your device
2. Select "HolySplit"
3. Click connect

### Managing Multiple Devices (Up to 5)

**To pair a new device:**
1. Access Layer 3
2. Press BT 0, BT 1, BT 2, BT 3, or BT 4 to select a slot
3. Keyboard enters pairing mode
4. Connect from your device's Bluetooth settings

**To switch between devices:**
1. Access Layer 3
2. Press the BT key (0-4) for the device you want

**To clear a profile:**
1. Access Layer 3
2. Select the profile
3. Press BT CLR

### Example Setup
- BT 0: Work laptop
- BT 1: Personal computer
- BT 2: Tablet
- BT 3: Phone
- BT 4: Gaming PC

---

## Battery and Charging

### Battery Life

- **Typical usage (no RGB):** 2-6 weeks
- **With RGB (low):** 3-7 days
- **With RGB (high):** 1-2 days

### Charging

Each keyboard half charges independently:
1. Connect USB-C cable to keyboard half
2. Connect to USB power source
3. Keyboard continues working while charging
4. Full charge: 2-3 hours

**When connected via USB to computer:**
- Left half automatically switches to USB mode (lower latency)
- Acts as wired keyboard
- Charges simultaneously

### Power Saving

Automatic power saving:
- **30 minutes idle:** Low-power mode
- **1 hour idle:** Deep sleep

Press any key to wake.

---

## Firmware Flashing

### When to Flash Firmware

Flash firmware to:
- Update to latest features
- Apply bug fixes
- Change key mappings
- Enable new functionality

### Required Equipment

- **SWD Programmer:** J-Link, ST-Link, or compatible
- **Connection wires:** 4 wires (SWDIO, SWCLK, GND, VCC)
- **Computer** with flashing software (nrfjprog, OpenOCD, or J-Link software)
- **Firmware files:** holysplit_left.uf2 and holysplit_right.uf2

### SWD Connection Points

Both keyboard halves have SWD programming pads:

**Required connections:**
- **SWDIO** - Serial Wire Debug I/O
- **SWCLK** - Serial Wire Clock
- **GND** - Ground
- **VCC** - 3.3V power (optional, can use USB power)

### Flashing Procedure

**For each half (left and right):**

1. **Connect SWD programmer**
   - Connect SWDIO, SWCLK, and GND pins
   - Ensure proper connection to keyboard's SWD pads

2. **Power the keyboard**
   - Either through SWD programmer's VCC
   - Or connect USB cable for power

3. **Flash firmware using nrfjprog:**
   ```bash
   # Erase chip
   nrfjprog --family NRF52 --eraseall
   
   # Flash firmware
   nrfjprog --family NRF52 --program holysplit_left.hex --verify
   
   # Reset
   nrfjprog --family NRF52 --reset
   ```

4. **Or flash using J-Link software:**
   - Open J-Flash Lite
   - Select device: nRF52840_xxAA
   - Load firmware .hex file
   - Program device
   - Verify and reset

5. **Or flash using OpenOCD:**
   ```bash
   openocd -f interface/jlink.cfg -f target/nrf52.cfg \
     -c "program holysplit_left.hex verify reset exit"
   ```

6. **Repeat for other half** with holysplit_right.hex

### Alternative: UF2 Bootloader Method

If your keyboard has UF2 bootloader installed:

1. **Enter bootloader mode:**
   - Double-press reset button quickly
   - Or hold reset while plugging in USB

2. **Keyboard appears as USB drive** named "NRF52BOOT"

3. **Copy firmware:**
   - Drag holysplit_left.uf2 to the USB drive
   - Keyboard automatically flashes and reboots

4. **Repeat for right half** with holysplit_right.uf2

### Post-Flash Testing

After flashing:
1. Power on both halves
2. Verify both halves pair with each other
3. Test all keys on both sides
4. Check RGB functionality (Layer 4)
5. Verify Bluetooth connectivity

### Troubleshooting Flash Issues

**Programmer not detected:**
- Check cable connections
- Install programmer drivers
- Try different USB port

**Flash verification fails:**
- Erase chip completely first
- Check power supply is stable
- Verify correct firmware file

**Keyboard doesn't work after flash:**
- Re-flash firmware
- Try different firmware version
- Check SWD connections weren't damaged

---

## Troubleshooting

### Keyboard Not Responding

**Solutions:**
1. Check both halves are powered on
2. Charge if battery is low
3. Press any key to wake from sleep
4. Power cycle both halves

### Split Halves Not Syncing

**Solutions:**
1. Power off both halves
2. Power on right half first, wait 5 seconds
3. Power on left half
4. Should automatically reconnect

### Bluetooth Won't Connect

**Solutions:**
1. Clear Bluetooth profile (Layer 3 → BT CLR)
2. Remove "HolySplit" from device's Bluetooth settings
3. Try pairing from scratch
4. Try different profile slot (BT 0-4)

### RGB Not Working

**Solutions:**
1. Toggle RGB on (Layer 4 → RGB TOG)
2. Increase brightness (Layer 4 → RGB BRI+)
3. Check battery level - low battery disables RGB
4. Charge keyboard

### Battery Drains Quickly

**Solutions:**
1. Turn off RGB lighting
2. Reduce RGB brightness
3. Ensure keyboard enters sleep mode
4. Check for stuck keys

---

## Technical Specifications

| Feature | Specification |
|---------|--------------|
| **MCU** | nRF52840 (both halves) |
| **Connectivity** | Bluetooth 5.0 + USB-C |
| **Battery** | LiPo rechargeable (each half) |
| **Charging** | USB-C, 5V |
| **RGB** | Per-key SK6812 Mini-E LEDs |
| **Firmware** | ZMK (Zephyr-based) |
| **Bluetooth Profiles** | 5 simultaneous pairings |
| **Polling Rate (USB)** | 1000Hz (1ms) |
| **Latency (BLE)** | 7-15ms typical |
| **Programming Interface** | SWD (Serial Wire Debug) |
| **Flash Memory** | 1MB |
| **RAM** | 256KB |

---

## Quick Reference

### Layer Access
- **Layer 1:** Hold left thumb "Layer1"
- **Layer 2:** Hold right thumb "Layer2"
- **Layer 3:** Hold "Layer3"
- **Layer 4:** Hold left thumb "Layer4"
- **Layer 5:** Hold right thumb "Layer5"

### Bluetooth
- **Switch profile:** Layer 3 → BT 0/1/2/3/4
- **Clear profile:** Layer 3 → BT CLR

### RGB
- **Toggle:** Layer 4 → RGB TOG
- **Brightness:** Layer 4 → RGB BRI+/-
- **Effects:** Layer 4 → RGB EFF/EFF-

### Flashing
- **Connect SWD:** SWDIO, SWCLK, GND
- **Flash command:** `nrfjprog --program firmware.hex`
- **Or use UF2:** Double-press reset, drag .uf2 file

---

## Safety Information

- Use only USB-C cables rated for data and power
- Do not disassemble battery
- Keep away from extreme heat (>60°C)
- Dispose according to local e-waste regulations

---

**For firmware updates and technical support, contact your keyboard provider.**

*Document Version 1.0*