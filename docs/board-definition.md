# Board Definition

## Project

**Project-Parallel-Circuit**

## Design targets

| Item | Value |
|---|---|
| Supply voltage | 5 V DC |
| Outputs | 2 LED indicators |
| Topology | Two parallel branches |
| Target LED current | Approximately 9 mA per LED |
| Current-limiting resistors | 330 Ω each |
| Input connector | 2-pin, 2.54 mm through-hole header |
| PCB type | 2-layer |
| Board thickness | 1.6 mm |

Each branch contains one 330 Ω resistor and one LED in series. The two complete resistor/LED branches are connected in parallel between +5 V and GND.
