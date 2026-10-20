# Blog Danny Marchiano

Blog minimalis dan responsif yang dibuat dengan Astro, koleksi konten Markdown/MDX, dan Tailwind CSS. Tema terang/gelap mengikuti preferensi perangkat dan dapat diganti melalui tombol di navigasi.

## Menjalankan proyek

1. Pasang Node.js versi 22.22.0 atau lebih baru.
2. Dari folder proyek, pasang dependensi:

   ```sh
   npm install
   ```

3. Jalankan server pengembangan:

   ```sh
   npm run dev
   ```

4. Buka alamat lokal yang ditampilkan Astro di terminal.
5. Buat versi produksi dan uji pratinjaunya:

   ```sh
   npm run build
   npm run preview
   ```

## Menambahkan artikel

Buat file `.md` atau `.mdx` di `src/content/blog/`, lalu sertakan frontmatter berikut:

```yaml
---
title: "Judul artikel"
description: "Ringkasan singkat artikel."
pubDate: 2025-03-01
author: "Danny Marchiano"
image: "https://alamat-gambar-anda/contoh.jpg"
tags:
  - Desain
  - Web
---
```

Isi setelah frontmatter ditulis sebagai Markdown. Slug URL dibuat dari nama file, misalnya `catatan-baru.md` menjadi `/blog/catatan-baru/`. Artikel otomatis muncul di halaman utama dan arsip blog.

## Struktur proyek

```text
.
├── astro.config.mjs
├── package.json
├── src/
│   ├── components/
│   │   ├── BlogCard.astro
│   │   ├── Footer.astro
│   │   └── Header.astro
│   ├── content/
│   │   ├── blog/
│   │   │   └── desain-web-yang-tenang.md
│   │   └── config.ts
│   ├── content.config.ts
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── blog/
│   │   │   ├── [slug].astro
│   │   │   └── index.astro
│   │   └── index.astro
│   └── styles/
│       └── global.css
└── tsconfig.json
```

`src/content/config.ts` mendefinisikan skema artikel, sedangkan `src/content.config.ts` mengekspor koleksi pada lokasi konfigurasi Content Collections Astro 5.
