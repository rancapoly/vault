# Visual System — Spesifikasi Teknis Polytron

## Warna dalam Berbagai Format

### Warna Primer
| Nama | HEX | RGB | CMYK (Print) |
|------|-----|-----|--------------|
| Polytron Red | `#E8002D` | 232, 0, 45 | 0, 100, 81, 9 |
| Pure White | `#FFFFFF` | 255, 255, 255 | 0, 0, 0, 0 |
| Deep Black | `#1A1A1A` | 26, 26, 26 | 0, 0, 0, 90 |

### Warna Sekunder
| Nama | HEX | RGB | Penggunaan Utama |
|------|-----|-----|-----------------|
| Polytron Yellow | `#F5C518` | 245, 197, 24 | HR Learning, badge, callout |
| Charcoal | `#2C2C2C` | 44, 44, 44 | Background dark, heading bold |
| Light Gray BG | `#F5F5F5` | 245, 245, 245 | Background netral slide/dokumen |
| Medium Gray | `#9E9E9E` | 158, 158, 158 | Teks sekunder, caption |
| Dark Gray | `#4A4A4A` | 74, 74, 74 | Body text, paragraf |
| Divider Gray | `#DDDDDD` | 221, 221, 221 | Border tabel, garis pemisah |

### Warna Aksen
| Nama | HEX | Konteks |
|------|-----|---------|
| Alert Red Dark | `#CC0000` | Sanksi, pelanggaran, larangan keras |
| Success Green | `#2E7D32` | Approved, positif, centang |
| Info Blue | `#1565C0` | Link, referensi, catatan informasi |

---

## Grid System

### Untuk Presentasi (16:9 — 1920×1080px)
- **Safe zone:** 80px dari semua tepi
- **Gutter antar kolom:** 24px
- **Layout 2 kolom:** 50%/50% atau 40%/60%
- **Logo area (kiri atas):** max 200×60px, posisi: 60px dari kiri, 40px dari atas
- **Footer height:** 40px, posisi: 0px dari bawah
- **Footer content padding:** 60px kiri, 60px kanan

### Untuk Dokumen A4 (DOCX/PDF)
- **Margin atas:** 2.54cm
- **Margin bawah:** 2.54cm
- **Margin kiri:** 3.17cm (lebih besar untuk binding)
- **Margin kanan:** 2.54cm
- **Header height:** 1.5cm
- **Footer height:** 1.25cm
- **Gutter (binding):** 0.5cm tambahan di kiri

---

## Tipografi — Spesifikasi Detail

### Hierarki Font untuk Presentasi (PPTX)
| Level | Font | Style | Ukuran | Warna Default |
|-------|------|-------|--------|---------------|
| Judul Slide Utama (H1) | Montserrat | ExtraBold | 40–60pt | `#1A1A1A` atau `#FFFFFF` |
| Sub-judul (H2) | Montserrat | Bold | 28–36pt | `#1A1A1A` atau `#E8002D` |
| Heading Konten (H3) | Montserrat | SemiBold | 20–24pt | `#1A1A1A` |
| Body / Bullet | Montserrat | Regular | 14–18pt | `#4A4A4A` |
| Caption / Label | Montserrat | Medium | 10–12pt | `#9E9E9E` |
| Footer | Open Sans | Regular | 9–10pt | `#9E9E9E` atau `#FFFFFF` |

### Hierarki Font untuk Dokumen (DOCX)
| Level | Font | Style | Ukuran | Warna |
|-------|------|-------|--------|-------|
| Judul Dokumen | Montserrat / Arial | Bold | 18–24pt | `#1A1A1A` |
| Heading 1 | Montserrat / Arial | Bold | 14–16pt | `#E8002D` |
| Heading 2 | Montserrat / Arial | SemiBold | 12–13pt | `#1A1A1A` |
| Heading 3 | Montserrat / Arial | Medium | 11–12pt | `#2C2C2C` |
| Body Normal | Open Sans / Arial | Regular | 10–11pt | `#4A4A4A` |
| Tabel Header | Montserrat / Arial | Bold | 10pt | `#FFFFFF` |
| Tabel Cell | Open Sans / Arial | Regular | 9–10pt | `#1A1A1A` |
| Footer | Open Sans / Arial | Regular | 8–9pt | `#9E9E9E` |

