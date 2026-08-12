# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · Italiano · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

Un template minimo per applicazioni desktop multipiattaforma con Tauri, React, TypeScript, Rsbuild, Bun e Biome.

## Panoramica e funzionalità

Unisce una shell nativa Tauri 2 con backend Rust, interfaccia React, build Rsbuild/Rspack, Bun e controlli Biome. È una base di sviluppo, non un prodotto pronto per l’utente.

## Requisiti

- Ultima versione stabile di Bun.
- Toolchain Rust stabile con Cargo.
- Dipendenze indicate nei [prerequisiti Tauri](https://v2.tauri.app/start/prerequisites/).

## Installazione

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

Prima di creare un prodotto cambiare nome del pacchetto, product name, bundle identifier, metadati del crate Rust, autore e icone.

## Avvio rapido e utilizzo

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri crea pacchetti solo per la piattaforma host; per tutte le piattaforme servono runner CI separati.

## Configurazione

`rsbuild.config.ts` configura il frontend, `src-tauri/tauri.conf.json` app e pacchetti, `src-tauri/Cargo.toml` Rust e `biome.json` i controlli. Il server usa `http://localhost:3000`; gli asset di produzione sono in `dist/`.

## Sicurezza, contributi e licenza

Sostituire l’ID di esempio e verificare capabilities e CSP prima della distribuzione. Segnalare vulnerabilità con [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new). Aprire una issue prima di cambiare lo stack; le PR devono superare `bun run check` e `bun run build`. [Licenza MIT](LICENSE).
