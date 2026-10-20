# RF Integrated Circuits (EE6320)

Design projects from **EE6320: RF Integrated Circuits** at IIT Madras (Jan–May 2026), taught by Prof. Sankaran Aniruddhan.

Course website: <https://www.ee.iitm.ac.in/vlsi/courses/ee6320_2026/start>

**Author:** N Yasho Srikar Adithya Reddy, B.Tech Electrical Engineering, IIT Madras

The four projects together form the building blocks of a **3.45–3.55 GHz direct-conversion transceiver front end**, all designed in **IBM 130 nm CMOS** with a **1.2 V** supply in Cadence Virtuoso (Spectre, ADE L). Inductors are modelled with finite Q (Q = 20 at 3.5 GHz; Q = 50 for the off-chip LNA gate inductor).

## Projects

**Project 1: Design of a differential cascoded common-source low noise amplifier for 3.45–3.55 GHz.**
→ [`LNA/`](LNA/)

**Project 2: Design of a double-balanced Gilbert cell mixer with I/Q outputs for a direct-conversion receiver (RF 3.45–3.55 GHz).** Includes the LNA + mixer cascade.
→ [`Mixer/`](Mixer/)

**Project 3: Design of a 6.9–7.1 GHz LC voltage-controlled oscillator with a divide-by-two quadrature divider (LO 3.45–3.55 GHz).**
→ [`VCO/`](VCO/)

**Project 4: Design of a differential power amplifier for 3.45–3.55 GHz.**
→ [`PA/`](PA/)

## Results at a glance

| Block | Key results (as reported) |
|---|---|
| **LNA** | Gain 30.551–31.478 dB, NF 1.819–1.859 dB, worst-case S11 −11.7292 dB, IIP3 −9.97 dBm, 525.36 µW |
| **Mixer** | Conversion gain 20.26 dB, SSB NF 10.643 dB, IIP2 68.46 dBm, IIP3 −4.0029 dBm, 0.782 mW |
| **LNA + Mixer** | Gain 39.017 dB, NF 2.22 dB, IIP3 −26.57 dBm, 1.401 mW |
| **VCO + Divider** | Phase noise −128.14 dBc/Hz @ 1 MHz (3500 MHz), tuning range 248 MHz, 3-bit coarse tuning, average KVCO 68 MHz, quadrature 0/90/180/270° LO outputs |
| **PA** | Output P1dB 13.06 / 13.058 / 13.0472 dBm, AM-PM ≤ 0.85°, voltage gain 4.354–4.357, 69.25 mW |

## Repository structure

```
LNA/     Project 1: report, figures, Cadence cells (ee6320_2026_lna, LNA_TB)
Mixer/   Project 2: report, figures, Cadence cells (ee6320_2026_mixer, mixer_tb)
VCO/     Project 3: report, figures, Cadence cells (ee6320_2026_vco, VCO_TB, VCO_Divider)
PA/      Project 4: report, figures, Cadence cells (ee6320_2026_pa, PA_TB)
```

Each folder's README has the full performance table, component values, design procedure and plots.

## A note on the process design kit

The Cadence cells reference IBM 130 nm devices. The foundry model files and design kit are **not** included in this repository. To re-simulate, you will need your own licensed access to the PDK and must update the model path in the simulation states.