### Line Spacing
- Heading: 1.0–1.15 line spacing
- Body text dokumen: 1.15–1.5
- Slide body: 1.1–1.3
- Before paragraph: 6pt; After paragraph: 6pt

---

## Elemen Visual Spesifik

### Red Accent Bar (Elemen Signature)
- Digunakan di slide cover sebagai pembatas vertikal di kiri logo
- Ukuran: 4–6px lebar, 60–80% tinggi area header
- Warna: `#E8002D`
- Fungsi: memisahkan logo dari judul, memberikan kesan tegas

### Footer Bar Merah (Signature Slide)
- Tinggi: 38–45px
- Background: `#E8002D`
- Konten: URL kiri | Nama Divisi kanan
- Font: 9–10pt, white, regular
- Posisi: benar-benar di bagian paling bawah slide

### Kotak Callout
```
Tipe 1 — Kritis/Warning:
  Background: #E8002D | Teks: #FFFFFF | Border: none

Tipe 2 — Penting/Definisi:
  Background: #F5C518 | Teks: #1A1A1A | Border: none

Tipe 3 — Informasi:
  Background: #F5F5F5 | Teks: #4A4A4A | Border: 1px #DDDDDD

Tipe 4 — Sukses/Konfirmasi:
  Background: #E8F5E9 | Teks: #2E7D32 | Border: 1px #A5D6A7
```

### Tabel Standard
```
Header Row:
  Background: #E8002D (untuk unit C&B, GCG)
              #F5C518 (untuk unit HR Learning, OD)
  Teks: #FFFFFF (di atas merah) | #1A1A1A (di atas kuning)
  Font: Bold

Data Row Ganjil: #FFFFFF
Data Row Genap: #F9F9F9
Border: 1px #DDDDDD

Total/Summary Row:
  Background: #2C2C2C | Teks: #FFFFFF | Font: Bold
```

### Badge / Label
- Shape: Rounded rectangle (radius 4px) atau pill shape
- Warna background sesuai konteks:
  - Level/Grade: Merah untuk level tinggi, kuning untuk menengah, abu untuk dasar
  - Status: Hijau = approved, Merah = rejected, Kuning = pending
- Ukuran teks: 8–10pt, uppercase, bold

---

## Diagram dan Flowchart

### Konvensi Warna dalam Diagram
Berdasarkan dokumen CBHRM:
- **Kotak Proses:** Background `#F5C518`, border `#2C2C2C`, teks `#1A1A1A`
- **Diamond Keputusan:** Background `#F5C518`, border `#2C2C2C`, teks `#1A1A1A`
- **Start/End (Oval/Capsule):** Background `#F5C518`, teks `#1A1A1A`
- **Arrow/Connector:** `#2C2C2C`, ketebalan 1.5–2pt
- **Label panah Yes/No:** Font kecil, abu gelap

### Pie/Donut Chart
- Urutan warna: Merah → Kuning → Abu gelap → Abu terang
- Background chart: Transparan / putih
- Label: Di luar chart, dengan garis leader tipis

### Bar Chart / Column Chart
- Bar warna primer: `#E8002D`
- Bar komparatif: `#F5C518` (pembanding) + `#9E9E9E` (benchmark)
- Grid lines: `#EEEEEE`, sangat tipis
- Axis labels: 9–10pt, `#4A4A4A`

---

## Do's and Don'ts Visual

### DO ✅
- Gunakan banyak white space — Polytron lebih suka clean daripada penuh
- Satu pesan utama per slide
- Konsisten gunakan palet yang sudah ditentukan
- Foto berkualitas tinggi dengan resolusi minimal 150dpi
- Alignment ketat — semua elemen rata terhadap grid
- Gunakan nomor/angka besar sebagai visual "anchor" untuk data penting

### DON'T ❌
- Jangan menggunakan lebih dari 3 warna dominant dalam satu halaman
- Jangan stretched atau distorsi logo/gambar
- Jangan font berbeda-beda dalam satu dokumen (maks. 2 font family)
- Jangan teks kecil di atas background merah — minimal 10pt, bold
- Jangan wallpaper/pattern yang ramai sebagai latar
- Jangan shadow dan gradient yang berlebihan
- Jangan clip art atau ikon usang (gunakan flat icon yang bersih)
