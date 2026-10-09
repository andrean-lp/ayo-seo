# Ayo SEO — AI Agent Senior SEO Content Specialist

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Plugin Antigravity untuk generate artikel berkualitas tinggi berstandar **Google E-E-A-T**, dengan gaya bahasa santai aku-kamu yang natural, optimasi **GEO/AEO**, dan struktur **Pilar–Cluster** yang solid.

> Terinspirasi dari [Ponytail](https://ponytail.dev) — tapi kalau Ponytail adalah "lazy senior developer", Ayo SEO adalah **"senior SEO specialist"** yang memastikan setiap artikel layak bersaing di Google, AI Overviews, dan Answer Engine.

## Fitur Utama

| Fitur | Deskripsi |
|-------|-----------|
| **3 Mode Artikel** | 🏛️ **Pilar** (komprehensif, 2.500–4.000+ kata), 🎯 **Cluster** (fokus spesifik, 1.200–2.000 kata), dan 📖 **Glossary** (definisi istilah, 500-800 kata) |
| **Riset E-E-A-T** | Riset mendalam sebelum menulis: Search Intent, Entity Mapping, Information Gain, Gap Kompetitor |
| **Key Takeaways / TL;DR** | Poin intisari di awal artikel untuk optimasi GEO & AEO (Google AI Overviews, Perplexity, ChatGPT Search) |
| **FAQ (Tanya Jawab)** | 3–5 pertanyaan berbasis intent pencarian + rekomendasi Schema JSON-LD `FAQPage` |
| **Outbound Link Dofollow** | Referensi otoritatif internasional (bukan website Indonesia) — hanya editorial, bukan spam |
| **Tone Natural** | Gaya aku-kamu, santai, humble, tidak terlihat seperti tulisan AI |
| **Internal Linking Strategy** | Saran artikel cluster (dari pilar) atau anchor text kembali ke pilar (dari cluster) |

## Instalasi

### Sebagai Plugin Antigravity (Global)

Copy folder ini ke direktori plugin Antigravity:

```bash
# Clone repo
git clone https://github.com/<username>/ayo-seo.git

# Copy ke plugin directory
cp -r ayo-seo ~/.gemini/config/plugins/ayo-seo
```

Restart Antigravity untuk mengaktifkan plugin.

### Sebagai Plugin di Repository (Per-Project)

Letakkan folder ini di `.gemini/plugins/ayo-seo/` di dalam repository kamu.

## Cara Pakai

Cukup minta agent untuk membuat artikel:

```
Buatkan artikel tentang "cara meningkatkan domain authority"
```

Agent akan otomatis:
1. **Tanya mode** — Pilar, Cluster, atau Glossary?
2. **Riset** — Search intent, entitas, nilai tambah
3. **Generate** — Artikel lengkap dengan Key Takeaways, FAQ, outbound link, dan saran internal linking

### Contoh Prompt

| Prompt | Mode |
|--------|------|
| `Buat artikel pilar komprehensif tentang SEO on-page` | Pilar |
| `Buat artikel cluster tentang cara optimasi meta description` | Cluster |
| `Buat artikel glossary yang menjelaskan apa itu Backlink` | Glossary |
| `Riset topik dan struktur konten untuk "email marketing"` | Riset saja |

## Struktur Plugin

```
ayo-seo/
├── plugin.json              # Manifest plugin
├── rules/AGENTS.md          # Rules untuk agent (karakter & mindset)
├── skills/ayo-seo/SKILL.md  # Skill utama: flow, format, pedoman
├── references/              # Referensi kualitas artikel
│   └── artikel-berkualitas.md
├── LICENSE                   # MIT License
└── README.md                 # Dokumentasi (file ini)
```

## Pedoman Kualitas Artikel (Ringkasan)

Berdasarkan panduan resmi [Google Search Central](https://developers.google.com/search/docs/fundamentals/creating-helpful-content) dan [Google SEO Starter Guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide):

1. **People-First Content** — Konten dibuat terutama untuk membantu manusia, bukan sekadar memanipulasi algoritma pencarian.
2. **E-E-A-T** — Experience, Expertise, Authoritativeness, Trustworthiness.
3. **Information Gain** — Memberikan nilai tambah, perspektif baru, dan data yang belum ada di artikel kompetitor.
4. **Anchor Text Deskriptif** — Teks tautan menjelaskan tujuan halaman secara alami; hindari teks generik ("klik di sini").
5. **Aksesibilitas & Gambar** — Sertakan ide gambar kontekstual dengan deskripsi `alt text` yang relevan.
6. **Struktur URL & Meta Snippet** — URL slug bersih/ringkas, meta title menarik (50–60 karakter), dan meta description informatif (130–155 karakter).
7. **Outbound Link Kredibel** — Dofollow hanya untuk sitasi editorial ke sumber otoritatif internasional; nofollow/sponsored untuk link berbayar/afiliasi.
8. **GEO/AEO Ready** — Key Takeaways dan FAQ Schema agar konten mudah dikutip oleh AI Search (Google AI Overviews, Perplexity, ChatGPT Search).

## Pedoman Outbound Link

| Kondisi | Aksi |
|---------|------|
| Mengutip data riset/statistik dari sumber kredibel internasional | ✅ Dofollow |
| Merujuk dokumentasi teknis resmi (Google, W3C, MDN) | ✅ Dofollow |
| Link afiliasi atau sponsor | ❌ `rel="sponsored"` |
| Konten buatan pengguna (komentar, forum) | ❌ `rel="ugc"` |
| Link tidak relevan hanya untuk "memperbanyak link" | ❌ Jangan pasang |
| Website mencurigakan / low-quality | ❌ Jangan pasang |

> **Sumber:** [Qualify Outbound Links for SEO — Google Search Central](https://developers.google.com/search/docs/crawling-indexing/qualify-outbound-links)

## Sumber & Referensi

- [Panduan Memulai SEO (Google SEO Starter Guide)](https://developers.google.com/search/docs/fundamentals/seo-starter-guide?hl=id)
- [Creating Helpful, Reliable, People-First Content](https://developers.google.com/search/docs/fundamentals/creating-helpful-content)
- [Google Search Essentials](https://developers.google.com/search/docs/essentials)
- [Google's Guidance on AI-Generated Content](https://developers.google.com/search/docs/fundamentals/using-gen-ai-content)
- [Qualify Outbound Links for SEO](https://developers.google.com/search/docs/crawling-indexing/qualify-outbound-links)
- [Panduan Lengkap Artikel Pilar — Saungwriter](https://saungwriter.com/artikel-pilar)

## Saran untuk Hasil Maksimal

1. **Selalu berikan konteks niche/website kamu** saat meminta artikel — agent akan menyesuaikan tone dan sudut pandang
2. **Mulai dari artikel pilar**, lalu bangun cluster articles di sekitarnya untuk topical authority
3. **Review & edit hasil AI** — tambahkan pengalaman pribadi, studi kasus nyata, data internal untuk memperkuat E-E-A-T
4. **Gunakan slug & meta description** yang di-generate langsung ke form SEO CMS kamu
5. **Pasang FAQ Schema** di CMS kamu (Schema.org FAQPage) untuk meningkatkan peluang rich snippets & AI Overview
6. **Jangan publish massal** tanpa quality check — Google menghukum konten massal tanpa nilai tambah

## Changelog

### v1.2.1 (2026-10-09)
- Penambahan pengingat otomatis di awal chat agar pengguna memakai model **Gemini 3.1 Pro (High)** demi hasil tulisan dan penalaran yang maksimal.

### v1.2.0 (2026-10-09)
- Penambahan mode **Glossary** (Kamus Istilah) untuk melayani *search intent* definisi istilah dengan ringkas dan terfokus.

### v1.1.0 (2026-10-09)
- Penyelarasan penuh dengan **Google SEO Starter Guide**:
  - Rekomendasi URL Slug bersih dan ringkas.
  - Standarisasi Meta Title & Meta Description.
  - Rekomendasi Gambar & Alt Text aksesibel.
  - Teks tautan (Anchor text) deskriptif (anti teks generik "klik di sini").

### v1.0.0 (2026-10-09)
- Initial release
- Skill `ayo-seo` dengan 2 mode: Pilar & Cluster
- Rules AGENTS.md untuk karakter Senior SEO Specialist
- Pedoman E-E-A-T, outbound link, GEO/AEO
- Key Takeaways / TL;DR dan FAQ wajib di setiap artikel
- Referensi artikel berkualitas dari Google Search Central
- Gaya bahasa aku-kamu, humble, natural

## Lisensi

[MIT License](LICENSE)

