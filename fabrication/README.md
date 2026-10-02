# Fabrication Outputs

This directory contains the manufacturing outputs generated from the final KiCad PCB revision.

## Gerbers

`gerbers/` contains:

- `Project-Parallel-Circuit-F_Cu.gbr`
- `Project-Parallel-Circuit-B_Cu.gbr`
- `Project-Parallel-Circuit-F_Mask.gbr`
- `Project-Parallel-Circuit-B_Mask.gbr`
- `Project-Parallel-Circuit-F_Silkscreen.gbr`
- `Project-Parallel-Circuit-B_Silkscreen.gbr`
- `Project-Parallel-Circuit-Edge_Cuts.gbr`
- `Project-Parallel-Circuit-job.gbrjob`

## Drill files

`drill/` contains:

- `Project-Parallel-Circuit-PTH.drl`
- `Project-Parallel-Circuit-NPTH.drl`

The PTH file contains the plated through-holes used by J1, R1, R2, D1, and D2. The NPTH file is intentionally empty because this revision contains no non-plated mechanical holes.

## Manufacturing ZIP

`Project-Parallel-Circuit-Gerbers.zip` contains the Gerber and drill files together for convenient upload to a PCB manufacturer.

## Verification

The exported data was checked for basic layer separation:

- `Edge_Cuts` contains only the closed board profile.
- `F.Cu` contains the front copper routing and through-hole pads.
- `B.Cu` contains through-hole pad copper and no copied front-side routing.
- solder-mask outputs contain the expected pad openings.
- the front silkscreen contains the board labels and component markings.
- the PTH drill file contains 10 component holes.

Always inspect the manufacturing ZIP in the PCB manufacturer's Gerber viewer before ordering boards.
