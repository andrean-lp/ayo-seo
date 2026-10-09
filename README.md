# Ayo SEO — AI Agent Senior SEO Content Specialist

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-1.4.0-blue.svg)]()
[![Platform](https://img.shields.io/badge/Platform-Antigravity-orange.svg)]()

**Ayo SEO** adalah plugin (AI Agent) khusus untuk Antigravity yang dirancang agar bertindak sebagai **Senior SEO Content Strategist**. Plugin ini tidak sekadar menghasilkan teks layaknya robot, melainkan memikirkan strategi *Topical Authority*, meriset entitas semantik, dan mengeksekusi artikel berstandar **Google E-E-A-T** (Experience, Expertise, Authoritativeness, Trustworthiness) yang siap mendominasi pencarian Google dan AI Search (GEO/AEO).

> *"Ubah Kontenmu Jadi Aset Digital Yang Bekerja Jangka Panjang. Saat konten medsos mudah hilang dan tenggelam, Website dan YouTube adalah aset digital yang terus hidup."*

---

## 🌟 Kenapa Harus Ayo SEO?

Di era *Helpful Content System*, Google menghukum keras artikel AI yang kaku, penuh *keyword stuffing*, dan tidak memberikan *Information Gain* (nilai tambah). 

**Ayo SEO diciptakan untuk menyelesaikan masalah tersebut:**
1. **Bukan Sekadar Penulis, Tapi Ahli Strategi:** Agent ini melakukan riset *Search Intent* dan pemetaan entitas sebelum menulis.
2. **Gaya Bahasa "Manusia":** Menggunakan *tone* "aku-kamu" yang santai, humble, dan natural. Tidak ada lagi kalimat klise seperti *"Di era digital saat ini..."* atau *"Kesimpulannya adalah..."*
3. **Mendukung Ekosistem Affiliate:** Sangat cocok untuk *Affiliate Marketer* (seperti Shopee Affiliate / YouTube Shopping) yang butuh mengubah *traffic* organik menjadi *passive income*.
4. **Siap Menghadapi AI Overviews (SGE):** Artikel otomatis dilengkapi dengan *Key Takeaways* (TL;DR) dan Skema FAQ.

---

## 🚀 Daftar Mode Artikel

Ayo SEO memiliki 3 mode utama yang dirancang untuk membangun hierarki website (*Topical Authority*) yang sempurna:

### 1. 🏛️ Mode Pilar (Pillar Post)
- **Karakter:** Panduan super komprehensif, luas, dan mendalam. Menjadi "pusat" dari sebuah topik besar.
- **Panjang Kata:** 2.500 - 4.000+ kata.
- **Tugas Khusus:** Wajib memiliki *Outbound Link* ke sumber kredibel dunia (relasi Dofollow) untuk membuktikan otoritas.

### 2. 🎯 Mode Cluster (Supporting Post)
- **Karakter:** Pembahasan tajam dan sangat spesifik. Sangat cocok untuk membidik *long-tail keywords* (4+ kata).
- **Panjang Kata:** 1.200 - 2.000 kata.
- **Tugas Khusus:** Membangun *Internal Link* kembali ke Artikel Pilar untuk menyalurkan *PageRank*. Tidak wajib memiliki *Outbound Link* kecuali sangat mendesak.

### 3. 📖 Mode Glossary (Kamus Istilah)
- **Karakter:** Penjelasan ringkas, *to the point*, dan ramah pemula. Titik masuk untuk *traffic* di fase *awareness*.
- **Panjang Kata:** 500 - 800 kata.
- **Tugas Khusus:** Menjembatani pengunjung awal menuju ke artikel Pilar atau Halaman Layanan/Produk utama agar tidak terjadi *bounce rate* tinggi.

---

## ⚡ Slash Commands & Strategi Hemat Token

Untuk mempercepat kerja (*workflow*), kamu bisa langsung memanggil mode yang diinginkan melalui kolom *chat* tanpa harus melewati tahap "tanya jawab" awal.

| Command | Fungsi | Model AI yang Disarankan |
|---------|--------|--------------------------|
| `/ayo-seo` | **General Router** (Tanya jawab & Edukasi Riset Keyword) | Fleksibel |
| `/ayo-seo-pilar` | Langsung eksekusi **Artikel Pilar** | **Gemini 3.1 Pro (High)** (Butuh penalaran logis & E-E-A-T maksimal) |
| `/ayo-seo-cluster`| Langsung eksekusi **Artikel Cluster** | **Gemini 3.8 Flash (High)** (Cepat, tajam, hemat token) |
| `/ayo-seo-glossary`| Langsung eksekusi **Artikel Glossary** | **Gemini 3.8 Flash (High)** (Cepat, tajam, hemat token) |

**Contoh Penggunaan Cepat:**
> `/ayo-seo-cluster Cara daftar YouTube Shopping Affiliate Shopee`

---

## 🔧 Fitur SEO Teknis (Bawaan Otomatis)

Setiap artikel yang di-*generate* akan langsung menyertakan elemen SEO Teknis di bagian atas (*ready to copy-paste* ke CMS seperti Keystatic, WordPress, atau PagesCMS):
- **URL Slug:** Bersih, huruf kecil, dan dipisahkan tanda hubung.
- **Meta Title:** Menarik (*click-worthy*), dibatasi 50-60 karakter.
- **Meta Description:** Padat, informatif, dibatasi 130-155 karakter (anti terpotong di Google).
- **Struktur Heading:** H2, H3, H4 yang logis.
- **Saran Alt Text Gambar:** Rekomendasi penempatan visual + deskripsi aksesibilitas.
- **Pojok Edukasi SEO:** Di akhir artikel, agent akan memberikan *copywriting* persis untuk strategi *Internal Linking* dan panduan *Outbound Link*.

---

## 🤖 Integrasi API CMS & Skema Autopilot

Ayo SEO tidak hanya bisa dipakai secara manual via chat, tapi arsitektur *output* Markdown-nya (khususnya *Universal Markdown*) dirancang agar kompatibel penuh jika kamu ingin mengotomatisasinya menggunakan ekosistem *Agentic AI* (seperti OpenClaw / Hermes). 

Jika kamu ingin merangkai sistem penulisan dan *upload* otomatis (*Programmatic SEO*), Ayo SEO sangat mendukung integrasi dengan API CMS populer berikut:

1. **WordPress (WP REST API):** 
   Sistem dapat mengonversi output Ayo SEO dan menembakkannya langsung ke *endpoint* `POST /wp-json/wp/v2/posts`. Cukup gunakan *Application Password* di WordPress-mu untuk autentikasi yang aman.
2. **Google Blogger (Blogger API v3):** 
   Sangat cocok untuk *spamming* blog *dummy* atau PBN berbiaya rendah. Gunakan Google Cloud Console untuk mendapatkan kredensial, dan arahkan hasil ke *endpoint* Blogger API v3.
3. **Git-Based CMS (PagesCMS / Keystatic):** 
   Tidak butuh API CMS khusus! Agent hanya perlu menggunakan **GitHub API** untuk melakukan `git push` file Markdown `.md` langsung ke repositorimu. Sangat bersih, ter-versi (*version control*), dan anti-hack.

> **Tips:** Silakan baca *blueprint* spesifik untuk otomatisasi ini di file `rules/AUTOPILOT_ARCHITECTURE.md`.

---

## 📦 Cara Instalasi

### Sebagai Plugin Antigravity (Global)
Buka terminal dan jalankan perintah ini agar plugin terpasang secara permanen di sistem Antigravity lokalmu:

```bash
# Clone repo
git clone https://github.com/andrean-lp/ayo-seo.git

# Copy ke plugin directory
cp -r ayo-seo ~/.gemini/config/plugins/ayo-seo
```
*Restart Antigravity untuk mengaktifkan plugin.*

---

## 💡 Pedoman Kualitas Artikel (SEO Playbook)

Ayo SEO dilatih dengan aturan ketat dari [Google Search Essentials](https://developers.google.com/search/docs/essentials):

1. **Anchor Text Deskriptif:** Dilarang keras menggunakan teks generik seperti "klik di sini", "baca selengkapnya". *Anchor text* harus mendeskripsikan secara jelas isi halaman tujuan.
2. **Manajemen Outbound Link:**
   - ✅ **Dofollow:** Hanya untuk sitasi editorial ke sumber otoritatif (Jurnal, Statista, W3C, Google Developers).
   - ❌ **Nofollow/Sponsored:** Wajib digunakan untuk *link* afiliasi (misal: Shopee, Amazon) atau artikel bersponsor.
3. **No Wall of Text:** Paragraf dijaga tetap pendek (2-3 kalimat per paragraf), menggunakan tabel, dan *bullet points* agar mudah di-*skim* oleh pembaca.
4. **Information Gain Pertama:** AI diwajibkan untuk mencari *angle* atau sudut pandang baru yang belum dibahas oleh kompetitor di Halaman 1 Google.

---

## 📝 Changelog Terbaru

- **v1.4.0 (2026-10-09):** Perombakan besar-besaran dokumentasi (README.md) menjadi *Playbook* komprehensif. Penegasan *positioning* untuk Website, YouTube, dan Affiliate.
- **v1.3.6:** Penambahan fitur edukasi keberadaan *Slash Commands* di rute utama `/ayo-seo`.
- **v1.3.5:** Penambahan edukasi dinamis untuk penghematan token (Rekomendasi *Gemini 3.8 Flash* untuk Cluster/Glossary).
- **v1.3.4:** Penambahan *Pojok Edukasi SEO (Outbound & Internal Link)* di bagian penutup setiap artikel hasil *generate*.

## 📄 Lisensi
[MIT License](LICENSE)
