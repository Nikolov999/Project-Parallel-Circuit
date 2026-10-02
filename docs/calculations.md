# Electrical Calculations

## Design values

| Quantity | Symbol | Value |
|---|---|---:|
| Supply voltage | `Vs` | 5 V |
| Assumed LED forward voltage | `Vf` | ~2 V |
| Branch resistance | `R1`, `R2` | 330 Ω |
| Approx. branch current | `I1`, `I2` | ~9.1 mA |
| Approx. total current | `Itotal` | ~18.2 mA |

## One branch

Each branch is a series combination of one resistor and one LED:

```text
+5 V -> 330 Ω -> LED -> GND
```

The complete branch is connected across the full 5 V supply.

### Resistor voltage

The LED is assumed to have an approximately 2 V forward voltage:

```text
Vr = Vs - Vf
Vr = 5 V - 2 V
Vr = 3 V
```

### Branch current

Using Ohm's law:

```text
I = V / R
I = 3 V / 330 Ω
I = 0.00909 A
I ≈ 9.1 mA
```

The resistor and LED are in series inside the branch, so the same current flows through both.

## Parallel behaviour

Both branches are connected between +5 V and GND, therefore both branches have the same supply voltage across them.

For nominally identical branches:

```text
I1 ≈ 9.1 mA
I2 ≈ 9.1 mA
```

Kirchhoff's Current Law gives the total source current:

```text
Itotal = I1 + I2
Itotal ≈ 9.1 mA + 9.1 mA
Itotal ≈ 18.2 mA
```

## Resistor power

For each resistor:

```text
P = V × I
P = 3 V × 0.00909 A
P ≈ 0.0273 W
```

The selected DIN0207 footprint corresponds to a common 0.25 W through-hole resistor form factor, giving significant power margin at the assumed operating point.

## Important assumption

The 2 V LED forward voltage is not a fixed universal value. Actual `Vf` depends on the installed LED and its operating conditions. The design calculation is therefore an approximation used to choose a sensible resistor value for the learning project.
