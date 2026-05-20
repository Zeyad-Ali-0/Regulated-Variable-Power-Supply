# ⚡ Regulated Variable Power Supply

[![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)](https://github.com/Zeyad-Ali-0/Regulated-Variable-Power-Supply)
[![Tool](https://img.shields.io/badge/Simulation-Multisim-yellow?style=flat-square)](https://github.com/Zeyad-Ali-0/Regulated-Variable-Power-Supply)
[![Module](https://img.shields.io/badge/Module-Intro%20to%20Electronic%20Systems%204FTC2028-orange?style=flat-square)](https://github.com/Zeyad-Ali-0/Regulated-Variable-Power-Supply)

---

## 👥 Team

| Gana Ahmed | Youssef Hussein | Mohamed Medhat | Zeyad Alaaeldin |
|---|---|---|---|

---

## 📌 Overview

A fully designed, simulated, and physically implemented **Regulated Variable Power Supply (RPS)** built on a PCB perfboard. Converts a **220V AC mains input** into a stable, regulated DC output at either **5V or 12V**, suitable for powering microcontrollers, sensors, and low-power digital circuits.

---

## 🔌 System Pipeline

```
[220V AC Mains]
      │
      ▼
[Step-Down Transformer]   ← reduces to low AC voltage
      │
      ▼
[Full-Bridge Rectifier]   ← converts AC → pulsating DC (4 diodes)
      │
      ▼
[Filter Capacitors]       ← smooths ripple (2200µF + 470µF)
      │
      ▼
[Voltage Regulators]      ← LM7805 (fixed 5V) / LM317 (adjustable 12V)
      │
      ▼
[Stable DC Output]        ← clean, regulated voltage
```

---

## 🧰 Components

| Component | Role |
|---|---|
| Transformer | Steps 220V AC down to safe low AC level |
| Full-Bridge Rectifier (4× diodes) | Converts both AC half-cycles to pulsating DC |
| 2200µF + 470µF Capacitors | Filter and smooth the rectified DC |
| 0.1µF Capacitors | High-frequency noise suppression |
| LM7805 Voltage Regulator | Fixed 5V output |
| LM317 Adjustable Regulator | Variable output (set to 12V via resistor divider) |
| Potentiometer | Fine voltage adjustment |
| Resistors | Set LM317 output voltage; protect components |
| Voltage Sensor | Monitors and verifies output voltage |

---

## 🛠️ Design Process

1. **Theoretical Design** — Circuit topology planned, component values calculated
2. **Simulation** — Full circuit simulated in Multisim to validate behaviour before build
3. **PCB Perfboard Implementation** — Components soldered onto perfboard with careful layout
4. **Testing** — Output voltage verified at both 5V and 12V under load conditions

---

## ⚠️ Safety Features

- **Protection diodes** — Prevent reverse current flow
- **High-rating resistors** — Limit current and protect downstream components
- **Filter capacitors** — Stabilise voltage and absorb transient surges
- **Voltage regulator thermal dissipation** — Regulators selected for safe operating range

---

## 📁 Repository Contents

| File | Description |
|---|---|
| `Multisim schematic` | Circuit simulation file |
| `Report.pdf` | Full project report with design justification |
| `Photos` | Perfboard implementation and component close-ups |

---

## 🔮 Future Improvements

- Add a digital voltmeter display for real-time output reading
- Implement a short-circuit protection fuse
- Design a custom PCB (replacing the perfboard) for a cleaner build
- Expand output range with additional regulator stages
