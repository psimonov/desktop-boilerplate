# Desktop Boilerplate

English · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

A minimal cross-platform desktop application starter built with Tauri, React, TypeScript, Rsbuild, Bun, and Biome.

## Overview

Desktop Boilerplate provides a small, understandable baseline for teams starting a native desktop application with a web UI and Rust host. It wires together development, production builds, Tauri packaging, type checking, and code-quality tooling without imposing an application architecture or UI framework.

This repository is a development template, not a ready-to-distribute end-user product.

## Features

- Tauri 2 native application shell with a Rust backend.
- React and TypeScript frontend.
- Rsbuild/Rspack development and production builds.
- Bun package management and script execution.
- Biome formatting and static analysis.
- Tauri packaging configuration for Windows, macOS, and Linux.

## Requirements

- Latest stable Bun.
- Stable Rust toolchain with Cargo.
- Platform-specific prerequisites required by Tauri 2.
- Windows, macOS, or Linux development environment supported by Tauri.

Follow the official [Tauri prerequisites](https://v2.tauri.app/start/prerequisites/) before running the desktop application. Linux system packages vary by distribution.

## Installation

Use this repository as a template or clone it, then install dependencies:

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

Rename the package, Tauri product name, bundle identifier, Rust crate, author metadata, and application icons before starting a real product.

## Quick start

Run the desktop application with hot reload:

```bash
bun run tauri:dev
```

Run only the frontend development server:

```bash
bun run dev
```

## Usage

Build the frontend:

```bash
bun run build
```

Create native platform packages:

```bash
bun run tauri:build
```

Run code-quality checks or formatting:

```bash
bun run check
bun run format
```

Tauri builds only for the current host platform. Producing installers for every target requires CI runners for Windows, macOS, and Linux.

## Configuration

- `rsbuild.config.ts` configures the frontend build and development server.
- `src-tauri/tauri.conf.json` configures the desktop application, bundle identifier, windows, frontend commands, and package targets.
- `src-tauri/Cargo.toml` defines the Rust crate and Tauri dependencies.
- `biome.json` defines formatting and static-analysis rules.

The default development server is `http://localhost:3000`, and production frontend assets are read from `dist/`.

## Project structure

```text
desktop-boilerplate/
├── public/
├── src/
├── src-tauri/
├── biome.json
├── bun.lock
├── package.json
├── rsbuild.config.ts
└── tsconfig.json
```

## Security

Replace the sample bundle identifier and review Tauri capabilities and content security policy before shipping a product. Report template vulnerabilities privately through [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new).

## Contributing

Open an issue before changing the baseline stack or introducing an opinionated application dependency. Pull requests should keep the template minimal and pass `bun run check` and `bun run build`.

## License

Distributed under the [MIT License](LICENSE).
