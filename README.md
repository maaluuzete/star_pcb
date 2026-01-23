# LED Star Chaser
This is a small and fun electronics project:  
a star-shaped LED chaser built using a classic NE555 timer and two CD4017 decade counters.
The idea was to mix simple logic, old-school components, and a creative PCB shape into something that’s both educational and nice to look at. It’s not meant to be complicated, just satisfying to build and fun to watch!.

## How it works

### NE555 Timer (Astable Oscillator)

The NE555 is configured as an astable oscillator, meaning it continuously generates a square wave.
- The frequency is set by:
  - R1 (1 kΩ);
  - RV1 (50 kΩ potentiometer);
  - C1/C2 (timing capacitors).

By turning the potentiometer, you can make the LEDs chase faster or slower. The output of the 555 goes directly to the clock inputs of the CD4017s.
---

### CD4017 Decade Counters

Two **CD4017** ICs handle the LED sequencing.
- Each 4017 turns on one output at a time (Q0->Q9);
- Each output drives one LED;
- After the last LED, the sequence resets and starts again.
This creates the classic running-light!

---

## Project Structure

```
star_pcb/
├── images/
│ └── star_3d.png
│ └── star_pcb.png
│ └── star_schematic.png
├── kicad/
│ └── gerbers.zip
│ └── starpcb.kicad_pcb
│ └── starpcb.kicad_pro
│ └── starpcb.kicad_sch
├── LICENSE
├── notes.md
└── README.md
```