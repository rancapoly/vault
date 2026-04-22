---
name: board-deck-composer
description: >
  Skill untuk menyusun Board Deck / Management Presentation berkualitas tinggi dalam format
  PowerPoint (.pptx) untuk Polytron — PT Hartono Istana Teknologi, khususnya untuk tiga
  jenis deck utama: Quarterly Business Review (QBR), Crisis / Issue Briefing, dan
  HR Monthly Meeting. Output dirancang untuk audiens Top Management Team dan Board of
  Directors / Komisaris, dengan standar visual Polytron Persona.

  SELALU gunakan skill ini ketika pengguna meminta: Board Deck, Management Deck,
  Quarterly Review, QBR, business review presentation, crisis briefing, issue briefing,
  HR monthly report, monthly people update, laporan bulanan HR, slide untuk meeting
  direksi, presentasi untuk board, deck untuk komisaris, atau menyebut istilah seperti
  "deck QBR", "slide crisis", "HR monthly deck", "management presentation", "board update",
  "executive briefing", atau meminta slide yang ditujukan untuk Top Management / C-Suite.
  Juga aktif saat pengguna menyebut "decision needed", "board approval", "action required",
  atau meminta visualisasi KPI / OKR untuk keperluan management review.
---

# Board Deck Composer — Polytron
## Panduan End-to-End Penyusunan Management Presentation

Skill ini menghasilkan PowerPoint deck berkualitas board-ready untuk tiga jenis
presentation utama Polytron: QBR, Crisis Briefing, dan HR Monthly Meeting.

---

## ALUR KERJA WAJIB

### Langkah 1 — Identifikasi Deck Type

Tentukan jenis deck yang dibutuhkan:

| Deck Type | Trigger Kata Kunci | Reference File |
|---|---|---|
| **Quarterly Business Review (QBR)** | QBR, business review, quarterly update, kinerja kuartal | `references/qbr-deck.md` |
| **Crisis / Issue Briefing** | krisis, issue, insiden, masalah mendesak, emergency briefing | `references/crisis-deck.md` |
| **HR Monthly Meeting** | HR monthly, people update, laporan HR bulanan, HR metrics | `references/hr-monthly-deck.md` |

> Jika deck type tidak jelas dari permintaan pengguna, tanyakan sebelum melanjutkan.

---

### Langkah 2 — Kumpulkan Data yang Diperlukan

Sebelum membuat slide, identifikasi data apa yang tersedia:

**Jika data tersedia** → Gunakan data aktual, isi placeholder secara langsung
**Jika data belum tersedia** → Gunakan placeholder `[X]` dan tandai dengan catatan

Untuk setiap deck type, data minimum yang dibutuhkan:

| Deck Type | Data Minimum |
|---|---|
| QBR | Revenue vs target, KPI aktual vs target, 3 highlight, 3 risiko, next quarter priorities |
| Crisis Briefing | Deskripsi insiden, timeline kejadian, dampak bisnis, action plan, owner & timeline |
| HR Monthly | Headcount, turnover, time-to-fill, engagement score, top hiring update, learning metrics |

---

### Langkah 3 — Baca Reference File & Eksekusi

Baca reference file deck type yang dipilih, lalu:
1. Buat file JavaScript menggunakan pptxgenjs
2. Terapkan **Polytron Visual Identity** (lihat bagian bawah)
3. Jalankan QA: `extract-text output.pptx` untuk validasi konten
4. Konversi ke gambar untuk visual check jika diperlukan

---

## POLYTRON VISUAL IDENTITY — WAJIB DITERAPKAN

### Palet Warna

```javascript
// WAJIB digunakan di semua deck Polytron
const C = {
  RED:       "E8002D",   // Polytron Red — aksen utama, header
  DARK_RED:  "CC0000",   // Alert, peringatan kritis
  BLACK:     "1A1A1A",   // Teks utama, judul besar
  CHARCOAL:  "2C2C2C",   // Background dark section
  DARKGRAY:  "4A4A4A",   // Body text
  MIDGRAY:   "9E9E9E",   // Caption, footer, label ringan
  LIGHTGRAY: "F5F5F5",   // Background netral, alternating rows
  WHITE:     "FFFFFF",   // Background utama
  YELLOW:    "F5C518",   // Highlight, callout positif
  GREEN:     "2E7D32",   // Status positif, on-track
  AMBER:     "F57C00",   // Status at-risk, warning
};
```

