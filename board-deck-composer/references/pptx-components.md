# PPTX Components — Reusable Code Snippets
## Board Deck Composer — Polytron

File ini berisi komponen pptxgenjs yang siap digunakan di semua deck type.
Import dan adaptasi sesuai kebutuhan.

---

## SETUP DASAR

```javascript
const pptxgen = require("pptxgenjs");
const pres = new pptxgen();
pres.layout = 'LAYOUT_16x9'; // 10" × 5.625"

// Polytron Color Constants
const C = {
  RED:       "E8002D",
  DARK_RED:  "CC0000",
  BLACK:     "1A1A1A",
  CHARCOAL:  "2C2C2C",
  DARKGRAY:  "4A4A4A",
  MIDGRAY:   "9E9E9E",
  LIGHTGRAY: "F5F5F5",
  WHITE:     "FFFFFF",
  YELLOW:    "F5C518",
  GREEN:     "2E7D32",
  GREEN_LT:  "E8F5E9",
  AMBER:     "F57C00",
  AMBER_LT:  "FFF3E0",
  RED_LT:    "FDECEA",
};

// Slide dimensions
const W = 10, H = 5.625;
const MARGIN = 0.4;
const HEADER_H = 0.72;
const FOOTER_H = 0.35;
const CONTENT_Y = HEADER_H + 0.15;
const CONTENT_H = H - HEADER_H - FOOTER_H - 0.15;
```

---

## KOMPONEN 1 — SLIDE HEADER

```javascript
// Header merah (untuk slide konten standar)
function addRedHeader(slide, title, sectionLabel = null) {
  // Background bar
  slide.addShape(pres.shapes.RECTANGLE, {
    x: 0, y: 0, w: W, h: HEADER_H,
    fill: { color: C.RED }, line: { color: C.RED }
  });
  // Logo placeholder (kiri)
  slide.addText("POLYTRON", {
    x: MARGIN, y: 0.08, w: 2.2, h: 0.38,
    fontSize: 18, bold: true, color: C.WHITE, fontFace: "Arial Black",
    valign: "middle", margin: 0
  });
  // Section label jika ada (kanan)
  if (sectionLabel) {
    slide.addText(sectionLabel, {
      x: 6.5, y: 0.06, w: 3.1, h: 0.22,
      fontSize: 9, color: "FFCCCC", fontFace: "Arial",
      align: "right", valign: "top", margin: 0
    });
  }
  // Judul slide
  slide.addText(title, {
    x: MARGIN, y: 0.3, w: W - MARGIN * 2, h: 0.38,
    fontSize: 14, bold: true, color: C.WHITE, fontFace: "Arial",
    valign: "middle", margin: 0
  });
}

// Header charcoal (untuk slide keputusan / crisis)
function addDarkHeader(slide, title, sectionLabel = null) {
  slide.addShape(pres.shapes.RECTANGLE, {
    x: 0, y: 0, w: W, h: HEADER_H,
    fill: { color: C.CHARCOAL }, line: { color: C.CHARCOAL }
  });
  slide.addText("POLYTRON", {
    x: MARGIN, y: 0.08, w: 2.2, h: 0.38,
    fontSize: 18, bold: true, color: C.RED, fontFace: "Arial Black",
    valign: "middle", margin: 0
  });
  if (sectionLabel) {
    slide.addText(sectionLabel, {
      x: 6.5, y: 0.06, w: 3.1, h: 0.22,
      fontSize: 9, color: C.MIDGRAY, fontFace: "Arial",
      align: "right", valign: "top", margin: 0
    });
  }
  slide.addText(title, {
    x: MARGIN, y: 0.3, w: W - MARGIN * 2, h: 0.38,
    fontSize: 14, bold: true, color: C.WHITE, fontFace: "Arial",
    valign: "middle", margin: 0
  });
}
```

---

## KOMPONEN 2 — SLIDE FOOTER

```javascript
function addFooter(slide, pageNum, totalPages, dateStr, deckTitle) {
  // Background bar
  slide.addShape(pres.shapes.RECTANGLE, {
    x: 0, y: H - FOOTER_H, w: W, h: FOOTER_H,
    fill: { color: C.LIGHTGRAY }, line: { color: "DDDDDD", width: 0.5 }
  });
  // Kiri: URL perusahaan
  slide.addText("www.polytron.co.id", {
    x: MARGIN, y: H - FOOTER_H + 0.05, w: 3, h: 0.25,
    fontSize: 8, color: C.MIDGRAY, fontFace: "Arial", valign: "middle", margin: 0
  });
  // Tengah: Judul deck
  slide.addText(`${deckTitle} | STRICTLY CONFIDENTIAL`, {
    x: 3, y: H - FOOTER_H + 0.05, w: 4, h: 0.25,
    fontSize: 8, color: C.MIDGRAY, fontFace: "Arial",
    align: "center", valign: "middle", margin: 0
  });
  // Kanan: Nomor halaman + tanggal
  slide.addText(`${dateStr}  |  ${pageNum} / ${totalPages}`, {
    x: 7, y: H - FOOTER_H + 0.05, w: 2.6, h: 0.25,
    fontSize: 8, color: C.MIDGRAY, fontFace: "Arial",
    align: "right", valign: "middle", margin: 0
  });
}
```

