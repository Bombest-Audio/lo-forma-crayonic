# Lo-Forma: Crayonic Edition 🎛️🖍️  
*A lo-fi additive synth you can build, bend, and color outside the lines.*  
  
Lo-Forma: **Crayonics Edition** is an open-source hardware + firmware project for building a **lo-fi additive synthesizer** with a playful, “crayonic” personality: gritty harmonics, charming aliasing, and musical imperfection on purpose.  
  
This project is designed as a **tutorial series** and a **shareable reference build**: schematic → breadboard → PCB → enclosure, with code and audio demos along the way.  
  
## What it is  
- **Additive synthesis core** (harmonics + partial control)    
- **Lo-fi character** by design (intentional limitations + vibe controls)    
- **Hands-on hardware build** you can actually finish    
- **Firmware + DSP playground** for experimenting with sound    
  
## Goals  
- Make something that sounds *alive* without needing a DAW.    
- Keep the build approachable: each stage is usable even if you stop early.    
- Document everything like a lab notebook: decisions, mistakes, fixes, revisions.    
  
## Hardware + system overview (high level)  
- Microcontroller-based synth engine (targeting the Raspberry Pi Pico / Pico H class)    
- I2S audio output path to a DAC module (clean enough, still vibey)    
- Physical controls for harmonic shaping, tone, and performance macros    
- Optional extras: CV-ish control ideas, MIDI input, preset saving, display support    
  
> Exact parts and wiring live in `/hardware` and `/docs` as the design stabilizes.  
  
## Repo layout  
- `hardware/` – schematics, PCB files, wiring diagrams, BOM    
- `firmware/` – synth engine + DSP + IO (controls, MIDI, etc.)    
- `docs/` – build guide, calibration, troubleshooting, design notes    
- `examples/` – demo patches, audio examples, presets    
- `tools/` – helper scripts, audio test tools, measurement utilities    
  
## Build stages (the intended journey)  
1. **Breadboard prototype** – prove the sound engine + audio output    
2. **Perfboard / wiring harness** – stabilize the circuit + controls    
3. **PCB revision** – make it reproducible    
4. **Enclosure** – finish it like a real instrument    
  
## Documentation philosophy  
This repo is meant to be readable by:  
- builders who like solder smoke and progress    
- firmware folks who want to tweak DSP parameters    
- curious humans who want to learn synthesis by touching it    
  
## Contributing  
PRs are welcome—especially:  
- BOM improvements + alternate parts    
- calibration/test procedures    
- sound demos + patch ideas    
- PCB review and layout suggestions    
  
## License  
TBD (recommended: **CERN-OHL-P** for hardware + **MIT** for firmware), unless we decide otherwise.  
  
## Credits / Inspiration  
Crayonics Edition is inspired by lo-fi synthesis culture and the idea that instruments should be *fun*, not fragile.  
  
---  
  
### Status  
**Early build + documentation phase.**    
Expect rapid iteration and messy notes (the good kind).
