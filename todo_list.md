# Project: Trident Split Keyboard - Roadmap

## Phase 1: Electronics & Firmware (The "Brains")
- [ ] **Hardware Selection**
    - [ ] Finalize trackpad module (e.g., Cirque 35mm/40mm)
    - [ ] Select RP2040 board (Zero, Pico, or Custom)
    - [ ] Select USB-C connector type (PCB mount vs. cable)
- [ ] **Wiring Schematic**
    - [ ] Map I2C pins for trackpads (SDA, SCL, VDD, GND)
    - [ ] Map UART/PIO pins for inter-half communication
    - [ ] Map switch matrix (Rows/Columns)
    - [ ] Power rail planning (3.3V regulation)
- [ ] **Firmware Strategy**
    - [ ] Decide on Framework (Rust/Embassy, QMK, or ZMK)
    - [ ] Implement I2C driver for trackpad
    - [ ] Implement "Algorithmic Lift" detection logic

## Phase 2: Mechanical Design - CAD (The "Body")
- [ ] **Plate Design (FreeCAD)**
    - [ ] Import Ergogen layout
    - [ ] Design switch retention tabs (ensure MX switches don't fall out)
    - [ ] Define M2 mounting hole positions
    - [ ] Create "Bridge" supports for the trackpad area
- [ ] **Case Design (FreeCAD)**
    - [ ] Design outer shell (based on Ergogen dimensions)
    - [ ] Design internal cavity (account for switch heights + PCB stack)
    - [ ] Design trackpad mounting system (standoffs/spacers)
    - [ ] Design USB-C port cutout and orientation
    - [ ] Design "Bezel" for trackpad
- [ ] **Assembly Hardware**
    - [ ] Specify M2 screw sizes
    - [ ] Decide on Heat-set inserts vs. Self-tapping screws

## Phase 3: Manufacturing & Testing
- [ ] **Test Prints**
    - [ ] Print 1:1 scale paper test (Complete)
    - [ ] Print 3D "Fit Test" for plate + switch stack
    - [ ] Print 3D "Fit Test" for trackpad + bezel
- [ ] **Production**
    - [ ] 3D Print final case parts (Material: PETG/ASA/PLA?)
    - [ ] Cut/Mill plate
    - [ ] Solder switch matrix and wiring
- [ ] **Final Assembly**
    - [ ] Assemble halves
    - [ ] Flash firmware
    - [ ] Final QA testing

---
*Status: Layout PoC Completed. Moving to Phase 1.*
