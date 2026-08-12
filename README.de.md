# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · Deutsch · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

Eine minimale Vorlage für plattformübergreifende Desktop-Anwendungen mit Tauri, React, TypeScript, Rsbuild, Bun und Biome.

## Überblick und Funktionen

Sie verbindet eine native Tauri-2-Shell mit Rust-Backend, React-Oberfläche, Rsbuild/Rspack, Bun und Biome. Sie ist eine Entwicklungsbasis, kein fertiges Endprodukt.

## Voraussetzungen

- Neueste stabile Bun-Version.
- Stabile Rust-Toolchain mit Cargo.
- Abhängigkeiten aus den offiziellen [Tauri-Voraussetzungen](https://v2.tauri.app/start/prerequisites/).

## Installation

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

Ändern Sie vor dem Produktstart Paketname, product name, bundle identifier, Rust-Crate-Metadaten, Autor und Symbole.

## Schnellstart und Verwendung

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri erstellt Pakete nur für die Host-Plattform; für alle Plattformen sind getrennte CI-Runner nötig.

## Konfiguration

`rsbuild.config.ts` steuert das Frontend, `src-tauri/tauri.conf.json` App und Pakete, `src-tauri/Cargo.toml` Rust und `biome.json` die Prüfungen. Der Server läuft auf `http://localhost:3000`, Produktionsassets liegen in `dist/`.

## Sicherheit, Mitwirkung und Lizenz

Ersetzen Sie die Beispiel-ID und prüfen Sie capabilities und CSP vor der Veröffentlichung. Melden Sie Schwachstellen über [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new). Erstellen Sie vor Stack-Änderungen ein Issue; PRs müssen `bun run check` und `bun run build` bestehen. [MIT-Lizenz](LICENSE).
