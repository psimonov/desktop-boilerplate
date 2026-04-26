# 🖥️ Desktop Boilerplate (Cross-Platform)

A modern starter template for building cross-platform desktop applications using **React + Tauri + Rsbuild + Biome**.

---

## ⚙️ Tech Stack

- **Rsbuild** – fast build tool powered by Rspack
- **React + TypeScript** – frontend UI layer
- **Tauri** – lightweight native desktop runtime (Windows / macOS / Linux)
- **Biome** – ultra-fast formatter and linter (alternative to ESLint + Prettier)

---

## 📦 Requirements

Before starting, make sure you have installed:

- Node.js or Bun (Bun is used in this project)
- Bun → https://bun.sh
- Rust toolchain → https://rustup.rs
- Platform-specific Tauri dependencies → https://tauri.app/start/prerequisites

---

## 🚀 Project Setup

### 1. Create project with Rsbuild

```bash
bun create rsbuild@latest
```

Select options:

* Project name: `desktop-boilerplate`
* Framework: `React`
* Language: `TypeScript`
* Additional tools: `Biome`
* Optional skills: `None`

### 2. Install dependencies

```bash
bun install
```

### 3. Add Tauri CLI

```bash
bun add -D @tauri-apps/cli@latest
```

### 4. Initialize Tauri

```bash
bun tauri init
```

Configuration:

* App name: `desktop-boilerplate`
* Window title: `Desktop Boilerplate`
* Web assets location: `../dist`
* Dev server URL: `http://localhost:3000`
* Frontend dev command: `bun run dev`
* Frontend build command: `bun run build`

---

## 🧪 Development

Start frontend

```bash
bun dev
```

Start Tauri app

```bash
bun tauri dev
```

---

📦 Production Build

```bash
bun build
```

```bash
bun tauri build
```

---

## 📁 Project Structure

```text
desktop-boilerplate/
├── src/                 # React frontend
├── src-tauri/           # Tauri (Rust backend)
│   ├── src/
│   ├── Cargo.toml
│   └── tauri.conf.json
├── public/
├── rsbuild.config.ts
├── package.json
└── biome.json
```

---

## 🧹 Code Quality

Run Biome checks:

```bash
bunx biome check .
```

Format code:

```bash
bunx biome format .
```

---

## 🧠 Notes

### Tauri configuration

Make sure:
* `dist` output matches Rsbuild build output
* dev server URL matches `http://localhost:3000`

---

### Common issues

Blank window in Tauri

* Check devPath in tauri.conf.json
* Ensure frontend dev server is running


Frontend not loading

* Verify dev server URL matches configuration


Rust build issues

```bash
rustup update
```

---

## 🎯 Purpose

This boilerplate is designed for:

* Cross-platform desktop MVPs
* Internal tools
* Lightweight enterprise utilities
* Electron alternatives with lower resource usage

---

## 🧩 Possible Improvements

* State management (Zustand / Redux Toolkit)
* UI kit integration (shadcn/ui or custom design system)
* Auto-updater for Tauri
* IPC abstraction layer
* CI/CD pipelines (GitHub Actions)
* Multi-platform release automation
