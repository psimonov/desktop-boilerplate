# Desktop Boilerplate

[English](README.md) · [Español](README.es.md) · [Français](README.fr.md) · [Português](README.pt.md) · [Deutsch](README.de.md) · [Italiano](README.it.md) · [Русский](README.ru.md) · [简体中文](README.zh-CN.md) · [हिन्दी](README.hi.md) · العربية · [日本語](README.ja.md) · [한국어](README.ko.md)

---

<div dir="rtl">

قالب صغير لتطبيقات سطح المكتب متعددة المنصات باستخدام Tauri وReact وTypeScript وRsbuild وBun وBiome.

## نظرة عامة والميزات

يجمع القالب غلاف Tauri 2 الأصلي وbackend بلغة Rust مع واجهة React وبناء Rsbuild/Rspack وإدارة الحزم عبر Bun وفحوص Biome. إنه نقطة بداية للتطوير وليس منتجاً جاهزاً للمستخدم.

## المتطلبات

- أحدث إصدار مستقر من Bun؛
- Rust toolchain مستقر مع Cargo؛
- حزم النظام المذكورة في [متطلبات Tauri الرسمية](https://v2.tauri.app/start/prerequisites/).

## التثبيت

</div>

```bash
git clone https://github.com/psimonov/desktop-boilerplate.git
cd desktop-boilerplate
bun install
```

<div dir="rtl">

قبل بدء منتج فعلي غيّر اسم الحزمة وproduct name وbundle identifier وبيانات Rust crate والمؤلف والأيقونات.

## البدء السريع والاستخدام

</div>

```bash
bun run tauri:dev
bun run dev
bun run build
bun run tauri:build
bun run check
bun run format
```

<div dir="rtl">

يبني Tauri للمنصة المضيفة فقط؛ تتطلب جميع المنصات CI runners منفصلة. تتحكم `rsbuild.config.ts` في frontend و`src-tauri/tauri.conf.json` في التطبيق والحزم و`src-tauri/Cargo.toml` في Rust و`biome.json` في الفحوص. يعمل dev server على `http://localhost:3000` وتوجد assets في `dist/`.

## الأمان والمساهمة والترخيص

استبدل المعرّف التجريبي وراجع Tauri capabilities وCSP قبل النشر. أبلغ عن الثغرات عبر [GitHub Security Advisories](https://github.com/psimonov/desktop-boilerplate/security/advisories/new). افتح issue قبل تغيير التقنية الأساسية؛ يجب أن تجتاز PR أوامر `bun run check` و`bun run build`. [رخصة MIT](LICENSE).

</div>
