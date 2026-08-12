# Desktop Boilerplate

[English](README.md) · Español · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

Una plantilla mínima para aplicaciones de escritorio multiplataforma con Tauri, React, TypeScript, Rsbuild, Bun y Biome.

## Descripción y funciones

Combina una shell nativa Tauri 2 con backend Rust, interfaz React, compilación Rsbuild/Rspack, paquetes con Bun y controles Biome. Es una base de desarrollo, no un producto final.

## Requisitos

- Última versión estable de Bun.
- Toolchain estable de Rust con Cargo.
- Dependencias de los [requisitos oficiales de Tauri](https://v2.tauri.app/start/prerequisites/).

## Instalación

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

Antes de crear un producto, cambie el nombre del paquete, product name, bundle identifier, metadatos del crate Rust, autor e iconos.

## Inicio rápido y uso

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri genera paquetes solo para la plataforma host; todas las plataformas requieren runners CI separados.

## Configuración

`rsbuild.config.ts` configura el frontend; `src-tauri/tauri.conf.json`, la aplicación y sus paquetes; `src-tauri/Cargo.toml`, Rust; y `biome.json`, el análisis. El servidor usa `http://localhost:3000` y los assets de producción están en `dist/`.

## Seguridad, contribución y licencia

Cambie el identificador de ejemplo y revise capabilities y CSP antes de distribuir. Informe vulnerabilidades mediante [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new). Abra un issue antes de cambiar el stack base; los PR deben superar `bun run check` y `bun run build`. [Licencia MIT](LICENSE).
