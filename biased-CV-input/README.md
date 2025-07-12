# patch_bits // biased-cv-input

**SDIY building block for clean CV-to-ADC conversion with potentiometer bias.**  
This tiny PCB lets you mix a unipolar 0–3.3V CV signal with a DC bias from a panel-mounted potentiometer, buffer it with a low-noise op-amp, and send it cleanly into your microcontroller’s ADC—perfect for applications like linear FM, CV-controlled modulation depths, and more.

[Schematic](./biased-CV-input.svg)

## 🔧 Features

- 📎 Mixes CV signal and knob-generated bias voltage
- 🎛️ Pot directly mounts to PCB for tight panel integration
- 🔌 Accepts unipolar PWM or CV input (0–3.3V range)
- 🧠 Buffered via TLV9061 (low-noise, rail-to-rail op amp)
- 🌊 AC-coupled output removes DC bias—ideal for FM signals
- 🔒 Input protection via Schottky diode and current-limiting resistor
- 🧷 Optional jumpers for jack normalization and CV detect

---

## 🧪 Use Case: Linear FM

This circuit is especially useful when you're feeding a sine wave or other modulator into an ADC for **linear frequency modulation**. The onboard AC coupling ensures **no DC bias slips through**, preserving pitch integrity and ensuring your FM stays clean and musically locked.

---

## 📦 Pinout (J2 Header)

| Pin | Signal        | Description                          |
|-----|---------------|--------------------------------------|
| 1   | +3.3V         | Power (shared with system 3.3V rail) |
| 2   | `JACK_DETECT` | Optional logic detect (pulled LOW when jack inserted) |
| 3   | `OUT`         | AC-coupled output to ADC input       |
| 4   | GND           | Ground                               |

---

## 🛠️ Panel Wiring

- Mount a standard 9mm 10k linear pot directly to the board.
- Wire `OUT` to any 3.3V-capable microcontroller ADC pin (e.g., RP2040).
- Send unipolar PWM or CV (0–3.3V) into the jack.
- Adjust bias with the pot to tune modulation range.
- Add optional logic via `JACK_DETECT` pin.

---

## 🧰 Specs

| Component     | Value / Notes                          |
|---------------|----------------------------------------|
| Op Amp        | TLV9061 (SOT-23-5, rail-to-rail)       |
| Potentiometer | 10k linear, 9mm panel mount            |
| Input Filter  | 100nF bypass cap (optional)            |
| AC Coupling   | 100nF ceramic cap to ground            |
| Output Resistor | 100Ω series for safety + filtering   |
| Diode         | BAT54S Schottky clamp to 3.3V/GND      |

---

## 🔓 License

This project is open-source under the **CERN-OHL-W** license.  
You’re free to remix, manufacture, and sell your own versions.  
If you do, give credit and consider supporting the original creator.

---

## 🧯 Safety Notes

This circuit is designed for **3.3V systems only**.  
Do **not** use with ±12V Eurorack signals without modification.

---

## 📸 Photos & Demos

> _(Coming soon)_

---

Part of the **patch_bits** series — SDIY building blocks.
