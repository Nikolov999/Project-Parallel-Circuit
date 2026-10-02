# Design Notes

## Purpose

This project was created as a first complete KiCad exercise focused on understanding the relationship between circuit theory and physical PCB implementation.

The design deliberately keeps the electronics simple so that the complete workflow can be studied clearly:

```text
requirements
-> calculations
-> schematic
-> ERC
-> footprints
-> PCB placement
-> routing
-> Edge.Cuts
-> silkscreen
-> DRC
-> PCB/schematic parity
-> 3D inspection
```

## Net structure

The PCB source defines these principal nets:

### +5V

- J1 pad 1
- R1 pad 1
- R2 pad 1

### Branch 1 internal net

- R1 pad 2
- D1 pad 2 (anode)

### Branch 2 internal net

- R2 pad 2
- D2 pad 2 (anode)

### GND

- J1 pad 2
- D1 pad 1 (cathode)
- D2 pad 1 (cathode)

## LED polarity

The KiCad LED symbol and chosen footprint use:

```text
Pad 1 = K = cathode
Pad 2 = A = anode
```

The intended path is therefore:

```text
+5 V -> resistor -> LED anode -> LED cathode -> GND
```

## PCB implementation

Current source data:

- KiCad generator version: 10.0
- PCB thickness: 1.6 mm
- Board outline: 102 mm × 42 mm
- Routing: front copper only
- Track width: 0.20 mm
- Through-hole components
- No vias
- Top silkscreen includes project name, 5V/GND, resistor values, and LED labels

The large physical spacing is intentional for the first project: it makes the two parallel branches and their routing visually easy to inspect.
