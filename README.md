<div align="center">

<img src="https://cdn2.steamgriddb.com/logo/5f5c19fa671886b5f7f205d541157c1f.png" width="350" alt="Duke Nukem 3D Logo">

# ☢️ DUKE NUKEM 3D: WEB PORT ☢️
### *Run the classic 90s FPS natively in your browser using WebAssembly.*

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)]()
[![Platform](https://img.shields.io/badge/platform-WebAssembly-orange.svg)]()
[![License](https://img.shields.io/badge/license-GPLv3-blue.svg)]()

> *"It's time to kick ass and chew bubble gum... and I'm all out of gum."*

</div>

---

## 🚀 Overview

This repository is a native web port of **Duke Nukem 3D**. Instead of using slow emulation layers like DOSBox, this project compiles the original C++ source code directly into **WebAssembly (WASM)** so it runs fast and clean right inside your browser.

### Key Features
* **Zero Emulation:** Direct C++ to WASM compilation.
* **Hardware Acceleration:** WebGL-powered rendering.
* **Asset Loading:** Mounts your `DUKE3D.GRP` file directly into memory.

---

## ⚙️ How It Works

<pre>
[ C++ Source Code ] 
       │
       ▼ (Emscripten Compiler)
[ WebAssembly (WASM) ] ──> [ HTML5 Canvas / WebGL ]
       │
[ DUKE3D.GRP Assets ]  ──> [ Virtual File System ]
</pre>

---

## 📦 Requirements

You must provide your own legally obtained game assets to run this port.
* **Asset File:** `DUKE3D.GRP` (from the original CD, Atomic Edition, or Steam release).
* **Browser:** Any modern browser supporting WebAssembly and WebGL.

---

## 🛠️ Building the Port

To compile the source code using Emscripten:

```bash
emcc src/*.cpp -O3 -s USE_SDL=2 -s USE_SDL_MIXER=2 -s ALLOW_MEMORY_GROWTH=1 --preload-file assets/DUKE3D.GRP@/DUKE3D.GRP -o index.html
```

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## 🏆 Credits & Acknowledgments

* **3D Realms & Apogee Software** for creating Duke Nukem 3D.
* **Ken Silverman** for writing the legendary Build Engine.
* **The Emscripten Project** for making C-to-WebAssembly compilation possible.

---

## 🛡️ License

Distributed under the GNU General Public License v3.0. See `LICENSE` for details.

<div align="center">

***

*“Hail to the King, baby.”*  
**Built with pure adrenaline and WebAssembly.**

</div>
