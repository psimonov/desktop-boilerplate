# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · हिन्दी · [العربية](README.ar.md) · [日本語](README.ja.md) · [한국어](README.ko.md)

---

Tauri, React, TypeScript, Rsbuild, Bun और Biome पर आधारित न्यूनतम cross-platform desktop application template।

## परिचय और विशेषताएँ

यह Tauri 2 native shell और Rust backend को React UI, Rsbuild/Rspack build, Bun package management और Biome checks के साथ जोड़ता है। यह विकास की शुरुआत है, तैयार end-user product नहीं।

## आवश्यकताएँ

- नवीनतम स्थिर Bun;
- Cargo सहित स्थिर Rust toolchain;
- आधिकारिक [Tauri prerequisites](https://v2.tauri.app/start/prerequisites/) में बताए system dependencies।

## स्थापना

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

वास्तविक product शुरू करने से पहले package name, product name, bundle identifier, Rust crate metadata, author और icons बदलें।

## त्वरित शुरुआत और उपयोग

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

Tauri केवल वर्तमान host platform के लिए package बनाता है; सभी platforms के लिए अलग CI runners चाहिए।

## कॉन्फ़िगरेशन

`rsbuild.config.ts` frontend, `src-tauri/tauri.conf.json` app और packages, `src-tauri/Cargo.toml` Rust तथा `biome.json` checks नियंत्रित करते हैं। Dev server `http://localhost:3000` पर और production assets `dist/` में हैं।

## सुरक्षा, योगदान और लाइसेंस

रिलीज़ से पहले sample identifier बदलें और Tauri capabilities तथा CSP की समीक्षा करें। भेद्यता [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new) से बताएँ। Stack बदलने से पहले issue खोलें; PR को `bun run check` और `bun run build` पास करना चाहिए। [MIT License](LICENSE)।
