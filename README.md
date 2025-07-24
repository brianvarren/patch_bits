# patch_bits

**SDIY building blocks.** Tiny helper boards that that make quick prototyping fun and easy.

---

## What is this?

A growing collection of hardware abstractions for recurring problems in mixed-signal synth DIY. My intent is to provide simple touch points: inputs, outputs, power, ground. Everything else should be refined, reliable boilerplate. Being fully open-hardware, these helpers can become reusable design blocks, to be implemented in larger custom synth PCBs or modules as you (or I) see fit.

---

## Philosophy

- Open-source hardware (CERN-OHL-W)
- Built for speed, not purity
- Easy to chain, mount, and mod

---

## A Note on Voltage & Signal Standards

For my personal builds, I decided some time ago to eschew Eurorack dual-rail power supplies and 10Vpp bipolar signals in favor of unipolar 0-3.3V DC-coupled MCU-friendly signals. I did this both out of frustration and laziness. My aim is to prototype quickly, learn in the process, and most of all, have fun. I found myself spending more time designing and debugging analog pre- and post- stages than I did designing the synths themselves. Some may argue that that is an important part of synth design; I can't argue. But, to me, a simplified, unipolar 3.3V signal format represents the freedom to explore without boundaries.

These helpers are designed to be compatible with both 3.3V and 5V systems. They may work with other single-rail voltages too (check the datasheets of the individual components).

Adapting to dual-rail supplies would require significant rework in most cases.

---

## Use it

- Build your own from the files
- Order from JLC
- Or [buy a prebuilt one](#) if you’re lazy or busy (no shame)

---

## License

CERN-OHL-W v2  
If you make changes and share them, cool. If you don’t, don’t sell them.
