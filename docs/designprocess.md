# Project: Trident Split Keyboard - Design Process

## Project Overview
A custom hand-wired split keyboard featuring a 3x5 key matrix, dual trackpads, and a controller knob. The design prioritizes ergonomic reach and parametric consistency.

## Layout Evolution & Iterations
- **Grid Configuration:** Settled on a 3x5 matrix plus a two-key thumb cluster and one "side" key.
- **Trackpad Positioning:** Iteratively moved to a center of `[106, -13]` (relative to matrix) to optimize thumb reach while maintaining clearance from the index column.
- **Trackpad Dimensions:** Selected 35mm Cirque modules. The plate cutout is set to 36mm (18mm radius) with a 38-40mm bezel to ensure structural integrity and sufficient clearance for keycaps.
- **Thumb Cluster:** A two-key thumb cluster was added below the pad. The inner key is a 1.5u cap tilted clockwise to accommodate its width and prevent collision with the outer thumb key.
- **Side Key:** Added a single key between the home and top rows of the index column. This position is now designated for a rotary encoder knob.

## Component Decisions
- **Microcontrollers:** Dual RP2040 Pro-Micro.
- **Trackpads:** Cirque 35mm modules via I2C.
- **Rotary Encoder:** DFRobot SEN0235 module.
- **Inter-half Link:** UART/PIO serial link.
- **Wiring:** Hand-wired matrix; KiCad utilized for schematic mapping and net labeling.

## Firmware Strategy
- **Base Firmware:** QMK.
- **Features:** VIA support for real-time key remapping.
- **Logic:** Custom gesture software for advanced trackpad and encoder interaction.

## Technical Stack
- **Layout Engine:** Ergogen (YAML-driven)
- **3D Modeling:** FreeCAD (Part Design workbench)
- **EDA:** KiCad (Schematic only)
- **Firmware:** QMK / VIA / Rust (where applicable)
