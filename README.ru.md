# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · Русский · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

Минимальный шаблон кроссплатформенного desktop-приложения на Tauri, React, TypeScript, Rsbuild, Bun и Biome.

## Обзор и возможности

Шаблон объединяет нативную оболочку Tauri 2 с Rust-бэкендом, React-интерфейс, сборку Rsbuild/Rspack, управление пакетами через Bun и проверки Biome. Это основа для разработки, а не готовый пользовательский продукт.

## Требования

- Последняя стабильная версия Bun.
- Стабильный Rust toolchain с Cargo.
- Системные зависимости из официальных [требований Tauri](https://v2.tauri.app/start/prerequisites/).

## Установка

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

Перед разработкой продукта замените имя пакета, product name, bundle identifier, метаданные Rust crate, автора и иконки.

## Быстрый старт и использование

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri создаёт пакеты только для текущей host-платформы; для всех ОС нужны отдельные CI runners.

## Конфигурация

`rsbuild.config.ts` управляет frontend-сборкой, `src-tauri/tauri.conf.json` — desktop-приложением и пакетами, `src-tauri/Cargo.toml` — Rust-зависимостями, `biome.json` — анализом и форматированием. Dev server работает на `http://localhost:3000`, production assets находятся в `dist/`.

## Безопасность

Перед выпуском замените sample identifier и проверьте Tauri capabilities и CSP. Уязвимости сообщайте через [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new).

## Участие и лицензия

Перед изменением базового стека создайте issue. Pull request должен сохранять минимальность шаблона и проходить `bun run check` и `bun run build`. Проект распространяется по [лицензии MIT](LICENSE).
