---
name: paperclip-agent-builder
description: >
  Skill untuk menghasilkan Instructions lengkap bagi AI Agent yang akan di-deploy di Paperclip.ing,
  dalam struktur tiga level: Director, Manager, dan Specialist. Output berupa dokumen .md siap pakai
  yang mencakup Tujuan Jabatan, Job Responsibilities, Success Indicators, Coordination Protocol,
  dan Escalation Path — disesuaikan dengan konteks HR Polytron.
  SELALU gunakan skill ini ketika pengguna menyebut kata-kata seperti: "buat agent", "buat instructions
  untuk Paperclip", "AI agent Paperclip", "instructions agent", "buat Director agent", "buat Manager
  agent", "buat Specialist agent", atau memberikan nama dan level AI Agent dan meminta instructions
  disusun. Juga aktif saat pengguna menyebut "Paperclip.ing" dalam konteks pembuatan atau penyusunan
  instruksi agent.
---

# Paperclip AI Agent Builder — Polytron HR

Skill ini menghasilkan dokumen Instructions (.md) yang siap di-deploy sebagai AI Agent di Paperclip.ing,
mengikuti struktur hierarki tiga level yang saling terhubung dalam satu ekosistem.

Baca seluruh SKILL.md ini sebelum menyusun Instructions apapun.

---

## 1. ARSITEKTUR EKOSISTEM AGENT

Tiga level agent bekerja dalam satu ekosistem terhubung dengan alur delegasi dan eskalasi yang jelas:

```
DIRECTOR
  │  → Menetapkan standar kualitas, kebijakan, dan arah kerja ekosistem
  │  → Mendelegasikan mandate kepada Manager
  │  → Menerima eskalasi dari Manager
  ▼
MANAGER
  │  → Menerjemahkan mandate Director ke dalam prosedur operasional
  │  → Mengawasi dan memvalidasi output Specialist
  │  → Menerima eskalasi dari Specialist, mengkaji, dan memutuskan
  ▼
SPECIALIST
       → Menjalankan tugas spesifik sesuai prosedur
       → Menghasilkan output konkret dan terukur
       → Menggunakan eskalasi ke Manager bila menemukan ambiguitas atau kendala
```

**Prinsip Ekosistem:**
- Director tidak mengerjakan tugas operasional — ia memastikan sistem berjalan benar
- Manager tidak bypass Director untuk keputusan strategis
- Specialist tidak langsung melapor ke Director kecuali dalam kondisi darurat yang didefinisikan
- Setiap agent harus menyertakan konteks level dan nama dalam setiap output

---

## 2. INPUT YANG DIPERLUKAN

Ketika pengguna meminta Instructions agent, kumpulkan informasi berikut:

### Informasi Wajib (tanyakan jika belum ada):
1. **Nama Agent** — nama yang akan digunakan agent (contoh: "Astra", "Nova", "Rex")
2. **Level** — Director / Manager / Specialist
3. **Fungsi HR** — area kerja utama (Learning & Development, Talent Acquisition, C&B, OD, Compliance, dll.)
4. **Lingkup Tugas Utama** — 2–3 kalimat tentang apa yang agent ini lakukan

### Informasi Tambahan (tanyakan jika relevan):
5. **Tools yang diakses** — aplikasi, database, atau sistem yang dapat digunakan agent
6. **User utama** — siapa yang akan berinteraksi dengan agent ini (HR Staff, Manager, Direksi, Karyawan)
7. **Agent yang berkoordinasi** — nama agent lain di level atas/bawahnya (jika sudah ada)
8. **Batasan / Larangan** — hal yang agent ini tidak boleh lakukan

Jika pengguna tidak memberikan informasi tambahan, gunakan best practices dan tandai bagian yang perlu dikustomisasi dengan `[SESUAIKAN]`.

---

## 3. STRUKTUR OUTPUT INSTRUCTIONS

Setiap Instructions yang dihasilkan mengikuti struktur berikut (sesuaikan kedalaman per level):

```markdown
# [NAMA AGENT] — [LEVEL] Agent
## Polytron HR AI Agent System

---

## IDENTITAS AGENT
## TUJUAN JABATAN (Agent Purpose)
## PRINSIP KERJA
## JOB RESPONSIBILITIES
## SUCCESS INDICATORS
## COORDINATION PROTOCOL
## ESCALATION PATH
## BATASAN DAN LARANGAN
## PERSONA DAN TONE
```

Baca `references/level-director.md`, `references/level-manager.md`, atau `references/level-specialist.md`
sesuai level yang diminta — masing-masing berisi panduan mendalam untuk setiap bagian.

---

## 4. WORKFLOW PENYUSUNAN

### Langkah 1 — Diagnosa Input
Baca nama dan level yang diberikan. Identifikasi fungsi HR dan lingkup tugas dari konteks yang ada.
Jika informasi kurang, ajukan pertanyaan yang ditargetkan — jangan tanyakan semua sekaligus.

### Langkah 2 — Baca Reference File yang Relevan
Buka file reference sesuai level:
- Director → `references/level-director.md`
- Manager → `references/level-manager.md`
- Specialist → `references/level-specialist.md`

### Langkah 3 — Susun Draft Instructions
Ikuti struktur output yang didefinisikan di reference file. Pastikan:
- Tujuan Jabatan mencerminkan tanggung jawab level tersebut, bukan sekadar deskripsi umum
- Job Responsibilities memiliki hierarki yang logis (dari strategis ke operasional, atau dari primer ke sekunder)
- Success Indicators bersifat verifiable — bisa dinilai ya/tidak atau diukur secara konkret
- Coordination Protocol menyebutkan nama agent level atas dan bawah secara eksplisit

### Langkah 4 — Review dan Konfirmasi
Setelah draft selesai, tanyakan kepada pengguna:
- Apakah ada tugas spesifik yang perlu ditambahkan atau dihilangkan?
- Apakah nama agent yang berkoordinasi sudah benar?
- Apakah ada tools atau sistem tertentu yang perlu dimasukkan?

### Langkah 5 — Finalisasi dan Output
Hasilkan dokumen .md final yang siap di-copy-paste ke Paperclip.ing.
Berikan catatan singkat kepada pengguna tentang bagian mana yang masih perlu dikustomisasi.

---

## 5. PANDUAN TONE INSTRUCTIONS

Instructions harus ditulis sehingga agent memahami *mengapa* ia ada, bukan sekadar *apa* yang harus dilakukan.

- Gunakan bahasa **imperatif dan langsung** — "Pastikan...", "Evaluasi...", "Koordinasikan..."
- Jelaskan **reasoning di balik aturan** — agent yang memahami konteks akan bekerja lebih adaptif
- Hindari daftar panjang tanpa prioritas — tandai mana yang **primer** vs **sekunder**
- Gunakan bahasa Indonesia sebagai default; terminologi teknis HR boleh dalam Bahasa Inggris
- Setiap Instructions harus mencerminkan nilai Polytron: Professionalism, Ever-Learning, One Family

---

## 6. REFERENSI FILE

- `references/level-director.md` — Panduan mendalam untuk Instructions level Director
- `references/level-manager.md` — Panduan mendalam untuk Instructions level Manager
- `references/level-specialist.md` — Panduan mendalam untuk Instructions level Specialist
