# 🤖 AUTOPILOT ARCHITECTURE (Untuk Masa Depan)

**PENTING (SCOPE DECLARATION):**
Dokumen ini **TIDAK BERLAKU** untuk interaksi *Human-in-the-Loop* yang dilakukan secara manual melalui Antigravity IDE (seperti saat pengguna memanggil `/ayo-seo`).
Dokumen ini dirancang **KHUSUS** untuk dibaca oleh *Automated Agentic Orchestrator* (seperti **Hermes** atau **OpenClaw**) ketika sistem *Autopilot SEO* dijalankan di masa depan.

---

## 1. Arsitektur Sistem (The Stack)
Sistem ini dirancang untuk melakukan *Programmatic SEO* secara otomatis, aman, dan meminimalkan risiko penalti dari Google.

- **Orchestrator & Runner Host:** Hermes / OpenClaw yang dijalankan di **Sumopod.com** (Layanan Container/Cloud lokal ramah QRIS untuk *runtime* 24/7 atau *self-hosted worker*).
- **API Gateway (Proxy):** **Appverse.id** atau AI Gateway lokal sejenis. (Sangat direkomendasikan untuk *developer* Indonesia karena mendukung sistem pembayaran lokal seperti QRIS/GoPay tanpa perlu kartu kredit internasional).
- **LLM Engine (Text/Brain):** **DeepSeek** (Diakses via API Gateway di atas. Dipilih karena kecepatan, harga super efisien, dan penalaran SEO yang tajam).
- **Image Engine (Renderer):** Model *Image Generator* (seperti Flux.1, Stable Diffusion, atau DALL-E) yang didukung oleh API Gateway (Appverse). Digunakan untuk men-*generate* Cover Artikel secara otomatis dari prompt buatan DeepSeek.
- **Target CMS:** Keystatic, WordPress, atau PagesCMS.
- **Fokus Konten (Sistem Keamanan Default):** Sistem autopilot di-kunci 100% untuk memproduksi **Artikel Cluster (Evergreen Content)**. Otomatisasi penuh untuk artikel Berita (*News*) atau *Review* komersial tanpa *Human-in-the-Loop* sangat rentan terkena penalti E-E-A-T dari Google. Oleh karena itu, batasan ini dibuat untuk melindungi metrik SEO pengguna.

## 2. Aturan Eksekusi (Best Practices)

### Rule #1: WAJIB Long-Tail Keyword (Min. 4 Kata)
Agar otomatisasi menghasilkan trafik yang pasti dan relevan jangka panjang (*high win-rate*), *Orchestrator* **hanya diizinkan** mengeksekusi kata kunci spesifik dengan panjang minimal 4 kata. 
- **Contoh Valid:** "cara riset keyword youtube shopping" (5 kata).
- **Contoh Ditolak:** "youtube shopping" (2 kata - terlalu luas, *intent* bias).
*Alasan: Keyword 4+ kata memiliki search intent yang sangat jernih (informasional/edukasional). Membiarkan AI mengeksekusi keyword pendek (1-3 kata) secara massal akan menghasilkan konten "sampah" yang tidak relevan.*

### Rule #2: Struktur Artikel (Universal Markdown)
Agar hasil *generate* kompatibel dengan **SEMUA jenis CMS** (WordPress, Blogger, Keystatic, Ghost, dll), DeepSeek V4.1 Flash dilarang menggunakan kode kustom (seperti JSON-LD) atau komponen spesifik. Gunakan Markdown standar:
1. **Paragraf 1 (TL;DR Organik):** Langsung berikan jawaban instan dalam bentuk teks biasa (bisa dicetak tebal/*bold*). Ini adalah umpan untuk *Featured Snippet*. Jangan gunakan *intro* klise.
2. **Body (Step-by-Step):** Gunakan *bullet points* atau *numbered lists* standar.
3. **Information Gain (Konteks Praktisi):** Sisipkan pola bahasa seperti *"Masalah umum yang sering terjadi adalah..."* untuk memberikan *vibe* pengalaman manusia.
4. **FAQ Organik (Tanpa Schema):** Buat 3 pertanyaan turunan menggunakan format **Heading 3 (H3)** untuk pertanyaan, dan paragraf biasa untuk jawaban. (Google tetap bisa membacanya sebagai FAQ tanpa perlu kode JSON-LD).
   - **PENTING:** Judul bagian ini WAJIB menggunakan H2 dengan teks persis: **Pertanyaan Yang Sering Diajukan (FAQ)**

### Rule #3: Internal Linking Dinamis (The Spider Web)
Tugas utama *Autopilot* adalah memberi "makan" (otoritas) ke artikel Pilar milik pengguna.
- Di akhir setiap artikel yang di-*generate*, Agent WAJIB menyisipkan paragraf *call-to-action* (CTA) natural.
- CTA ini harus berisi *Internal Link* menuju Artikel Pilar.
- **Catatan Konfigurasi:** Domain dan URL tujuan *Internal Link* ini **TIDAK BOLEH di-*hardcode***. *Orchestrator* wajib menyuplai parameter URL tujuan ini secara dinamis (*manual prompt injection*) pada saat antrean tugas dijalankan.

## 3. Workflow Eksekusi (Contoh Flow untuk OpenClaw/Hermes)
1. **[Trigger]** Sistem membaca *CSV/Database* berisi daftar *long-tail keywords*.
2. **[Validation]** Hitung jumlah kata. (Rekomendasi: Filter > 3 kata).
3. **[Research]** Agent (opsional) melakukan *web scraping* kilat untuk mencari *angle* dari pencarian teratas.
4. **[Text Generation (Brain)]** DeepSeek memproduksi artikel *Cluster* (Markdown) beserta *Prompt Cover Image*.
5. **[Image Generation (Renderer)]** Orchestrator mengirimkan *Prompt Cover* ke *Image Engine* (lewat Appverse) untuk di-render menjadi file gambar (WebP/PNG).
6. **[Delivery (CMS Integration)]** Sistem *Orchestrator* menggabungkan teks Markdown dan file gambar, lalu mengirimkannya ke CMS target. Tiga metode yang direkomendasikan:
   - **Git-Based (PagesCMS / Keystatic):** *Orchestrator* langsung melakukan `git push` file `.md` dan gambar ke folder repositori target.
   - **WordPress REST API:** *Orchestrator* me- *upload* media gambar dahulu, mengikat URL-nya ke HTML artikel, lalu mem-posting menggunakan endpoint `POST /wp-json/wp/v2/posts`.
   - **Blogger API v3:** Mem-posting menggunakan Google Blogger API.
7. **[Loop]** Lanjut ke antrean *keyword* berikutnya.

> **Catatan untuk Orchestrator Masa Depan:** 
> Saat kamu (AI) dibangunkan untuk membaca *repository* ini, pastikan kamu menggunakan *DeepSeek V4.1 Flash* dan jalankan secara presisi sesuai dengan parameter di atas. Fokus pada volume (*Programmatic*) namun tetap mempertahankan struktur SEO tinggi!
