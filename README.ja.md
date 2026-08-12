# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · 日本語 · [한국어](README.ko.md)

---

Tauri、React、TypeScript、Rsbuild、Bun、Biomeを使用した最小構成のクロスプラットフォームDesktopアプリテンプレートです。

## 概要と機能

Tauri 2ネイティブシェルとRust backend、React UI、Rsbuild/Rspack、Bun、Biomeを統合します。開発の土台であり、配布可能な完成品ではありません。

## 要件

- 最新安定版Bun
- Cargoを含む安定版Rust toolchain
- 公式[Tauri prerequisites](https://v2.tauri.app/start/prerequisites/)に記載されたシステム依存関係

## インストール

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

実際の製品を始める前に、package name、product name、bundle identifier、Rust crate metadata、author、iconsを変更してください。

## クイックスタートと使用方法

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauriは現在のhost platform向けのみを構築します。全platformには個別のCI runnersが必要です。

## 設定

`rsbuild.config.ts`はfrontend、`src-tauri/tauri.conf.json`はappとpackage、`src-tauri/Cargo.toml`はRust、`biome.json`は検査を設定します。Dev serverは`http://localhost:3000`、production assetsは`dist/`です。

## セキュリティ、貢献、ライセンス

配布前にsample identifierを変更し、Tauri capabilitiesとCSPを確認してください。脆弱性は[GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new)へ報告してください。基本stack変更前にissueを作成し、PRは`bun run check`と`bun run build`を通過させてください。[MIT License](LICENSE)。
