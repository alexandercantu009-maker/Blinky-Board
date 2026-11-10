# Blinky Board – Cybertruck Edition

A blinky board I designed in KiCad for Hack Club Twisted. A 555 timer clocks a CD4017 counter, which lights 10 LEDs one after another along the truck's body. The board is shaped like a Cybertruck, with wheels and window art on the silkscreen.

<img src="Blinky%20Board.png" alt="3D view of the Blinky Board" width="700">

## Schematic

<img src="schematic.png" alt="Schematic of the Blinky Board" width="700">

## How it works
- The NE555P runs as an astable oscillator. The 50 kΩ potentiometer (RV2) changes the speed.
- Each clock pulse moves the CD4017 to its next output (Q0 to Q9), so the 10 LEDs light in sequence.
- Power comes from a 9 V battery on a battery clip, plugged into the 2-pin header J1 (red wire to pin 1 = positive, black wire to pin 2 = GND).

## Bill of materials

| Component | Ref | Qty | Unit cost | Line cost | Buy |
|---|---|---|---|---|---|
| 1 µF 50 V electrolytic capacitor | C1 | 1 | $0.025 | $0.02 | [C62934](https://www.lcsc.com/product-detail/C62934.html) |
| 0.01 µF (10 nF) capacitor | C2 | 1 | $0.036 | $0.04 | [C249157](https://www.lcsc.com/product-detail/C249157.html) |
| 5 mm LED | D1-D10 | 10 | $0.024 | $0.24 | [C2895480](https://www.lcsc.com/product-detail/C2895480.html) |
| 2-pin 2.54 mm power header | J1 | 1 | $0.013 | $0.01 | [C492401](https://www.lcsc.com/product-detail/C492401.html) |
| 1 kΩ resistor | R1 | 1 | $0.007 | $0.01 | [C713997](https://www.lcsc.com/product-detail/C713997.html) |
| 470 Ω resistor | R2 | 1 | $0.010 | $0.01 | [C58592](https://www.lcsc.com/product-detail/C58592.html) |
| 50 kΩ trimmer potentiometer | RV2 | 1 | $0.178 | $0.18 | [C118912](https://www.lcsc.com/product-detail/C118912.html) |
| NE555P timer (DIP-8) | U1 | 1 | $0.228 | $0.23 | [C46749](https://www.lcsc.com/product-detail/C46749.html) |
| CD4017BE counter (DIP-16) | U2 | 1 | $0.519 | $0.52 | [C34519](https://www.lcsc.com/product-detail/C34519.html) |
| 9 V battery clip (off-board, plugs into J1) | – | 1 | $0.160 | $0.16 | [Tayda A-5266](https://www.taydaelectronics.com/connectors-sockets/battery-connectors-holders/9v-9-volt-battery-clip-connector-snap-black-color.html) |
| **Total** | | | | **$1.42** | |

Prices are approximate LCSC listings (the battery clip is from Tayda) for one board's worth of parts. The 9 V battery itself is not in the BOM, so any standard 9 V battery works. LCSC sells some parts in minimum quantities, so an actual order costs more.

The same list, with footprints and part numbers, is in [`BOM.csv`](BOM.csv).

## Files
- `Blinky Board.kicad_pro`, `.kicad_sch`, `.kicad_pcb`: KiCad project, schematic, and PCB
- `Gerbers.zip`: manufacturing files
- `BOM.csv`: bill of materials with costs and links
- `Blinky Board.png`: 3D render
- `schematic.png`: schematic image