---

## KOMPONEN 3 — KPI CARD (Stat Callout)

```javascript
// Single KPI card dengan angka besar, label, trend, dan traffic light
// x, y, w, h: posisi dan ukuran card
// data: { value, label, trend, status, subtext }
// status: "green" | "amber" | "red"
function addKpiCard(slide, x, y, w, h, data) {
  const statusColors = { green: C.GREEN, amber: C.AMBER, red: C.DARK_RED };
  const statusFills  = { green: C.GREEN_LT, amber: C.AMBER_LT, red: C.RED_LT };

  // Card background
  slide.addShape(pres.shapes.RECTANGLE, {
    x, y, w, h,
    fill: { color: C.WHITE },
    line: { color: "DDDDDD", width: 0.75 },
    shadow: { type: "outer", color: "000000", opacity: 0.08, blur: 4, offset: 2, angle: 135 }
  });

  // Status top bar (thin, colored)
  slide.addShape(pres.shapes.RECTANGLE, {
    x, y, w: w, h: 0.05,
    fill: { color: statusColors[data.status] },
    line: { color: statusColors[data.status] }
  });

  // Value (besar)
  slide.addText(data.value, {
    x: x + 0.1, y: y + 0.08, w: w - 0.2, h: h * 0.45,
    fontSize: 32, bold: true, color: C.BLACK, fontFace: "Arial Black",
    align: "center", valign: "middle", margin: 0
  });

  // Label
  slide.addText(data.label, {
    x: x + 0.1, y: y + h * 0.52, w: w - 0.2, h: 0.3,
    fontSize: 10, bold: false, color: C.DARKGRAY, fontFace: "Arial",
    align: "center", valign: "top", margin: 0
  });

  // Trend + subtext
  if (data.subtext) {
    slide.addText(data.subtext, {
      x: x + 0.1, y: y + h * 0.74, w: w - 0.2, h: 0.22,
      fontSize: 9, color: statusColors[data.status], fontFace: "Arial",
      align: "center", bold: true, margin: 0
    });
  }
}
```

---

## KOMPONEN 4 — TRAFFIC LIGHT DOT

```javascript
// Lingkaran status kecil (traffic light)
function addStatusDot(slide, x, y, size, status) {
  const colors = { green: C.GREEN, amber: C.AMBER, red: C.DARK_RED, gray: C.MIDGRAY };
  slide.addShape(pres.shapes.OVAL, {
    x, y, w: size, h: size,
    fill: { color: colors[status] || C.MIDGRAY },
    line: { color: colors[status] || C.MIDGRAY }
  });
}
```

---

## KOMPONEN 5 — SECTION DIVIDER SLIDE

```javascript
// Slide pemisah antar section (background merah, teks besar)
function addSectionDivider(pres, sectionNum, sectionTitle, sectionSubtitle = "") {
  const slide = pres.addSlide();
  slide.background = { color: C.RED };

  slide.addText("POLYTRON", {
    x: MARGIN, y: 0.3, w: 3, h: 0.4,
    fontSize: 16, bold: true, color: C.WHITE, fontFace: "Arial Black", margin: 0
  });

  slide.addText(`0${sectionNum}`, {
    x: MARGIN, y: 1.2, w: 1.5, h: 1.5,
    fontSize: 80, bold: true, color: "FFFFFF", fontFace: "Arial Black",
    valign: "middle", margin: 0
  });

  slide.addText(sectionTitle, {
    x: MARGIN, y: 2.7, w: W - MARGIN * 2, h: 0.9,
    fontSize: 32, bold: true, color: C.WHITE, fontFace: "Arial Black",
    valign: "middle", margin: 0
  });

  if (sectionSubtitle) {
    slide.addText(sectionSubtitle, {
      x: MARGIN, y: 3.6, w: W - MARGIN * 2, h: 0.4,
      fontSize: 14, color: "FFCCCC", fontFace: "Arial", margin: 0
    });
  }
  return slide;
}
```

---

## KOMPONEN 6 — DATA TABLE (KPI TABLE)

