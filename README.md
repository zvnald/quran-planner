<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>خطة القرآن الكريم</title>

<!-- PWA: manifest + icons + platform meta tags so the plan can be "installed" as an app -->
<link rel="manifest" href="data:application/json;base64,ewogICJuYW1lIjogItiu2LfYqSDYp9mE2YLYsdii2YYg2KfZhNmD2LHZitmFIC0g2K3Zgdi4INmI2YXYsdin2KzYudipIiwKICAic2hvcnRfbmFtZSI6ICLYrti32Kkg2KfZhNmC2LHYotmGIiwKICAiZGVzY3JpcHRpb24iOiAi2KrYt9io2YrZgiDZhNiq2K7Yt9mK2Lcg2K3Zgdi4INmI2YXYsdin2KzYudipINin2YTZgtix2KLZhiDYp9mE2YPYsdmK2YUiLAogICJzdGFydF91cmwiOiAiLiIsCiAgInNjb3BlIjogIi4iLAogICJkaXNwbGF5IjogInN0YW5kYWxvbmUiLAogICJvcmllbnRhdGlvbiI6ICJwb3J0cmFpdCIsCiAgImJhY2tncm91bmRfY29sb3IiOiAiI2ZmZmRmYSIsCiAgInRoZW1lX2NvbG9yIjogIiM0YTMwMjAiLAogICJkaXIiOiAicnRsIiwKICAibGFuZyI6ICJhciIsCiAgImljb25zIjogWwogICAgeyAic3JjIjogImRhdGE6aW1hZ2Uvc3ZnK3htbDtiYXNlNjQsUEhOMlp5QjRiV3h1Y3owaWFIUjBjRG92TDNkM2R5NTNNeTV2Y21jdk1qQXdNQzl6ZG1jaUlIWnBaWGRDYjNnOUlqQWdNQ0ExTVRJZ05URXlJajRLSUNBOFpHVm1jejRLSUNBZ0lEeHNhVzVsWVhKSGNtRmthV1Z1ZENCcFpEMGlaeUlnZURFOUlqQWlJSGt4UFNJd0lpQjRNajBpTVNJZ2VUSTlJakVpUGdvZ0lDQWdJQ0E4YzNSdmNDQnZabVp6WlhROUlqQWlJSE4wYjNBdFkyOXNiM0k5SWlNM1lUVXlNellpTHo0S0lDQWdJQ0FnUEhOMGIzQWdiMlptYzJWMFBTSXhJaUJ6ZEc5d0xXTnZiRzl5UFNJak1tSXhZekV6SWk4K0NpQWdJQ0E4TDJ4cGJtVmhja2R5WVdScFpXNTBQZ29nSUR3dlpHVm1jejRLSUNBOGNtVmpkQ0IzYVdSMGFEMGlOVEV5SWlCb1pXbG5hSFE5SWpVeE1pSWdjbmc5SWprMklpQm1hV3hzUFNKMWNtd29JMmNwSWk4K0NpQWdQSFJsZUhRZ2VEMGlNalUySWlCNVBTSXpOREFpSUdadmJuUXRjMmw2WlQwaU1qY3dJaUIwWlhoMExXRnVZMmh2Y2owaWJXbGtaR3hsSWlCbWFXeHNQU0lqWmpabFptVXpJaUJtYjI1MExXWmhiV2xzZVQwaVIyVnZjbWRwWVN3Z0oxUnBiV1Z6SUU1bGR5QlNiMjFoYmljc0lITmxjbWxtSWlCbWIyNTBMWGRsYVdkb2REMGlOekF3SWo3Wmdqd3ZkR1Y0ZEQ0S1BDOXpkbWMrQ2c9PSIsICJzaXplcyI6ICIxOTJ4MTkyIiwgInR5cGUiOiAiaW1hZ2Uvc3ZnK3htbCIsICJwdXJwb3NlIjogImFueSIgfSwKICAgIHsgInNyYyI6ICJkYXRhOmltYWdlL3N2Zyt4bWw7YmFzZTY0LFBITjJaeUI0Yld4dWN6MGlhSFIwY0RvdkwzZDNkeTUzTXk1dmNtY3ZNakF3TUM5emRtY2lJSFpwWlhkQ2IzZzlJakFnTUNBMU1USWdOVEV5SWo0S0lDQThaR1ZtY3o0S0lDQWdJRHhzYVc1bFlYSkhjbUZrYVdWdWRDQnBaRDBpWnlJZ2VERTlJakFpSUhreFBTSXdJaUI0TWowaU1TSWdlVEk5SWpFaVBnb2dJQ0FnSUNBOGMzUnZjQ0J2Wm1aelpYUTlJakFpSUhOMGIzQXRZMjlzYjNJOUlpTTNZVFV5TXpZaUx6NEtJQ0FnSUNBZ1BITjBiM0FnYjJabWMyVjBQU0l4SWlCemRHOXdMV052Ykc5eVBTSWpNbUl4WXpFeklpOCtDaUFnSUNBOEwyeHBibVZoY2tkeVlXUnBaVzUwUGdvZ0lEd3ZaR1ZtY3o0S0lDQThjbVZqZENCM2FXUjBhRDBpTlRFeUlpQm9aV2xuYUhROUlqVXhNaUlnY25nOUlqazJJaUJtYVd4c1BTSjFjbXdvSTJjcElpOCtDaUFnUEhSbGVIUWdlRDBpTWpVMklpQjVQU0l6TkRBaUlHWnZiblF0YzJsNlpUMGlNamN3SWlCMFpYaDBMV0Z1WTJodmNqMGliV2xrWkd4bElpQm1hV3hzUFNJalpqWmxabVV6SWlCbWIyNTBMV1poYldsc2VUMGlSMlZ2Y21kcFlTd2dKMVJwYldWeklFNWxkeUJTYjIxaGJpY3NJSE5sY21sbUlpQm1iMjUwTFhkbGFXZG9kRDBpTnpBd0lqN1pnand2ZEdWNGRENEtQQzl6ZG1jK0NnPT0iLCAic2l6ZXMiOiAiNTEyeDUxMiIsICJ0eXBlIjogImltYWdlL3N2Zyt4bWwiLCAicHVycG9zZSI6ICJhbnkiIH0sCiAgICB7ICJzcmMiOiAiZGF0YTppbWFnZS9zdmcreG1sO2Jhc2U2NCxQSE4yWnlCNGJXeHVjejBpYUhSMGNEb3ZMM2QzZHk1M015NXZjbWN2TWpBd01DOXpkbWNpSUhacFpYZENiM2c5SWpBZ01DQTFNVElnTlRFeUlqNEtJQ0E4WkdWbWN6NEtJQ0FnSUR4c2FXNWxZWEpIY21Ga2FXVnVkQ0JwWkQwaVp5SWdlREU5SWpBaUlIa3hQU0l3SWlCNE1qMGlNU0lnZVRJOUlqRWlQZ29nSUNBZ0lDQThjM1J2Y0NCdlptWnpaWFE5SWpBaUlITjBiM0F0WTI5c2IzSTlJaU0zWVRVeU16WWlMejRLSUNBZ0lDQWdQSE4wYjNBZ2IyWm1jMlYwUFNJeElpQnpkRzl3TFdOdmJHOXlQU0lqTW1JeFl6RXpJaTgrQ2lBZ0lDQThMMnhwYm1WaGNrZHlZV1JwWlc1MFBnb2dJRHd2WkdWbWN6NEtJQ0E4Y21WamRDQjNhV1IwYUQwaU5URXlJaUJvWldsbmFIUTlJalV4TWlJZ2NuZzlJamsySWlCbWFXeHNQU0oxY213b0kyY3BJaTgrQ2lBZ1BIUmxlSFFnZUQwaU1qVTJJaUI1UFNJek5EQWlJR1p2Ym5RdGMybDZaVDBpTWpjd0lpQjBaWGgwTFdGdVkyaHZjajBpYldsa1pHeGxJaUJtYVd4c1BTSWpaalpsWm1VeklpQm1iMjUwTFdaaGJXbHNlVDBpUjJWdmNtZHBZU3dnSjFScGJXVnpJRTVsZHlCU2IyMWhiaWNzSUhObGNtbG1JaUJtYjI1MExYZGxhV2RvZEQwaU56QXdJajdaZ2p3dmRHVjRkRDRLUEM5emRtYytDZz09IiwgInNpemVzIjogIjUxMng1MTIiLCAidHlwZSI6ICJpbWFnZS9zdmcreG1sIiwgInB1cnBvc2UiOiAibWFza2FibGUiIH0KICBdCn0K" />
<meta name="theme-color" content="#4a3020" />
<link rel="icon" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIj4KICA8ZGVmcz4KICAgIDxsaW5lYXJHcmFkaWVudCBpZD0iZyIgeDE9IjAiIHkxPSIwIiB4Mj0iMSIgeTI9IjEiPgogICAgICA8c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiM3YTUyMzYiLz4KICAgICAgPHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSIjMmIxYzEzIi8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogIDwvZGVmcz4KICA8cmVjdCB3aWR0aD0iNTEyIiBoZWlnaHQ9IjUxMiIgcng9Ijk2IiBmaWxsPSJ1cmwoI2cpIi8+CiAgPHRleHQgeD0iMjU2IiB5PSIzNDAiIGZvbnQtc2l6ZT0iMjcwIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmaWxsPSIjZjZlZmUzIiBmb250LWZhbWlseT0iR2VvcmdpYSwgJ1RpbWVzIE5ldyBSb21hbicsIHNlcmlmIiBmb250LXdlaWdodD0iNzAwIj7ZgjwvdGV4dD4KPC9zdmc+Cg==" type="image/svg+xml" />
<link rel="apple-touch-icon" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MTIgNTEyIj4KICA8ZGVmcz4KICAgIDxsaW5lYXJHcmFkaWVudCBpZD0iZyIgeDE9IjAiIHkxPSIwIiB4Mj0iMSIgeTI9IjEiPgogICAgICA8c3RvcCBvZmZzZXQ9IjAiIHN0b3AtY29sb3I9IiM3YTUyMzYiLz4KICAgICAgPHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSIjMmIxYzEzIi8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogIDwvZGVmcz4KICA8cmVjdCB3aWR0aD0iNTEyIiBoZWlnaHQ9IjUxMiIgcng9Ijk2IiBmaWxsPSJ1cmwoI2cpIi8+CiAgPHRleHQgeD0iMjU2IiB5PSIzNDAiIGZvbnQtc2l6ZT0iMjcwIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBmaWxsPSIjZjZlZmUzIiBmb250LWZhbWlseT0iR2VvcmdpYSwgJ1RpbWVzIE5ldyBSb21hbicsIHNlcmlmIiBmb250LXdlaWdodD0iNzAwIj7ZgjwvdGV4dD4KPC9zdmc+Cg==" />
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
<meta name="apple-mobile-web-app-title" content="خطة القرآن" />
<meta name="mobile-web-app-capable" content="yes" />
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
  .student-name-field {
    position: relative;
    display: flex;
    align-items: center;
    gap: 0.6rem;
    justify-content: center;
    flex-wrap: wrap;
    margin: 0.9rem auto 0;
    max-width: 420px;
  }
  .student-name-field label {
    font-size: clamp(0.78rem, 2vw, 0.88rem);
    font-weight: 700;
    color: var(--sand);
    white-space: nowrap;
  }
  .student-name-field input {
    flex: 1;
    min-width: 160px;
    min-height: 42px;
    border-radius: 12px;
    border: 1.5px solid var(--caramel);
    background: var(--paper);
    color: var(--espresso);
    font-family: 'Tajawal', sans-serif;
    font-weight: 500;
    font-size: clamp(0.85rem, 2vw, 0.95rem);
    padding: 0.4rem 0.8rem;
    text-align: center;
  }
  .student-name-field input:focus {
    outline: none;
    border-color: var(--latte);
    box-shadow: 0 0 0 3px rgba(203,165,115,0.35);
  }
  .cal-plan-student { font-size: 0.85rem; font-weight: 700; color: var(--espresso); margin: 4px 0 0; }
  .cal-month-badge-hijri {
    display: block;
    font-family: 'Tajawal', sans-serif;
    font-weight: 500;
    font-size: 0.62rem;
    color: var(--sand);
    margin-top: 2px;
    text-align: center;
  }

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

  /* ---- Structured upcoming-schedule table (real dates + daily ranges) ---- */
  .sched-table-card { margin-top: 0.9rem; }
  .sched-table-wrap { overflow-x: auto; border-radius: 12px; border: 1px solid var(--sand); }
  .sched-table { width: 100%; border-collapse: collapse; font-size: clamp(0.76rem, 1.9vw, 0.86rem); white-space: nowrap; }
  .sched-table th {
    background: linear-gradient(135deg, var(--coffee), var(--espresso));
    color: var(--paper);
    font-weight: 700;
    padding: 0.55rem 0.6rem;
    text-align: center;
    position: sticky;
    top: 0;
  }
  .sched-table td { padding: 0.5rem 0.6rem; text-align: center; color: var(--espresso); border-top: 1px solid var(--sand); }
  .sched-table tbody tr:nth-child(even) { background: var(--linen); }
  .sched-table tr.sched-row-rest td { color: var(--cinnamon); background: #efe6d6; opacity: 0.85; }
  .sched-table td.sched-cell-memo { color: var(--coffee); font-weight: 700; }
  .sched-table td.sched-cell-review { color: var(--cinnamon); }

  .days-select-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(min(64px, 100%), 1fr)); gap: 0.5rem; margin-top: 0.7rem; }
  .day-toggle-btn {
    min-height: 44px;
    border-radius: 12px;
    border: 1.5px solid var(--sand);
    background: var(--paper);
    font-family: 'Tajawal', sans-serif;
    font-weight: 700;
    font-size: clamp(0.72rem, 1.8vw, 0.8rem);
    color: var(--cinnamon);
    cursor: pointer;
    padding: 0.4rem 0.2rem;
    transition: all .2s ease;
  }
  .day-toggle-btn.active {
    border-color: var(--caramel);
    background: linear-gradient(160deg, #f3e4cd, var(--linen));
    color: var(--espresso);
  }

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

  /* ---- Print calendar (built off-screen, used only for PDF export) ----
     Wrapped in a zero-size, overflow-hidden, non-fixed container instead of a huge
     negative offset: some mobile/webview renderers turn ancestors with a transform
     into a new containing block, which breaks "position:fixed; top:-99999px" and can
     leave the raw calendar markup visible at the bottom of the page. A 0x0 clipped
     box in normal flow has no such failure mode and still lays out/paints its
     full-size children so html2canvas can capture them correctly. */
  #pdf-calendar-wrap {
    position: absolute;
    top: 0;
    left: 0;
    width: 0;
    height: 0;
    overflow: hidden;
    pointer-events: none;
  }
  #pdf-calendar-root {
    width: 1200px;
    background: var(--paper);
  }
  @media print {
    #pdf-calendar-wrap { display: none !important; }
  }
  .cal-page {
    width: 1200px;
    height: 849px;
    background: var(--paper);
    padding: 30px 34px 20px;
    font-family: 'Tajawal', sans-serif;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    overflow: hidden;
  }
  .cal-page-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 2px solid var(--sand);
    padding-bottom: 12px;
    margin-bottom: 14px;
    flex: 0 0 auto;
  }
  .cal-plan-title { font-family: 'Amiri', serif; font-weight: 700; font-size: 1.35rem; color: var(--coffee); margin: 0; }
  .cal-plan-sub { font-size: 0.8rem; color: var(--cinnamon); margin: 3px 0 0; }
  .cal-month-badge {
    background: linear-gradient(135deg, var(--coffee), var(--espresso));
    color: var(--paper);
    font-family: 'Amiri', serif;
    font-weight: 700;
    font-size: 1.15rem;
    padding: 8px 26px 7px;
    border-radius: 22px;
    box-shadow: 0 6px 14px rgba(43,28,19,0.25);
    text-align: center;
    line-height: 1.35;
  }
  .cal-grid {
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    grid-template-rows: auto repeat(6, 1fr);
    gap: 8px;
    flex: 1 1 auto;
    min-height: 0;
  }
  .cal-dow {
    text-align: center;
    font-size: 0.82rem;
    font-weight: 700;
    color: var(--cinnamon);
    padding-bottom: 4px;
  }
  .cal-cell {
    border: 1.5px solid var(--sand);
    border-radius: 12px;
    min-height: 0;
    height: 100%;
    padding: 8px 10px;
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
  .cal-cell.cal-cell-combined { min-height: 0; }
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
  .cal-task-mini.memo.is-rest { color: var(--cinnamon); background: transparent; }
  .cal-task-mini.review { background: #efe6d6; color: var(--coffee); border: 1px dashed var(--caramel); }
  .cal-task-mini.review.is-rest { color: var(--cinnamon); background: transparent; }

  .cal-page-footer {
    margin-top: 10px;
    text-align: center;
    font-size: 0.72rem;
    color: var(--caramel);
    flex: 0 0 auto;
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
      <div class="student-name-field">
        <label for="student-name-input">اسم الطالب/ـة</label>
        <input type="text" id="student-name-input" placeholder="اكتب الاسم هنا (اختياري)" autocomplete="off" />
      </div>
      <button class="action-btn secondary" id="btn-install-app" style="display:none; margin-top:0.6rem;">📲 تثبيت كتطبيق على الجهاز</button>
    </header>

    <div id="start-date-card"></div>

    <div class="tabs">
      <button class="tab-btn active" id="tab-memorize">خطة الحفظ</button>
      <button class="tab-btn" id="tab-review">جدول المراجعة</button>
      <button class="tab-btn" id="tab-combined">خطة شاملة (حفظ ومراجعة)</button>
    </div>

    <div id="tab-content"></div>

    <div class="actions">
      <button class="action-btn primary" id="btn-pdf">حفظ الخطة PDF</button>
      <button class="action-btn secondary" id="btn-save">حفظ الخطة</button>
      <button class="action-btn secondary" id="btn-load">استرجاع الخطة المحفوظة</button>
    </div>
    <p class="save-notice" id="save-notice" style="display:none;"></p>
  </div>
</div>
<div id="pdf-calendar-wrap"><div id="pdf-calendar-root"></div></div>

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
    studentName: "",
    memo: {
      mode: "duration", years: 3, months: 0, pagesPerWeek: 7,
      direction: "forward",
      preMemorized: { enabled: false, mode: "range", fromPage: 1, toPage: 20, count: 20, secondRangeEnabled: false, fromPage2: 500, toPage2: 604 },
      daysMode: "all", activeDays: ["السبت", "الأحد", "الاثنين", "الثلاثاء", "الأربعاء", "الخميس", "الجمعة"],
    },
    review: {
      rangeMode: "pages", fromPage: 1, toPage: 20, fromSurah: 0, toSurah: 5,
      durationValue: 10, durationUnit: "days",
      daysMode: "custom", activeDays: ["السبت", "الأحد", "الاثنين", "الثلاثاء", "الأربعاء", "الخميس"],
      cyclicMode: false, cycleValue: 7, cycleUnit: "days", growWithMemo: false,
      programValue: 1, programUnit: "months",
      endMode: "duration", calendarType: "gregorian", endDate: null,
      reverseMode: false, reversePagesPerDay: 6, reverseRepeat: false,
    },
    // تاريخ بداية الخطة: "today" (اليوم) | "weekday" (أقرب يوم قادم باسمه) | "custom" (تاريخ محدد يدوياً)
    startDate: {
      mode: "today",
      weekday: null,
      calendarType: "gregorian",
      customDate: null,
    },
  };

  // يحسب تاريخ بداية الخطة الفعلي (كائن Date عند منتصف الليل) بناءً على اختيار المستخدم في state.startDate.
  // كل بناء للجدول اليومي في التطبيق (حفظ / مراجعة / خطة شاملة / تقويم PDF) ينطلق من هذا التاريخ بدل "اليوم" الفعلي مباشرة.
  function getPlanStartDate() {
    const t = new Date();
    const todayMidnight = new Date(t.getFullYear(), t.getMonth(), t.getDate());
    const sd = state.startDate;

    if (sd.mode === "custom" && sd.customDate && sd.customDate.year && sd.customDate.month && sd.customDate.day) {
      const g = sd.calendarType === "hijri" ? convertDateParts("hijri", "gregorian", sd.customDate) : sd.customDate;
      const d = new Date(g.year, g.month - 1, g.day);
      return isNaN(d.getTime()) ? todayMidnight : d;
    }

    if (sd.mode === "weekday" && sd.weekday) {
      const targetIdx = WEEK_DAYS.indexOf(sd.weekday);
      if (targetIdx === -1) return todayMidnight;
      const todayIdx = (todayMidnight.getDay() + 1) % 7; // متوافق مع ترتيب WEEK_DAYS (يبدأ بالسبت)
      const diff = (targetIdx - todayIdx + 7) % 7; // صفر يعني أن اليوم المختار هو اليوم نفسه
      return addDays(todayMidnight, diff);
    }

    return todayMidnight; // mode === "today" أو أي حالة غير مكتملة
  }

  // مكافئ todayHijriParts لكن مبني على تاريخ بداية الخطة (وليس التاريخ الفعلي)، يُستخدم لضبط سنة الأساس
  // في منتقي التاريخ الهجري حتى تظهر السنوات المناسبة عندما تكون بداية الخطة في تاريخ لاحق.
  function planStartHijriParts() {
    const d = getPlanStartDate();
    return jdnToHijri(gregorianToJDN(d.getFullYear(), d.getMonth() + 1, d.getDate()));
  }

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

  /* ---------------- Small debounce helper (used on numeric/date inputs) ---------------- */
  function debounce(fn, delay) {
    let t = null;
    return function (...args) {
      clearTimeout(t);
      t = setTimeout(() => fn.apply(this, args), delay);
    };
  }

  /* ---------------- Weekly active-days selection (أيام الحفظ / أيام المراجعة) ---------------- */
  // activeDays === null/undefined/empty/all-7 means "every day is active" (no rest days)
  function isDayActive(dayName, activeDays) {
    if (!activeDays || !activeDays.length || activeDays.length >= WEEK_DAYS.length) return true;
    return activeDays.indexOf(dayName) !== -1;
  }
  function getEffectiveActiveDays(obj) {
    if (obj.daysMode !== "custom") return null;
    return (obj.activeDays && obj.activeDays.length) ? obj.activeDays : null;
  }
  function getActiveDaysCountPerWeek(obj) {
    const eff = getEffectiveActiveDays(obj);
    return eff ? eff.length : WEEK_DAYS.length;
  }
  function buildDaysSelectHTML(obj, prefix, key, label) {
    const mode = obj.daysMode || "all";
    const active = (obj.activeDays && obj.activeDays.length) ? obj.activeDays : WEEK_DAYS;
    const daysButtonsHTML = WEEK_DAYS.map((d) =>
      `<button type="button" class="day-toggle-btn${active.indexOf(d) !== -1 ? " active" : ""}" id="${prefix}${key}-day-${d}">${d}</button>`
    ).join("");
    return `
      <div class="card form-card">
        <label class="field-label">${label}</label>
        <div class="mode-switch">
          <button class="mode-btn${mode !== "custom" ? " active" : ""}" id="${prefix}${key}-days-all">كل يوم</button>
          <button class="mode-btn${mode === "custom" ? " active" : ""}" id="${prefix}${key}-days-custom">أيام محددة</button>
        </div>
        ${mode === "custom" ? `
        <div class="days-select-grid">${daysButtonsHTML}</div>
        <p class="hint">الأيام غير المحددة تُعتبر أيام راحة ولن يُوزَّع عليها أي مقرر.</p>` : ""}
      </div>`;
  }
  function bindDaysSelectEvents(obj, prefix, key, onModeChange, onInputChange) {
    document.getElementById(`${prefix}${key}-days-all`).onclick = () => { obj.daysMode = "all"; onModeChange(); };
    document.getElementById(`${prefix}${key}-days-custom`).onclick = () => {
      obj.daysMode = "custom";
      if (!obj.activeDays || !obj.activeDays.length) obj.activeDays = WEEK_DAYS.slice();
      onModeChange();
    };
    if ((obj.daysMode || "all") === "custom") {
      WEEK_DAYS.forEach((d) => {
        const btn = document.getElementById(`${prefix}${key}-day-${d}`);
        if (!btn) return;
        btn.onclick = () => {
          const current = (obj.activeDays && obj.activeDays.length) ? obj.activeDays : WEEK_DAYS.slice();
          const set = new Set(current);
          if (set.has(d)) {
            if (set.size > 1) { set.delete(d); btn.classList.remove("active"); }
          } else {
            set.add(d);
            btn.classList.add("active");
          }
          obj.activeDays = WEEK_DAYS.filter((x) => set.has(x));
          onInputChange();
        };
      });
    }
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
    const d = addDays(getPlanStartDate(), 30);
    const g = { year: d.getFullYear(), month: d.getMonth() + 1, day: d.getDate() };
    return calendarType === "hijri" ? convertDateParts("gregorian", "hijri", g) : g;
  }
  function daysInHijriMonth() { return 30; }
  function daysInGregorianMonth(year, month) { return new Date(year, month, 0).getDate(); }

  /* ---------------- تاريخ بداية الخطة (Custom Start Date) — إعداد عام يؤثر في كل التبويبات ---------------- */
  function buildStartDateCardHTML() {
    const sd = state.startDate;
    const mode = sd.mode || "today";
    const isHijri = sd.calendarType === "hijri";
    const planStart = getPlanStartDate();

    const weekdayOptionsHTML = WEEK_DAYS.map((d) =>
      `<option value="${d}"${sd.weekday === d ? " selected" : ""}>${d} القادم</option>`
    ).join("");

    let customPickerHTML = "";
    if (mode === "custom") {
      const parts = sd.customDate || (isHijri ? todayHijriParts() : { year: new Date().getFullYear(), month: new Date().getMonth() + 1, day: new Date().getDate() });
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
      for (let y = baseYear - 1; y <= baseYear + 4; y++) {
        yearOptions += `<option value="${y}"${y === parts.year ? " selected" : ""}>${y}</option>`;
      }

      customPickerHTML = `
        <div class="mode-switch" style="margin-top:0.7rem;">
          <button class="mode-btn${!isHijri ? " active" : ""}" id="sd-caltype-gregorian">ميلادي</button>
          <button class="mode-btn${isHijri ? " active" : ""}" id="sd-caltype-hijri">هجري</button>
        </div>
        <div class="field-row" style="margin-top:0.6rem;">
          <div class="field-group">
            <span>اليوم</span>
            <select id="sd-day">${dayOptions}</select>
          </div>
          <div class="field-group">
            <span>الشهر</span>
            <select id="sd-month">${monthOptions}</select>
          </div>
          <div class="field-group">
            <span>السنة</span>
            <select id="sd-year">${yearOptions}</select>
          </div>
        </div>`;
    }

    const weekdayPickerHTML = mode === "weekday" ? `
        <div class="field-row" style="margin-top:0.6rem;">
          <div class="field-group wide">
            <span>ابدأ من</span>
            <select id="sd-weekday">${weekdayOptionsHTML}</select>
          </div>
        </div>` : "";

    return `
      <div class="card form-card" id="start-date-card-inner">
        <label class="field-label">تاريخ بداية الخطة</label>
        <div class="mode-switch">
          <button class="mode-btn${mode === "today" ? " active" : ""}" id="sd-mode-today">اليوم</button>
          <button class="mode-btn${mode === "weekday" ? " active" : ""}" id="sd-mode-weekday">يوم قادم محدد</button>
          <button class="mode-btn${mode === "custom" ? " active" : ""}" id="sd-mode-custom">تاريخ محدد</button>
        </div>
        ${weekdayPickerHTML}
        ${customPickerHTML}
        <p class="hint">ستبدأ الخطة فعلياً بتاريخ: ${formatDualDate(planStart)} (${WEEK_DAYS[(planStart.getDay() + 1) % 7]})</p>
      </div>`;
  }

  function refreshAllPlanResults() {
    if (state.tab === "memorize" && document.getElementById("memo-results")) updateMemoResults();
    else if (state.tab === "review" && document.getElementById("review-results")) updateReviewResults();
    else if (state.tab === "combined" && document.getElementById("combined-results")) updateCombinedResults();
  }

  function renderStartDateCard() {
    document.getElementById("start-date-card").innerHTML = buildStartDateCardHTML();
    bindStartDateCardEvents();
  }

  function bindStartDateCardEvents() {
    const sd = state.startDate;
    const mode = sd.mode || "today";

    document.getElementById("sd-mode-today").onclick = () => {
      state.startDate.mode = "today";
      renderStartDateCard();
      refreshAllPlanResults();
    };
    document.getElementById("sd-mode-weekday").onclick = () => {
      state.startDate.mode = "weekday";
      if (!state.startDate.weekday) state.startDate.weekday = WEEK_DAYS[(new Date().getDay() + 1) % 7];
      renderStartDateCard();
      refreshAllPlanResults();
    };
    document.getElementById("sd-mode-custom").onclick = () => {
      state.startDate.mode = "custom";
      if (!state.startDate.customDate) {
        const t = new Date();
        state.startDate.customDate = state.startDate.calendarType === "hijri"
          ? todayHijriParts()
          : { year: t.getFullYear(), month: t.getMonth() + 1, day: t.getDate() };
      }
      renderStartDateCard();
      refreshAllPlanResults();
    };

    if (mode === "weekday") {
      document.getElementById("sd-weekday").onchange = (e) => {
        state.startDate.weekday = e.target.value;
        renderStartDateCard();
        refreshAllPlanResults();
      };
    }

    if (mode === "custom") {
      document.getElementById("sd-caltype-gregorian").onclick = () => {
        if (state.startDate.calendarType !== "gregorian") {
          if (state.startDate.customDate) state.startDate.customDate = convertDateParts("hijri", "gregorian", state.startDate.customDate);
          state.startDate.calendarType = "gregorian";
          renderStartDateCard();
          refreshAllPlanResults();
        }
      };
      document.getElementById("sd-caltype-hijri").onclick = () => {
        if (state.startDate.calendarType !== "hijri") {
          if (state.startDate.customDate) state.startDate.customDate = convertDateParts("gregorian", "hijri", state.startDate.customDate);
          state.startDate.calendarType = "hijri";
          renderStartDateCard();
          refreshAllPlanResults();
        }
      };
      document.getElementById("sd-day").onchange = (e) => {
        state.startDate.customDate.day = Number(e.target.value);
        renderStartDateCard();
        refreshAllPlanResults();
      };
      document.getElementById("sd-month").onchange = (e) => {
        state.startDate.customDate.month = Number(e.target.value);
        renderStartDateCard();
        refreshAllPlanResults();
      };
      document.getElementById("sd-year").onchange = (e) => {
        state.startDate.customDate.year = Number(e.target.value);
        renderStartDateCard();
        refreshAllPlanResults();
      };
    }
  }

  /* ---------------- Pre-memorized pages (الحفظ المسبق) ---------------- */
  // Returns the list of already-memorized page ranges the user entered: 1-2 ranges when
  // pm.mode === "range", a single prefix range [1..count] when pm.mode === "count", and
  // empty when pre-memorization is off entirely.
  function getPreMemorizedRanges(m) {
    const pm = m.preMemorized;
    if (!pm || !pm.enabled) return [];
    if (pm.mode !== "range") {
      const count = Math.max(0, Math.min(Number(pm.count) || 0, TOTAL_PAGES));
      return count > 0 ? [{ from: 1, to: count }] : [];
    }
    const ranges = [];
    const from1 = Math.max(1, Math.min(Number(pm.fromPage) || 1, TOTAL_PAGES));
    const to1 = Math.max(from1, Math.min(Number(pm.toPage) || from1, TOTAL_PAGES));
    ranges.push({ from: from1, to: to1 });
    if (pm.secondRangeEnabled) {
      const from2 = Math.max(1, Math.min(Number(pm.fromPage2) || 1, TOTAL_PAGES));
      const to2 = Math.max(from2, Math.min(Number(pm.toPage2) || from2, TOTAL_PAGES));
      ranges.push({ from: from2, to: to2 });
    }
    return ranges;
  }
  // Merges the memorized ranges and returns whatever is left of the mushaf (1..604) as an
  // ascending list of gap segments. Two disjoint memorized ranges (e.g. 1-77 و 500-604) produce
  // the single gap between them; more complex inputs can produce several gaps. Returns
  // [{from:1,to:604}] when nothing is marked memorized, and [] when the whole mushaf is covered.
  function getRemainingSegments(m) {
    const memorized = getPreMemorizedRanges(m);
    if (!memorized.length) return [{ from: 1, to: TOTAL_PAGES }];
    const sorted = memorized.slice().sort((a, b) => a.from - b.from);
    const merged = [];
    sorted.forEach((r) => {
      if (merged.length && r.from <= merged[merged.length - 1].to + 1) {
        merged[merged.length - 1].to = Math.max(merged[merged.length - 1].to, r.to);
      } else {
        merged.push({ from: r.from, to: r.to });
      }
    });
    const segments = [];
    let cursor = 1;
    merged.forEach((r) => {
      if (r.from > cursor) segments.push({ from: cursor, to: r.from - 1 });
      cursor = Math.max(cursor, r.to + 1);
    });
    if (cursor <= TOTAL_PAGES) segments.push({ from: cursor, to: TOTAL_PAGES });
    return segments;
  }
  function getPreMemorizedCount(m) {
    const pm = m.preMemorized;
    if (!pm || !pm.enabled) return 0;
    const remaining = getRemainingSegments(m).reduce((s, seg) => s + (seg.to - seg.from + 1), 0);
    return Math.min(Math.max(TOTAL_PAGES - remaining, 0), TOTAL_PAGES - 1);
  }
  // "بداية الخطة" للعرض فقط: أول صفحة متبقية (اتجاه أمامي) أو آخر صفحة متبقية (اتجاه معكوس، من سورة الناس).
  function getRemainingStartPage(m) {
    const segs = getRemainingSegments(m);
    if (!segs.length) return TOTAL_PAGES;
    return m.direction === "reverse" ? segs[segs.length - 1].to : segs[0].from;
  }
  function getRemainingPages(m) {
    const total = getRemainingSegments(m).reduce((s, seg) => s + (seg.to - seg.from + 1), 0);
    return Math.max(total, 1);
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

  // يبني جدولاً منظّماً (تاريخ + يوم + الورد) لأول أيام أي خطة قادمة، اعتماداً على تواريخ حقيقية
  // محسوبة من تاريخ بداية الخطة (getPlanStartDate) مع مراعاة أيام الراحة الأسبوعية.
  // days: مصفوفة عناصر { date, isRest, fromPage, toPage, isFilled } كما تُنتجها دوال buildDailyAssignments/buildReverseDailyAssignments/buildCyclicAssignments.
  function buildUpcomingScheduleTableHTML(days, opts) {
    opts = opts || {};
    const limit = opts.limit || 14;
    const rangeLabelFn = opts.rangeLabelFn || ((d) => {
      if (d.isRest) return "يوم راحة";
      if (d.isFilled || d.fromPage == null) return "✓ تمّ الختم";
      return d.fromPage === d.toPage ? `صفحة ${d.fromPage}` : `من ${d.fromPage} إلى ${d.toPage}`;
    });
    const shown = days.slice(0, limit);
    const rows = shown.map((d) => {
      const dayName = WEEK_DAYS[(d.date.getDay() + 1) % 7];
      return `<tr class="${d.isRest ? "sched-row-rest" : ""}">
        <td>${formatDate(d.date)}</td>
        <td>${dayName}</td>
        <td>${rangeLabelFn(d)}</td>
      </tr>`;
    }).join("");
    const moreNote = days.length > limit
      ? `<p class="hint">وتتواصل الخطة يوماً بعد يوم حتى تاريخ ${formatDate(days[days.length - 1].date)} بإذن الله.</p>`
      : "";
    return `
      <div class="card sched-table-card">
        <h3 class="week-title">${opts.title || "النطاق اليومي والتواريخ"}</h3>
        <div class="sched-table-wrap">
          <table class="sched-table">
            <thead><tr><th>التاريخ</th><th>اليوم</th><th>${opts.rangeColLabel || "الورد"}</th></tr></thead>
            <tbody>${rows}</tbody>
          </table>
        </div>
        ${moreNote}
      </div>`;
  }
  // نسخة مخصّصة للخطة الشاملة: عمود للحفظ وعمود للمراجعة جنباً إلى جنب لكل تاريخ.
  function buildCombinedUpcomingScheduleTableHTML(days, opts) {
    opts = opts || {};
    const limit = opts.limit || 14;
    const labelFor = (d) => {
      if (!d) return "✓ اكتمل";
      if (d.isRest) return "راحة";
      if (d.isFilled || d.fromPage == null) return "✓ تمّ";
      return d.fromPage === d.toPage ? `ص${d.fromPage}` : `${d.fromPage}-${d.toPage}`;
    };
    const shown = days.slice(0, limit);
    const rows = shown.map((d) => {
      const dayName = WEEK_DAYS[(d.date.getDay() + 1) % 7];
      const memoRest = d.memo && d.memo.isRest;
      const reviewRest = d.review && d.review.isRest;
      const bothRest = memoRest && reviewRest;
      return `<tr class="${bothRest ? "sched-row-rest" : ""}">
        <td>${formatDate(d.date)}</td>
        <td>${dayName}</td>
        <td class="sched-cell-memo">${labelFor(d.memo)}</td>
        <td class="sched-cell-review">${labelFor(d.review)}</td>
      </tr>`;
    }).join("");
    const moreNote = days.length > limit
      ? `<p class="hint">وتتواصل الخطة يوماً بعد يوم حتى تاريخ ${formatDate(days[days.length - 1].date)} بإذن الله.</p>`
      : "";
    return `
      <div class="card sched-table-card">
        <h3 class="week-title">${opts.title || "النطاق اليومي والتواريخ (حفظ ومراجعة)"}</h3>
        <div class="sched-table-wrap">
          <table class="sched-table">
            <thead><tr><th>التاريخ</th><th>اليوم</th><th>الحفظ</th><th>المراجعة</th></tr></thead>
            <tbody>${rows}</tbody>
          </table>
        </div>
        ${moreNote}
      </div>`;
  }

  /* ---------------- Memorization calculations ---------------- */
  function computeDuration(m) {
    const remaining = getRemainingPages(m);
    const totalMonths = Math.max(m.years * 12 + Number(m.months || 0), 1);
    const totalDays = totalMonths * 30;
    const perWeek = (remaining / totalDays) * 7;
    const activeDaysPerWeek = getActiveDaysCountPerWeek(m);
    const perDay = perWeek / activeDaysPerWeek; // pages per active memorization day
    const ajzaPerMonth = ((remaining / totalDays) * 30) / 20;
    return { perDay, perWeek, ajzaPerMonth, finishDate: addDays(getPlanStartDate(), totalDays), totalDays, remaining };
  }
  function computePace(m) {
    const remaining = getRemainingPages(m);
    const perWeek = Math.max(Number(m.pagesPerWeek) || 0.0001, 0.0001);
    const totalWeeks = remaining / perWeek;
    const totalDays = Math.ceil(totalWeeks * 7);
    const totalYears = totalDays / 365;
    const activeDaysPerWeek = getActiveDaysCountPerWeek(m);
    const perDay = perWeek / activeDaysPerWeek; // pages per active memorization day
    return { totalWeeks, totalDays, totalYears, perDay, finishDate: addDays(getPlanStartDate(), totalDays), remaining };
  }
  // مدة خطة الحفظ بالأيام (تُستخدم لربط نهاية المراجعة بنهاية خطة الحفظ)
  function getMemoProgramDays(m) {
    const totalDays = (m.mode === "duration") ? computeDuration(m).totalDays : computePace(m).totalDays;
    return Math.max(Math.round(totalDays), 1);
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
    const pm = m.preMemorized || { enabled: false, mode: "range", fromPage: 1, toPage: 20, count: 20, secondRangeEnabled: false, fromPage2: 500, toPage2: TOTAL_PAGES };
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
        </div>
        <div class="mode-switch" style="margin-top:0.6rem;">
          <button class="mode-btn${!pm.secondRangeEnabled ? " active" : ""}" id="${prefix}memo-premem-range2-off">نطاق واحد فقط</button>
          <button class="mode-btn${pm.secondRangeEnabled ? " active" : ""}" id="${prefix}memo-premem-range2-on">إضافة نطاق آخر محفوظ</button>
        </div>
        ${pm.secondRangeEnabled ? `
        <div class="field-row" style="margin-top:0.5rem;">
          <div class="field-group">
            <span>من صفحة (٢)</span>
            <input type="number" min="1" max="${TOTAL_PAGES}" id="${prefix}memo-premem-from2" value="${pm.fromPage2 || 500}" />
          </div>
          <div class="field-group">
            <span>إلى صفحة (٢)</span>
            <input type="number" min="1" max="${TOTAL_PAGES}" id="${prefix}memo-premem-to2" value="${pm.toPage2 || TOTAL_PAGES}" />
          </div>
        </div>` : ""}` : `
        <div class="field-group wide">
          <input type="number" min="0" max="${TOTAL_PAGES - 1}" id="${prefix}memo-premem-count" value="${pm.count}" />
          <span>صفحة محفوظة</span>
        </div>`;

    const preMemCount = getPreMemorizedCount(m);
    const remainingSegs = pm.enabled ? getRemainingSegments(m) : [];
    const remainingTotal = getRemainingPages(m);
    let remainingHint;
    if (pm.mode !== "range") {
      remainingHint = `سيبدأ التخطيط من الصفحة ${getRemainingStartPage(m)} حتى ختم الباقي (${remainingTotal} صفحة).`;
    } else if (!remainingSegs.length) {
      remainingHint = `أتممت حفظ القرآن الكريم بالكامل بحسب ما أدخلته 🎉`;
    } else if (remainingSegs.length === 1) {
      remainingHint = m.direction === "reverse"
        ? `سيبدأ التخطيط من الصفحة ${remainingSegs[0].to} تنازلياً حتى الصفحة ${remainingSegs[0].from} (${remainingTotal} صفحة).`
        : `سيبدأ التخطيط من الصفحة ${remainingSegs[0].from} حتى ختم الباقي (${remainingTotal} صفحة).`;
    } else {
      remainingHint = `تبقّى ${remainingSegs.length} مقاطع للحفظ (${remainingSegs.map((s) => `${s.from}-${s.to}`).join("، ")}) بإجمالي ${remainingTotal} صفحة، وسيوزَّع الحفظ عليها بالترتيب.`;
    }

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
        <p class="hint">المحفوظ حالياً: ${preMemCount} صفحة — ${remainingHint}</p>
        ` : ""}
      </div>`;

    const directionHTML = `
      <div class="card form-card">
        <label class="field-label">اتجاه الحفظ</label>
        <div class="mode-switch">
          <button class="mode-btn${m.direction !== "reverse" ? " active" : ""}" id="${prefix}memo-dir-forward">من البداية (الفاتحة)</button>
          <button class="mode-btn${m.direction === "reverse" ? " active" : ""}" id="${prefix}memo-dir-reverse">حفظ معكوس (من الناس)</button>
        </div>
        <p class="hint">${m.direction === "reverse" ? "سيبدأ الحفظ من نهاية القرآن الكريم (سورة الناس) ويتراجع صفحة فصفحة نحو البداية." : "الحفظ بالترتيب المعتاد من الفاتحة حتى ختم القرآن الكريم."}</p>
      </div>`;

    return `
      <div class="mode-switch">
        <button class="mode-btn${m.mode === "duration" ? " active" : ""}" id="${prefix}memo-mode-duration">الحساب بالمدة</button>
        <button class="mode-btn${m.mode === "pace" ? " active" : ""}" id="${prefix}memo-mode-pace">الحساب بعدد الصفحات</button>
      </div>
      ${formHTML}
      ${buildDaysSelectHTML(m, prefix, "memo", "أيام الحفظ الأسبوعية")}
      ${directionHTML}
      ${preMemHTML}
    `;
  }

  function bindMemoFormEvents(prefix, onModeChange, onInputChange) {
    const debouncedInputChange = debounce(onInputChange, 200);
    document.getElementById(`${prefix}memo-mode-duration`).onclick = () => { state.memo.mode = "duration"; onModeChange(); };
    document.getElementById(`${prefix}memo-mode-pace`).onclick = () => { state.memo.mode = "pace"; onModeChange(); };
    const m = state.memo;
    if (m.mode === "duration") {
      document.getElementById(`${prefix}memo-years`).oninput = (e) => { state.memo.years = Number(e.target.value); debouncedInputChange(); };
      document.getElementById(`${prefix}memo-months`).oninput = (e) => { state.memo.months = Number(e.target.value); debouncedInputChange(); };
    } else {
      document.getElementById(`${prefix}memo-pace`).oninput = (e) => { state.memo.pagesPerWeek = e.target.value; debouncedInputChange(); };
    }

    if (!m.preMemorized) m.preMemorized = { enabled: false, mode: "range", fromPage: 1, toPage: 20, count: 20, secondRangeEnabled: false, fromPage2: 500, toPage2: TOTAL_PAGES };
    document.getElementById(`${prefix}memo-premem-off`).onclick = () => { state.memo.preMemorized.enabled = false; onModeChange(); };
    document.getElementById(`${prefix}memo-premem-on`).onclick = () => { state.memo.preMemorized.enabled = true; onModeChange(); };
    if (m.preMemorized.enabled) {
      document.getElementById(`${prefix}memo-premem-mode-range`).onclick = () => { state.memo.preMemorized.mode = "range"; onModeChange(); };
      document.getElementById(`${prefix}memo-premem-mode-count`).onclick = () => { state.memo.preMemorized.mode = "count"; onModeChange(); };
      if (m.preMemorized.mode === "range") {
        document.getElementById(`${prefix}memo-premem-from`).oninput = (e) => { state.memo.preMemorized.fromPage = e.target.value; debouncedInputChange(); };
        document.getElementById(`${prefix}memo-premem-to`).oninput = (e) => { state.memo.preMemorized.toPage = e.target.value; debouncedInputChange(); };
        document.getElementById(`${prefix}memo-premem-range2-off`).onclick = () => { state.memo.preMemorized.secondRangeEnabled = false; onModeChange(); };
        document.getElementById(`${prefix}memo-premem-range2-on`).onclick = () => { state.memo.preMemorized.secondRangeEnabled = true; onModeChange(); };
        if (m.preMemorized.secondRangeEnabled) {
          document.getElementById(`${prefix}memo-premem-from2`).oninput = (e) => { state.memo.preMemorized.fromPage2 = e.target.value; debouncedInputChange(); };
          document.getElementById(`${prefix}memo-premem-to2`).oninput = (e) => { state.memo.preMemorized.toPage2 = e.target.value; debouncedInputChange(); };
        }
      } else {
        document.getElementById(`${prefix}memo-premem-count`).oninput = (e) => { state.memo.preMemorized.count = e.target.value; debouncedInputChange(); };
      }
    }
    document.getElementById(`${prefix}memo-dir-forward`).onclick = () => { state.memo.direction = "forward"; onModeChange(); };
    document.getElementById(`${prefix}memo-dir-reverse`).onclick = () => { state.memo.direction = "reverse"; onModeChange(); };
    bindDaysSelectEvents(state.memo, prefix, "memo", onModeChange, onInputChange);
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
    let totalDays;
    if (m.mode === "duration") {
      const r = computeDuration(m);
      totalDays = Math.max(Math.round(r.totalDays), 1);
      filledBeads = Math.min(TOTAL_AJZA, Math.round(r.ajzaPerMonth));
      html += `<div class="stats-grid">
        ${statCardHTML(r.perDay.toFixed(2), "صفحة في يوم الحفظ")}
        ${statCardHTML(r.perWeek.toFixed(1), "صفحة أسبوعياً")}
        ${statCardHTML(r.ajzaPerMonth.toFixed(1), "جزء شهرياً تقريباً")}
      </div>`;
      html += inspireHTML(`بإذن الله، بناءً على خطتك ستبدأ بتاريخ ${formatDualDate(getPlanStartDate())} وتختم حفظ ${hasPreMem ? "بقية" : ""} القرآن الكريم بتاريخ ${formatDualDate(r.finishDate)}${m.direction === "reverse" ? " (حفظاً معكوساً من سورة الناس)" : ""}`);
    } else {
      const r = computePace(m);
      totalDays = Math.max(Math.round(r.totalDays), 1);
      filledBeads = Math.min(TOTAL_AJZA, Math.round(((r.totalWeeks > 0 ? (Number(m.pagesPerWeek) * 30 / 7) : 0) / 20)));
      html += `<div class="stats-grid">
        ${statCardHTML(r.perDay.toFixed(2), "صفحة في يوم الحفظ")}
        ${statCardHTML(r.totalYears.toFixed(2), "سنة تقريباً")}
        ${statCardHTML(Math.ceil(r.totalWeeks), "أسبوعاً")}
      </div>`;
      html += inspireHTML(`بإذن الله، بناءً على معدلك ستبدأ بتاريخ ${formatDualDate(getPlanStartDate())} وتختم حفظ ${hasPreMem ? "بقية" : ""} القرآن الكريم بتاريخ ${formatDualDate(r.finishDate)}${m.direction === "reverse" ? " (حفظاً معكوساً من سورة الناس)" : ""}`);
    }
    if (hasPreMem) {
      filledBeads = Math.max(filledBeads, Math.min(TOTAL_AJZA, Math.round((preMemCount * 30) / TOTAL_PAGES)));
    }
    html += beadsHTML(filledBeads, `${filledBeads} من ${TOTAL_AJZA} جزءاً${hasPreMem ? " (شاملاً المحفوظ مسبقاً)" : " يمكن إنجازها في الشهر تقريباً"}`);

    const memoDays = buildSegmentedDailyAssignments(getRemainingSegments(m), totalDays, getEffectiveActiveDays(m), getPlanStartDate(), m.direction);
    html += buildUpcomingScheduleTableHTML(memoDays, { title: m.direction === "reverse" ? "النطاق اليومي والتواريخ (حفظ معكوس من الناس)" : "النطاق اليومي والتواريخ (حفظ)", rangeColLabel: "ورد الحفظ" });

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
    const planStart = getPlanStartDate();
    const startJDN = gregorianToJDN(planStart.getFullYear(), planStart.getMonth() + 1, planStart.getDate());
    const parts = r.endDate || defaultEndDateParts(r.calendarType);
    const targetJDN = r.calendarType === "hijri" ? hijriToJDN(parts.year, parts.month, parts.day) : gregorianToJDN(parts.year, parts.month, parts.day);
    return Math.max(targetJDN - startJDN, 1);
  }
  // Resolves the cyclic/repeating program's total length in days, whichever end-mode is active.
  // "withMemo" ties the review program's end to however long the memorization plan (state.memo)
  // takes to finish — e.g. memorization finishing in a month stops the review after that same month.
  function getProgramDays(r) {
    if (r.endMode === "withMemo") return getMemoProgramDays(state.memo);
    return r.endMode === "date" ? computeProgramDaysFromEndDate(r) : computeProgramDays(r);
  }
  function computeSchedule(r, totalPages, totalDays) {
    const activeDaysList = getEffectiveActiveDays(r);
    const planStart = getPlanStartDate();
    const todayIndex = (planStart.getDay() + 1) % 7;
    let activeOccurrences = 0;
    for (let i = 0; i < totalDays; i++) {
      const dow = (todayIndex + i) % 7;
      if (isDayActive(WEEK_DAYS[dow], activeDaysList)) activeOccurrences++;
    }
    const activeDays = Math.max(activeOccurrences, 1);
    const perDay = Math.ceil(totalPages / activeDays);
    const finishDate = addDays(planStart, totalDays);
    const weekPlan = WEEK_DAYS.map((day) => {
      const isRest = !isDayActive(day, activeDaysList);
      return { day, isRest, pages: isRest ? 0 : perDay };
    });
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
    const baseYear = isHijri ? planStartHijriParts().year : getPlanStartDate().getFullYear();
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

  // "طريقة تحديد نهاية برنامج المراجعة" (duration vs. specific end-date) + the matching fields.
  // Shared between the forward cyclic-review mode and the reverse-review-with-repeat mode, since
  // both need the exact same "how long should this keep repeating" setting.
  function buildProgramDurationFieldsHTML(r, prefix, showWithMemoOption) {
    return `
      <label class="field-label" style="margin-top:0.9rem;">طريقة تحديد نهاية برنامج المراجعة</label>
      <div class="mode-switch">
        <button class="mode-btn${r.endMode !== "date" && r.endMode !== "withMemo" ? " active" : ""}" id="${prefix}review-endmode-duration">مدة زمنية</button>
        <button class="mode-btn${r.endMode === "date" ? " active" : ""}" id="${prefix}review-endmode-date">تاريخ انتهاء محدد</button>
        ${showWithMemoOption ? `<button class="mode-btn${r.endMode === "withMemo" ? " active" : ""}" id="${prefix}review-endmode-withmemo">مع نهاية خطة الحفظ</button>` : ""}
      </div>

      ${r.endMode === "date" ? buildEndDatePickerHTML(r, prefix) : r.endMode === "withMemo" && showWithMemoOption ? `
      <p class="hint" style="margin-top:0.6rem;">ستتوقف المراجعة تلقائياً بمجرد انتهاء خطة الحفظ الحالية (بعد ${getMemoProgramDays(state.memo)} يوماً، بتاريخ ${formatDualDate(addDays(getPlanStartDate(), getMemoProgramDays(state.memo)))})، حتى لو لم تكتمل دورة المراجعة الجارية.</p>
      ` : `
      <label class="field-label" style="margin-top:0.9rem;">المدة الإجمالية للبرنامج (تكرار المراجعة حتى)</label>
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
    `;
  }
  function bindProgramDurationFieldEvents(prefix, onModeChange, onInputChange, showWithMemoOption) {
    const debouncedInputChange = debounce(onInputChange, 200);
    const r = state.review;
    document.getElementById(`${prefix}review-endmode-duration`).onclick = () => { state.review.endMode = "duration"; onModeChange(); };
    document.getElementById(`${prefix}review-endmode-date`).onclick = () => {
      if (!state.review.endDate) state.review.endDate = defaultEndDateParts(state.review.calendarType);
      state.review.endMode = "date";
      onModeChange();
    };
    if (showWithMemoOption) {
      const withMemoBtn = document.getElementById(`${prefix}review-endmode-withmemo`);
      if (withMemoBtn) withMemoBtn.onclick = () => { state.review.endMode = "withMemo"; onModeChange(); };
    }
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
    } else if (!(r.endMode === "withMemo" && showWithMemoOption)) {
      document.getElementById(`${prefix}review-program-value`).oninput = (e) => { state.review.programValue = e.target.value; debouncedInputChange(); };
      document.getElementById(`${prefix}review-program-unit`).onchange = (e) => { state.review.programUnit = e.target.value; onInputChange(); };
    }
  }

  function buildReviewFormHTML(r, prefix) {
    const rangeForHints = computeRange(r);
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

    const reviewDaysSelectHTML = buildDaysSelectHTML(r, prefix, "review", "أيام المراجعة الأسبوعية");

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

        ${buildProgramDurationFieldsHTML(r, prefix, prefix === "c-")}

        <p class="hint">سيتكرر ختم هذا النطاق تلقائياً بنفس الدورة حتى نهاية البرنامج، وينعكس هذا التكرار كاملاً على تقويم PDF. ملاحظة: تتوقف المراجعة فوراً عند بلوغ تاريخ الانتهاء، حتى لو لم تكتمل الدورة الجارية.</p>
        ${reviewDaysSelectHTML}

        <label class="field-label" style="margin-top:0.9rem;">زيادة المراجعة تلقائياً مع تقدّم الحفظ</label>
        <div class="mode-switch">
          <button class="mode-btn${!r.growWithMemo ? " active" : ""}" id="${prefix}review-grow-off">نطاق ثابت (بدون زيادة)</button>
          <button class="mode-btn${r.growWithMemo ? " active" : ""}" id="${prefix}review-grow-on">نطاق متزايد (يضم الحفظ الجديد)</button>
        </div>
        <p class="hint">${r.growWithMemo
          ? `مع كل دورة مراجعة جديدة (كل ${computeCycleDays(r)} يوماً)، سيُضاف ما تم حفظه في الدورة السابقة إلى نطاق المراجعة، ويُعاد توزيع صفحات المراجعة يومياً بحيث يُختم النطاق الجديد بالكامل خلال الدورة — وتستمر الزيادة تلقائياً حتى تنتهي خطة الحفظ الحالية.`
          : `النطاق المحدد أعلاه (${rangeForHints.from}-${rangeForHints.to}) سيبقى ثابتاً ويتكرر ختمه كما هو طوال البرنامج، دون إضافة ما يُحفظ جديداً.`}</p>
      </div>` : r.reverseMode ? `
      <div class="card form-card">
        <label class="field-label">عدد الصفحات يومياً (تنازلياً من الصفحة الأعلى)</label>
        <div class="field-row">
          <div class="field-group">
            <input type="number" min="1" id="${prefix}review-reverse-pages" value="${r.reversePagesPerDay}" />
          </div>
        </div>

        <label class="field-label" style="margin-top:0.9rem;">بعد الوصول إلى الصفحة ${rangeForHints.from}</label>
        <div class="mode-switch">
          <button class="mode-btn${!r.reverseRepeat ? " active" : ""}" id="${prefix}review-repeat-off">لمرة واحدة</button>
          <button class="mode-btn${r.reverseRepeat ? " active" : ""}" id="${prefix}review-repeat-on">تكرار المراجعة الدوري (نفس المراجعة)</button>
        </div>

        ${r.reverseRepeat ? buildProgramDurationFieldsHTML(r, prefix, prefix === "c-") : ""}

        <p class="hint">${r.reverseRepeat
          ? `ستبدأ الخطة من الصفحة ${rangeForHints.to} وتتراجع تنازلياً حتى الصفحة ${rangeForHints.from}، ثم تعيد نفس المراجعة العكسية من جديد تلقائياً حتى نهاية البرنامج.`
          : `تبدأ الخطة من الصفحة ${rangeForHints.to} (الأقرب حفظاً) وتتراجع يوماً بعد يوم حتى الوصول إلى الصفحة ${rangeForHints.from}، دون تحديد مدة مسبقة.`}</p>
        ${reviewDaysSelectHTML}
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
        ${reviewDaysSelectHTML}
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
        <button class="mode-btn${!r.cyclicMode && !r.reverseMode ? " active" : ""}" id="${prefix}review-cycle-off">مراجعة لمرة واحدة</button>
        <button class="mode-btn${r.cyclicMode ? " active" : ""}" id="${prefix}review-cycle-on">تكرار المراجعة الدوري</button>
        <button class="mode-btn${r.reverseMode ? " active" : ""}" id="${prefix}review-mode-reverse">مراجعة عكسية</button>
      </div>

      ${scheduleFieldsHTML}
    `;
  }

  function bindReviewFormEvents(prefix, onModeChange, onInputChange) {
    const debouncedInputChange = debounce(onInputChange, 200);
    document.getElementById(`${prefix}review-mode-pages`).onclick = () => { state.review.rangeMode = "pages"; onModeChange(); };
    document.getElementById(`${prefix}review-mode-surah`).onclick = () => { state.review.rangeMode = "surah"; onModeChange(); };

    document.getElementById(`${prefix}review-cycle-off`).onclick = () => { state.review.cyclicMode = false; state.review.reverseMode = false; onModeChange(); };
    document.getElementById(`${prefix}review-cycle-on`).onclick = () => { state.review.cyclicMode = true; state.review.reverseMode = false; onModeChange(); };
    document.getElementById(`${prefix}review-mode-reverse`).onclick = () => { state.review.cyclicMode = false; state.review.reverseMode = true; onModeChange(); };

    const r = state.review;
    if (r.rangeMode === "pages") {
      document.getElementById(`${prefix}review-from-page`).oninput = (e) => { state.review.fromPage = e.target.value; debouncedInputChange(); };
      document.getElementById(`${prefix}review-to-page`).oninput = (e) => { state.review.toPage = e.target.value; debouncedInputChange(); };
    } else {
      document.getElementById(`${prefix}review-from-surah`).onchange = (e) => { state.review.fromSurah = Number(e.target.value); onInputChange(); };
      document.getElementById(`${prefix}review-to-surah`).onchange = (e) => { state.review.toSurah = Number(e.target.value); onInputChange(); };
    }

    if (r.cyclicMode) {
      document.getElementById(`${prefix}review-cycle-value`).oninput = (e) => { state.review.cycleValue = e.target.value; debouncedInputChange(); };
      document.getElementById(`${prefix}review-cycle-unit`).onchange = (e) => { state.review.cycleUnit = e.target.value; onInputChange(); };
      bindProgramDurationFieldEvents(prefix, onModeChange, onInputChange, prefix === "c-");
      document.getElementById(`${prefix}review-grow-off`).onclick = () => { state.review.growWithMemo = false; onModeChange(); };
      document.getElementById(`${prefix}review-grow-on`).onclick = () => { state.review.growWithMemo = true; onModeChange(); };
    } else if (r.reverseMode) {
      document.getElementById(`${prefix}review-reverse-pages`).oninput = (e) => { state.review.reversePagesPerDay = e.target.value; debouncedInputChange(); };
      document.getElementById(`${prefix}review-repeat-off`).onclick = () => { state.review.reverseRepeat = false; onModeChange(); };
      document.getElementById(`${prefix}review-repeat-on`).onclick = () => { state.review.reverseRepeat = true; onModeChange(); };
      if (r.reverseRepeat) {
        bindProgramDurationFieldEvents(prefix, onModeChange, onInputChange, prefix === "c-");
      }
    } else {
      document.getElementById(`${prefix}review-duration-value`).oninput = (e) => { state.review.durationValue = e.target.value; debouncedInputChange(); };
      document.getElementById(`${prefix}review-duration-unit`).onchange = (e) => { state.review.durationUnit = e.target.value; onInputChange(); };
    }
    bindDaysSelectEvents(state.review, prefix, "review", onModeChange, onInputChange);
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

    if (r.cyclicMode && r.growWithMemo) {
      const cycleDays = computeCycleDays(r);
      const programDays = getProgramDays(r);
      const numCycles = Math.max(Math.round(programDays / cycleDays), 1);
      const planStart = getPlanStartDate();
      const programFinish = addDays(planStart, programDays);
      const memoDays = getMemoDaysForGrowth();
      const finalSegments = getGrowingReviewFinalSegments(range.from, range.to, memoDays);
      const finalPageCount = getGrowingReviewFinalPageCount(range.from, range.to, memoDays);
      const finalDesc = describeReviewSegments(finalSegments);

      const firstCycle = buildDailyAssignments(range.from, range.to, cycleDays, getEffectiveActiveDays(r), planStart);
      const cycleSchedule = computeSchedule(r, totalPages, cycleDays);
      const schedTableHTML = buildUpcomingScheduleTableHTML(firstCycle, { title: "جدول الدورة الأولى (سينمو النطاق تلقائياً بعد كل دورة)", limit: Math.max(cycleDays, 7) });

      const endText = r.endMode === "date"
        ? `حتى تاريخ الانتهاء المحدد: ${formatDualDate(programFinish)} (${numCycles} دورة تقريباً)`
        : r.endMode === "withMemo"
        ? `حتى انتهاء خطة الحفظ بتاريخ ${formatDualDate(programFinish)} (${numCycles} دورة تقريباً)`
        : `على مدار البرنامج حتى ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`;

      const html = `
        <div class="stats-grid">
          ${statCardHTML(cycleSchedule.perDay, "صفحة يومياً في الدورة الأولى")}
          ${statCardHTML(cycleDays, "يوماً لكل دورة")}
          ${statCardHTML(finalPageCount, "إجمالي صفحات المراجعة أخيراً")}
        </div>
        ${inspireHTML(`ستبدأ الخطة بتاريخ ${formatDualDate(planStart)} بمراجعة الصفحات من ${range.from} إلى ${range.to}، ثم مع كل دورة جديدة كل ${cycleDays} يوماً يُضاف إليها ما تم حفظه حديثاً في تلك الدورة (بحسب مكانه الفعلي من القرآن)، حتى يشمل النطاق النهائي: ${finalDesc} (${finalPageCount} صفحة)، ${endText} بإذن الله`)}
        ${schedTableHTML}
      `;
      document.getElementById("review-results").innerHTML = html;
      return;
    }

    if (r.cyclicMode) {
      const cycleDays = computeCycleDays(r);
      const programDays = getProgramDays(r);
      const cycleSchedule = computeSchedule(r, totalPages, cycleDays);
      const numCycles = Math.max(Math.round(programDays / cycleDays), 1);
      const planStart = getPlanStartDate();
      const programFinish = addDays(planStart, programDays);

      const firstCycle = buildDailyAssignments(range.from, range.to, cycleDays, getEffectiveActiveDays(r), planStart);
      const schedTableHTML = buildUpcomingScheduleTableHTML(firstCycle, { title: "جدول الدورة الأولى (تتكرر تلقائياً)", limit: Math.max(cycleDays, 7) });

      const endText = r.endMode === "date"
        ? `حتى تاريخ الانتهاء المحدد: ${formatDualDate(programFinish)} (${numCycles} دورة تقريباً)، وستتوقف المراجعة فور بلوغ هذا التاريخ`
        : r.endMode === "withMemo"
        ? `حتى انتهاء خطة الحفظ بتاريخ ${formatDualDate(programFinish)} (${numCycles} دورة تقريباً)، وستتوقف المراجعة فوراً عند ذلك حتى لو لم تكتمل الدورة الجارية`
        : `على مدار البرنامج حتى ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`;

      const html = `
        <div class="stats-grid">
          ${statCardHTML(cycleSchedule.perDay, "صفحة يومياً بالدورة")}
          ${statCardHTML(cycleDays, "يوماً لكل دورة")}
          ${statCardHTML(numCycles, "دورة ختم بالبرنامج")}
        </div>
        ${inspireHTML(`ستبدأ الخطة بتاريخ ${formatDualDate(planStart)}، وستتكرر دورة ختم هذا النطاق كل ${cycleDays} يوماً ${endText}`)}
        ${schedTableHTML}
      `;
      document.getElementById("review-results").innerHTML = html;
      return;
    }

    if (r.reverseMode) {
      const perDay = Math.max(Math.round(Number(r.reversePagesPerDay) || 1), 1);
      const planStart = getPlanStartDate();

      if (r.reverseRepeat) {
        const programDays = getProgramDays(r);
        const reverseDays = buildReverseCyclicAssignments(range.from, range.to, perDay, programDays, getEffectiveActiveDays(r), planStart);
        const programFinish = addDays(planStart, programDays);
        const schedTableHTML = buildUpcomingScheduleTableHTML(reverseDays, { title: "النطاق اليومي والتواريخ (عكسية متكررة)" });
        const endText = r.endMode === "date"
          ? `حتى تاريخ الانتهاء المحدد: ${formatDualDate(programFinish)}، وستتوقف المراجعة فور بلوغ هذا التاريخ`
          : r.endMode === "withMemo"
          ? `حتى انتهاء خطة الحفظ بتاريخ ${formatDualDate(programFinish)}، وستتوقف فوراً عند ذلك`
          : `على مدار البرنامج حتى ${formatDualDate(programFinish)} بإذن الله`;

        const html = `
          <div class="stats-grid">
            ${statCardHTML(perDay, "صفحة يومياً تنازلياً")}
            ${statCardHTML(totalPages, "إجمالي صفحات النطاق")}
            ${statCardHTML(programDays, "يوماً لبرنامج التكرار")}
          </div>
          ${inspireHTML(`ستبدأ المراجعة العكسية بتاريخ ${formatDualDate(planStart)} من الصفحة ${range.to} وتتراجع تنازلياً حتى الصفحة ${range.from}، ثم تعيد نفس المراجعة من جديد ${endText}`)}
          ${schedTableHTML}
        `;
        document.getElementById("review-results").innerHTML = html;
        return;
      }

      const reverseDays = buildReverseDailyAssignments(range.from, range.to, perDay, getEffectiveActiveDays(r), planStart);
      const activeDays = reverseDays.filter((d) => !d.isRest).length;
      const finishDate = reverseDays.length ? reverseDays[reverseDays.length - 1].date : planStart;
      const schedTableHTML = buildUpcomingScheduleTableHTML(reverseDays, { title: "النطاق اليومي والتواريخ (تنازلياً)" });

      const html = `
        <div class="stats-grid">
          ${statCardHTML(perDay, "صفحة يومياً تنازلياً")}
          ${statCardHTML(activeDays, "يوم مراجعة فعلي")}
          ${statCardHTML(totalPages, "إجمالي الصفحات")}
        </div>
        ${inspireHTML(`ستبدأ المراجعة العكسية بتاريخ ${formatDualDate(planStart)} من الصفحة ${range.to} وتتراجع تنازلياً حتى الصفحة ${range.from}، لتختم بتاريخ ${formatDate(finishDate)} بإذن الله`)}
        ${schedTableHTML}
      `;
      document.getElementById("review-results").innerHTML = html;
      return;
    }

    const totalDays = computeTotalDays(r);
    const schedule = computeSchedule(r, totalPages, totalDays);
    const planStart = getPlanStartDate();
    const dailyDays = buildDailyAssignments(range.from, range.to, totalDays, getEffectiveActiveDays(r), planStart);
    const schedTableHTML = buildUpcomingScheduleTableHTML(dailyDays, { title: "النطاق اليومي والتواريخ" });

    const html = `
      <div class="stats-grid">
        ${statCardHTML(schedule.perDay, "صفحة يومياً")}
        ${statCardHTML(totalDays, "يوماً للمراجعة")}
        ${statCardHTML(totalPages, "إجمالي الصفحات")}
      </div>
      ${inspireHTML(`ستبدأ الخطة بتاريخ ${formatDualDate(planStart)} وتختم مراجعة هذا النطاق بتاريخ ${formatDate(schedule.finishDate)} بإذن الله`)}
      ${schedTableHTML}
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
    const planStart = getPlanStartDate();

    let memoPerDay, memoFinish, memoTotalDays;
    if (m.mode === "duration") {
      const rr = computeDuration(m);
      memoPerDay = rr.perDay;
      memoFinish = rr.finishDate;
      memoTotalDays = Math.max(Math.round(rr.totalDays), 1);
    } else {
      const rr = computePace(m);
      memoPerDay = rr.perDay;
      memoFinish = rr.finishDate;
      memoTotalDays = Math.max(Math.round(rr.totalDays), 1);
    }
    const memoDays = buildSegmentedDailyAssignments(getRemainingSegments(m), memoTotalDays, getEffectiveActiveDays(m), planStart, m.direction);

    const range = computeRange(r);
    const totalPages = range.to - range.from + 1;

    let reviewStatCardHTML, reviewDays, reviewInspireText;
    if (r.cyclicMode && r.growWithMemo) {
      const cycleDays = computeCycleDays(r);
      const programDays = getProgramDays(r);
      const numCycles = Math.max(Math.round(programDays / cycleDays), 1);
      const programFinish = addDays(planStart, programDays);
      const finalDesc = describeReviewSegments(getGrowingReviewFinalSegments(range.from, range.to, memoDays));
      const finalPageCount = getGrowingReviewFinalPageCount(range.from, range.to, memoDays);
      reviewDays = buildGrowingCyclicAssignments(range.from, range.to, cycleDays, programDays, getEffectiveActiveDays(r), planStart, memoDays);

      reviewStatCardHTML = statCardHTML(cycleDays, "يوماً لكل دورة مراجعة");
      const endText = r.endMode === "date"
        ? `حتى تتوقف فوراً بتاريخ ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`
        : r.endMode === "withMemo"
        ? `حتى تتوقف تلقائياً مع انتهاء خطة الحفظ بتاريخ ${formatDualDate(programFinish)} (${numCycles} دورة تقريباً)`
        : `حتى ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`;
      reviewInspireText = `وستراجع من الصفحة ${range.from} إلى الصفحة ${range.to} كل ${cycleDays} يوماً، مع إضافة ما يُحفظ حديثاً إلى نطاق المراجعة تلقائياً بعد كل دورة (حسب مكانه الفعلي من القرآن)، حتى يشمل النطاق النهائي: ${finalDesc} (${finalPageCount} صفحة)، ${endText}`;
    } else if (r.cyclicMode) {
      const cycleDays = computeCycleDays(r);
      const programDays = getProgramDays(r);
      const cycleSchedule = computeSchedule(r, totalPages, cycleDays);
      const numCycles = Math.max(Math.round(programDays / cycleDays), 1);
      const programFinish = addDays(planStart, programDays);
      reviewDays = buildCyclicAssignments(range.from, range.to, cycleDays, programDays, getEffectiveActiveDays(r), planStart);

      reviewStatCardHTML = statCardHTML(cycleDays, "يوماً لكل دورة مراجعة");
      reviewInspireText = r.endMode === "date"
        ? `وستتكرر دورة مراجعة هذا النطاق كل ${cycleDays} يوماً حتى تتوقف فوراً بتاريخ ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`
        : r.endMode === "withMemo"
        ? `وستتكرر دورة مراجعة هذا النطاق كل ${cycleDays} يوماً حتى تتوقف تلقائياً مع انتهاء خطة الحفظ بتاريخ ${formatDualDate(programFinish)} (${numCycles} دورة تقريباً)`
        : `وستتكرر دورة مراجعة هذا النطاق كل ${cycleDays} يوماً حتى ${formatDualDate(programFinish)} بإذن الله (${numCycles} دورة تقريباً)`;
    } else if (r.reverseMode && r.reverseRepeat) {
      const perDay = Math.max(Math.round(Number(r.reversePagesPerDay) || 1), 1);
      const programDays = getProgramDays(r);
      const programFinish = addDays(planStart, programDays);
      reviewDays = buildReverseCyclicAssignments(range.from, range.to, perDay, programDays, getEffectiveActiveDays(r), planStart);

      reviewStatCardHTML = statCardHTML(perDay, "صفحة مراجعة يومياً (تنازلياً متكررة)");
      reviewInspireText = `وستكرر مراجعة عكسية تنازلية من الصفحة ${range.to} إلى الصفحة ${range.from} حتى ${formatDualDate(programFinish)} بإذن الله`;
    } else if (r.reverseMode) {
      const perDay = Math.max(Math.round(Number(r.reversePagesPerDay) || 1), 1);
      reviewDays = buildReverseDailyAssignments(range.from, range.to, perDay, getEffectiveActiveDays(r), planStart);
      const finishDate = reviewDays.length ? reviewDays[reviewDays.length - 1].date : planStart;

      reviewStatCardHTML = statCardHTML(perDay, "صفحة مراجعة يومياً (تنازلياً)");
      reviewInspireText = `وستراجع تنازلياً من الصفحة ${range.to} إلى الصفحة ${range.from}، لتختم بتاريخ ${formatDate(finishDate)} بإذن الله`;
    } else {
      const totalDays = computeTotalDays(r);
      const schedule = computeSchedule(r, totalPages, totalDays);
      reviewDays = buildDailyAssignments(range.from, range.to, totalDays, getEffectiveActiveDays(r), planStart);

      reviewStatCardHTML = statCardHTML(schedule.perDay, "صفحة مراجعة يومياً");
      reviewInspireText = `وستختم مراجعة هذا النطاق بتاريخ ${formatDate(schedule.finishDate)}، بإذن الله`;
    }

    const zipLen = Math.min(Math.max(memoDays.length, reviewDays.length), 30);
    const zippedDays = [];
    for (let i = 0; i < zipLen; i++) {
      zippedDays.push({ date: addDays(planStart, i), memo: memoDays[i] || null, review: reviewDays[i] || null });
    }
    const schedTableHTML = buildCombinedUpcomingScheduleTableHTML(zippedDays);

    const html = `
      <div class="stats-grid">
        ${statCardHTML(memoPerDay.toFixed(2), "صفحة حفظ يومياً")}
        ${reviewStatCardHTML}
        ${statCardHTML(totalPages, "صفحات نطاق المراجعة")}
      </div>
      <div class="inspire-card">
        <span class="inspire-icon">✦</span>
        <p>ستبدأ الخطة بتاريخ ${formatDualDate(planStart)}، وستختم حفظ القرآن الكريم بتاريخ ${formatDate(memoFinish)}، ${reviewInspireText}</p>
      </div>
      ${schedTableHTML}
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
      const payload = { tab: state.tab, memoState: state.memo, reviewState: state.review, startDateState: state.startDate, studentName: state.studentName };
      const result = await window.storage.set(STORAGE_KEY, JSON.stringify(payload), false);
      showNotice(result ? "تم حفظ الخطة بنجاح ✓" : "تعذّر حفظ الخطة، حاول مرة أخرى", 2500);
    } catch (e) {
      showNotice("تعذّر حفظ الخطة، حاول مرة أخرى", 2500);
    } finally {
      btn.disabled = false;
      btn.textContent = "حفظ الخطة";
    }
  });

  /* Explicit "استرجاع الخطة المحفوظة" — loading a saved plan is now something the user must
     press on purpose. Previously this ran silently on every page load and could race with the
     user's own typing (the storage fetch resolving *after* they'd already started entering new
     numbers), silently wiping out what they'd just entered and making "حفظ الخطة PDF" export the
     old saved plan instead. The live state (and therefore every PDF export) now only ever changes
     because of the user's own input on this screen, never a background fetch. */
  document.getElementById("btn-load").addEventListener("click", async function () {
    const btn = this;
    btn.disabled = true;
    const originalText = btn.textContent;
    btn.textContent = "جارٍ الاسترجاع...";
    try {
      const result = await window.storage.get(STORAGE_KEY, false);
      if (result && result.value) {
        const data = JSON.parse(result.value);
        if (data.tab) state.tab = data.tab;
        if (data.memoState) Object.assign(state.memo, data.memoState);
        if (data.reviewState) Object.assign(state.review, data.reviewState);
        if (data.startDateState) Object.assign(state.startDate, data.startDateState);
        if (typeof data.studentName === "string") {
          state.studentName = data.studentName;
          document.getElementById("student-name-input").value = data.studentName;
        }
        renderStartDateCard();
        renderTab();
        showNotice("تم استرجاع خطتك المحفوظة ✓", 2200);
      } else {
        showNotice("لا توجد خطة محفوظة بعد", 2200);
      }
    } catch (e) {
      showNotice("تعذّر استرجاع الخطة المحفوظة", 2200);
    } finally {
      btn.disabled = false;
      btn.textContent = originalText;
    }
  });

  /* اسم الطالب: يُخزَّن في state ليظهر في عنوان ملف PDF وداخل كل صفحة من صفحات الخطة */
  document.getElementById("student-name-input").oninput = function (e) {
    state.studentName = e.target.value;
  };

  /* Initial render: always starts from the plain default state — never touches storage — so the
     form the user sees (and therefore every PDF/print) reflects only what's on screen. */
  renderStartDateCard();
  renderTab();

  /* ---------------- Build day-by-day plan assignments ---------------- */
  // Returns an array (length totalDays) of { date, isRest, fromPage, toPage, isFilled }
  function buildDailyAssignments(startPage, endPage, totalDays, activeDaysList, startDateObj) {
    const totalPagesToCover = Math.max(endPage - startPage + 1, 1);

    // Count active (non-rest) days first
    let activeDaysCount = 0;
    for (let i = 0; i < totalDays; i++) {
      const dow = (startDateObj.getDay() + 1 + i) % 7; // align with WEEK_DAYS (starts Saturday)
      if (isDayActive(WEEK_DAYS[dow], activeDaysList)) activeDaysCount++;
    }
    activeDaysCount = Math.max(activeDaysCount, 1);

    const days = [];
    let assignedSoFar = 0;
    let activeSeen = 0;

    for (let i = 0; i < totalDays; i++) {
      const date = addDays(startDateObj, i);
      const dow = (startDateObj.getDay() + 1 + i) % 7;
      const isRest = !isDayActive(WEEK_DAYS[dow], activeDaysList);

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

  // Like buildDailyAssignments but spreads the pages across one or more page SEGMENTS instead of a
  // single contiguous range — used for memorization when the user has memorized pages in more than
  // one place (e.g. 1-77 and 500-604) and the remaining gap(s) need to be filled in. direction
  // "reverse" walks the segments from the last one backward (starting "from Surat An-Nas"); the
  // default walks them forward. Each day's pages always stay inside a single segment: once a
  // segment is exhausted the plan moves on to the next one instead of jumping across a gap.
  function buildSegmentedDailyAssignments(segments, totalDays, activeDaysList, startDateObj, direction) {
    const isReverse = direction === "reverse";
    const orderedSegments = isReverse ? segments.slice().reverse() : segments;
    const totalPagesToCover = orderedSegments.reduce((s, r) => s + (r.to - r.from + 1), 0) || 1;

    let activeDaysCount = 0;
    for (let i = 0; i < totalDays; i++) {
      const dow = (startDateObj.getDay() + 1 + i) % 7;
      if (isDayActive(WEEK_DAYS[dow], activeDaysList)) activeDaysCount++;
    }
    activeDaysCount = Math.max(activeDaysCount, 1);

    const days = [];
    let assignedSoFar = 0;
    let activeSeen = 0;
    let segIdx = 0;
    let cursor = orderedSegments.length ? (isReverse ? orderedSegments[0].to : orderedSegments[0].from) : 1;

    for (let i = 0; i < totalDays; i++) {
      const date = addDays(startDateObj, i);
      const dow = (startDateObj.getDay() + 1 + i) % 7;
      const isRest = !isDayActive(WEEK_DAYS[dow], activeDaysList);
      if (isRest) { days.push({ date, isRest: true }); continue; }

      if (assignedSoFar >= totalPagesToCover || segIdx >= orderedSegments.length) {
        days.push({ date, isRest: false, fromPage: null, toPage: null, isFilled: true });
        activeSeen++;
        continue;
      }

      const daysRemainingActive = activeDaysCount - activeSeen;
      const pagesRemaining = totalPagesToCover - assignedSoFar;
      const quota = Math.max(Math.round(pagesRemaining / Math.max(daysRemainingActive, 1)), 1);

      const seg = orderedSegments[segIdx];
      let fromP, toP, take;
      if (isReverse) {
        const segRemaining = cursor - seg.from + 1;
        take = Math.max(Math.min(quota, segRemaining), 1);
        toP = cursor;
        fromP = cursor - take + 1;
        cursor = fromP - 1;
        if (cursor < seg.from) { segIdx++; if (orderedSegments[segIdx]) cursor = orderedSegments[segIdx].to; }
      } else {
        const segRemaining = seg.to - cursor + 1;
        take = Math.max(Math.min(quota, segRemaining), 1);
        fromP = cursor;
        toP = cursor + take - 1;
        cursor = toP + 1;
        if (cursor > seg.to) { segIdx++; if (orderedSegments[segIdx]) cursor = orderedSegments[segIdx].from; }
      }

      assignedSoFar += take;
      days.push({ date, isRest: false, fromPage: fromP, toPage: toP, isFilled: false });
      activeSeen++;
    }
    return days;
  }

  // "المراجعة العكسية" (reverse review): the daily quota is fixed by the user (pagesPerDay) instead of
  // being derived from a duration, and pages are assigned in descending order — starting from the TOP
  // of the range (endPage, the most recently memorized pages) and working backward day by day until
  // startPage is reached. The plan's length (in calendar days) falls out of the page count, so there is
  // no separate "totalDays" input: the loop simply stops once every page has been covered.
  function buildReverseDailyAssignments(startPage, endPage, pagesPerDay, activeDaysList, startDateObj) {
    const totalPagesToCover = Math.max(endPage - startPage + 1, 1);
    const perDay = Math.max(Math.round(Number(pagesPerDay) || 1), 1);
    const neededActiveDays = Math.max(Math.ceil(totalPagesToCover / perDay), 1);

    const days = [];
    let remainingTop = endPage; // highest page not yet assigned
    let activeSeen = 0;
    let i = 0;
    // Safety cap in case activeDaysList somehow matches no day of the week (isDayActive always false).
    const maxIterations = neededActiveDays * 14 + 400;

    while (activeSeen < neededActiveDays && i < maxIterations) {
      const date = addDays(startDateObj, i);
      const dow = (startDateObj.getDay() + 1 + i) % 7; // align with WEEK_DAYS (starts Saturday)
      const isRest = !isDayActive(WEEK_DAYS[dow], activeDaysList);

      if (isRest) {
        days.push({ date, isRest: true });
        i++;
        continue;
      }

      const toP = remainingTop;
      const fromP = Math.max(toP - perDay + 1, startPage);
      days.push({ date, isRest: false, fromPage: fromP, toPage: toP, isFilled: false });

      remainingTop = fromP - 1;
      activeSeen++;
      i++;
    }
    return days;
  }

  // "المراجعة العكسية الدورية" (repeating reverse review): repeats a single reverse pass
  // (buildReverseDailyAssignments) back-to-back — each pass restarts from the top of the range
  // (endPage) — until totalDays (calendar days) is covered. Mirrors buildCyclicAssignments, but
  // for the reverse/tanazuli direction.
  function buildReverseCyclicAssignments(fromPage, toPage, pagesPerDay, totalDays, activeDaysList, startDateObj) {
    const days = [];
    let offset = 0;
    while (offset < totalDays) {
      const chunk = buildReverseDailyAssignments(fromPage, toPage, pagesPerDay, activeDaysList, addDays(startDateObj, offset));
      if (!chunk.length) break;
      for (let i = 0; i < chunk.length && offset < totalDays; i++, offset++) {
        days.push(chunk[i]);
      }
    }
    return days;
  }

  // Repeats a single review cycle (start -> end, ختم واحد) back-to-back until totalDays is covered.
  // Each cycle restarts the page range from the beginning, exactly like a recurring "ختم" of the same portion.
  function buildCyclicAssignments(fromPage, toPage, cycleDays, totalDays, activeDaysList, startDateObj) {
    const days = [];
    let offset = 0;
    while (offset < totalDays) {
      const chunkLen = Math.min(cycleDays, totalDays - offset);
      const chunkStart = addDays(startDateObj, offset);
      const chunkDays = buildDailyAssignments(fromPage, toPage, chunkLen, activeDaysList, chunkStart);
      days.push(...chunkDays);
      offset += chunkLen;
    }
    return days;
  }

  // Computes the memorization plan's own day-by-day assignments (independent of which tab is
  // active) so the "زيادة المراجعة تلقائياً" feature can look up how many pages were memorized
  // during any given stretch of days, regardless of whether the user is on the review tab or the
  // combined tab.
  function getMemoDaysForGrowth() {
    const m = state.memo;
    const totalDays = getMemoProgramDays(m);
    return buildSegmentedDailyAssignments(getRemainingSegments(m), totalDays, getEffectiveActiveDays(m), getPlanStartDate(), m.direction);
  }

  // Sums how many pages the memorization plan (memoDays) has newly memorized strictly before
  // calendar-day index `beforeIndex` (0-based, relative to the plan's start date). Rest days and
  // "already fully memorized" filler days contribute nothing. (Kept for stats that just need a count.)
  function sumMemoPagesBefore(memoDays, beforeIndex) {
    let total = 0;
    const limit = Math.min(beforeIndex, memoDays.length);
    for (let i = 0; i < limit; i++) {
      const d = memoDays[i];
      if (d && !d.isRest && !d.isFilled && d.fromPage != null && d.toPage != null) {
        total += d.toPage - d.fromPage + 1;
      }
    }
    return total;
  }

  // Returns the actual page range (min..max page number) the memorization plan (memoDays) has
  // covered strictly before calendar-day index `beforeIndex`. Unlike a simple page COUNT, this
  // captures exactly where the newly memorized pages sit in the book — essential for "reverse"
  // memorization (from the end backward) or when the memorized pages land nowhere near the
  // review range's own upper bound. Returns null if nothing has been memorized yet.
  function getMemoRangeMemorizedBefore(memoDays, beforeIndex) {
    let minP = null, maxP = null;
    const limit = Math.min(beforeIndex, memoDays.length);
    for (let i = 0; i < limit; i++) {
      const d = memoDays[i];
      if (d && !d.isRest && !d.isFilled && d.fromPage != null && d.toPage != null) {
        if (minP === null || d.fromPage < minP) minP = d.fromPage;
        if (maxP === null || d.toPage > maxP) maxP = d.toPage;
      }
    }
    return minP === null ? null : { from: minP, to: maxP };
  }

  // Merges a list of {from,to} page segments, combining any that touch or overlap into one
  // contiguous segment. Segments that stay far apart (e.g. review range 500-604 plus a newly
  // memorized range 20-60) are correctly kept as separate blocks rather than being force-joined.
  function mergeReviewSegments(segs) {
    const sorted = segs.slice().sort((a, b) => a.from - b.from);
    const merged = [];
    for (const s of sorted) {
      const last = merged[merged.length - 1];
      if (last && s.from <= last.to + 1) {
        last.to = Math.max(last.to, s.to);
      } else {
        merged.push({ from: s.from, to: s.to });
      }
    }
    return merged;
  }

  // "المراجعة المتزايدة" (growing/incremental review): at the start of every new cycle, the review
  // scope grows to also include the ACTUAL pages the memorization plan (memoDays) newly memorized
  // during all previous cycles — wherever those pages fall in the book, and regardless of
  // memorization direction. A newly memorized block that sits right next to the existing scope
  // simply extends it (from either side); a block memorized somewhere unrelated is added as its
  // own separate segment so it still gets reviewed. Growth stops naturally once the memorization
  // plan itself is finished. Each cycle's daily quota is recalculated from scratch so the full
  // (possibly larger, possibly multi-segment) scope still gets covered within that cycle.
  function buildGrowingCyclicAssignments(initialFrom, initialTo, cycleDays, totalDays, activeDaysList, startDateObj, memoDays) {
    const days = [];
    let offset = 0;
    let segments = [{ from: initialFrom, to: initialTo }];
    while (offset < totalDays) {
      const chunkLen = Math.min(cycleDays, totalDays - offset);
      const chunkStart = addDays(startDateObj, offset);
      const newRange = getMemoRangeMemorizedBefore(memoDays, offset);
      if (newRange) segments = mergeReviewSegments([...segments, newRange]);
      const chunkDays = buildSegmentedDailyAssignments(segments, chunkLen, activeDaysList, chunkStart, "forward");
      days.push(...chunkDays);
      offset += chunkLen;
    }
    return days;
  }

  // The final set of page segments the growing review range will cover once the memorization
  // plan finishes (used for display text) — e.g. [{from:20,to:604}] if everything merged into one
  // block, or multiple entries if some newly memorized pages ended up unrelated to the original range.
  function getGrowingReviewFinalSegments(initialFrom, initialTo, memoDays) {
    let segments = [{ from: initialFrom, to: initialTo }];
    const finalRange = getMemoRangeMemorizedBefore(memoDays, memoDays.length);
    if (finalRange) segments = mergeReviewSegments([...segments, finalRange]);
    return segments;
  }

  // Total number of distinct pages covered by the final growing-review segments.
  function getGrowingReviewFinalPageCount(initialFrom, initialTo, memoDays) {
    return getGrowingReviewFinalSegments(initialFrom, initialTo, memoDays)
      .reduce((sum, s) => sum + (s.to - s.from + 1), 0);
  }

  // Human-readable "من X إلى Y" / "من X إلى Y و من A إلى B" description of a segment list.
  function describeReviewSegments(segments) {
    return segments.map((s) => (s.from === s.to ? `${s.from}` : `من ${s.from} إلى ${s.to}`)).join("، و ");
  }

  // Central place resolving the review tab's page range into an actual day-by-day schedule,
  // honoring all combinations of "مرة واحدة"/"تكرار دوري"/"عكسية" — including reverse review
  // combined with periodic repeat (r.reverseMode && r.reverseRepeat), which repeats the same
  // reverse pass back-to-back like the forward cyclic mode does.
  function resolveReviewSchedule(r, activeDaysList, startDateObj) {
    const range = computeRange(r);
    if (r.cyclicMode) {
      const cycleDays = computeCycleDays(r);
      const programDays = getProgramDays(r);
      const numCycles = Math.max(Math.round(programDays / cycleDays), 1);
      if (r.growWithMemo) {
        const memoDays = getMemoDaysForGrowth();
        const days = buildGrowingCyclicAssignments(range.from, range.to, cycleDays, programDays, activeDaysList, startDateObj, memoDays);
        const finalSegments = getGrowingReviewFinalSegments(range.from, range.to, memoDays);
        const finalDesc = describeReviewSegments(finalSegments);
        const finalPageCount = getGrowingReviewFinalPageCount(range.from, range.to, memoDays);
        return { kind: "growing", days, range, cycleDays, programDays, numCycles, finalDesc, finalPageCount };
      }
      const days = buildCyclicAssignments(range.from, range.to, cycleDays, programDays, activeDaysList, startDateObj);
      return { kind: "cyclic", days, range, cycleDays, programDays, numCycles };
    }
    if (r.reverseMode) {
      const perDay = Math.max(Math.round(Number(r.reversePagesPerDay) || 1), 1);
      if (r.reverseRepeat) {
        const programDays = getProgramDays(r);
        const days = buildReverseCyclicAssignments(range.from, range.to, perDay, programDays, activeDaysList, startDateObj);
        return { kind: "reverse-repeat", days, range, perDay, programDays };
      }
      const days = buildReverseDailyAssignments(range.from, range.to, perDay, activeDaysList, startDateObj);
      return { kind: "reverse", days, range, perDay };
    }
    const totalDays = computeTotalDays(r);
    const days = buildDailyAssignments(range.from, range.to, totalDays, activeDaysList, startDateObj);
    return { kind: "once", days, range, totalDays };
  }

  // Figures out the current plan's daily assignments based on the active tab
  function getActivePlanAssignments() {
    const today = getPlanStartDate();
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
      const days = buildSegmentedDailyAssignments(getRemainingSegments(m), totalDays, getEffectiveActiveDays(m), today, m.direction);
      const isReverse = m.direction === "reverse";
      return {
        days,
        title: isReverse ? "خطة الحفظ المعكوس" : "خطة الحفظ",
        subtitle: hasPreMem
          ? `${totalDays} يوماً لختم حفظ باقي القرآن الكريم (${isReverse ? `معكوساً حتى الصفحة ${startPage}` : `من الصفحة ${startPage}`}) بإذن الله`
          : `${totalDays} يوماً لختم حفظ القرآن الكريم ${isReverse ? "معكوساً من سورة الناس" : ""} بإذن الله`,
      };
    } else {
      const r = state.review;
      const sched = resolveReviewSchedule(r, getEffectiveActiveDays(r), today);
      const range = sched.range;
      if (sched.kind === "growing") {
        const endText = r.endMode === "date"
          ? `حتى ${formatDualDate(addDays(today, sched.programDays))}`
          : r.endMode === "withMemo"
          ? `حتى انتهاء خطة الحفظ (${formatDualDate(addDays(today, sched.programDays))})`
          : `${sched.numCycles} دورة تقريباً`;
        return {
          days: sched.days,
          title: "جدول المراجعة المتزايدة",
          subtitle: `مراجعة تبدأ من الصفحات ${range.from} إلى ${range.to} كل ${sched.cycleDays} يوماً، ويضاف إليها ما يُحفظ جديداً في كل دورة (حسب مكانه الفعلي من القرآن)، حتى يشمل النطاق النهائي: ${sched.finalDesc} (${sched.finalPageCount} صفحة) — ${endText}`,
        };
      }
      if (sched.kind === "cyclic") {
        const endText = r.endMode === "date"
          ? `حتى ${formatDualDate(addDays(today, sched.programDays))}`
          : r.endMode === "withMemo"
          ? `حتى انتهاء خطة الحفظ (${formatDualDate(addDays(today, sched.programDays))})`
          : `${sched.numCycles} دورة تقريباً`;
        return {
          days: sched.days,
          title: "جدول المراجعة الدوري",
          subtitle: `تكرار ختم الصفحات من ${range.from} إلى ${range.to} كل ${sched.cycleDays} يوماً — ${endText}`,
        };
      }
      if (sched.kind === "reverse-repeat") {
        const endText = r.endMode === "date"
          ? `حتى ${formatDualDate(addDays(today, sched.programDays))}`
          : r.endMode === "withMemo"
          ? `حتى انتهاء خطة الحفظ (${formatDualDate(addDays(today, sched.programDays))})`
          : `على مدار البرنامج`;
        return {
          days: sched.days,
          title: "جدول المراجعة العكسية الدوري",
          subtitle: `تكرار مراجعة تنازلية من الصفحة ${range.to} إلى الصفحة ${range.from} بمعدل ${sched.perDay} صفحة يومياً — ${endText}`,
        };
      }
      if (sched.kind === "reverse") {
        return {
          days: sched.days,
          title: "جدول المراجعة العكسية",
          subtitle: `مراجعة تنازلية من الصفحة ${range.to} إلى الصفحة ${range.from} بمعدل ${sched.perDay} صفحة يومياً`,
        };
      }
      return { days: sched.days, title: "جدول المراجعة", subtitle: `مراجعة الصفحات من ${range.from} إلى ${range.to} خلال ${sched.totalDays} يوماً` };
    }
  }

  // Combines the memorization plan and the review schedule into a single day-by-day list
  function getCombinedPlanAssignments() {
    const today = getPlanStartDate();

    const m = state.memo;
    let memoTotalDays = (m.mode === "duration") ? computeDuration(m).totalDays : computePace(m).totalDays;
    memoTotalDays = Math.max(Math.round(memoTotalDays), 1);
    const memoStartPage = getRemainingStartPage(m);
    const memoDays = buildSegmentedDailyAssignments(getRemainingSegments(m), memoTotalDays, getEffectiveActiveDays(m), today, m.direction);

    const r = state.review;
    const sched = resolveReviewSchedule(r, getEffectiveActiveDays(r), today);
    const range = sched.range;
    let reviewSubtitle;
    if (sched.kind === "growing") {
      const endText = r.endMode === "date"
        ? `حتى ${formatDualDate(addDays(today, sched.programDays))}`
        : r.endMode === "withMemo"
        ? `تتوقف مع انتهاء خطة الحفظ بتاريخ ${formatDualDate(addDays(today, sched.programDays))}`
        : `${sched.numCycles} دورة تقريباً`;
      reviewSubtitle = `مع مراجعة متزايدة تبدأ من الصفحات ${range.from} إلى ${range.to} وتضيف كل ${sched.cycleDays} يوماً ما تم حفظه حديثاً (حسب مكانه الفعلي من القرآن)، حتى يشمل النطاق النهائي: ${sched.finalDesc} (${sched.finalPageCount} صفحة) (${endText})`;
    } else if (sched.kind === "cyclic") {
      const endText = r.endMode === "date"
        ? `حتى ${formatDualDate(addDays(today, sched.programDays))}`
        : r.endMode === "withMemo"
        ? `تتوقف مع انتهاء خطة الحفظ بتاريخ ${formatDualDate(addDays(today, sched.programDays))}`
        : `${sched.numCycles} دورة تقريباً`;
      reviewSubtitle = `مع تكرار ختم مراجعة الصفحات من ${range.from} إلى ${range.to} كل ${sched.cycleDays} يوماً (${endText})`;
    } else if (sched.kind === "reverse-repeat") {
      const endText = r.endMode === "date"
        ? `حتى ${formatDualDate(addDays(today, sched.programDays))}`
        : r.endMode === "withMemo"
        ? `تتوقف مع انتهاء خطة الحفظ بتاريخ ${formatDualDate(addDays(today, sched.programDays))}`
        : `على مدار البرنامج`;
      reviewSubtitle = `ومع تكرار مراجعة عكسية تنازلية من الصفحة ${range.to} إلى الصفحة ${range.from} بمعدل ${sched.perDay} صفحة يومياً (${endText})`;
    } else if (sched.kind === "reverse") {
      reviewSubtitle = `ومراجعة عكسية تنازلية من الصفحة ${range.to} إلى الصفحة ${range.from} بمعدل ${sched.perDay} صفحة يومياً`;
    } else {
      reviewSubtitle = `ومراجعة الصفحات من ${range.from} إلى ${range.to}`;
    }
    const reviewDays = sched.days;

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
      subtitle: `${getPreMemorizedCount(m) > 0 ? `حفظ باقي القرآن ${m.direction === "reverse" ? "معكوساً من سورة الناس" : `من الصفحة ${memoStartPage}`}` : (m.direction === "reverse" ? "حفظ القرآن كاملاً معكوساً من سورة الناس" : "حفظ القرآن كاملاً")}، ${reviewSubtitle}`,
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

  // يبني نص الشهر الهجري المقابل بالاعتماد على أول وآخر يوم في هذا الشهر الميلادي —
  // إن اختلف الشهر الهجري بينهما (وهو الغالب) تُعرض الفترة كاملة مثل "شعبان - رمضان 1447هـ".
  function buildHijriMonthLabel(year, month, daysInMonth) {
    const firstH = jdnToHijri(gregorianToJDN(year, month + 1, 1));
    const lastH = jdnToHijri(gregorianToJDN(year, month + 1, daysInMonth));
    if (firstH.month === lastH.month && firstH.year === lastH.year) {
      return `${HIJRI_MONTHS[firstH.month - 1]} ${firstH.year}هـ`;
    }
    if (firstH.year === lastH.year) {
      return `${HIJRI_MONTHS[firstH.month - 1]} - ${HIJRI_MONTHS[lastH.month - 1]} ${lastH.year}هـ`;
    }
    return `${HIJRI_MONTHS[firstH.month - 1]} ${firstH.year}هـ - ${HIJRI_MONTHS[lastH.month - 1]} ${lastH.year}هـ`;
  }

  function buildMonthPageHTML(monthGroup, planTitle, planSubtitle, studentName) {
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
    // Pad out to exactly 6 full weeks (42 cells) so the grid always matches the
    // fixed CSS row template and never leaves blank space at the page bottom.
    let totalCells = firstDow + daysInMonth;
    while (totalCells < 42) { cells += `<div class="cal-cell cal-empty"></div>`; totalCells++; }

    const dowHeader = WEEK_DAYS.map((d) => `<div class="cal-dow">${d}</div>`).join("");

    return `
      <div class="cal-page">
        <div class="cal-page-header">
          <div>
            <p class="cal-plan-title">${planTitle}</p>
            ${studentName ? `<p class="cal-plan-student">الطالب/ـة: ${studentName}</p>` : ""}
            <p class="cal-plan-sub">${planSubtitle}</p>
          </div>
          <div class="cal-month-badge">${ARABIC_MONTHS[month]} ${year}<span class="cal-month-badge-hijri">${buildHijriMonthLabel(year, month, daysInMonth)}</span></div>
        </div>
        <div class="cal-grid">${dowHeader}${cells}</div>
        <p class="cal-page-footer">﷽ — خطة القرآن الكريم${studentName ? ` — ${studentName}` : ""}</p>
      </div>
    `;
  }

  function buildCombinedMonthPageHTML(monthGroup, planTitle, planSubtitle, studentName) {
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
      let memoIsRest = false;
      if (!memoDay) {
        memoLabel = "✓ تمّ الختم";
      } else if (memoDay.isRest) {
        memoLabel = "راحة حفظ";
        memoIsRest = true;
      } else if (memoDay.isFilled || memoDay.fromPage == null) {
        memoLabel = "✓ تمّ الختم";
      } else {
        memoLabel = memoDay.fromPage === memoDay.toPage
          ? `حفظ: ص${memoDay.fromPage}`
          : `حفظ: ${memoDay.fromPage}-${memoDay.toPage}`;
      }

      const reviewDay = a.review;
      let reviewLabel;
      let reviewIsRest = false;
      if (!reviewDay) {
        reviewLabel = "✓ اكتملت المراجعة";
      } else if (reviewDay.isRest) {
        reviewLabel = "راحة مراجعة";
        reviewIsRest = true;
      } else if (reviewDay.isFilled || reviewDay.fromPage == null) {
        reviewLabel = "✓ اكتملت المراجعة";
      } else {
        reviewLabel = reviewDay.fromPage === reviewDay.toPage
          ? `مراجعة: ص${reviewDay.fromPage}`
          : `مراجعة: ${reviewDay.fromPage}-${reviewDay.toPage}`;
      }

      const isRest = memoIsRest && reviewIsRest;
      cells += `<div class="cal-cell cal-cell-combined${isRest ? " cal-rest" : ""}">
        <span class="cal-date-num">${dnum}</span>
        <div class="cal-task-group">
          <span class="cal-task-mini memo${memoIsRest ? " is-rest" : ""}">${memoLabel}</span>
          <span class="cal-task-mini review${reviewIsRest ? " is-rest" : ""}">${reviewLabel}</span>
        </div>
      </div>`;
    }
    // Pad out to exactly 6 full weeks (42 cells) so the grid always matches the
    // fixed CSS row template and never leaves blank space at the page bottom.
    let totalCellsC = firstDow + daysInMonth;
    while (totalCellsC < 42) { cells += `<div class="cal-cell cal-empty"></div>`; totalCellsC++; }

    const dowHeader = WEEK_DAYS.map((d) => `<div class="cal-dow">${d}</div>`).join("");

    return `
      <div class="cal-page">
        <div class="cal-page-header">
          <div>
            <p class="cal-plan-title">${planTitle}</p>
            ${studentName ? `<p class="cal-plan-student">الطالب/ـة: ${studentName}</p>` : ""}
            <p class="cal-plan-sub">${planSubtitle}</p>
          </div>
          <div class="cal-month-badge">${ARABIC_MONTHS[month]} ${year}<span class="cal-month-badge-hijri">${buildHijriMonthLabel(year, month, daysInMonth)}</span></div>
        </div>
        <div class="cal-grid">${dowHeader}${cells}</div>
        <p class="cal-page-footer">﷽ — الخطة الشاملة لحفظ ومراجعة القرآن${studentName ? ` — ${studentName}` : ""}</p>
      </div>
    `;
  }

  /* ---------------- PDF export ---------------- */
  // Waits for the browser to actually paint the freshly-injected calendar markup
  // (fonts loaded + at least two animation frames) before html2canvas reads it.
  async function waitForPaint(node) {
    if (document.fonts && document.fonts.ready) {
      try { await document.fonts.ready; } catch (e) { /* ignore */ }
    }
    node.offsetHeight; // force a synchronous reflow
    await new Promise((res) => requestAnimationFrame(() => requestAnimationFrame(res)));
  }

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

      // Read the CURRENT state fresh, at the exact moment of export, so any edit the
      // user just made is always reflected — never a stale, previously-built plan.
      const isCombined = state.tab === "combined";
      const plan = isCombined ? getCombinedPlanAssignments() : getActivePlanAssignments();
      const monthRenderer = isCombined ? buildCombinedMonthPageHTML : buildMonthPageHTML;
      const months = groupByMonth(plan.days);
      if (months.length === 0) throw new Error("لا توجد بيانات كافية لبناء التقويم");

      // Lower the render scale a bit for long plans to keep memory use in check.
      const scale = months.length > 18 ? 1.25 : months.length > 8 ? 1.5 : 2;

      const { jsPDF } = window.jspdf;
      const pdf = new jsPDF({ orientation: "landscape", unit: "pt", format: "a4" });
      const pageWidth = pdf.internal.pageSize.getWidth();
      const pageHeight = pdf.internal.pageSize.getHeight();

      for (let i = 0; i < months.length; i++) {
        showNotice(`جارٍ تجهيز شهر ${i + 1} من ${months.length}...`);
        calRoot.innerHTML = monthRenderer(months[i], plan.title, plan.subtitle, state.studentName.trim());

        const pageNode = calRoot.querySelector(".cal-page");
        await waitForPaint(pageNode);

        let canvas = await window.html2canvas(pageNode, {
          scale,
          backgroundColor: "#fffdfa",
          useCORS: true,
        });

        const imgData = canvas.toDataURL("image/png");

        // Stretch the page image to cover the PDF page edge-to-edge (full bleed),
        // since .cal-page is authored at the same aspect ratio as A4 landscape —
        // this guarantees no blank strips or leftover empty margins on any page.
        if (i > 0) pdf.addPage();
        pdf.addImage(imgData, "PNG", 0, 0, pageWidth, pageHeight);

        // Release this month's canvas/DOM immediately instead of waiting until the
        // very end — keeps memory use flat regardless of how many months there are.
        canvas.width = 0;
        canvas.height = 0;
        canvas = null;
        calRoot.innerHTML = "";
      }

      const nameSuffix = state.studentName.trim() ? `-${state.studentName.trim()}` : "";
      pdf.save((isCombined ? "تقويم-الخطة-الشاملة" : "تقويم-خطة-القرآن") + nameSuffix + ".pdf");
      showNotice("تم إنشاء تقويم PDF بنجاح ✓", 2500);
    } catch (err) {
      calRoot.innerHTML = "";
      showNotice("تعذّر إنشاء ملف PDF، حاول مرة أخرى", 2500);
    } finally {
      btn.disabled = false;
      btn.textContent = originalText;
    }
  });

  /* ---------------- تثبيت الخطة كتطبيق (PWA) ---------------- */
  (function setupInstallApp() {
    const installBtn = document.getElementById("btn-install-app");
    if (!installBtn) return;

    const isStandaloneAlready =
      window.matchMedia("(display-mode: standalone)").matches ||
      window.navigator.standalone === true; // iOS Safari flag

    if (isStandaloneAlready) return; // already running as an installed app — nothing to offer

    const isIOS = /iphone|ipad|ipod/i.test(window.navigator.userAgent);
    let deferredPrompt = null;

    // Chrome/Edge/Android: fires only when the page meets install criteria
    // (served over HTTPS with a valid manifest + registered service worker).
    window.addEventListener("beforeinstallprompt", (e) => {
      e.preventDefault();
      deferredPrompt = e;
      installBtn.style.display = "inline-block";
    });

    window.addEventListener("appinstalled", () => {
      installBtn.style.display = "none";
      deferredPrompt = null;
    });

    // iOS Safari never fires beforeinstallprompt — show the button with manual steps instead.
    if (isIOS) {
      installBtn.style.display = "inline-block";
    }

    installBtn.addEventListener("click", async () => {
      if (deferredPrompt) {
        installBtn.disabled = true;
        deferredPrompt.prompt();
        try { await deferredPrompt.userChoice; } catch (e) {}
        deferredPrompt = null;
        installBtn.disabled = false;
        installBtn.style.display = "none";
        return;
      }
      if (isIOS) {
        showNotice("لتثبيت التطبيق: اضغط زر المشاركة ⬆️ في متصفح Safari، ثم اختر «إضافة إلى الشاشة الرئيسية»", 6000);
      } else {
        showNotice("لتثبيت التطبيق: افتح قائمة المتصفح (⋮) واختر «تثبيت التطبيق» أو «إضافة إلى الشاشة الرئيسية»", 6000);
      }
    });

    // Best-effort service worker registration (needed on Android/Chrome for the native install
    // prompt to appear). Skipped automatically on file:// pages and older browsers, since service
    // workers require the page to be hosted over HTTPS (or localhost) to work at all.
    if ("serviceWorker" in navigator && (location.protocol === "https:" || location.hostname === "localhost")) {
      const swCode = `
        const CACHE_NAME = "quran-plan-v1";
        self.addEventListener("install", (e) => { self.skipWaiting(); });
        self.addEventListener("activate", (e) => { self.clients.claim(); });
        self.addEventListener("fetch", (e) => {
          e.respondWith(
            caches.open(CACHE_NAME).then((cache) =>
              fetch(e.request).then((res) => { cache.put(e.request, res.clone()); return res; })
                .catch(() => cache.match(e.request))
            )
          );
        });
      `;
      try {
        const swUrl = URL.createObjectURL(new Blob([swCode], { type: "text/javascript" }));
        navigator.serviceWorker.register(swUrl).catch(() => {});
      } catch (e) {}
    }
  })();
})();
</script>
</body>
</html>
