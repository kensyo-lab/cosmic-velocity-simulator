# 🚀 Cosmic Velocity Simulator

**日本語版 → [README.md](README.md)**

An interactive orbital mechanics simulator that runs entirely in your browser.  
No external libraries — a single HTML file is all you need.

![simulator screenshot](screenshot.png)

---

## ✨ Features

- **5 simultaneous orbital trajectories**
  - 4.0 km/s — Suborbital (impact trajectory)
  - 7.9 km/s — First cosmic velocity (circular orbit)
  - 9.5 km/s — Elliptical orbit (bound state)
  - 11.2 km/s — Second cosmic velocity (escape trajectory)
  - Custom — freely adjustable from 1 to 20 km/s via slider
- **Real-time Energy Monitor**
  - Live bar display of Kinetic Energy (KE), Gravitational Potential (PE), and Total Energy (E)
  - Color-coded "bound / escape" state based on the sign of total energy
- **Auto zoom-out** — camera follows the escaping body as it recedes
- **Start / Pause / Reset** controls
- Simulation speed slider

---

## 🔭 Physics Background

| Velocity | Orbit type | Total energy E |
|----------|-----------|----------------|
| v < v₁ (7.9 km/s) | Impact trajectory | E < 0 (falls back) |
| v = v₁ | Circular orbit (first cosmic velocity) | E < 0 (minimum bound) |
| v₁ < v < v₂ | Elliptical orbit | E < 0 (bound state) |
| v = v₂ (11.2 km/s) | Escape trajectory (second cosmic velocity) | E = 0 |
| v > v₂ | Hyperbolic trajectory | E > 0 (unbound) |

### Energy equations

```
Kinetic energy:            KE = ½mv²
Gravitational potential:   PE = −GMm/r
Total mechanical energy:   E  = KE + PE
```

- **E < 0** → Bound orbit (circular or elliptical)  
- **E ≥ 0** → Escape trajectory (parabolic or hyperbolic)

The **vertical line at the center of each energy bar represents E = 0**.  
Slowly move the custom velocity slider near 11.2 km/s to watch the total energy bar cross zero and turn orange in real time.

---

## 🚀 Getting Started

### Run locally

```bash
git clone https://github.com/YOUR_USERNAME/cosmic-velocity-simulator.git
cd cosmic-velocity-simulator
open cosmic_velocity_simulator.html        # macOS
start cosmic_velocity_simulator.html       # Windows
xdg-open cosmic_velocity_simulator.html   # Linux
```

### Deploy with GitHub Pages

Go to **Settings → Pages → Source**, set it to the `main` branch root,  
and your simulator will be live at:

```
https://YOUR_USERNAME.github.io/cosmic-velocity-simulator/cosmic_velocity_simulator.html
```

---

## 🎮 Controls

| Control | Description |
|---------|-------------|
| ▶ Start | Begin the simulation |
| ⏸ Pause | Pause (click Start again to resume) |
| ⏮ Reset | Reset everything to the initial state |
| Sim speed slider | Control how fast time progresses (1–100) |
| Custom velocity slider | Set the initial speed of the purple trajectory (1–20 km/s) |

---

## 🛠 Technical Details

| Item | Detail |
|------|--------|
| Languages | HTML / CSS / Vanilla JavaScript |
| Dependencies | None (zero external libraries) |
| Physics | 4-step sub-step Euler integration (RK4-equivalent) |
| Rendering | Canvas 2D API |
| Browser support | Chrome / Firefox / Safari / Edge (all modern browsers) |

---

## 📁 Repository Structure

```
cosmic-velocity-simulator/
├── cosmic_velocity_simulator.html  # The simulator — fully self-contained
├── README.md                       # Japanese documentation
└── README_en.md                    # This file
```

---

## 💡 Educational Use Cases

- Visualizing why **orbital velocity** is not about "going up" but about going *sideways fast enough*
- Demonstrating the **virial theorem**: for a bound orbit, |PE| = 2 × KE on average
- Showing intuitively why **escape velocity** is √2 times the circular orbital velocity
- Classroom supplement for introductory orbital mechanics or astrophysics

---

## 📝 License

MIT License — free to use, modify, and redistribute for any purpose, including education and research.

---

## 👤 Author

**Kensho**  
- Niconico: [窮理学 (Kyūrigaku)](https://www.nicovideo.jp/) — Physics & Space science series  
- GitHub: [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)
