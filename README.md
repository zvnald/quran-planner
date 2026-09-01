<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>خطة القرآن</title>
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
  html, body { margin: 0; padding: 0; }

  .app-shell {
    min-height: 100vh;
    background: linear-gradient(180deg, #ffffff 0%, #fdfbf8 35%, #f7efe2 100%);
    font-family: 'Tajawal', sans-serif;
    color: var(--espresso);
    padding: 1.1rem 0.9rem 3rem;
    -webkit-print-color-adjust: exact;
    print-color-adjust: exact;
  }
  .container { max-width: 560px; margin: 0 auto; }

  /* ---- Header: dark espresso banner fading into the page ---- */
  .header-banner {
    position: relative;
    overflow: hidden;
    text-align: center;
    border-radius: 26px;
    padding: 2rem 1.4rem 1.7rem;
    margin-bottom: 1.5rem;
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
  .header .ornament { font-family: 'Amiri', serif; color: var(--latte); font-size: 1.5rem; letter-spacing: 0.25rem; position: relative; }
  .header-banner h1 {
    font-family: 'Amiri', serif;
    font-weight: 700;
    font-size: 2.05rem;
    margin: 0.3rem 0 0.3rem;
    color: var(--paper);
    position: relative;
  }
  .header-banner p { margin: 0; font-size: 0.92rem; color: var(--sand); position: relative; }

  .tabs {
    display: flex;
    background: var(--linen);
    border: 1px solid var(--sand);
    border-radius: 999px;
    padding: 4px;
    margin-bottom: 1.3rem;
    box-shadow: inset 0 1px 3px rgba(74,48,32,0.08);
  }
  .tab-btn {
    flex: 1;
    border: none;
    background: transparent;
    padding: 0.65rem 0.5rem;
    border-radius: 999px;
    font-family: 'Tajawal', sans-serif;
    font-weight: 700;
    font-size: 0.92rem;
    color: var(--cinnamon);
    cursor: pointer;
    transition: all .25s ease;
  }
  .tab-btn.active {
    background: linear-gradient(135deg, var(--coffee), var(--espresso));
    color: var(--paper);
    box-shadow: 0 5px 14px rgba(43,28,19,0.3);
  }

  .mode-switch { display: flex; gap: 0.5rem; margin-bottom: 0.9rem; }
  .mode-btn {
    flex: 1;
    padding: 0.55rem 0.4rem;
    border-radius: 12px;
    border: 1.5px solid var(--sand);
    background: var(--paper);
    font-family: 'Tajawal', sans-serif;
    font-weight: 500;
    font-size: 0.85rem;
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
    border-radius: 18px;
    padding: 1rem 1.1rem;
    margin-bottom: 1rem;
    box-shadow: 0 4px 16px rgba(74,48,32,0.06);
    break-inside: avoid;
  }
  .field-label { display: block; font-weight: 700; font-size: 0.88rem; margin-bottom: 0.55rem; color: var(--coffee); }
  .field-row { display: flex; gap: 0.6rem; flex-wrap: wrap; }
  .field-group {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--linen);
    border: 1px solid var(--sand);
    border-radius: 10px;
    padding: 0.45rem 0.7rem;
    flex: 1;
    min-width: 130px;
    font-size: 0.85rem;
    color: var(--cinnamon);
  }
  .field-group.wide { min-width: 100%; }
  .field-group input, .field-group select {
    width: 100%;
    border: none;
    background: transparent;
    font-family: 'Tajawal', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    color: var(--espresso);
    outline: none;
  }
  .hint { font-size: 0.78rem; color: var(--cinnamon); margin: 0.5rem 0 0; }

  .stats-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.55rem; margin-bottom: 1rem; }
  .stat-card {
    background: linear-gradient(160deg, var(--paper), var(--linen));
    border: 1px solid var(--sand);
    border-radius: 16px;
    padding: 0.85rem 0.4rem;
    text-align: center;
    break-inside: avoid;
  }
  .stat-value { font-family: 'Amiri', serif; font-weight: 700; font-size: 1.5rem; color: var(--coffee); }
  .stat-label { font-size: 0.7rem; color: var(--cinnamon); margin-top: 0.15rem; }

  .inspire-card {
    display: flex;
    align-items: center;
    gap: 0.6rem;
    background: linear-gradient(120deg, var(--espresso), var(--coffee));
    color: var(--linen);
    border-radius: 18px;
    padding: 0.95rem 1.1rem;
    margin-bottom: 1.2rem;
    box-shadow: 0 8px 20px rgba(43,28,19,0.22);
    break-inside: avoid;
  }
  .inspire-card p { margin: 0; font-size: 0.88rem; line-height: 1.6; }
  .inspire-icon { color: var(--latte); font-size: 1.1rem; }

  .beads-wrap { text-align: center; margin-bottom: 0.5rem; }
  .beads-row { display: flex; flex-wrap: wrap; justify-content: center; gap: 6px; direction: ltr; margin-bottom: 0.5rem; }
  .bead {
    width: 14px; height: 14px; border-radius: 50%;
    background: var(--sand);
    border: 1px solid var(--latte);
    display: inline-block;
  }
  .bead-filled { background: radial-gradient(circle at 30% 30%, var(--latte), var(--coffee)); border-color: var(--coffee); }
  .beads-label { font-size: 0.78rem; color: var(--cinnamon); }

  .week-table { margin-top: 0.3rem; }
  .week-title { font-family: 'Amiri', serif; font-size: 1.1rem; margin: 0 0 0.7rem; color: var(--coffee); }
  .week-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(70px,1fr)); gap: 0.5rem; }
  .day-card {
    background: var(--linen);
    border: 1px solid var(--sand);
    border-radius: 12px;
    padding: 0.6rem 0.3rem;
    text-align: center;
  }
  .day-card.day-rest { background: #efe6d6; opacity: 0.75; }
  .day-name { display: block; font-size: 0.72rem; color: var(--cinnamon); margin-bottom: 0.25rem; }
  .day-pages { display: block; font-weight: 700; color: var(--coffee); font-size: 0.85rem; }

  .actions { display: flex; gap: 0.55rem; margin-top: 1.2rem; }
  .action-btn {
    flex: 1;
    padding: 0.8rem;
    border-radius: 14px;
    border: none;
    font-family: 'Tajawal', sans-serif;
    font-weight: 700;
    font-size: 0.88rem;
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
      <h1>خطة القرآن</h1>
      <p>خطط حفظك ومراجعتك للقرآن الكريم بخطوات واضحة</p>
    </header>

    <div class="tabs">
      <button class="tab-btn active" id="tab-memorize">خطة الحفظ</button>
      <button class="tab-btn" id="tab-review">جدول المراجعة</button>
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
  const STORAGE_KEY = "quran-planner-state";

  const state = {
    tab: "memorize",
    memo: { mode: "duration", years: 3, months: 0, pagesPerWeek: 7 },
    review: {
      rangeMode: "pages", fromPage: 1, toPage: 20, fromSurah: 0, toSurah: 5,
      durationValue: 10, durationUnit: "days", restDay: "الجمعة",
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
    const totalMonths = Math.max(m.years * 12 + Number(m.months || 0), 1);
    const totalDays = totalMonths * 30;
    const perDay = TOTAL_PAGES / totalDays;
    const perWeek = perDay * 7;
    const ajzaPerMonth = (perDay * 30) / 20;
    return { perDay, perWeek, ajzaPerMonth, finishDate: addDays(startDate, totalDays), totalDays };
  }
  function computePace(m) {
    const perWeek = Math.max(Number(m.pagesPerWeek) || 0.0001, 0.0001);
    const totalWeeks = TOTAL_PAGES / perWeek;
    const totalDays = Math.ceil(totalWeeks * 7);
    const totalYears = totalDays / 365;
    return { totalWeeks, totalDays, totalYears, finishDate: addDays(startDate, totalDays) };
  }

  function renderMemoPanel() {
    const m = state.memo;
    let formHTML = "";
    if (m.mode === "duration") {
      formHTML = `
        <div class="card form-card">
          <label class="field-label">أريد إتمام حفظ القرآن خلال:</label>
          <div class="field-row">
            <div class="field-group">
              <input type="number" min="0" id="memo-years" value="${m.years}" />
              <span>سنة</span>
            </div>
            <div class="field-group">
              <input type="number" min="0" max="11" id="memo-months" value="${m.months}" />
              <span>شهر</span>
            </div>
          </div>
        </div>`;
    } else {
      formHTML = `
        <div class="card form-card">
          <label class="field-label">أستطيع حفظ هذا العدد من الصفحات أسبوعياً:</label>
          <div class="field-group wide">
            <input type="number" min="0.5" step="0.5" id="memo-pace" value="${m.pagesPerWeek}" />
            <span>صفحة / أسبوع</span>
          </div>
        </div>`;
    }

    const html = `
      <div class="mode-switch">
        <button class="mode-btn${m.mode === "duration" ? " active" : ""}" id="memo-mode-duration">الحساب بالمدة</button>
        <button class="mode-btn${m.mode === "pace" ? " active" : ""}" id="memo-mode-pace">الحساب بعدد الصفحات</button>
      </div>
      ${formHTML}
      <div id="memo-results"></div>
    `;
    document.getElementById("tab-content").innerHTML = html;

    document.getElementById("memo-mode-duration").onclick = () => { state.memo.mode = "duration"; renderMemoPanel(); };
    document.getElementById("memo-mode-pace").onclick = () => { state.memo.mode = "pace"; renderMemoPanel(); };

    if (m.mode === "duration") {
      document.getElementById("memo-years").oninput = (e) => { state.memo.years = Number(e.target.value); updateMemoResults(); };
      document.getElementById("memo-months").oninput = (e) => { state.memo.months = Number(e.target.value); updateMemoResults(); };
    } else {
      document.getElementById("memo-pace").oninput = (e) => { state.memo.pagesPerWeek = e.target.value; updateMemoResults(); };
    }

    updateMemoResults();
  }

  function updateMemoResults() {
    const m = state.memo;
    let html = "";
    let filledBeads = 0;
    if (m.mode === "duration") {
      const r = computeDuration(m);
      filledBeads = Math.min(TOTAL_AJZA, Math.round(r.ajzaPerMonth));
      html += `<div class="stats-grid">
        ${statCardHTML(r.perDay.toFixed(2), "صفحة يومياً")}
        ${statCardHTML(r.perWeek.toFixed(1), "صفحة أسبوعياً")}
        ${statCardHTML(r.ajzaPerMonth.toFixed(1), "جزء شهرياً تقريباً")}
      </div>`;
      html += inspireHTML(`بإذن الله، بناءً على خطتك ستختم حفظ القرآن الكريم بتاريخ ${formatDate(r.finishDate)}`);
    } else {
      const r = computePace(m);
      filledBeads = Math.min(TOTAL_AJZA, Math.round(((r.totalWeeks > 0 ? (Number(m.pagesPerWeek) * 30 / 7) : 0) / 20)));
      html += `<div class="stats-grid">
        ${statCardHTML(Math.ceil(r.totalDays), "يوماً لإتمام الحفظ")}
        ${statCardHTML(r.totalYears.toFixed(2), "سنة تقريباً")}
        ${statCardHTML(Math.ceil(r.totalWeeks), "أسبوعاً")}
      </div>`;
      html += inspireHTML(`بإذن الله، بناءً على معدلك ستختم حفظ القرآن الكريم بتاريخ ${formatDate(r.finishDate)}`);
    }
    html += beadsHTML(filledBeads, `${filledBeads} من ${TOTAL_AJZA} جزءاً يمكن إنجازها في الشهر تقريباً`);
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

  function renderReviewPanel() {
    const r = state.review;
    let rangeFieldsHTML = "";
    if (r.rangeMode === "pages") {
      rangeFieldsHTML = `
        <div class="field-row">
          <div class="field-group">
            <span>من صفحة</span>
            <input type="number" min="1" max="${TOTAL_PAGES}" id="review-from-page" value="${r.fromPage}" />
          </div>
          <div class="field-group">
            <span>إلى صفحة</span>
            <input type="number" min="1" max="${TOTAL_PAGES}" id="review-to-page" value="${r.toPage}" />
          </div>
        </div>`;
    } else {
      rangeFieldsHTML = `
        <div class="field-row">
          <div class="field-group wide">
            <span>من سورة</span>
            <select id="review-from-surah">${surahOptionsHTML(r.fromSurah)}</select>
          </div>
          <div class="field-group wide">
            <span>إلى سورة</span>
            <select id="review-to-surah">${surahOptionsHTML(r.toSurah)}</select>
          </div>
        </div>`;
    }

    const html = `
      <div class="mode-switch">
        <button class="mode-btn${r.rangeMode === "pages" ? " active" : ""}" id="review-mode-pages">بأرقام الصفحات</button>
        <button class="mode-btn${r.rangeMode === "surah" ? " active" : ""}" id="review-mode-surah">بالسور</button>
      </div>

      <div class="card form-card">
        <label class="field-label">نطاق المراجعة</label>
        ${rangeFieldsHTML}
        <p class="hint" id="review-range-hint"></p>
      </div>

      <div class="card form-card">
        <label class="field-label">أريد إتمام هذه المراجعة خلال</label>
        <div class="field-row">
          <div class="field-group">
            <input type="number" min="1" id="review-duration-value" value="${r.durationValue}" />
          </div>
          <div class="field-group wide">
            <select id="review-duration-unit">
              <option value="days"${r.durationUnit === "days" ? " selected" : ""}>يوماً</option>
              <option value="weeks"${r.durationUnit === "weeks" ? " selected" : ""}>أسبوعاً (ختم دوري)</option>
              <option value="months"${r.durationUnit === "months" ? " selected" : ""}>شهراً</option>
            </select>
          </div>
        </div>
        <label class="field-label" style="margin-top:0.9rem;">يوم الراحة الأسبوعي</label>
        <div class="field-group wide">
          <select id="review-rest-day">
            <option value="بدون راحة"${r.restDay === "بدون راحة" ? " selected" : ""}>بدون يوم راحة</option>
            ${WEEK_DAYS.map((d) => `<option value="${d}"${r.restDay === d ? " selected" : ""}>${d}</option>`).join("")}
          </select>
        </div>
      </div>

      <div id="review-results"></div>
    `;
    document.getElementById("tab-content").innerHTML = html;

    document.getElementById("review-mode-pages").onclick = () => { state.review.rangeMode = "pages"; renderReviewPanel(); };
    document.getElementById("review-mode-surah").onclick = () => { state.review.rangeMode = "surah"; renderReviewPanel(); };

    if (r.rangeMode === "pages") {
      document.getElementById("review-from-page").oninput = (e) => { state.review.fromPage = e.target.value; updateReviewResults(); };
      document.getElementById("review-to-page").oninput = (e) => { state.review.toPage = e.target.value; updateReviewResults(); };
    } else {
      document.getElementById("review-from-surah").onchange = (e) => { state.review.fromSurah = Number(e.target.value); updateReviewResults(); };
      document.getElementById("review-to-surah").onchange = (e) => { state.review.toSurah = Number(e.target.value); updateReviewResults(); };
    }
    document.getElementById("review-duration-value").oninput = (e) => { state.review.durationValue = e.target.value; updateReviewResults(); };
    document.getElementById("review-duration-unit").onchange = (e) => { state.review.durationUnit = e.target.value; updateReviewResults(); };
    document.getElementById("review-rest-day").onchange = (e) => { state.review.restDay = e.target.value; updateReviewResults(); };

    updateReviewResults();
  }

  function updateReviewResults() {
    const r = state.review;
    const range = computeRange(r);
    const totalPages = range.to - range.from + 1;
    const totalDays = computeTotalDays(r);
    const schedule = computeSchedule(r, totalPages, totalDays);

    const hintEl = document.getElementById("review-range-hint");
    if (hintEl) {
      hintEl.textContent = `النطاق المحدد: من الصفحة ${range.from} إلى الصفحة ${range.to} (${totalPages} صفحة)` +
        (r.rangeMode === "surah" ? " — تقريبي حسب الطبعة الشائعة ذات ٦٠٤ صفحة" : "");
    }

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

  /* ---------------- Tabs ---------------- */
  function renderTab() {
    document.getElementById("tab-memorize").classList.toggle("active", state.tab === "memorize");
    document.getElementById("tab-review").classList.toggle("active", state.tab === "review");
    if (state.tab === "memorize") renderMemoPanel();
    else renderReviewPanel();
  }
  document.getElementById("tab-memorize").onclick = () => { state.tab = "memorize"; renderTab(); };
  document.getElementById("tab-review").onclick = () => { state.tab = "review"; renderTab(); };

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
      const days = buildDailyAssignments(1, TOTAL_PAGES, totalDays, null, today);
      return { days, title: "خطة الحفظ", subtitle: `${totalDays} يوماً لختم حفظ القرآن الكريم بإذن الله` };
    } else {
      const r = state.review;
      const range = computeRange(r);
      const totalDays = computeTotalDays(r);
      const days = buildDailyAssignments(range.from, range.to, totalDays, r.restDay, today);
      return { days, title: "جدول المراجعة", subtitle: `مراجعة الصفحات من ${range.from} إلى ${range.to} خلال ${totalDays} يوماً` };
    }
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
        <p class="cal-page-footer">﷽ — خطة القرآن</p>
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

      const plan = getActivePlanAssignments();
      const months = groupByMonth(plan.days);
      if (months.length === 0) throw new Error("لا توجد بيانات كافية لبناء التقويم");

      const { jsPDF } = window.jspdf;
      const pdf = new jsPDF({ orientation: "portrait", unit: "pt", format: "a4" });
      const pageWidth = pdf.internal.pageSize.getWidth();
      const pageHeight = pdf.internal.pageSize.getHeight();

      for (let i = 0; i < months.length; i++) {
        showNotice(`جارٍ تجهيز شهر ${i + 1} من ${months.length}...`);
        calRoot.innerHTML = buildMonthPageHTML(months[i], plan.title, plan.subtitle);
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
      pdf.save("تقويم-خطة-القرآن.pdf");
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
