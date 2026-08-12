# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · 한국어

---

Tauri, React, TypeScript, Rsbuild, Bun, Biome을 사용하는 최소 구성의 크로스 플랫폼 desktop application template입니다.

## 개요와 기능

Tauri 2 native shell과 Rust backend, React UI, Rsbuild/Rspack build, Bun package management, Biome checks를 결합합니다. 개발 출발점이며 배포 가능한 완제품은 아닙니다.

## 요구 사항

- 최신 안정 버전 Bun
- Cargo를 포함한 안정 Rust toolchain
- 공식 [Tauri prerequisites](https://v2.tauri.app/start/prerequisites/)의 시스템 의존성

## 설치

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

실제 제품을 시작하기 전에 package name, product name, bundle identifier, Rust crate metadata, author, icons를 변경하세요.

## 빠른 시작과 사용법

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri는 현재 host platform용만 빌드합니다. 모든 platform을 지원하려면 별도 CI runners가 필요합니다.

## 설정

`rsbuild.config.ts`는 frontend, `src-tauri/tauri.conf.json`은 app과 packages, `src-tauri/Cargo.toml`은 Rust, `biome.json`은 checks를 설정합니다. Dev server는 `http://localhost:3000`, production assets는 `dist/`에 있습니다.

## 보안, 기여 및 라이선스

배포 전에 sample identifier를 바꾸고 Tauri capabilities와 CSP를 검토하세요. 취약점은 [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new)로 보고하세요. 기본 stack 변경 전 issue를 만들고 PR은 `bun run check`와 `bun run build`를 통과해야 합니다. [MIT License](LICENSE).
