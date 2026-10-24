# 🕹️ PAC-MAN 3D: Arcade Remastered

![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=flat&logo=three.js)
![JavaScript](https://img.shields.io/badge/Language-Vanilla%20ES6+-yellow?style=flat&logo=javascript)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat)

A high-performance, fully 3D arcade remake of the legendary Pac-Man built from scratch with **Three.js** and procedural **Web Audio API** synthesizers. Features authentic ghost AI targeting algorithms, dynamic multiple camera perspectives, a persistent glassmorphism scoreboard, and a developer/admin debug panel.

---

## 🌟 Key Features

### 🎮 True-to-Arcade Ghost AI
Faithful recreation of the original 1980 arcade AI logic using grid-based targeting vectors and timed **Scatter ⇄ Chase** state machines:
- 🔴 **Blinky (Shadow)**: Direct targeter — relentlessly pursues Pac-Man's exact tile coordinates.
- 🌸 **Pinky (Speedy)**: Ambush predator — aims 4 tiles ahead of Pac-Man's trajectory.
- 🔷 **Inky (Bashful)**: Complex vector flanker — calculates target using doubled vector from Blinky through Pac-Man's forward offset.
- 🟠 **Clyde (Pokey)**: Cowardly proximity chaser — hunts Pac-Man until within 8 tiles, then retreats back to his scatter home corner.
- ⚡ **Frightened / Blue Phase**: Ghosts turn vulnerable with flashing warnings and dynamic score scaling ($200 \rightarrow 400 \rightarrow 800 \rightarrow 1600$).
- 👀 **Eaten / Eyes Mode**: Disembodied eyes pathfind directly back to the central ghost house to regenerate.

---

### 🎥 Dynamic Camera Modes (`C` key)
Seamlessly switch between multiple real-time camera perspectives:
1. **Third-Person Follow Cam**: Dynamic cinematic camera trailing Pac-Man through the neon corridors.
2. **Top-Down Classic Arcade**: Traditional isometric/overhead bird's-eye view of the full arena.
3. **Cinematic Free Orbit**: Smooth rotating showcase camera perfect for game over screens and demos.

---

### 🛠️ Developer & Admin Suite (`` ` `` or `~` key)
An interactive real-time control panel built for debugging, testing, and customization:
- **Real-Time Cheats**:
  - 🛡️ God Mode / Invulnerability
  - ❄️ Freeze Ghosts
  - 👻 Instant Frighten Mode Trigger
  - ⏩ Instant Level / Round Clear
  - ❤️ Extra Lives & Score Injection
- **Engine Tuning**:
  - Live velocity sliders for Pac-Man and ghost speeds.
  - Camera Field of View (FOV) adjustment.
- **3D AI Debug Visualizer**:
  - Projects colored 3D vector lines and ground markers showing real-time targeting coordinates for all 4 ghosts.
- **Audio Synthesizer Sandbox**:
  - Individual audition buttons for all procedural sound effects (Waka, Sirens, Eat Ghost, Death, Energizer).

---

### 🏆 Scoreboard & Hall of Fame (`H` key)
- Glassmorphism modal with local persistence via `localStorage`.
- Tracks player callsign/name, high scores, levels cleared, survival time, and dates.
- Dynamic reward badges for scoring milestones.
- Export and import capability via JSON for tournament leaderboards.

---

### 🔊 100% Procedural Audio Engine
- Zero external `.mp3` or `.wav` dependencies.
- Synthesized using the native **Web Audio API**:
  - Frequency-modulated sine sweeps for authentic "Waka-Waka" chomps.
  - Multi-tone oscillator sirens that change pitch during Frightened and Eyes modes.
  - Arpeggiated chromatic sequence for the iconic death tune.

---

## ⌨️ Controls

| Action | Keyboard Input | On-Screen / Touch |
| :--- | :--- | :--- |
| **Move Up** | `W` / `↑ Up Arrow` | Touch D-Pad Up / Swipe Up |
| **Move Down** | `S` / `↓ Down Arrow` | Touch D-Pad Down / Swipe Down |
| **Move Left** | `A` / `← Left Arrow` | Touch D-Pad Left / Swipe Left |
| **Move Right** | `D` / `→ Right Arrow` | Touch D-Pad Right / Swipe Right |
| **Switch Camera** | `C` | "Cam" HUD Button |
| **Open Admin Panel** | Backtick (`` ` `` / `~`) | "Admin" Gear Button |
| **Open Scoreboard** | `H` | "Scoreboard" Trophy Button |
| **Pause / Resume** | `P` / `Esc` | "Pause" Button |
| **Mute Audio** | `M` | Audio Toggle Button |

---

## 🚀 Getting Started

### Prerequisites
- Any modern web browser that supports **WebGL** and **Web Audio API** (Chrome, Firefox, Safari, Edge, Brave, Opera).
- No Node.js build steps or package installations are required.

### Running Locally
1. Clone or download this repository:
   ```bash
   git clone [https://github.com/your-username/pacman-3d-arcade.git](https://github.com/your-username/pacman-3d-arcade.git)
   cd pacman-3d-arcade
