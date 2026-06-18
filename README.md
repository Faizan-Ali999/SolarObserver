# SolarObserver — Understand your Environment Effectively. Set any coordinates on Earth. Watch the Sun move. See your building's solar exposure in minutes.

Built a fully browser-based solar simulation tool that lets you visualize the Sun's true astronomical path for any location on Earth, any date, any timezone — all in real-time 3D.

**No backend. No installation. Just open and simulate.**

---

## 🚀 Live Demo
🔗 **https://faizan-ali999.github.io/SolarObserver/**

---

## 🌍 What it does
Drop in any coordinates (or search an address) and watch the Sun trace its actual trajectory across the sky **based on real astronomical calculations — not a fake circular orbit.** The simulation accounts for seasonal variation, latitude, and hemisphere, so a winter solstice in **Lahore** looks **completely different** from a summer solstice in **London.**

The 3D scene runs a modern villa with a full rooftop solar array mounted on visible steel frames. Shadows update in real time as the Sun moves. You can scrub through the full 24-hour day manually or **let it play at up to 1440× speed and watch an entire day pass in 60 seconds.**

---

## ✨ Core Features

* ☀️ **Accurate Solar Position Engine:** Computes azimuth, altitude, sunrise, solar noon, and sunset using the Jean Meeus low-precision algorithm (same core as the widely-used SunCalc library), accurate to within ~0.1°.
* 🏠 **Procedural 3D Scene:** A modern flat-roof villa with floor-to-ceiling glazing, entrance canopy, garage, rear pool, and a rooftop solar array on proper steel mounting frames — all built procedurally in Three.js.
* 📐 **Solar Panel Analysis:** Live analytics tracking incidence angle, daily exposure efficiency, estimated kWh output, and color-coded panel performance feedback (green / amber / red).
* 🌒 **Dynamic Shadow Casting:** Real-time shadow casting with physically soft edges (PCF shadow maps) that shift direction and length accurately across the day.
* 🌍 **Global Location Search:** Powered by OpenStreetMap Nominatim geocoding — type any city or address to load its exact coordinates instantly.
* 📅 **Seasonal Comparison Mode:** Overlay Spring Equinox, Summer Solstice, and Winter Solstice sun trajectories simultaneously to visualize how dramatically the solar path changes across the year.
* 🔥 **Solar Heatmap Overlay:** Visualize cumulative ground-level solar exposure across the site as a color-coded heat gradient (toggle via the top bar).
* 🔄 **Full Orbit Camera:** Free drag, zoom, and overhead perspective — drag all the way over the top to watch the sun arc from above.
* 🎨 **Futuristic Glassmorphic UI:** Dark-themed analytics dashboard with live readouts for altitude, azimuth, day length, efficiency %, sunrise/sunset times, and estimated daily kWh — plus a dynamic timeline bar that repositions sunrise/sunset markers for your exact location.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| 3D Rendering | Three.js r128 + WebGL |
| Tone Mapping | ACES Filmic (built into Three.js) |
| Shadow System | PCF Soft Shadow Maps (2048×2048) |
| Sky | Custom GLSL fragment shader |
| Solar Math | Jean Meeus algorithm (inline, no library) |
| Geocoding | OpenStreetMap Nominatim API |
| Fonts | Space Grotesk + Inter (Google Fonts) |
| Build Tools | None — single HTML file |

---

## 🧠 Why I Built This
Most solar tools are either oversimplified 2D diagrams or expensive desktop software. I wanted something architects, solar installers, students, and curious homeowners could open in a browser tab and immediately understand — ***how does the sun actually move over my building, and when does my roof see the most light?***

---

## 🚀 Getting Started

This is a **single HTML file with no build step.** Just clone and open.

```bash
git clone https://github.com/yourusername/SolarObserver.git
cd SolarObserver
```

Then open `index.html` directly in any modern browser (Chrome, Firefox, Edge, Safari).

> **Note:** The geocoding search requires an internet connection to call the OpenStreetMap API. Everything else runs fully offline.

---

## 🗺️ Roadmap


* [ ] AI-Powered Orientation Advisor — recommend optimal panel angle and building rotation for your latitude
* [ ] Annual Yield Engine — month-by-month historical energy yield breakdowns
* [ ] PDF Export — generate shadow study reports for architectural presentations
* [ ] GIS Map Integration — load real-world buildings from OpenStreetMap via CesiumJS / Mapbox
---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome. Feel free to open an issue or submit a PR.

---

*Built with Three.js and a lot of trigonometry.*
