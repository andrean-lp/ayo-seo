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
- **Fokus Konten:** 100% **Artikel Cluster** (Informational / Edukasional). Sistem autopilot dilarang keras memproduksi artikel berita (*News*) atau artikel *Review/Commercial* murni untuk mencegah isu E-E-A-T.

## 2. Aturan Emas Eksekusi (Golden Rules)

### Rule #1: Wajib Long-Tail Keyword (Min. 4 Kata)
Agen Autopilot **dilarang keras** mengeksekusi kata kunci umum (1-3 kata). 
Setiap target kata kunci yang masuk ke dalam antrean (Queue) harus diverifikasi:
- **Valid:** "cara riset keyword youtube shopping" (5 kata) -> Lanjut Eksekusi.
- **Tidak Valid:** "youtube shopping" (2 kata) -> *Skip* / *Drop Task*.
*Alasan: Keyword 4+ kata memiliki search intent yang sangat jernih (menjawab pertanyaan/tutorial) sehingga model DeepSeek V4.1 Flash bisa menjawabnya secara akurat tanpa halusinasi "pengalaman palsu".*

### Rule #2: Struktur Artikel Cluster (DeepSeek Prompting)
Ketika DeepSeek V4.1 Flash mengeksekusi *long-tail keyword*, wajib mengikuti kerangka ini:
1. **Paragraf 1 (TL;DR):** Langsung berikan jawaban instan (*Featured Snippet Target*). Jangan menggunakan *intro* berbunga-bunga.
2. **Body (Step-by-Step):** Gunakan *bullet points* atau *numbered lists*.
3. **Information Gain (Konteks Manusia):** Jika memungkinkan, *Agent* harus diarahkan untuk memasukkan konteks *"Masalah umum yang sering terjadi adalah..."* untuk memberikan *vibe* pengalaman praktisi.
4. **Skema FAQ:** Wajib buatkan 3 pertanyaan turunan dalam format JSON-LD `FAQPage`.

### Rule #3: Internal Linking Otomatis (The Spider Web)
Tugas utama *Autopilot* ini adalah memberi "makan" artikel Pilar.
- Di akhir setiap artikel yang di-*generate*, Agent WAJIB menyisipkan paragraf *call-to-action* (CTA) natural.
- CTA ini harus berisi *Internal Link* menuju Artikel Pilar yang relevan di `andrean.web.id/blog/`.

## 3. Workflow Eksekusi (Contoh Flow untuk OpenClaw/Hermes)
1. **[Trigger]** Sistem membaca *CSV/Database* berisi daftar *long-tail keywords*.
2. **[Validation]** Hitung jumlah kata. Jika < 4 kata, batalkan.
3. **[Research]** Agent (opsional) melakukan *web scraping* kilat untuk mencari *angle* dari hasil pencarian teratas.
4. **[Generation]** DeepSeek V4.1 Flash memproduksi artikel *Cluster* menggunakan *Artifact/Markdown rules*.
5. **[Delivery]** Agent melakukan *commit* & *push* file `.md` ke repositori Github (folder Keystatic `/artikel/` atau `/blog/`).
6. **[Loop]** Lanjut ke antrean *keyword* berikutnya.

> **Catatan untuk Orchestrator Masa Depan:** 
> Saat kamu (AI) dibangunkan untuk membaca *repository* ini, pastikan kamu menggunakan *DeepSeek V4.1 Flash* dan jalankan secara presisi sesuai dengan parameter di atas. Fokus pada volume (*Programmatic*) namun tetap mempertahankan struktur SEO tinggi!