```javascript
// Tabel KPI dengan header merah dan alternating rows
// headers: array of {text, w} — w dalam inches
// rows: array of arrays
// statusCol: index kolom status (akan ditambah dot), atau null
function addKpiTable(slide, x, y, w, headers, rows) {
  const colW = headers.map(h => h.w);
  const tableData = [];

  // Header row
  tableData.push(headers.map(h => ({
    text: h.text,
    options: {
      fill: { color: C.CHARCOAL },
      color: C.WHITE, bold: true,
      fontSize: 10, fontFace: "Arial",
      align: "center", valign: "middle",
      margin: [4, 6, 4, 6]
    }
  })));

  // Data rows
  rows.forEach((row, i) => {
    tableData.push(row.map((cell, j) => ({
      text: typeof cell === 'object' ? cell.text : cell,
      options: {
        fill: { color: i % 2 === 0 ? C.WHITE : C.LIGHTGRAY },
        color: typeof cell === 'object' ? (cell.color || C.DARKGRAY) : C.DARKGRAY,
        bold: typeof cell === 'object' ? (cell.bold || false) : false,
        fontSize: 10, fontFace: "Arial",
        align: j === 0 ? "left" : "center",
        valign: "middle",
        margin: [4, 6, 4, 6]
      }
    })));
  });

  slide.addTable(tableData, {
    x, y, w, colW,
    border: { pt: 0.5, color: "DDDDDD" }
  });
}
```

---

## KOMPONEN 7 — ISSUE CARD (4-BOX)

```javascript
// 4-box issue card untuk Crisis Briefing slide 2
// boxes: [{title, content, bg, titleColor}]
function addFourBoxIssueCard(slide, x, y, w, h, boxes) {
  const bw = w / 2 - 0.05;
  const bh = h / 2 - 0.05;
  const positions = [
    {bx: x, by: y},
    {bx: x + bw + 0.1, by: y},
    {bx: x, by: y + bh + 0.1},
    {bx: x + bw + 0.1, by: y + bh + 0.1}
  ];

  boxes.slice(0, 4).forEach((box, i) => {
    const {bx, by} = positions[i];
    // Box background
    slide.addShape(pres.shapes.RECTANGLE, {
      x: bx, y: by, w: bw, h: bh,
      fill: { color: box.bg || C.LIGHTGRAY },
      line: { color: "DDDDDD", width: 0.5 }
    });
    // Box title
    slide.addText(box.title, {
      x: bx + 0.1, y: by + 0.08, w: bw - 0.2, h: 0.3,
      fontSize: 11, bold: true, color: box.titleColor || C.WHITE,
      fontFace: "Arial", margin: 0
    });
    // Box content
    slide.addText(box.content, {
      x: bx + 0.1, y: by + 0.42, w: bw - 0.2, h: bh - 0.55,
      fontSize: 10, color: box.textColor || C.DARKGRAY,
      fontFace: "Arial", valign: "top", margin: 0
    });
  });
}
```

---

## KOMPONEN 8 — COVER SLIDE

