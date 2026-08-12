# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · Português · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

Um template mínimo para aplicações desktop multiplataforma com Tauri, React, TypeScript, Rsbuild, Bun e Biome.

## Visão geral e recursos

Combina uma shell nativa Tauri 2 com backend Rust, interface React, build Rsbuild/Rspack, pacotes via Bun e verificações Biome. É uma base de desenvolvimento, não um produto final.

## Requisitos

- Última versão estável do Bun.
- Toolchain Rust estável com Cargo.
- Dependências dos [pré-requisitos oficiais do Tauri](https://v2.tauri.app/start/prerequisites/).

## Instalação

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

Antes de iniciar um produto, altere nome do pacote, product name, bundle identifier, metadados do crate Rust, autor e ícones.

## Início rápido e uso

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri compila apenas para a plataforma host; todas as plataformas exigem runners CI separados.

## Configuração

`rsbuild.config.ts` configura o frontend; `src-tauri/tauri.conf.json`, o aplicativo e pacotes; `src-tauri/Cargo.toml`, Rust; e `biome.json`, as verificações. O servidor usa `http://localhost:3000` e os assets de produção ficam em `dist/`.

## Segurança, contribuição e licença

Troque o identificador de exemplo e revise capabilities e CSP antes de distribuir. Relate vulnerabilidades por [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new). Abra uma issue antes de mudar o stack; PRs devem passar `bun run check` e `bun run build`. [Licença MIT](LICENSE).
