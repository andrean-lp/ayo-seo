# 🤖 AUTOPILOT ARCHITECTURE (Untuk Masa Depan)

**PENTING (SCOPE DECLARATION):**
Dokumen ini **TIDAK BERLAKU** untuk interaksi *Human-in-the-Loop* yang dilakukan secara manual melalui Antigravity IDE (seperti saat pengguna memanggil `/ayo-seo`).
Dokumen ini dirancang **KHUSUS** untuk dibaca oleh *Automated Agentic Orchestrator* (seperti **Hermes** atau **OpenClaw**) ketika sistem *Autopilot SEO* dijalankan di masa depan.

---

## 1. Arsitektur Sistem (The Stack)
Sistem ini dirancang untuk melakukan *Programmatic SEO* secara otomatis, aman, dan meminimalkan risiko penalti dari Google.

- **Orchestrator:** Hermes / OpenClaw (Sebagai *Task Manager* dan *Executor*).
- **LLM Engine:** **DeepSeek V4.1 Flash** (Dipilih karena kecepatan, efisiensi harga, dan kemampuan penalaran logis yang mumpuni untuk *intent* informasional).
- **Target CMS:** Keystatic (Push otomatis ke Github Repo sebagai `.md` / `.mdx` files).
- **Fokus Konten (Rekomendasi Default):** Sangat direkomendasikan agar sistem autopilot difokuskan 100% untuk **Artikel Cluster** (Informasional). Otomatisasi penuh untuk artikel Berita (*News*) atau *Review* komersial murni memiliki risiko penalti E-E-A-T yang tinggi tanpa *Human-in-the-Loop*.

## 2. Aturan Eksekusi (Best Practices)

### Rule #1: Strategi Long-Tail Keyword (Min. 4 Kata)
Agar otomatisasi menghasilkan trafik yang pasti (*high win-rate*), sangat direkomendasikan agar *Orchestrator* menyeleksi kata kunci turunan yang spesifik (minimal 4 kata). 
- **Contoh Valid:** "cara riset keyword youtube shopping" (5 kata).
*Alasan: Keyword 4+ kata memiliki search intent yang sangat jernih, sehingga model AI bisa menjawabnya secara akurat tanpa rentan halusinasi.*

### Rule #2: Struktur Artikel Cluster (DeepSeek Prompting)
Ketika DeepSeek V4.1 Flash mengeksekusi *long-tail keyword*, wajib mengikuti kerangka ini:
1. **Paragraf 1 (TL;DR):** Langsung berikan jawaban instan (*Featured Snippet Target*). Jangan menggunakan *intro* berbunga-bunga.
2. **Body (Step-by-Step):** Gunakan *bullet points* atau *numbered lists*.
3. **Information Gain (Konteks Praktisi):** Arahkan *Agent* untuk memasukkan pola bahasa seperti *"Masalah umum yang sering terjadi adalah..."* untuk memberikan *vibe* pengalaman praktisi.
4. **Skema FAQ:** Wajib buatkan 3 pertanyaan turunan dalam format JSON-LD `FAQPage`.

### Rule #3: Internal Linking Dinamis (The Spider Web)
Tugas utama *Autopilot* adalah memberi "makan" (otoritas) ke artikel Pilar milik pengguna.
- Di akhir setiap artikel yang di-*generate*, Agent WAJIB menyisipkan paragraf *call-to-action* (CTA) natural.
- CTA ini harus berisi *Internal Link* menuju Artikel Pilar.
- **Catatan Konfigurasi:** Domain dan URL tujuan *Internal Link* ini **TIDAK BOLEH di-*hardcode***. *Orchestrator* wajib menyuplai parameter URL tujuan ini secara dinamis (*manual prompt injection*) pada saat antrean tugas dijalankan.

## 3. Workflow Eksekusi (Contoh Flow untuk OpenClaw/Hermes)
1. **[Trigger]** Sistem membaca *CSV/Database* berisi daftar *long-tail keywords*.
2. **[Validation]** Hitung jumlah kata. (Rekomendasi: Filter > 3 kata).
3. **[Research]** Agent (opsional) melakukan *web scraping* kilat untuk mencari *angle* dari pencarian teratas.
4. **[Generation]** DeepSeek V4.1 Flash memproduksi artikel *Cluster* menggunakan *Artifact rules*.
5. **[Delivery]** Agent melakukan *commit* & *push* file `.md` ke repositori Github atau via API CMS yang digunakan pengguna.
6. **[Loop]** Lanjut ke antrean *keyword* berikutnya.

> **Catatan untuk Orchestrator Masa Depan:** 
> Saat kamu (AI) dibangunkan untuk membaca *repository* ini, pastikan kamu menggunakan *DeepSeek V4.1 Flash* dan jalankan secara presisi sesuai dengan parameter di atas. Fokus pada volume (*Programmatic*) namun tetap mempertahankan struktur SEO tinggi!
