# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · 简体中文 · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

基于 Tauri、React、TypeScript、Rsbuild、Bun 和 Biome 的精简跨平台桌面应用模板。

## 概述与功能

模板结合 Tauri 2 原生外壳与 Rust 后端、React UI、Rsbuild/Rspack 构建、Bun 包管理及 Biome 检查。它是开发起点，并非可直接交付的终端产品。

## 要求

- 最新稳定版 Bun；
- 带 Cargo 的稳定 Rust toolchain；
- 官方 [Tauri prerequisites](https://v2.tauri.app/start/prerequisites/) 中列出的系统依赖。

## 安装

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

开始实际产品前，请替换包名、product name、bundle identifier、Rust crate 元数据、作者和图标。

## 快速开始与使用

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri 只为当前 host 平台构建；覆盖全部平台需要独立的 CI runners。

## 配置

`rsbuild.config.ts` 管理前端，`src-tauri/tauri.conf.json` 管理应用和打包，`src-tauri/Cargo.toml` 管理 Rust，`biome.json` 管理检查。开发地址为 `http://localhost:3000`，生产 assets 位于 `dist/`。

## 安全、贡献与许可证

发布前请替换示例标识符并审查 Tauri capabilities 和 CSP。通过 [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new) 私下报告漏洞。更改基础技术栈前请创建 issue；PR 必须通过 `bun run check` 和 `bun run build`。采用 [MIT 许可证](LICENSE)。
