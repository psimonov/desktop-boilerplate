# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · Français · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

Un modèle minimal d’application desktop multiplateforme avec Tauri, React, TypeScript, Rsbuild, Bun et Biome.

## Présentation et fonctionnalités

Il associe une enveloppe native Tauri 2 et un backend Rust à une interface React, une build Rsbuild/Rspack, Bun et Biome. C’est une base de développement, pas un produit prêt à distribuer.

## Prérequis

- Dernière version stable de Bun.
- Toolchain Rust stable avec Cargo.
- Dépendances indiquées dans les [prérequis Tauri](https://v2.tauri.app/start/prerequisites/).

## Installation

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

Avant de créer un produit, remplacez le nom du paquet, product name, bundle identifier, les métadonnées du crate Rust, l’auteur et les icônes.

## Démarrage et utilisation

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri ne construit que pour la plateforme hôte ; des runners CI séparés sont requis pour toutes les plateformes.

## Configuration

`rsbuild.config.ts` configure le frontend, `src-tauri/tauri.conf.json` l’application et ses paquets, `src-tauri/Cargo.toml` Rust, et `biome.json` l’analyse. Le serveur utilise `http://localhost:3000` et les assets de production se trouvent dans `dist/`.

## Sécurité, contribution et licence

Remplacez l’identifiant d’exemple et vérifiez capabilities et CSP avant distribution. Signalez les vulnérabilités via [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new). Ouvrez une issue avant de modifier le stack ; les PR doivent réussir `bun run check` et `bun run build`. [Licence MIT](LICENSE).