```javascript
// Cover slide merah (QBR / Strategic)
function addRedCoverSlide(pres, title, subtitle, period, audience, deckType) {
  const slide = pres.addSlide();
  slide.background = { color: C.RED };

  slide.addText("POLYTRON", {
    x: MARGIN, y: 0.35, w: 4, h: 0.55,
    fontSize: 28, bold: true, color: C.WHITE, fontFace: "Arial Black", margin: 0
  });
  slide.addText("PT Hartono Istana Teknologi", {
    x: MARGIN, y: 0.88, w: 5, h: 0.28,
    fontSize: 11, color: "FFCCCC", fontFace: "Arial", margin: 0
  });
  slide.addText(deckType.toUpperCase(), {
    x: MARGIN, y: 1.6, w: W - MARGIN * 2, h: 0.35,
    fontSize: 13, bold: true, color: "FFCCCC", fontFace: "Arial",
    charSpacing: 4, margin: 0
  });
  slide.addText(title, {
    x: MARGIN, y: 1.95, w: W - MARGIN * 2, h: 1.4,
    fontSize: 34, bold: true, color: C.WHITE, fontFace: "Arial Black",
    valign: "top", margin: 0
  });
  slide.addText(subtitle, {
    x: MARGIN, y: 3.4, w: W - MARGIN * 2, h: 0.4,
    fontSize: 16, color: "FFDDDD", fontFace: "Arial", margin: 0
  });
  slide.addText(`Periode: ${period}`, {
    x: MARGIN, y: 3.9, w: 4, h: 0.28,
    fontSize: 11, color: "FFDDDD", fontFace: "Arial", margin: 0
  });
  slide.addText(`Untuk: ${audience}`, {
    x: MARGIN, y: 4.18, w: 6, h: 0.28,
    fontSize: 11, color: "FFDDDD", fontFace: "Arial", margin: 0
  });
  slide.addText("STRICTLY CONFIDENTIAL", {
    x: MARGIN, y: 4.96, w: W - MARGIN * 2, h: 0.28,
    fontSize: 10, bold: true, color: "FF9999", fontFace: "Arial", margin: 0
  });
  return slide;
}

// Cover slide charcoal (HR Monthly / Crisis)
function addDarkCoverSlide(pres, title, subtitle, period, audience, deckType, tagline = "") {
  const slide = pres.addSlide();
  slide.background = { color: C.CHARCOAL };

  slide.addText("POLYTRON", {
    x: MARGIN, y: 0.35, w: 4, h: 0.55,
    fontSize: 28, bold: true, color: C.RED, fontFace: "Arial Black", margin: 0
  });
  slide.addText("PT Hartono Istana Teknologi", {
    x: MARGIN, y: 0.88, w: 5, h: 0.28,
    fontSize: 11, color: C.MIDGRAY, fontFace: "Arial", margin: 0
  });
  slide.addText(deckType.toUpperCase(), {
    x: MARGIN, y: 1.6, w: W - MARGIN * 2, h: 0.35,
    fontSize: 13, bold: true, color: C.MIDGRAY, fontFace: "Arial",
    charSpacing: 4, margin: 0
  });
  slide.addText(title, {
    x: MARGIN, y: 1.95, w: W - MARGIN * 2, h: 1.4,
    fontSize: 34, bold: true, color: C.WHITE, fontFace: "Arial Black",
    valign: "top", margin: 0
  });
  slide.addText(subtitle, {
    x: MARGIN, y: 3.4, w: W - MARGIN * 2, h: 0.4,
    fontSize: 16, color: C.LIGHTGRAY, fontFace: "Arial", margin: 0
  });
  slide.addText(`Periode: ${period}`, {
    x: MARGIN, y: 3.9, w: 4, h: 0.28,
    fontSize: 11, color: C.MIDGRAY, fontFace: "Arial", margin: 0
  });
  slide.addText(`Untuk: ${audience}`, {
    x: MARGIN, y: 4.18, w: 6, h: 0.28,
    fontSize: 11, color: C.MIDGRAY, fontFace: "Arial", margin: 0
  });
  if (tagline) {
    slide.addText(`"${tagline}"`, {
      x: MARGIN, y: 4.5, w: W - MARGIN * 2, h: 0.28,
      fontSize: 10, italic: true, color: C.MIDGRAY, fontFace: "Arial", margin: 0
    });
  }
  slide.addText("STRICTLY CONFIDENTIAL", {
    x: MARGIN, y: 4.96, w: W - MARGIN * 2, h: 0.28,
    fontSize: 10, bold: true, color: C.DARK_RED, fontFace: "Arial", margin: 0
  });
  return slide;
}
```

---

## KOMPONEN 9 — CLOSING SLIDE

```javascript
function addClosingSlide(pres, commitment, nextMeeting, bgColor = C.RED) {
  const slide = pres.addSlide();
  slide.background = { color: bgColor };
  const textColor = bgColor === C.RED ? C.WHITE : C.WHITE;

  slide.addText("POLYTRON", {
    x: MARGIN, y: 0.4, w: 4, h: 0.5,
    fontSize: 22, bold: true, color: bgColor === C.RED ? C.WHITE : C.RED,
    fontFace: "Arial Black", margin: 0
  });
  slide.addText("Terima kasih.", {
    x: MARGIN, y: 1.5, w: W - MARGIN * 2, h: 1.0,
    fontSize: 44, bold: true, color: textColor, fontFace: "Arial Black",
    valign: "middle", margin: 0
  });
  slide.addText(commitment, {
    x: MARGIN, y: 2.6, w: W - MARGIN * 2, h: 0.8,
    fontSize: 15, italic: true, color: bgColor === C.RED ? "FFDDDD" : C.LIGHTGRAY,
    fontFace: "Arial", margin: 0
  });
  slide.addText(`Next Meeting: ${nextMeeting}`, {
    x: MARGIN, y: 4.5, w: W - MARGIN * 2, h: 0.35,
    fontSize: 11, color: bgColor === C.RED ? "FFCCCC" : C.MIDGRAY,
    fontFace: "Arial", margin: 0
  });
  return slide;
}
```

---

## PENGGUNAAN

Import komponen sesuai kebutuhan per deck type:

```javascript
// Di file utama deck
// 1. Setup pres + constants
// 2. Panggil addRedCoverSlide() atau addDarkCoverSlide()
// 3. Untuk setiap slide: addSlide() + addRedHeader() + konten + addFooter()
// 4. pres.writeFile({ fileName: "output.pptx" })
```
