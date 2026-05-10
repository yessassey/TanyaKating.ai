# TanyaKating.ai
FINAL PROJECT PELATIHAN HACKTIVE8 
# 🎀 TanyaKating – Temen Belajar AI Kamu!

> Final Project · AI Productivity and AI API Integration for Developers

[![Powered by Claude](https://img.shields.io/badge/Powered%20by-Claude%20Sonnet-FF6B9D)](https://anthropic.com)
[![HTML](https://img.shields.io/badge/Built%20with-HTML%2FJS-C084FC)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![License: MIT](https://img.shields.io/badge/License-MIT-34D399)](LICENSE)

---

## 🌸 Deskripsi Proyek

**TanyaKating** adalah chatbot AI berkarakter yang dirancang sebagai **teman belajar virtual** untuk pelajar dan mahasiswa Indonesia. Berbeda dari chatbot biasa, TanyaKating hadir dengan persona "Kating" — sosok teman yang asik, hangat, relatable, dan kebetulan pinter banget.

Chatbot ini menggunakan model Claude Sonnet dari Anthropic untuk memproses bahasa alami dan memberikan respons edukatif yang disesuaikan dengan mood dan kebutuhan pengguna — dari penjelasan santai, sesi belajar serius, drill soal, sampai jadi teman curhat!

---

## ✨ Fitur Utama

| Fitur | Deskripsi |
|---|---|
| 🎭 **Mode Kating** | 4 mode kepribadian: Santai, Serius, Drill Soal, Curhat |
| 🌈 **Branding Kating** | UI chat bergaya personal — pink, playful, dan fun |
| 📖 **Domain Pengetahuan** | 6 domain: Matematika, IPA, IPS, Bahasa Indonesia, Programming, Umum |
| 🎛️ **Parameter Kreatif** | Temperature slider & max tokens yang bisa diatur langsung |
| 💬 **Memori Multi-turn** | Konteks percakapan diingat hingga 12 pesan terakhir |
| 📊 **Statistik Live** | Monitor pesan, tokens, dan mode aktif secara real-time |
| 💡 **Pertanyaan Cepat** | Suggestion chips untuk mulai belajar instan |
| 📱 **Responsif** | Tampilan adaptif desktop dan mobile |

---

## 🎭 Mode-Mode Kating

### 😊 Santai aja, Kating!
Bahasa gaul, emoji relevan, analogi kehidupan sehari-hari. Cocok buat eksplorasi topik baru dengan santai.

### 📚 Fokus belajar
Lebih terstruktur: konsep → detail → contoh. Tetap hangat tapi sistematis. Ideal buat persiapan ujian.

### 🔥 Drill soal latihan
Mode latihan soal interaktif! Kating kasih soal, tunggu jawaban kamu, lalu bahas bareng. Ada hint kalau kesulitan.

### 💬 Mau curhat dulu
Mode empati — Kating jadi teman dengerin dan validasi perasaan kamu dulu sebelum kasih solusi.

---

## 🛠️ Teknologi

- **Frontend**: HTML5, CSS3 (CSS Variables, Grid, Flexbox), Vanilla JavaScript
- **AI Model**: `claude-sonnet-4-20250514` via [Anthropic Messages API](https://docs.anthropic.com/en/api/messages)
- **Font**: [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) — Google Fonts
- **Design**: Custom pink-purple palette, bubble chat UI

---

## ⚙️ Parameter AI yang Bisa Dikonfigurasi

### Temperature (0.0 – 1.0)
```
0.0 – 0.3  → Jawaban konsisten & faktual
0.4 – 0.7  → Keseimbangan akurasi & kreativitas
0.8 – 1.0  → Lebih ekspresif & kreatif (default Kating: 0.8)
```

### Max Tokens
```
256   → Singkat & padat — jawaban cepat
512   → Sedang — penjelasan dengan contoh (default)
1024  → Detail banget — lengkap dengan elaborasi
```

### Domain Pengetahuan
Setiap domain menyuntikkan konteks tambahan ke system prompt Kating untuk fokus pada bidang studi tertentu.

---

## 🚀 Cara Menjalankan

### Buka langsung di browser
```bash
git clone https://github.com/username/tanyakating.git
cd tanyakating
open index.html
```

### Pakai live server (direkomendasikan)
```bash
npx serve .
# Buka http://localhost:3000
```

### Deploy ke GitHub Pages
1. Push ke GitHub
2. **Settings → Pages → Source: main branch → / (root)**
3. Akses di `https://username.github.io/tanyakating`

---

## 🔑 Konfigurasi API Key

Tambahkan `x-api-key` header di fetch request pada `index.html` untuk penggunaan mandiri:

```javascript
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'YOUR_ANTHROPIC_API_KEY',
  'anthropic-version': '2023-06-01'
}
```

> ⚠️ Jangan commit API key ke repo publik. Gunakan environment variable atau backend proxy untuk produksi.

---

## 📁 Struktur Proyek

```
tanyakating/
├── tanya kating UI.html    ← Aplikasi lengkap (single-file)
└── README.md     ← Dokumentasi ini
```

---

## 🏗️ Arsitektur

```
Browser (index.html)
│
├── Sidebar
│   ├── Mode Kating (system prompt selector)
│   ├── Parameter AI (temperature, max tokens, domain)
│   └── Statistik sesi
│
└── Chat Interface
    ├── Header (Kating avatar + mood chips)
    ├── Messages (bubble chat UI)
    ├── Suggestion chips
    └── Input + Send
            │
            ▼ fetch() POST
    Anthropic Claude API
    /v1/messages · claude-sonnet-4-20250514
```

---

## 👩‍💻 Author (Yessa)

Dibuat sebagai **Final Project** pelatihan *AI Productivity and AI API Integration for Developers*.

---

*Made with 🎀 and lots of ✨ — TanyaKating siap nemenin belajar kapanpun!*
