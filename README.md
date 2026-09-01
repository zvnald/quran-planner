<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>خطة القرآن الكريم</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Tajawal:wght@400;500;700;900&display=swap');

  :root {
    --espresso: #2b1c13;
    --coffee: #4a3020;
    --cinnamon: #7a5236;
    --caramel: #a8794f;
    --latte: #cba573;
    --sand: #e7d7bd;
    --linen: #f6efe3;
    --paper: #fffdfa;
  }

  * { box-sizing: border-box; }
  html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    max-width: 100%;
    overflow-x: hidden;
  }

  .app-shell {
    min-height: 100vh;
    width: 100%;
    /* Faint decorative Islamic geometric watermark layered above the warm gradient.
       The SVG's own stroke-opacity keeps it extremely subtle so it never competes with the text. */
    background-image:
      url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='150' height='150' viewBox='0 0 150 150'><g fill='none' stroke='%234a3020' stroke-opacity='0.06' stroke-width='1.2'><path d='M75 10 L90 56 L136 71 L90 86 L75 132 L60 86 L14 71 L60 56 Z'/><circle cx='75' cy='71' r='22'/><circle cx='75' cy='71' r='34'/></g></svg>"),
      linear-gradient(180deg, #ffffff 0%, #fdfbf8 35%, #f7efe2 100%);
    background-repeat: repeat, no-repeat;
    background-size: 150px 150px, 100% 100%;
    background-attachment: fixed, scroll;
    font-family: 'Tajawal', sans-serif;
    color: var(--espresso);
    padding: clamp(0.9rem, 3vw, 2.2rem) clamp(0.7rem, 4vw, 1.6rem) clamp(2rem, 5vw, 3.2rem);
    -webkit-print-color-adjust: exact;
    print-color-adjust: exact;
  }
  .container { width: 100%; max-width: 800px; margin: 0 auto; }

  /* Two-column layout on wide screens, one column on narrow — no breakpoint needed:
     each column has a minimum of 300px, so it wraps to a single column automatically
     once the available width can no longer fit two of them side by side. */
  .panel-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(min(300px, 100%), 1fr));
    gap: clamp(1rem, 3vw, 1.7rem);
    align-items: start;
  }
  .panel-col { min-width: 0; } /* prevents grid children from overflowing their track */
  .panel-col-results { margin-top: 0; }
  @media (min-width: 640px) {
    .panel-col-form { position: sticky; top: 1rem; }
  }

  /* ---- Header: dark espresso banner fading into the page ---- */
  .header-banner {
    position: relative;
    overflow: hidden;
    text-align: center;
    border-radius: clamp(18px, 3vw, 26px);
    padding: clamp(1.4rem, 4vw, 2.6rem) clamp(1rem, 4vw, 2rem) clamp(1.2rem, 3vw, 2.1rem);
    margin-bottom: clamp(1rem, 3vw, 1.6rem);
    background: linear-gradient(150deg, var(--espresso) 0%, var(--coffee) 55%, var(--cinnamon) 100%);
    box-shadow: 0 16px 34px rgba(43, 28, 19, 0.28);
  }
  .header-banner::before {
    content: "";
    position: absolute;
    inset: 0;
    background-image: radial-gradient(circle at 85% -10%, rgba(203,165,115,0.35), transparent 55%),
                       radial-gradient(circle at 8% 115%, rgba(203,165,115,0.22), transparent 55%);
    pointer-events: none;
  }
  .header .ornament { font-family: 'Amiri', serif; color: var(--latte); font-size: clamp(1.2rem, 3vw, 1.6rem); letter-spacing: 0.25rem; position: relative; }
  .header-banner h1 {
    font-family: 'Amiri', serif;
    font-weight: 700;
    font-size: clamp(1.55rem, 5vw, 2.4rem);
    margin: 0.3rem 0 0.3rem;
    color: var(--paper);
    position: relative;
  }
  .header-banner p { margin: 0; font-size: clamp(0.8rem, 2.2vw, 0.98rem); color: var(--sand); position: relative; }

  .tabs {
    display: flex;
    flex-wrap: wrap;
    background: var(--linen);
    border: 1px solid var(--sand);
    border-radius: 18px;
    padding: 4px;
    margin-bottom: clamp(1rem, 3vw, 1.4rem);
    box-shadow: inset 0 1px 3px rgba(74,48,32,0.08);
  }
  .tab-btn {
    flex: 1;
    min-width: 96px;
    border: none;
    background: transparent;
    padding: clamp(0.55rem, 2vw, 0.7rem) 0.5rem;
    min-height: 44px;
    border-radius: 14px;
    font-family: 'Tajawal', sans-serif;
    font-weight: 700;
    font-size: clamp(0.72rem, 2vw, 0.9rem);
    line-height: 1.3;
    color: var(--cinnamon);
    cursor: pointer;
    transition: all .25s ease;
  }
  .tab-btn.active {
    background: linear-gradient(135deg, var(--coffee), var(--espresso));
    color: var(--paper);
    box-shadow: 0 5px 14px rgba(43,28,19,0.3);
  }

  .mode-switch { display: flex; gap: 0.5rem; margin-bottom: 0.9rem; flex-wrap: wrap; }
  .mode-btn {
    flex: 1;
    min-width: 140px;
    min-height: 44px;
    padding: clamp(0.5rem, 1.8vw, 0.6rem) 0.4rem;
    border-radius: 12px;
    border: 1.5px solid var(--sand);
    background: var(--paper);
    font-family: 'Tajawal', sans-serif;
    font-weight: 500;
    font-size: clamp(0.78rem, 2vw, 0.88rem);
    color: var(--cinnamon);
    cursor: pointer;
    transition: all .2s ease;
  }
  .mode-btn.active {
    border-color: var(--caramel);
    background: linear-gradient(160deg, #f3e4cd, var(--linen));
    color: var(--espresso);
    font-weight: 700;
  }

  .card {
    background: var(--paper);
    border: 1px solid var(--sand);
    border-radius: clamp(14px, 2vw, 18px);
    padding: clamp(0.85rem, 3vw, 1.1rem);
    margin-bottom: 1rem;
    box-shadow: 0 4px 16px rgba(74,48,32,0.06);
    break-inside: avoid;
  }
  .field-label { display: block; font-weight: 700; font-size: clamp(0.82rem, 2vw, 0.9rem); margin-bottom: 0.55rem; color: var(--coffee); }
  .combo-section-title {
    font-family: 'Amiri', serif;
    font-weight: 700;
    font-size: clamp(1rem, 2.6vw, 1.15rem);
    color: var(--coffee);
    margin: 1.1rem 0 0.6rem;
    padding-bottom: 0.35rem;
    border-bottom: 2px solid var(--sand);
  }
  .combo-section-title:first-child { margin-top: 0; }
  .field-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(min(140px, 100%), 1fr));
    gap: 0.6rem;
  }
  .field-group {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--linen);
    border: 1px solid var(--sand);
    border-radius: 10px;
    padding: 0.5rem 0.7rem;
    min-height: 44px;
    min-width: 0;
    font-size: clamp(0.8rem, 2vw, 0.88rem);
    color: var(--cinnamon);
  }
  .field-group.wide { grid-column: 1 / -1; }
  .field-group input, .field-group select {
    width: 100%;
    min-width: 0;
    border: none;
    background: transparent;
    font-family: 'Tajawal', sans-serif;
    font-size: clamp(0.92rem, 2.4vw, 1.05rem);
    font-weight: 700;
    color: var(--espresso);
    outline: none;
  }
  .hint { font-size: clamp(0.74rem, 1.8vw, 0.8rem); color: var(--cinnamon); margin: 0.5rem 0 0; }

  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(min(96px, 100%), 1fr));
    gap: 0.55rem;
    margin-bottom: 1rem;
  }
  .stat-card {
    background: linear-gradient(160deg, var(--paper), var(--linen));
    border: 1px solid var(--sand);
    border-radius: 16px;
    padding: clamp(0.7rem, 2.5vw, 0.9rem) 0.4rem;
    text-align: center;
    break-inside: avoid;
  }
  .stat-value { font-family: 'Amiri', serif; font-weight: 700; font-size: clamp(1.15rem, 3.6vw, 1.55rem); color: var(--coffee); }
  .stat-label { font-size: clamp(0.66rem, 1.7vw, 0.72rem); color: var(--cinnamon); margin-top: 0.15rem; }

  .inspire-card {
    display: flex;
    align-items: center;
    gap: 0.6rem;
    background: linear-gradient(120deg, var(--espresso), var(--coffee));
    color: var(--linen);
    border-radius: 18px;
    padding: clamp(0.85rem, 2.5vw, 1rem) clamp(0.9rem, 3vw, 1.15rem);
    margin-bottom: 1.2rem;
    box-shadow: 0 8px 20px rgba(43,28,19,0.22);
    break-inside: avoid;
  }
  .inspire-card p { margin: 0; font-size: clamp(0.82rem, 2.1vw, 0.9rem); line-height: 1.6; }
  .inspire-icon { color: var(--latte); font-size: 1.1rem; flex-shrink: 0; }

  .beads-wrap { text-align: center; margin-bottom: 0.5rem; }
  .beads-row {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    gap: clamp(4px, 1vw, 6px);
    direction: ltr;
    margin-bottom: 0.5rem;
  }
  .bead {
    width: clamp(10px, 2.6vw, 14px);
    height: clamp(10px, 2.6vw, 14px);
    border-radius: 50%;
    background: var(--sand);
    border: 1px solid var(--latte);
    display: inline-block;
    flex-shrink: 0;
  }
  .bead-filled { background: radial-gradient(circle at 30% 30%, var(--latte), var(--coffee)); border-color: var(--coffee); }
  .beads-label { font-size: clamp(0.72rem, 1.8vw, 0.78rem); color: var(--cinnamon); }

  .week-table { margin-top: 0.3rem; }
  .week-title { font-family: 'Amiri', serif; font-size: clamp(1rem, 2.6vw, 1.1rem); margin: 0 0 0.7rem; color: var(--coffee); }
  .week-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(min(64px, 100%), 1fr)); gap: 0.5rem; }
  .day-card {
    background: var(--linen);
    border: 1px solid var(--sand);
    border-radius: 12px;
    padding: 0.6rem 0.25rem;
    text-align: center;
    min-width: 0;
  }
  .day-card.day-rest { background: #efe6d6; opacity: 0.75; }
  .day-name { display: block; font-size: clamp(0.66rem, 1.7vw, 0.72rem); color: var(--cinnamon); margin-bottom: 0.25rem; }
  .day-pages { display: block; font-weight: 700; color: var(--coffee); font-size: clamp(0.78rem, 2vw, 0.85rem); }

  .actions { display: flex; gap: 0.55rem; margin-top: 1.2rem; flex-wrap: wrap; }
  .action-btn {
    flex: 1;
    min-width: 140px;
    min-height: 48px;
    padding: clamp(0.7rem, 2.2vw, 0.8rem) 0.6rem;
    border-radius: 14px;
    border: none;
    font-family: 'Tajawal', sans-serif;
    font-weight: 700;
    font-size: clamp(0.8rem, 2vw, 0.88rem);
    cursor: pointer;
    transition: transform .15s ease, box-shadow .15s ease, opacity .15s ease;
  }
  .action-btn:active { transform: scale(0.98); }
  .action-btn:disabled { opacity: 0.65; cursor: default; }
  .action-btn.primary {
    background: linear-gradient(135deg, var(--coffee), var(--espresso));
    color: var(--paper);
    box-shadow: 0 8px 18px rgba(43,28,19,0.28);
  }
  .action-btn.secondary {
    background: var(--linen);
    color: var(--coffee);
    border: 1.5px solid var(--sand);
  }
  .save-notice { text-align: center; font-size: 0.8rem; color: var(--coffee); margin-top: 0.6rem; font-weight: 700; }

  /* ---- Print calendar (built off-screen, used only for PDF export) ---- */
  #pdf-calendar-root {
    position: fixed;
    top: -99999px;
    left: -99999px;
    width: 780px;
    background: var(--paper);
  }
  .cal-page {
    width: 780px;
    min-height: 1040px;
    background: var(--paper);
    padding: 34px 30px 26px;
    font-family: 'Tajawal', sans-serif;
    box-sizing: border-box;
  }
  .cal-page-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 2px solid var(--sand);
    padding-bottom: 14px;
    margin-bottom: 18px;
  }
  .cal-plan-title { font-family: 'Amiri', serif; font-weight: 700; font-size: 1.35rem; color: var(--coffee); margin: 0; }
  .cal-plan-sub { font-size: 0.8rem; color: var(--cinnamon); margin: 3px 0 0; }
  .cal-month-badge {
    background: linear-gradient(135deg, var(--coffee), var(--espresso));
    color: var(--paper);
    font-family: 'Amiri', serif;
    font-weight: 700;
    font-size: 1.15rem;
    padding: 10px 26px;
    border-radius: 999px;
    box-shadow: 0 6px 14px rgba(43,28,19,0.25);
  }
  .cal-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 8px; }
  .cal-dow {
    text-align: center;
    font-size: 0.78rem;
    font-weight: 700;
    color: var(--cinnamon);
    padding-bottom: 4px;
  }
  .cal-cell {
    border: 1.5px solid var(--sand);
    border-radius: 12px;
    min-height: 96px;
    padding: 7px 8px;
    background: var(--paper);
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .cal-cell.cal-empty { background: transparent; border-color: transparent; }
  .cal-cell.cal-rest { background: #efe6d6; }
  .cal-cell.cal-done { background: linear-gradient(160deg, #f3e9d6, var(--linen)); }
  .cal-date-num { font-weight: 700; font-size: 0.85rem; color: var(--coffee); align-self: flex-start; }
  .cal-task {
    font-size: 0.72rem;
    font-weight: 700;
    color: var(--espresso);
    background: var(--linen);
    border: 1px solid var(--sand);
    border-radius: 8px;
    padding: 4px 5px;
    text-align: center;
    line-height: 1.35;
  }
  .cal-task.cal-task-rest { color: var(--cinnamon); background: transparent; border-style: dashed; }

  /* ---- Combined (memorize + review) calendar cell ---- */
  .cal-cell.cal-cell-combined { min-height: 118px; }
  .cal-task-group { display: flex; flex-direction: column; gap: 4px; }
  .cal-task-mini {
    font-size: 0.62rem;
    font-weight: 700;
    border-radius: 6px;
    padding: 3px 4px;
    text-align: center;
    line-height: 1.3;
  }
  .cal-task-mini.memo { background: var(--linen); color: var(--espresso); border: 1px solid var(--sand); }
  .cal-task-mini.review { background: #efe6d6; color: var(--coffee); border: 1px dashed var(--caramel); }
  .cal-task-mini.review.is-rest { color: var(--cinnamon); background: transparent; }

  .cal-page-footer {
    margin-top: 16px;
    text-align: center;
    font-size: 0.72rem;
    color: var(--caramel);
  }
</style>
</head>
<body>
<div class="app-shell">
  <div class="container" id="container">
    <header class="header header-banner">
      <div class="ornament">﷽</div>
      <h1>خطة القرآن الكريم</h1>
      <p>خطط حفظك ومراجعتك للقرآن الكريم بخطوات واضحة</p>
    </header>

    <div class="tabs">
      <button class="tab-btn active" id="tab-memorize">خطة الحفظ</button>
      <button class="tab-btn" id="tab-review">جدول المراجعة</button>
      <button class="tab-btn" id="tab-combined">خطة شاملة (حفظ ومراجعة)</button>
    </div>

    <div id="tab-content"></div>

    <div class="actions">
      <button class="action-btn primary" id="btn-pdf">حفظ الخطة PDF</button>
      <button class="action-btn secondary" id="btn-save">حفظ الخطة</button>
    </div>
    <p class="save-notice" id="save-notice" style="display:none;"></p>
  </div>
</div>
<div id="pdf-calendar-root"></div>

<script>
(function () {
  "use strict";

  const TOTAL_PAGES = 604;
  const TOTAL_AJZA = 30;

  const SURAHS = [
    ["الفاتحة", 1], ["البقرة", 2], ["آل عمران", 50], ["النساء", 77], ["المائدة", 106],
    ["الأنعام", 128], ["الأعراف", 151], ["الأنفال", 177], ["التوبة", 187], ["يونس", 208],
    ["هود", 221], ["يوسف", 235], ["الرعد", 249], ["إبراهيم", 255], ["الحجر", 262],
    ["النحل", 267], ["الإسراء", 282], ["الكهف", 293], ["مريم", 305], ["طه", 312],
    ["الأنبياء", 322], ["الحج", 332], ["المؤمنون", 342], ["النور", 350], ["الفرقان", 359],
    ["الشعراء", 367], ["النمل", 377], ["القصص", 385], ["العنكبوت", 396], ["الروم", 404],
    ["لقمان", 411], ["السجدة", 415], ["الأحزاب", 418], ["سبأ", 428], ["فاطر", 434],
    ["يس", 440], ["الصافات", 446], ["ص", 453], ["الزمر", 458], ["غافر", 467],
    ["فصلت", 477], ["الشورى", 483], ["الزخرف", 489], ["الدخان", 496], ["الجاثية", 499],
    ["الأحقاف", 502], ["محمد", 507], ["الفتح", 511], ["الحجرات", 515], ["ق", 518],
    ["الذاريات", 520], ["الطور", 523], ["النجم", 526], ["القمر", 528], ["الرحمن", 531],
    ["الواقعة", 534], ["الحديد", 537], ["المجادلة", 542], ["الحشر", 545], ["الممتحنة", 549],
    ["الصف", 551], ["الجمعة", 553], ["المنافقون", 554], ["التغابن", 556], ["الطلاق", 558],
    ["التحريم", 560], ["الملك", 562], ["القلم", 564], ["الحاقة", 566], ["المعارج", 568],
    ["نوح", 570], ["الجن", 572], ["المزمل", 574], ["المدثر", 575], ["القيامة", 577],
    ["الإنسان", 578], ["المرسلات", 580], ["النبأ", 582], ["النازعات", 583], ["عبس", 585],
    ["التكوير", 586], ["الانفطار", 587], ["المطففين", 587], ["الانشقاق", 589], ["البروج", 590],
    ["الطارق", 591], ["الأعلى", 591], ["الغاشية", 592], ["الفجر", 593], ["البلد", 594],
    ["الشمس", 595], ["الليل", 595], ["الضحى", 596], ["الشرح", 596], ["التين", 597],
    ["العلق", 597], ["القدر", 598], ["البينة", 598], ["الزلزلة", 599], ["العاديات", 599],
    ["القارعة", 600], ["التكاثر", 600], ["العصر", 601], ["الهمزة", 601], ["الفيل", 601],
    ["قريش", 602], ["الماعون", 602], ["الكوثر", 602], ["الكافرون", 603], ["النصر", 603],
    ["المسد", 603], ["الإخلاص", 604], ["الفلق", 604], ["الناس", 604],
  ];

  const WEEK_DAYS = ["السبت", "الأحد", "الاثنين", "الثلاثاء", "الأربعاء", "الخميس", "الجمعة"];
  const STORAGE_KEY = "خطة-القرآن-الكريم-المحفوظة";

  const state = {
    tab: "memorize",
    memo: {
      mode: "duration", years: 3, months: 0, pagesPerWeek: 7,
      preMemorized: { enabled: false, mode: "range", fromPage: 1, toPage: 20, count: 20 },
    },
    review: {
      rangeMode: "pages", fromPage: 1, toPage: 20, fromSurah: 0, toSurah: 5,
      durationValue: 10, durationUnit: "days", restDay: "الجمعة",
      cyclicMode: false, cycleValue: 7, cycleUnit: "days",
      programValue: 1, programUnit: "months",
      endMode: "duration", calendarType: "gregorian", endDate: null,
    },
  };

  const startDate = new Date();

  function surahEndPage(index) {
    return index + 1 < SURAHS.length ? SURAHS[index + 1][1] - 1 || SURAHS[index][1] : TOTAL_PAGES;
  }
  function formatDate(d) {
    return d.toLocaleDateString("ar-EG", { year: "numeric", month: "long", day: "numeric" });
  }
  function addDays(base, days) {
    const d = new Date(base);
    d.setDate(d.getDate() + days);
    return d;
  }

  /* ---------------- Hijri / Gregorian conversion (تقويم تقديري مبني على الحساب الفلكي التقريبي) ---------------- */
  const HIJRI_MONTHS = ["محرم","صفر","ربيع الأول","ربيع الآخر","جمادى الأولى","جمادى الآخرة","رجب","شعبان","رمضان","شوال","ذو القعدة","ذو الحجة"];

  function gregorianToJDN(y, m, d) {
    const a = Math.floor((14 - m) / 12);
    const y2 = y + 4800 - a;
    const m2 = m + 12 * a - 3;
    return d + Math.floor((153 * m2 + 2) / 5) + 365 * y2 + Math.floor(y2 / 4) - Math.floor(y2 / 100) + Math.floor(y2 / 400) - 32045;
  }
  function jdnToGregorian(jdn) {
    const a = jdn + 32044;
    const b = Math.floor((4 * a + 3) / 146097);
    const c = a - Math.floor((146097 * b) / 4);
    const d2 = Math.floor((4 * c + 3) / 1461);
    const e = c - Math.floor((1461 * d2) / 4);
    const m2 = Math.floor((5 * e + 2) / 153);
    const day = e - Math.floor((153 * m2 + 2) / 5) + 1;
    const month = m2 + 3 - 12 * Math.floor(m2 / 10);
    const year = 100 * b + d2 - 4800 + Math.floor(m2 / 10);
    return { year, month, day };
  }
  function hijriToJDN(y, m, d) {
    return Math.floor((11 * y + 3) / 30) + 354 * y + 30 * m - Math.floor((m - 1) / 2) + d + 1948440 - 385;
  }
  function jdnToHijri(jdn) {
    let l = jdn - 1948440 + 10632;
    const n = Math.floor((l - 1) / 10631);
    l = l - 10631 * n + 354;
    const j = (Math.floor((10985 - l) / 5316)) * (Math.floor((50 * l) / 17719)) + (Math.floor(l / 5670)) * (Math.floor((43 * l) / 15238));
    l = l - (Math.floor((30 - j) / 15)) * (Math.floor((17719 * j) / 50)) - (Math.floor(j / 16)) * (Math.floor((15238 * j) / 43)) + 29;
    const m = Math.floor((24 * l) / 709);
    const d = l - Math.floor((709 * m) / 24);
    const y = 30 * n + j - 30;
    return { year: y, month: m, day: d };
  }
  function todayHijriParts() {
    const t = new Date();
    return jdnToHijri(gregorianToJDN(t.getFullYear(), t.getMonth() + 1, t.getDate()));
  }
  function formatHijriDate(date) {
    const h = jdnToHijri(gregorianToJDN(date.getFullYear(), date.getMonth() + 1, date.getDate()));
    return `${h.day} ${HIJRI_MONTHS[h.month - 1]} ${h.year}هـ`;
  }
  function formatDualDate(date) {
    return `${formatDate(date)} م (موافق ${formatHijriDate(date)})`;
  }
  // Converts a {year,month,day} triple from one calendar system to the other, keeping the same absolute day.
  function convertDateParts(fromType, toType, parts) {
    if (!parts) return null;
    if (fromType === toType) return parts;
    const jdn = fromType === "hijri" ? hijriToJDN(parts.year, parts.month, parts.day) : gregorianToJDN(parts.year, parts.month, parts.day);
    return toType === "hijri" ? jdnToHijri(jdn) : jdnToGregorian(jdn);
  }
  function defaultEndDateParts(calendarType) {
    const d = addDays(new Date(), 30);
    const g = { year: d.getFullYear(), month: d.getMonth() + 1, day: d.getDate() };
    return calendarType === "hijri" ? convertDateParts("gregorian", "hijri", g) : g;
  }
  function daysInHijriMonth() { return 30; }
  function daysInGregorianMonth(year, month) { return new Date(year, month, 0).getDate(); }

  /* ---------------- Pre-memorized pages (الحفظ المسبق) ---------------- */
  function getPreMemorizedCount(m) {
    const pm = m.preMemorized;
    if (!pm || !pm.enabled) return 0;
    let count;
    if (pm.mode === "range") {
      const from = Math.max(1, Math.min(Number(pm.fromPage) || 1, TOTAL_PAGES));
      const to = Math.max(from, Math.min(Number(pm.toPage) || from, TOTAL_PAGES));
      count = to - from + 1;
    } else {
      count = Math.max(0, Number(pm.count) || 0);
    }
    return Math.min(count, TOTAL_PAGES - 1);
  }
  function getRemainingStartPage(m) {
    return Math.min(getPreMemorizedCount(m) + 1, TOTAL_PAGES);
  }
  function getRemainingPages(m) {
    return Math.max(TOTAL_PAGES - getPreMemorizedCount(m), 1);
  }
  function beadsHTML(filled, label) {
    let spans = "";
    for (let i = 0; i < TOTAL_AJZA; i++) {
      spans += `<span class="bead${i < filled ? " bead-filled" : ""}"></span>`;
    }
    return `<div class="beads-wrap"><div class="beads-row" dir="ltr">${spans}</div><p class="beads-label">${label}</p></div>`;
  }
  function statCardHTML(value, label) {
    return `<div class="stat-card"><div class="stat-value">${value}</div><div class="stat-label">${label}</div></div>`;
  }
  function inspireHTML(text) {
    return `<div class="inspire-card"><span class="inspire-icon">✦</span><p>${text}</p></div>`;
  }

  /* ---------------- Memorization calculations ---------------- */
  function computeDuration(m) {
    const remaining = getRemainingPages(m);
    const totalMonths = Math.max(m.years * 12 + Number(m.months || 0), 1);
    const totalDays = totalMonths * 30;
    const perDay = remaining / totalDays;
    const perWeek = perDay * 7;
    const ajzaPerMonth = (perDay * 30) / 20;
    return { perDay, perWeek, ajzaPerMonth, finishDate: addDays(startDate, totalDays), totalDays, remaining };
  }
  function computePace(m) {
    const remaining = getRemainingPages(m);
    const perWeek = Math.max(Number(m.pagesPerWeek) || 0.0001, 0.0001);
    const totalWeeks = remaining / perWeek;
    const totalDays = Math.ceil(totalWeeks * 7);
    const totalYears = totalDays / 365;
    return { totalWeeks, totalDays, totalYears, finishDate: addDays(startDate, totalDays), remaining };
  }

  function buildMemoFormHTML(m, prefix) {
    let formHTML = "";
    if (m.mode === "duration") {
      formHTML = `
        <div class="card form-card">
          <label class="field-label">أريد إتمام حفظ القرآن خلال:</label>
          <div class="field-row">
            <div class="field-group">
              <input type="number" min="0" id="${prefix}memo-years" value="${m.years}" />
              <span>سنة</span>
            </div>
            <div class="field-group">
              <input type="number" min="0" max="11" id="${prefix}memo-months" value="${m.months}" />
              <span>شهر</span>
            </div>
          </div>
        </div>`;
    } else {
      formHTML = `
        <div class="card form-card">
          <label class="field-label">أستطيع حفظ هذا العدد من الصفحات أسبوعياً:</label>
          <div class="field-group wide">
            <input type="number" min="0.5" step="0.5" id="${prefix}memo-pace" value="${m.pagesPerWeek}" />
            <span>صفحة / أسبوع</span>
          </div>
        </div>`;
    }
    const pm = m.preMemorized || { enabled: false, mode: "range", fromPage: 1, toPage: 20, count: 20 };
    const preMemFieldsHTML = pm.mode === "range" ? `
        <div class="field-row">
          <div class="field-group">
            <span>من صفحة</span>
            <input type="number" min="1" max="${TOTAL_PAGES}" id="${prefix}memo-premem-from" value="${pm.fromPage}" />
          </div>
          <div class="field-group">
            <span>إلى صفحة</span>
            <input type="number" min="1" max="${TOTAL_PAGES}" id="${prefix}memo-premem-to" value="${pm.toPage}" />
          </div>
        </div>` : `
        <div class="field-group wide">
          <input type="number" min="0" max="${TOTAL_PAGES - 1}" id="${prefix}memo-premem-count" value="${pm.count}" />
          <span>صفحة محفوظة</span>
        </div>`;

    const preMemCount = getPreMemorizedCount(m);
    const preMemHTML = `
      <div class="card form-card">
        <label class="field-label">هل حفظت جزءاً من القرآن الكريم مسبقاً؟</label>
        <div class="mode-switch">
          <button class="mode-btn${!pm.enabled ? " active" : ""}" id="${prefix}memo-premem-off">لا يوجد حفظ سابق</button>
          <button class="mode-btn${pm.enabled ? " active" : ""}" id="${prefix}memo-premem-on">لديّ حفظ سابق</button>
        </div>
        ${pm.enabled ? `
        <div class="mode-switch" style="margin-top:0.7rem;">
          <button class="mode-btn${pm.mode === "range" ? " active" : ""}" id="${prefix}memo-premem-mode-range">بنطاق الصفحات</button>
          <button class="mode-btn${pm.mode === "count" ? " active" : ""}" id="${prefix}memo-premem-mode-count">بعدد الصفحات</button>
        </div>
        <div style="margin-top:0.6rem;">${preMemFieldsHTML}</div>
        <p class="hint">المحفوظ حالياً: ${preMemCount} صفحة — سيبدأ التخطيط من الصفحة ${getRemainingStartPage(m)} حتى ختم الباقي (${getRemainingPages(m)} صفحة).</p>
        ` : ""}
      </div>`;

    return `
      <div class="mode-switch">
        <button class="mode-btn${m.mode === "duration" ? " active" : ""}" id="${prefix}memo-mode-duration">الحساب بالمدة</button>
        <button class="mode-btn${m.mode === "pace" ? " active" : ""}" id="${prefix}memo-mode-pace">الحساب بعدد الصفحات</button>
      </div>
      ${formHTML}
      ${preMemHTML}
    `;
  }

  function bindMemoFormEvents(prefix, onModeChange, onInputChange) {
    document.getElementById(`${prefix}memo-mode-duration`).onclick = () => { state.memo.mode = "duration"; onModeChange(); };
    document.getElementById(`${prefix}memo-mode-pace`).onclick = () => { state.memo.mode = "pace"; onModeChange(); };
    const m = state.memo;
    if (m.mode === "duration") {
      document.getElementById(`${prefix}memo-years`).oninput = (e) => { state.memo.years = Number(e.target.value); onInputChange(); };
      document.getElementById(`${prefix}memo-months`).oninput = (e) => { state.memo.months = Number(e.target.value); onInputChange(); };
    } else {
      document.getElementById(`${prefix}memo-pace`).oninput = (e) => { state.memo.pagesPerWeek = e.target.value; onInputChange(); };
    }

    if (!m.preMemorized) m.preMemorized = { enabled: false, mode: "range", fromPage: 1, toPage: 20, count: 20 };
    document.getElementById(`${prefix}memo-premem-off`).onclick = () => { state.memo.preMemorized.enabled = false; onModeChange(); };
    document.getElementById(`${prefix}memo-premem-on`).onclick = () => { state.memo.preMemorized.enabled = true; onModeChange(); };
    if (m.preMemorized.enabled) {
      document.getElementById(`${prefix}memo-premem-mode-range`).onclick = () => { state.memo.preMemorized.mode = "range"; onModeChange(); };
      document.getElementById(`${prefix}memo-premem-mode-count`).onclick = () => { state.memo.preMemorized.mode = "count"; onModeChange(); };
      if (m.preMemorized.mode === "range") {
        document.getElementById(`${prefix}memo-premem-from`).oninput = (e) => { state.memo.preMemorized.fromPage = e.target.value; onInputChange(); };
        document.getElementById(`${prefix}memo-premem-to`).oninput = (e) => { state.memo.preMemorized.toPage = e.target.value; onInputChange(); };
      } else {
        document.getElementById(`${prefix}memo-premem-count`).oninput = (e) => { state.memo.preMemorized.count = e.target.value; onInputChange(); };
      }
    }
  }

  function renderMemoPanel() {
    const m = state.memo;
    const html = `
      <div class="panel-grid">
        <div class="panel-col panel-col-form">${buildMemoFormHTML(m, "")}</div>
        <div class="panel-col panel-col-results" id="memo-results"></div>
      </div>
    `;
    document.getElementById("tab-content").innerHTML = html;
    bindMemoFormEvents("", renderMemoPanel, updateMemoResults);
    updateMemoResults();
  }

  function updateMemoResults() {
    const m = state.memo;
    const preMemCount = getPreMemorizedCount(m);
    const hasPreMem = m.preMemorized && m.preMemorized.enabled && preMemCount > 0;
    let html = "";

    if (hasPreMem) {
      html += `<div class="stats-grid">
        ${statCardHTML(preMemCount, "صفحة محفوظة مسبقاً")}
        ${statCardHTML(getRemainingPages(m), "صفحة متبقية للحفظ")}
        ${statCardHTML(getRemainingStartPage(m), "بداية الخطة من صفحة")}
      </div>`;
    }

    let filledBeads = 0;
    if (m.mode === "duration") {
      const r = computeDuration(m);
      filledBeads = Math.min(TOTAL_AJZA, Math.round(r.ajzaPerMonth));
      html += `<div class="stats-grid">
        ${statCardHTML(r.perDay.toFixed(2), "صفحة يومياً")}
        ${statCardHTML(r.perWeek.toFixed(1), "صفحة أسبوعياً")}
        ${statCardHTML(r.ajzaPerMonth.toFixed(1), "جزء شهرياً تقريباً")}
      </div>`;
      html += inspireHTML(`بإذن الله، بناءً على خطتك ستختم حفظ ${hasPreMem ? "بقية" : ""} القرآن الكريم بتاريخ ${formatDualDate(r.finishDate)}`);
    } else {
      const r = computePace(m);
      filledBeads = Math.min(TOTAL_AJZA, Math.round(((r.totalWeeks > 0 ? (Number(m.pagesPerWeek) * 30 / 7) : 0) / 20)));
      html += `<div class="stats-grid">
        ${statCardHTML(Math.ceil(r.totalDays), "يوماً لإتمام الحفظ")}
        ${statCardHTML(r.totalYears.toFixed(2), "سنة تقريباً")}
        ${statCardHTML(Math.ceil(r.totalWeeks), "أسبوعاً")}
      </div>`;
      html += inspireHTML(`بإذن الله، بناءً على معدلك ستختم حفظ ${hasPreMem ? "بقية" : ""} القرآن الكريم بتاريخ ${formatDualDate(r.finishDate)}`);
    }
    if (hasPreMem) {
      filledBeads = Math.max(filledBeads, Math.min(TOTAL_AJZA, Math.round((preMemCount * 30) / TOTAL_PAGES)));
    }
    html += beadsHTML(filledBeads, `${filledBeads} من ${TOTAL_AJZA} جزءاً${hasPreMem ? " (شاملاً المحفوظ مسبقاً)" : " يمكن إنجازها في الشهر تقريباً"}`);
    document.getElementById("memo-results").innerHTML = html;
  }

  /* ---------------- Review calculations ---------------- */
  function computeRange(r) {
    if (r.rangeMode === "pages") {
      const from = Math.max(1, Math.min(Number(r.fromPage) || 1, TOTAL_PAGES));
      const to = Math.max(from, Math.min(Number(r.toPage) || from, TOTAL_PAGES));
      return { from, to };
    }
    const from = SURAHS[r.fromSurah][1];
    const to = surahEndPage(Math.max(r.fromSurah, r.toSurah));
    return { from: Math.min(from, to), to: Math.max(from, to) };
  }
  function computeTotalDays(r) {
    const v = Math.max(Number(r.durationValue) || 1, 1);
    if (r.durationUnit === "days") return Math.round(v);
    if (r.durationUnit === "weeks") return Math.round(v * 7);
    return Math.round(v * 30);
  }
  // Length in days of a single review cycle (e.g. "ختم كل 7 أيام")
  function computeCycleDays(r) {
    const v = Math.max(Number(r.cycleValue) || 1, 1);
    return r.cycleUnit === "weeks" ? Math.round(v * 7) : Math.round(v);
  }
  // Total length in days of the whole cyclic program (e.g. "لمدة شهر")
  function computeProgramDays(r) {
    const v = Math.max(Number(r.programValue) || 1, 1);
    return r.programUnit === "months" ? Math.round(v * 30) : Math.round(v * 7);
  }
  // Total length in days of the program when the end is set via a specific Hijri/Gregorian date
  function computeProgramDaysFromEndDate(r) {
    const today = new Date();
    const todayJDN = gregorianToJDN(today.getFullYear(), today.getMonth() + 1, today.getDate());
    const parts = r.endDate || defaultEndDateParts(r.calendarType);
    const targetJDN = r.calendarType === "hijri" ? hijriToJDN(parts.year, parts.month, parts.day) : gregorianToJDN(parts.year, parts.month, parts.day);
    return Math.max(targetJDN - todayJDN, 1);
  }
  // Resolves the cyclic program's total length in days, whichever end-mode is active
  function getProgramDays(r) {
    return r.endMode === "date" ? computeProgramDaysFromEndDate(r) : computeProgramDays(r);
  }
  function computeSchedule(r, totalPages, totalDays) {
    const restIndex = r.restDay === "بدون راحة" ? -1 : WEEK_DAYS.indexOf(r.restDay);
    const today = new Date();
    const todayIndex = (today.getDay() + 1) % 7;
    let restOccurrences = 0;
    if (restIndex !== -1) {
      for (let i = 0; i < totalDays; i++) {
        if ((todayIndex + i) % 7 === restIndex) restOccurrences++;
      }
    }
    const activeDays = Math.max(totalDays - restOccurrences, 1);
    const perDay = Math.ceil(totalPages / activeDays);
    const finishDate = addDays(today, totalDays);
    const weekPlan = WEEK_DAYS.map((day, idx) => ({
      day, isRest: idx === restIndex, pages: idx === restIndex ? 0 : perDay,
    }));
    return { perDay, activeDays, finishDate, weekPlan };
  }

  function surahOptionsHTML(selectedIndex) {
    return SURAHS.map((s, i) => `<option value="${i}"${i === selectedIndex ? " selected" : ""}>${s[0]}</option>`).join("");
  }

  /* ---------------- End-date picker (هجري / ميلادي) for cyclic review ---------------- */
  function buildEndDatePickerHTML(r, prefix) {
    const type = r.calendarType || "gregorian";
    const parts = r.endDate || defaultEndDateParts(type);
    const isHijri = type === "hijri";
    const monthNames = isHijri ? HIJRI_MONTHS : ARABIC_MONTHS;
    const baseYear = isHijri ? todayHijriParts().year : new Date().getFullYear();
    const dayCount = isHijri ? 30 : daysInGregorianMonth(parts.year || baseYear, parts.month || 1);

    let dayOptions = "";
    for (let d = 1; d <= dayCount; d++) {
      dayOptions += `<option value="${d}"${d === parts.day ? " selected" : ""}>${d}</option>`;
    }
    let monthOptions = "";
    monthNames.forEach((name, idx) => {
      monthOptions += `<option value="${idx + 1}"${idx + 1 === parts.month ? " selected" : ""}>${name}</option>`;
    });
    let yearOptions = "";
    for (let y = baseYear; y <= baseYear + 6; y++) {
      yearOptions += `<option value="${y}"${y === parts.year ? " selected" : ""}>${y}</option>`;
    }

    const endDateObjForDisplay = isHijri
      ? (() => { const g = convertDateParts("hijri", "gregorian", parts); return new Date(g.year, g.month - 1, g.day); })()
      : new Date(parts.year, parts.month - 1, parts.day);

    return `
      <div class="mode-switch" style="margin-top:0.7rem;">
        <button class="mode-btn${!isHijri ? " active" : ""}" id="${prefix}review-caltype-gregorian">ميلادي</button>
        <button class="mode-btn${isHijri ? " active" : ""}" id="${prefix}review-caltype-hijri">هجري</button>
      </div>
      <div class="field-row" style="margin-top:0.6rem;">
        <div class="field-group">
          <span>اليوم</span>
          <select id="${prefix}review-end-day">${dayOptions}</select>
        </div>
        <div class="field-group">
          <span>الشهر</span>
          <select id="${prefix}review-end-month">${monthOptions}</select>
        </div>
        <div class="field-group">
          <span>السنة</span>
          <select id="${prefix}review-end-year">${yearOptions}</select>
        </div>
      </div>
      <p class="hint">تاريخ الانتهاء الموافق: ${formatDualDate(endDateObjForDisplay)}</p>
    `;
  }

  function buildReviewFormHTML(r, prefix) {
    let rangeFieldsHTML = "";
    if (r.rangeMode === "pages") {
      rangeFieldsHTML = `
        <div class="field-row">
          <div class="field-group">
            <span>من صفحة</span>
            <input type="number" min="1" max="${TOTAL_PAGES}" id="${prefix}review-from-page" value="${r.fromPage}" />
          </div>
          <div class="field-group">
            <span>إلى صفحة</span>
            <input type="number" min="1" max="${TOTAL_PAGES}" id="${prefix}review-to-page" value="${r.toPage}" />
          </div>
        </div>`;
    } else {
      rangeFieldsHTML = `
        <div class="field-row">
          <div class="field-group wide">
            <span>من سورة</span>
            <select id="${prefix}review-from-surah">${surahOptionsHTML(r.fromSurah)}</select>
          </div>
          <div class="field-group wide">
            <span>إلى سورة</span>
            <select id="${prefix}review-to-surah">${surahOptionsHTML(r.toSurah)}</select>
          </div>
        </div>`;
    }

    const restDaySelectHTML = `
      <label class="field-label" style="margin-top:0.9rem;">يوم الراحة الأسبوعي</label>
      <div class="field-group wide">
        <select id="${prefix}review-rest-day">
          <option value="بدون راحة"${r.restDay === "بدون راحة" ? " selected" : ""}>بدون يوم راحة</option>
          ${WEEK_DAYS.map((d) => `<option value="${d}"${r.restDay === d ? " selected" : ""}>${d}</option>`).join("")}
        </select>
      </div>`;

    const scheduleFieldsHTML = r.cyclicMode ? `
      <div class="card form-card">
        <label class="field-label">دورة المراجعة (مدة ختم النطاق مرة واحدة)</label>
        <div class="field-row">
          <div class="field-group">
            <input type="number" min="1" id="${prefix}review-cycle-value" value="${r.cycleValue}" />
          </div>
          <div class="field-group">
            <select id="${prefix}review-cycle-unit">
              <option value="days"${r.cycleUnit === "days" ? " selected" : ""}>يوماً</option>
              <option value="weeks"${r.cycleUnit === "weeks" ? " selected" : ""}>أسبوعاً</option>
            </select>
          </div>
        </div>

        <label class="field-label" style="margin-top:0.9rem;">طريقة تحديد نهاية برنامج المراجعة</label>
        <div class="mode-switch">
          <button class="mode-btn${r.endMode !== "date" ? " active" : ""}" id="${prefix}review-endmode-duration">مدة زمنية</button>
          <button class="mode-btn${r.endMode === "date" ? " active" : ""}" id="${prefix}review-endmode-date">تاريخ انتهاء محدد</button>
        </div>

        ${r.endMode === "date" ? buildEndDatePickerHTML(r, prefix) : `
        <label class="field-label" style="margin-top:0.9rem;">المدة الإجمالية للبرنامج (تكرار الدورة حتى)</label>
        <div class="field-row">
          <div class="field-group">
            <input type="number" min="1" id="${prefix}review-program-value" value="${r.programValue}" />
          </div>
          <div class="field-group">
            <select id="${prefix}review-program-unit">
              <option value="weeks"${r.programUnit === "weeks" ? " selected" : ""}>أسبوعاً</option>
              <option value="months"${r.programUnit === "months" ? " selected" : ""}>شهراً</option>
            </select>
          </div>
        </div>`}

        <p class="hint">سيتكرر ختم هذا النطاق تلقائياً بنفس الدورة حتى نهاية البرنامج، وينعكس هذا التكرار كاملاً على تقويم PDF. ملاحظة: تتوقف المراجعة فوراً عند بلوغ تاريخ الانتهاء، حتى لو لم تكتمل الدورة الجارية.</p>
        ${restDaySelectHTML}
      </div>` : `
      <div class="card form-card">
        <label class="field-label">أريد إتمام هذه المراجعة خلال</label>
        <div class="field-row">
          <div class="field-group">
            <input type="number" min="1" id="${prefix}review-duration-value" value="${r.durationValue}" />
          </div>
          <div class="field-group">
            <select id="${prefix}review-duration-unit">
              <option value="days"${r.durationUnit === "days" ? " selected" : ""}>يوماً</option>
              <option value="weeks"${r.durationUnit === "weeks" ? " selected" : ""}>أسبوعاً</option>
              <option value="months"${r.durationUnit === "months" ? " selected" : ""}>شهراً</option>
            </select>
          </div>
        </div>
        ${restDaySelectHTML}
      </div>`;

    return `
      <div class="mode-switch">
        <button class="mode-btn${r.rangeMode === "pages" ? " active" : ""}" id="${prefix}review-mode-pages">بأرقام الصفحات</button>
        <button class="mode-btn${r.rangeMode === "surah" ? " active" : ""}" id="${prefix}review-mode-surah">بالسور</button>
      </div>

      <div class="card form-card">
        <label class="field-label">نطاق المراجعة</label>
        ${rangeFieldsHTML}
        <p class="hint" id="${prefix}review-range-hint"></p>
      </div>

      <div class="mode-switch">
        <button class="mode-btn${!r.cyclicMode ? " active" : ""}" id="${prefix}review-cycle-off">مراجعة لمرة واحدة</button>
        <button class="mode-btn${r.cyclicMode ? " active" : ""}" id="${prefix}review-cycle-on">تكرار المراجعة الدوري</button>
      </div>

      ${scheduleFieldsHTML}
    `;
  }

  function bindReviewFormEvents(prefix, onModeChange, onInputChange) {
    document.getElementById(`${prefix}review-mode-pages`).onclick = () => { state.review.rangeMode = "pages"; onModeChange(); };
    document.getElementById(`${prefix}review-mode-surah`).onclick = () => { state.review.rangeMode = "surah"; onModeChange(); };

    document.getElementById(`${prefix}review-cycle-off`).onclick = () => { state.review.cyclicMode = false; onModeChange(); };
    document.getElementById(`${prefix}review-cycle-on`).onclick = () => { state.review.cyclicMode = true; onModeChange(); };

    const r = state.review;
    if (r.rangeMode === "pages") {
      document.getElementById(`${prefix}review-from-page`).oninput = (e) => { state.review.fromPage = e.target.value; onInputChange(); };
      document.getElementById(`${prefix}review-to-page`).oninput = (e) => { state.review.toPage = e.target.value; onInputChange(); };
    } else {
      document.getElementById(`${prefix}review-from-surah`).onchange = (e) => { state.review.fromSurah = Number(e.target.value); onInputChange(); };
      document.getElementById(`${prefix}review-to-surah`).onchange = (e) => { state.review.toSurah = Number(e.target.value); onInputChange(); };
    }

    if (r.cyclicMode) {
      document.getElementById(`${prefix}review-cycle-value`).oninput = (e) => { state.review.cycleValue = e.target.value; onInputChange(); };
      document.getElementById(`${prefix}review-cycle-unit`).onchange = (e) => { state.review.cycleUnit = e.target.value; onInputChange(); };

      document.getElementById(`${prefix}review-endmode-duration`).onclick = () => { state.review.endMode = "duration"; onModeChange(); };
      document.getElementById(`${prefix}review-endmode-date`).onclick = () => {
        if (!state.review.endDate) state.review.endDate = defaultEndDateParts(state.review.calendarType);
        state.review.endMode = "date";
        onModeChange();
      };

      if (r.endMode === "date") {
        if (!state.review.endDate) state.review.endDate = defaultEndDateParts(state.review.calendarType);
        document.getElementById(`${prefix}review-caltype-gregorian`).onclick = () => {
          state.review.endDate = convertDateParts(state.review.calendarType, "gregorian", state.review.endDate);
          state.review.calendarType = "gregorian";
          onModeChange();
        };
        document.getElementById(`${prefix}review-caltype-hijri`).onclick = () => {
          state.review.endDate = convertDateParts(state.review.calendarType, "hijri", state.review.endDate);
          state.review.calendarType = "hijri";
          onModeChange();
        };
        document.getElementById(`${prefix}review-end-day`).onchange = (e) => { state.review.endDate.day = Number(e.target.value); onInputChange(); };
        document.getElementById(`${prefix}review-end-month`).onchange = (e) => {
          state.review.endDate.month = Number(e.target.value);
          onModeChange(); // شهر جديد قد يغيّر عدد الأيام المتاحة
        };
        document.getElementById(`${prefix}review-end-year`).onchange = (e) => { state.review.endDate.year = Number(e.target.value); onInputChange(); };
      } else {
        document.getElementById(`${prefix}review-program-value`).oninput = (e) => { state.review.programValue = e.target.value; onInputChange(); };
        document.getElementById(`${prefix}review-program-unit`).onchange = (e) => { state.review.programUnit = e.target.value; onInputChange(); };
      }
    } else {
      document.getElementById(`${prefix}review-duration-value`).oninput = (e) => { state.review.durationValue = e.target.value; onInputChange(); };
      document.getElementById(`${prefix}review-duration-unit`).onchange = (e) => { state.review.durationUnit = e.target.value; onInputChange(); };
    }
    document.getElementById(`${prefix}review-rest-day`).onchange = (e) => { state.review.restDay = e.target.value; onInputChange(); };
  }

  function renderReviewPanel() {
    const r = state.review;
    const html = `
      <div class="panel-grid">
        <div class="panel-col panel-col-form">${buildReviewFormHTML(r, "")}</div>
        <div class="panel-col panel-col-results" id="review-results"></div>
      </div>
    `;
    document.getElementById("tab-content").innerHTML = html;
    bindReviewFormEvents("", renderReviewPanel, updateReviewResults);
    updateReviewResults();
  }

  function updateReviewResults() {
    const r = state.review;
    const range = computeRange(r);
    const totalPages = range.to - range.from + 1;

    const hintEl = document.getElementById("review-range-hint");
    if (hintEl) {
      hintEl.textContent = `النطاق المحدد: من الصفحة ${range.from} إلى الصفحة ${range.to} (${totalPages} صفحة)` +
        (r.rangeMode === "surah" ? " — تقريبي حسب الطبعة الشائعة ذات ٦٠٤ صفحة" : "");
    }

    if (r.cyclicMode) {
      const cycleDays = computeCycleDays(r);
      const programDays = getProgramDays(r);
      const cycleSchedule = computeSchedule(r, totalPages, cycleDays);
      const numCycles = Math.max(Math.round(programDays / cycleDays), 1);
      const programFinish = addDays(new Date(), programDays);

      const firstCycle = buildDailyAssignments(range.from, range.to, cycleDays, r.restDay, new Date());
      const weekGridHTML = firstCycle.map((d) => `
        <div class="day-card${d.isRest ? " day-rest" : ""}">
          <span class="day-name">${WEEK_DAYS[(d.date.getDay() + 1) % 7]}</span>
          <span class="day-pages">${d.isRest ? "راحة" : (d.isFilled || d.fromPage == null ? "✓ تمّ" : `${d.fromPage}-${d.toPage}`)}</span>
        </div>`).join("");

      const endText = r.endMode === "date"
        ? `حتى تاريخ الانتهاء المحدد: ${formatDualDate(programFinish)} (${numCycles} دورة تقريباً)، وستتوقف المراجعة فور بلوغ هذا التاريخ`
        : `على مدار البرنامج حتى ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`;

      const html = `
        <div class="stats-grid">
          ${statCardHTML(cycleSchedule.perDay, "صفحة يومياً بالدورة")}
          ${statCardHTML(cycleDays, "يوماً لكل دورة")}
          ${statCardHTML(numCycles, "دورة ختم بالبرنامج")}
        </div>
        ${inspireHTML(`ستتكرر دورة ختم هذا النطاق كل ${cycleDays} يوماً ${endText}`)}
        <div class="week-table card">
          <h3 class="week-title">جدول الدورة الواحدة (تتكرر تلقائياً)</h3>
          <div class="week-grid">${weekGridHTML}</div>
        </div>
      `;
      document.getElementById("review-results").innerHTML = html;
      return;
    }

    const totalDays = computeTotalDays(r);
    const schedule = computeSchedule(r, totalPages, totalDays);

    const weekGridHTML = schedule.weekPlan.map((d) => `
      <div class="day-card${d.isRest ? " day-rest" : ""}">
        <span class="day-name">${d.day}</span>
        <span class="day-pages">${d.isRest ? "راحة" : `${d.pages} صفحة`}</span>
      </div>`).join("");

    const html = `
      <div class="stats-grid">
        ${statCardHTML(schedule.perDay, "صفحة يومياً")}
        ${statCardHTML(totalDays, "يوماً للمراجعة")}
        ${statCardHTML(totalPages, "إجمالي الصفحات")}
      </div>
      ${inspireHTML(`ستختم مراجعة هذا النطاق بتاريخ ${formatDate(schedule.finishDate)} بإذن الله`)}
      <div class="week-table card">
        <h3 class="week-title">الجدول الأسبوعي</h3>
        <div class="week-grid">${weekGridHTML}</div>
      </div>
    `;
    document.getElementById("review-results").innerHTML = html;
  }

  /* ---------------- Combined plan (memorize + review together) ---------------- */
  function renderCombinedPanel() {
    const m = state.memo;
    const r = state.review;
    const html = `
      <div class="panel-grid">
        <div class="panel-col panel-col-form">
          <h3 class="combo-section-title">إعدادات الحفظ</h3>
          ${buildMemoFormHTML(m, "c-")}
          <h3 class="combo-section-title">إعدادات المراجعة</h3>
          ${buildReviewFormHTML(r, "c-")}
        </div>
        <div class="panel-col panel-col-results" id="combined-results"></div>
      </div>
    `;
    document.getElementById("tab-content").innerHTML = html;
    bindMemoFormEvents("c-", renderCombinedPanel, updateCombinedResults);
    bindReviewFormEvents("c-", renderCombinedPanel, updateCombinedResults);
    updateCombinedResults();
  }

  function updateCombinedResults() {
    const m = state.memo;
    const r = state.review;

    let memoPerDay, memoFinish;
    if (m.mode === "duration") {
      const rr = computeDuration(m);
      memoPerDay = rr.perDay;
      memoFinish = rr.finishDate;
    } else {
      const rr = computePace(m);
      memoPerDay = TOTAL_PAGES / Math.max(rr.totalDays, 1);
      memoFinish = rr.finishDate;
    }

    const range = computeRange(r);
    const totalPages = range.to - range.from + 1;

    let reviewStatCardHTML, weekGridHTML, reviewInspireText;
    if (r.cyclicMode) {
      const cycleDays = computeCycleDays(r);
      const programDays = getProgramDays(r);
      const cycleSchedule = computeSchedule(r, totalPages, cycleDays);
      const numCycles = Math.max(Math.round(programDays / cycleDays), 1);
      const programFinish = addDays(new Date(), programDays);
      const firstCycle = buildDailyAssignments(range.from, range.to, cycleDays, r.restDay, new Date());

      weekGridHTML = firstCycle.map((d) => `
        <div class="day-card${d.isRest ? " day-rest" : ""}">
          <span class="day-name">${WEEK_DAYS[(d.date.getDay() + 1) % 7]}</span>
          <span class="day-pages">حفظ: ${memoPerDay.toFixed(1)}</span>
          <span class="day-pages" style="margin-top:2px;">${d.isRest ? "راحة مراجعة" : (d.isFilled || d.fromPage == null ? "✓ تمّ" : `مراجعة: ${d.fromPage}-${d.toPage}`)}</span>
        </div>`).join("");
      reviewStatCardHTML = statCardHTML(cycleDays, "يوماً لكل دورة مراجعة");
      reviewInspireText = r.endMode === "date"
        ? `وستتكرر دورة مراجعة هذا النطاق كل ${cycleDays} يوماً حتى تتوقف فوراً بتاريخ ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`
        : `وستتكرر دورة مراجعة هذا النطاق كل ${cycleDays} يوماً حتى ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`;
    } else {
      const totalDays = computeTotalDays(r);
      const schedule = computeSchedule(r, totalPages, totalDays);

      weekGridHTML = schedule.weekPlan.map((d) => `
        <div class="day-card${d.isRest ? " day-rest" : ""}">
          <span class="day-name">${d.day}</span>
          <span class="day-pages">حفظ: ${memoPerDay.toFixed(1)}</span>
          <span class="day-pages" style="margin-top:2px;">${d.isRest ? "راحة مراجعة" : `مراجعة: ${d.pages}`}</span>
        </div>`).join("");
      reviewStatCardHTML = statCardHTML(schedule.perDay, "صفحة مراجعة يومياً");
      reviewInspireText = `وستختم مراجعة هذا النطاق بتاريخ ${formatDate(schedule.finishDate)}، بإذن الله`;
    }

    const html = `
      <div class="stats-grid">
        ${statCardHTML(memoPerDay.toFixed(2), "صفحة حفظ يومياً")}
        ${reviewStatCardHTML}
        ${statCardHTML(totalPages, "صفحات نطاق المراجعة")}
      </div>
      <div class="inspire-card">
        <span class="inspire-icon">✦</span>
        <p>ستختم حفظ القرآن الكريم بتاريخ ${formatDate(memoFinish)}، ${reviewInspireText}</p>
      </div>
      <div class="week-table card">
        <h3 class="week-title">نظرة أسبوعية سريعة (حفظ + مراجعة)</h3>
        <div class="week-grid">${weekGridHTML}</div>
      </div>
    `;
    document.getElementById("combined-results").innerHTML = html;
  }

  /* ---------------- Tabs ---------------- */
  function renderTab() {
    document.getElementById("tab-memorize").classList.toggle("active", state.tab === "memorize");
    document.getElementById("tab-review").classList.toggle("active", state.tab === "review");
    document.getElementById("tab-combined").classList.toggle("active", state.tab === "combined");
    if (state.tab === "memorize") renderMemoPanel();
    else if (state.tab === "review") renderReviewPanel();
    else renderCombinedPanel();
  }
  document.getElementById("tab-memorize").onclick = () => { state.tab = "memorize"; renderTab(); };
  document.getElementById("tab-review").onclick = () => { state.tab = "review"; renderTab(); };
  document.getElementById("tab-combined").onclick = () => { state.tab = "combined"; renderTab(); };

  /* ---------------- Save notice ---------------- */
  function showNotice(text, ms) {
    const el = document.getElementById("save-notice");
    el.textContent = text;
    el.style.display = "block";
    if (ms) setTimeout(() => { el.style.display = "none"; }, ms);
  }

  /* ---------------- Save plan (window.storage) ---------------- */
  document.getElementById("btn-save").addEventListener("click", async function () {
    const btn = this;
    btn.disabled = true;
    btn.textContent = "جارٍ الحفظ...";
    try {
      const payload = { tab: state.tab, memoState: state.memo, reviewState: state.review };
      const result = await window.storage.set(STORAGE_KEY, JSON.stringify(payload), false);
      showNotice(result ? "تم حفظ الخطة بنجاح ✓" : "تعذّر حفظ الخطة، حاول مرة أخرى", 2500);
    } catch (e) {
      showNotice("تعذّر حفظ الخطة، حاول مرة أخرى", 2500);
    } finally {
      btn.disabled = false;
      btn.textContent = "حفظ الخطة";
    }
  });

  /* Load any previously saved plan */
  (async function loadSaved() {
    try {
      const result = await window.storage.get(STORAGE_KEY, false);
      if (result && result.value) {
        const data = JSON.parse(result.value);
        if (data.tab) state.tab = data.tab;
        if (data.memoState) Object.assign(state.memo, data.memoState);
        if (data.reviewState) Object.assign(state.review, data.reviewState);
        showNotice("تم استرجاع خطتك المحفوظة ✓", 2200);
      }
    } catch (e) {
      // لا توجد خطة محفوظة بعد
    }
    renderTab();
  })();

  /* ---------------- Build day-by-day plan assignments ---------------- */
  // Returns an array (length totalDays) of { date, isRest, fromPage, toPage, isFilled }
  function buildDailyAssignments(startPage, endPage, totalDays, restDayName, startDateObj) {
    const restIndex = (!restDayName || restDayName === "بدون راحة") ? -1 : WEEK_DAYS.indexOf(restDayName);
    const totalPagesToCover = Math.max(endPage - startPage + 1, 1);

    // Count active (non-rest) days first
    let activeDaysCount = 0;
    for (let i = 0; i < totalDays; i++) {
      const dow = (startDateObj.getDay() + 1 + i) % 7; // align with WEEK_DAYS (starts Saturday)
      if (dow !== restIndex) activeDaysCount++;
    }
    activeDaysCount = Math.max(activeDaysCount, 1);

    const days = [];
    let assignedSoFar = 0;
    let activeSeen = 0;

    for (let i = 0; i < totalDays; i++) {
      const date = addDays(startDateObj, i);
      const dow = (startDateObj.getDay() + 1 + i) % 7;
      const isRest = dow === restIndex;

      if (isRest) {
        days.push({ date, isRest: true });
        continue;
      }

      const daysRemainingActive = activeDaysCount - activeSeen;
      const pagesRemaining = totalPagesToCover - assignedSoFar;
      let pagesToday = Math.round(pagesRemaining / Math.max(daysRemainingActive, 1));
      pagesToday = Math.max(pagesToday, 0);
      if (assignedSoFar >= totalPagesToCover) pagesToday = 0;

      const fromP = startPage + assignedSoFar;
      const toP = Math.min(fromP + pagesToday - 1, endPage);
      const isFilled = assignedSoFar >= totalPagesToCover;

      days.push({ date, isRest: false, fromPage: isFilled ? null : fromP, toPage: isFilled ? null : toP, isFilled });

      assignedSoFar += pagesToday;
      activeSeen++;
    }
    return days;
  }

  // Repeats a single review cycle (start -> end, ختم واحد) back-to-back until totalDays is covered.
  // Each cycle restarts the page range from the beginning, exactly like a recurring "ختم" of the same portion.
  function buildCyclicAssignments(fromPage, toPage, cycleDays, totalDays, restDayName, startDateObj) {
    const days = [];
    let offset = 0;
    while (offset < totalDays) {
      const chunkLen = Math.min(cycleDays, totalDays - offset);
      const chunkStart = addDays(startDateObj, offset);
      const chunkDays = buildDailyAssignments(fromPage, toPage, chunkLen, restDayName, chunkStart);
      days.push(...chunkDays);
      offset += chunkLen;
    }
    return days;
  }

  // Figures out the current plan's daily assignments based on the active tab
  function getActivePlanAssignments() {
    const today = new Date();
    if (state.tab === "memorize") {
      const m = state.memo;
      let totalDays;
      if (m.mode === "duration") {
        totalDays = computeDuration(m).totalDays;
      } else {
        totalDays = computePace(m).totalDays;
      }
      totalDays = Math.max(Math.round(totalDays), 1);
      const startPage = getRemainingStartPage(m);
      const hasPreMem = getPreMemorizedCount(m) > 0;
      const days = buildDailyAssignments(startPage, TOTAL_PAGES, totalDays, null, today);
      return {
        days,
        title: "خطة الحفظ",
        subtitle: hasPreMem
          ? `${totalDays} يوماً لختم حفظ باقي القرآن الكريم (من الصفحة ${startPage}) بإذن الله`
          : `${totalDays} يوماً لختم حفظ القرآن الكريم بإذن الله`,
      };
    } else {
      const r = state.review;
      const range = computeRange(r);
      if (r.cyclicMode) {
        const cycleDays = computeCycleDays(r);
        const totalDays = getProgramDays(r);
        const numCycles = Math.max(Math.round(totalDays / cycleDays), 1);
        const days = buildCyclicAssignments(range.from, range.to, cycleDays, totalDays, r.restDay, today);
        const endText = r.endMode === "date"
          ? `حتى ${formatDualDate(addDays(today, totalDays))}`
          : `${numCycles} دورة تقريباً`;
        return {
          days,
          title: "جدول المراجعة الدوري",
          subtitle: `تكرار ختم الصفحات من ${range.from} إلى ${range.to} كل ${cycleDays} يوماً — ${endText}`,
        };
      }
      const totalDays = computeTotalDays(r);
      const days = buildDailyAssignments(range.from, range.to, totalDays, r.restDay, today);
      return { days, title: "جدول المراجعة", subtitle: `مراجعة الصفحات من ${range.from} إلى ${range.to} خلال ${totalDays} يوماً` };
    }
  }

  // Combines the memorization plan and the review schedule into a single day-by-day list
  function getCombinedPlanAssignments() {
    const today = new Date();

    const m = state.memo;
    let memoTotalDays = (m.mode === "duration") ? computeDuration(m).totalDays : computePace(m).totalDays;
    memoTotalDays = Math.max(Math.round(memoTotalDays), 1);
    const memoStartPage = getRemainingStartPage(m);
    const memoDays = buildDailyAssignments(memoStartPage, TOTAL_PAGES, memoTotalDays, null, today);

    const r = state.review;
    const range = computeRange(r);
    let reviewDays, reviewSubtitle;
    if (r.cyclicMode) {
      const cycleDays = computeCycleDays(r);
      const programDays = getProgramDays(r);
      const numCycles = Math.max(Math.round(programDays / cycleDays), 1);
      reviewDays = buildCyclicAssignments(range.from, range.to, cycleDays, programDays, r.restDay, today);
      const endText = r.endMode === "date"
        ? `حتى ${formatDualDate(addDays(today, programDays))}`
        : `${numCycles} دورة تقريباً`;
      reviewSubtitle = `مع تكرار ختم مراجعة الصفحات من ${range.from} إلى ${range.to} كل ${cycleDays} يوماً (${endText})`;
    } else {
      const reviewTotalDays = computeTotalDays(r);
      reviewDays = buildDailyAssignments(range.from, range.to, reviewTotalDays, r.restDay, today);
      reviewSubtitle = `ومراجعة الصفحات من ${range.from} إلى ${range.to}`;
    }

    const totalDays = Math.max(memoDays.length, reviewDays.length);
    const days = [];
    for (let i = 0; i < totalDays; i++) {
      days.push({
        date: addDays(today, i),
        memo: memoDays[i] || null,
        review: reviewDays[i] || null,
      });
    }

    return {
      days,
      title: "الخطة الشاملة (حفظ ومراجعة)",
      subtitle: `${getPreMemorizedCount(m) > 0 ? `حفظ باقي القرآن من الصفحة ${memoStartPage}` : "حفظ القرآن كاملاً"}، ${reviewSubtitle}`,
    };
  }

  /* ---------------- Render calendar pages (one per month) as HTML ---------------- */
  function groupByMonth(days) {
    const months = [];
    let current = null;
    days.forEach((d) => {
      const key = `${d.date.getFullYear()}-${d.date.getMonth()}`;
      if (!current || current.key !== key) {
        current = { key, year: d.date.getFullYear(), month: d.date.getMonth(), days: [] };
        months.push(current);
      }
      current.days.push(d);
    });
    return months;
  }

  const ARABIC_MONTHS = ["يناير","فبراير","مارس","أبريل","مايو","يونيو","يوليو","أغسطس","سبتمبر","أكتوبر","نوفمبر","ديسمبر"];

  function buildMonthPageHTML(monthGroup, planTitle, planSubtitle) {
    const { year, month, days } = monthGroup;
    const firstDay = new Date(year, month, 1);
    // Align to Saturday-first week (matches WEEK_DAYS order)
    const firstDow = (firstDay.getDay() + 1) % 7;
    const daysInMonth = new Date(year, month + 1, 0).getDate();

    // Map date-number -> assignment (only for days that belong to the plan)
    const byDateNum = {};
    days.forEach((d) => { byDateNum[d.date.getDate()] = d; });

    let cells = "";
    for (let i = 0; i < firstDow; i++) {
      cells += `<div class="cal-cell cal-empty"></div>`;
    }
    for (let dnum = 1; dnum <= daysInMonth; dnum++) {
      const a = byDateNum[dnum];
      if (!a) {
        cells += `<div class="cal-cell cal-empty"><span class="cal-date-num" style="opacity:.35">${dnum}</span></div>`;
        continue;
      }
      if (a.isRest) {
        cells += `<div class="cal-cell cal-rest">
          <span class="cal-date-num">${dnum}</span>
          <span class="cal-task cal-task-rest">يوم راحة</span>
        </div>`;
      } else if (a.isFilled || a.fromPage == null) {
        cells += `<div class="cal-cell cal-done">
          <span class="cal-date-num">${dnum}</span>
          <span class="cal-task">✓ تمّ الختم</span>
        </div>`;
      } else {
        const label = a.fromPage === a.toPage ? `صفحة ${a.fromPage}` : `من ${a.fromPage} إلى ${a.toPage}`;
        cells += `<div class="cal-cell">
          <span class="cal-date-num">${dnum}</span>
          <span class="cal-task">${label}</span>
        </div>`;
      }
    }

    const dowHeader = WEEK_DAYS.map((d) => `<div class="cal-dow">${d}</div>`).join("");

    return `
      <div class="cal-page">
        <div class="cal-page-header">
          <div>
            <p class="cal-plan-title">${planTitle}</p>
            <p class="cal-plan-sub">${planSubtitle}</p>
          </div>
          <div class="cal-month-badge">${ARABIC_MONTHS[month]} ${year}</div>
        </div>
        <div class="cal-grid">${dowHeader}${cells}</div>
        <p class="cal-page-footer">﷽ — خطة القرآن الكريم</p>
      </div>
    `;
  }

  function buildCombinedMonthPageHTML(monthGroup, planTitle, planSubtitle) {
    const { year, month, days } = monthGroup;
    const firstDay = new Date(year, month, 1);
    const firstDow = (firstDay.getDay() + 1) % 7;
    const daysInMonth = new Date(year, month + 1, 0).getDate();

    const byDateNum = {};
    days.forEach((d) => { byDateNum[d.date.getDate()] = d; });

    let cells = "";
    for (let i = 0; i < firstDow; i++) {
      cells += `<div class="cal-cell cal-empty"></div>`;
    }
    for (let dnum = 1; dnum <= daysInMonth; dnum++) {
      const a = byDateNum[dnum];
      if (!a) {
        cells += `<div class="cal-cell cal-empty"><span class="cal-date-num" style="opacity:.35">${dnum}</span></div>`;
        continue;
      }

      const memoDay = a.memo;
      let memoLabel;
      if (!memoDay || memoDay.isFilled || memoDay.fromPage == null) {
        memoLabel = "✓ تمّ الختم";
      } else {
        memoLabel = memoDay.fromPage === memoDay.toPage
          ? `حفظ: ص${memoDay.fromPage}`
          : `حفظ: ${memoDay.fromPage}-${memoDay.toPage}`;
      }

      const reviewDay = a.review;
      let reviewLabel;
      let isRest = false;
      if (!reviewDay) {
        reviewLabel = "✓ اكتملت المراجعة";
      } else if (reviewDay.isRest) {
        reviewLabel = "راحة مراجعة";
        isRest = true;
      } else if (reviewDay.isFilled || reviewDay.fromPage == null) {
        reviewLabel = "✓ اكتملت المراجعة";
      } else {
        reviewLabel = reviewDay.fromPage === reviewDay.toPage
          ? `مراجعة: ص${reviewDay.fromPage}`
          : `مراجعة: ${reviewDay.fromPage}-${reviewDay.toPage}`;
      }

      cells += `<div class="cal-cell cal-cell-combined${isRest ? " cal-rest" : ""}">
        <span class="cal-date-num">${dnum}</span>
        <div class="cal-task-group">
          <span class="cal-task-mini memo">${memoLabel}</span>
          <span class="cal-task-mini review${isRest ? " is-rest" : ""}">${reviewLabel}</span>
        </div>
      </div>`;
    }

    const dowHeader = WEEK_DAYS.map((d) => `<div class="cal-dow">${d}</div>`).join("");

    return `
      <div class="cal-page">
        <div class="cal-page-header">
          <div>
            <p class="cal-plan-title">${planTitle}</p>
            <p class="cal-plan-sub">${planSubtitle}</p>
          </div>
          <div class="cal-month-badge">${ARABIC_MONTHS[month]} ${year}</div>
        </div>
        <div class="cal-grid">${dowHeader}${cells}</div>
        <p class="cal-page-footer">﷽ — الخطة الشاملة لحفظ ومراجعة القرآن</p>
      </div>
    `;
  }

  /* ---------------- PDF export ---------------- */
  document.getElementById("btn-pdf").addEventListener("click", async function () {
    const btn = this;
    if (btn.disabled) return;
    btn.disabled = true;
    const originalText = btn.textContent;
    btn.textContent = "جارٍ إنشاء PDF...";
    showNotice("جارٍ تجهيز التقويم...");

    const calRoot = document.getElementById("pdf-calendar-root");

    try {
      if (typeof window.html2canvas !== "function" || !window.jspdf || !window.jspdf.jsPDF) {
        throw new Error("لم يتم تحميل مكتبات PDF");
      }

      const isCombined = state.tab === "combined";
      const plan = isCombined ? getCombinedPlanAssignments() : getActivePlanAssignments();
      const monthRenderer = isCombined ? buildCombinedMonthPageHTML : buildMonthPageHTML;
      const months = groupByMonth(plan.days);
      if (months.length === 0) throw new Error("لا توجد بيانات كافية لبناء التقويم");

      const { jsPDF } = window.jspdf;
      const pdf = new jsPDF({ orientation: "portrait", unit: "pt", format: "a4" });
      const pageWidth = pdf.internal.pageSize.getWidth();
      const pageHeight = pdf.internal.pageSize.getHeight();

      for (let i = 0; i < months.length; i++) {
        showNotice(`جارٍ تجهيز شهر ${i + 1} من ${months.length}...`);
        calRoot.innerHTML = monthRenderer(months[i], plan.title, plan.subtitle);
        // Give the browser a tick to lay out fonts/DOM before capture
        await new Promise((res) => setTimeout(res, 30));

        const pageNode = calRoot.querySelector(".cal-page");
        const canvas = await window.html2canvas(pageNode, {
          scale: 2,
          backgroundColor: "#fffdfa",
          useCORS: true,
        });

        const imgData = canvas.toDataURL("image/png");
        const imgHeight = (canvas.height * pageWidth) / canvas.width;

        if (i > 0) pdf.addPage();
        pdf.addImage(imgData, "PNG", 0, 0, pageWidth, Math.min(imgHeight, pageHeight));
      }

      calRoot.innerHTML = "";
      pdf.save(isCombined ? "تقويم-الخطة-الشاملة.pdf" : "تقويم-خطة-القرآن.pdf");
      showNotice("تم إنشاء تقويم PDF بنجاح ✓", 2500);
    } catch (err) {
      calRoot.innerHTML = "";
      showNotice("تعذّر إنشاء ملف PDF، حاول مرة أخرى", 2500);
    } finally {
      btn.disabled = false;
      btn.textContent = originalText;
    }
  });
})();
</script>
</body>
</html>