### Layout Standar (16:9, 10" × 5.625")

```javascript
pres.layout = 'LAYOUT_16x9';
// Content area: x=0.4, y=0.9, w=9.2, h=4.4 (dengan header + footer)
// Header bar: y=0, h=0.75
// Footer bar: y=5.25, h=0.375
```

### Struktur Slide Standar

Setiap slide memiliki 3 zona tetap:

```
┌─────────────────────────────────────────┐
│ HEADER BAR (merah/charcoal, h=0.75")    │
│ [Logo area kiri] [Judul slide tengah]   │
├─────────────────────────────────────────┤
│                                         │
│         CONTENT AREA                    │
│         (h ≈ 4.5")                      │
│                                         │
├─────────────────────────────────────────┤
│ FOOTER (abu, h=0.375") | hal | tanggal  │
└─────────────────────────────────────────┘
```

### Typography

```javascript
// Font pairing: Arial Black (header) + Arial (body)
// Judul slide: fontSize: 22, bold: true, fontFace: "Arial Black"
// Sub-header: fontSize: 14, bold: true, fontFace: "Arial"
// Body: fontSize: 12, fontFace: "Arial"
// Caption/label: fontSize: 10, fontFace: "Arial", color: MIDGRAY
// Stat callout: fontSize: 36-48, bold: true (untuk angka besar)
```

### Slide Types yang Tersedia

| Type | Kapan Digunakan |
|---|---|
| **Cover** | Slide pertama, identitas deck |
| **Agenda** | Daftar topik, pembuka section |
| **Exec Summary** | 1 slide ringkasan — answer first |
| **KPI Dashboard** | Grid metrik dengan status traffic light |
| **Trend Chart** | Data time-series, pencapaian vs target |
| **Issue Card** | Format 4-box: Situasi / Dampak / Tindakan / Owner |
| **People Metrics** | Headcount, turnover, pipeline |
| **Action Table** | Tabel keputusan / tindak lanjut |
| **Closing / Next Steps** | Slide penutup, keputusan yang diminta |

---

## PRINSIP KONTEN BOARD DECK

### Answer First (Wajib)

Board tidak membaca dari awal ke akhir — mereka membaca kesimpulan dulu.
Setiap slide harus memiliki **Actionable Title**: judul yang sudah menyatakan kesimpulan.

```
❌ SALAH:  "Revenue Q3 2024"
✅ BENAR:  "Revenue Q3 melampaui target 12% — momentum perlu dijaga di Q4"

❌ SALAH:  "Update Insiden Produksi"
✅ BENAR:  "Insiden Lini 3 terkendali — potensi delay 2 minggu masih dapat dimitigasi"
```

### Traffic Light Status

Gunakan sistem status konsisten di semua deck:

| Status | Warna | Kode | Kondisi |
|---|---|---|---|
| On Track | Hijau `2E7D32` | 🟢 | ≥ 90% target |
| At Risk | Amber `F57C00` | 🟡 | 70–89% target |
| Off Track | Merah `CC0000` | 🔴 | < 70% target |

### "So What?" Test

Setiap slide harus lulus: *"Apa yang perlu dilakukan Board setelah membaca slide ini?"*
Jika tidak ada implikasi atau keputusan → slide tersebut tidak perlu ada.

### Jumlah Slide per Deck

| Deck Type | Ideal | Maksimum |
|---|---|---|
| QBR | 12–15 slide | 20 slide |
| Crisis Briefing | 5–8 slide | 10 slide |
| HR Monthly | 8–12 slide | 15 slide |

---

## INTEGRASI SKILL LAIN

| Kebutuhan | Skill |
|---|---|
| Data OKR untuk QBR | `ceo-strategic-planning` (M3) |
| Framing argumen Board | `consulting-frameworks` |
| Tone & brand Polytron | `polytron-persona` |
| Versi dokumen Word | `docx` skill |

---

## REFERENSI FILE

Baca **hanya** reference file sesuai deck type yang dikerjakan:

- `references/qbr-deck.md` — Struktur, slide sequence, dan template konten QBR
- `references/crisis-deck.md` — Struktur Crisis/Issue Briefing, Issue Card framework
- `references/hr-monthly-deck.md` — Struktur HR Monthly, people metrics, template slide
- `references/pptx-components.md` — Reusable code snippets: header, footer, KPI card, traffic light, chart
