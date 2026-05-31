<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tour de V2 Final Rankings | The Pad Santa Barbara</title>
  <style>
    :root {
      --pad-orange: #005CB9;
      --pad-orange-hot: #2f7fd2;
      --pad-black: #000000;
      --pad-dark: #323e48;
      --pad-gray: #7b868c;
      --pad-soft: #f5f1ea;
      --pad-white: #ffffff;
      --pad-ink: #161616;
      --pad-shadow: 0 24px 70px rgba(0, 0, 0, 0.18);
      --radius-xl: 28px;
      --radius-lg: 20px;
      --radius-md: 14px;
    }

    * { box-sizing: border-box; }

    html { scroll-behavior: smooth; }

    body {
      margin: 0;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background:
        radial-gradient(circle at 8% 8%, rgba(0, 92, 185, 0.28), transparent 28rem),
        radial-gradient(circle at 88% 12%, rgba(50, 62, 72, 0.22), transparent 24rem),
        linear-gradient(135deg, #f2f7ff 0%, #edf3fb 52%, #ffffff 100%);
      color: var(--pad-ink);
      min-height: 100vh;
    }

    a { color: inherit; }

    .site-shell {
      width: min(1180px, calc(100% - 32px));
      margin: 0 auto;
    }

    .topbar {
      position: sticky;
      top: 0;
      z-index: 10;
      backdrop-filter: blur(16px);
      background: rgba(255, 255, 255, 0.78);
      border-bottom: 1px solid rgba(50, 62, 72, 0.12);
    }

    .topbar-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 18px;
      padding: 14px 0;
    }

    .brand-lockup {
      display: flex;
      align-items: center;
      gap: 12px;
      font-weight: 900;
      letter-spacing: -0.04em;
      text-transform: uppercase;
    }

    .brand-mark {
      display: grid;
      place-items: center;
      width: 42px;
      height: 42px;
      border-radius: 50%;
      background: var(--pad-orange);
      color: var(--pad-black);
      box-shadow: 0 12px 30px rgba(0, 92, 185, 0.36);
      font-size: 0.78rem;
      font-weight: 1000;
      letter-spacing: -0.08em;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 10px;
      flex-wrap: wrap;
      justify-content: flex-end;
    }

    .nav-links a,
    .pill-button {
      border: 1px solid rgba(50, 62, 72, 0.18);
      border-radius: 999px;
      padding: 9px 13px;
      text-decoration: none;
      font-size: 0.88rem;
      font-weight: 800;
      background: rgba(255, 255, 255, 0.72);
      transition: transform 160ms ease, background 160ms ease, border-color 160ms ease;
    }

    .nav-links a:hover,
    .pill-button:hover {
      transform: translateY(-1px);
      background: var(--pad-white);
      border-color: var(--pad-orange);
    }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.12fr) minmax(320px, 0.88fr);
      gap: 30px;
      align-items: stretch;
      padding: 64px 0 34px;
    }

    .hero-card,
    .summary-card,
    .section-card {
      border: 1px solid rgba(50, 62, 72, 0.14);
      border-radius: var(--radius-xl);
      background: rgba(255, 255, 255, 0.88);
      box-shadow: var(--pad-shadow);
      overflow: hidden;
    }

    .hero-card {
      position: relative;
      min-height: 520px;
      padding: 44px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      inset: 0;
      background:
        linear-gradient(135deg, rgba(0, 92, 185, 0.25), transparent 45%),
        repeating-linear-gradient(135deg, rgba(50, 62, 72, 0.07) 0 2px, transparent 2px 18px);
      pointer-events: none;
    }

    .hero-content,
    .hero-bottom { position: relative; z-index: 1; }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      width: fit-content;
      border-radius: 999px;
      padding: 8px 12px;
      background: var(--pad-black);
      color: var(--pad-white);
      font-size: 0.78rem;
      font-weight: 900;
      letter-spacing: 0.08em;
      text-transform: uppercase;
    }

    .eyebrow::before {
      content: "";
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background: var(--pad-orange);
    }

    h1 {
      margin: 24px 0 12px;
      font-size: clamp(3.1rem, 8vw, 7.2rem);
      line-height: 0.82;
      letter-spacing: -0.09em;
      text-transform: uppercase;
    }

    .hero-copy {
      max-width: 760px;
      font-size: clamp(1.08rem, 2vw, 1.32rem);
      line-height: 1.45;
      color: rgba(22, 22, 22, 0.76);
      font-weight: 650;
    }

    .hero-bottom {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 22px;
      margin-top: 34px;
      flex-wrap: wrap;
    }

    .rule-card {
      max-width: 620px;
      padding: 18px;
      border-radius: var(--radius-lg);
      background: rgba(50, 62, 72, 0.92);
      color: var(--pad-white);
    }

    .rule-card strong { color: var(--pad-orange-hot); }

    .hero-badge {
      width: 170px;
      aspect-ratio: 1;
      border-radius: 50%;
      display: grid;
      place-items: center;
      text-align: center;
      background: var(--pad-orange);
      color: var(--pad-black);
      transform: rotate(-7deg);
      box-shadow: 0 16px 38px rgba(0, 92, 185, 0.42);
      font-weight: 1000;
      letter-spacing: -0.05em;
      text-transform: uppercase;
      line-height: 0.92;
      font-size: 1.35rem;
    }

    .summary-card {
      padding: 26px;
      display: flex;
      flex-direction: column;
      gap: 18px;
      background: linear-gradient(180deg, rgba(255, 255, 255, 0.92), rgba(255, 255, 255, 0.76));
    }

    .summary-card h2,
    .section-heading h2 {
      margin: 0;
      letter-spacing: -0.06em;
      line-height: 0.96;
      font-size: clamp(2rem, 4vw, 3.2rem);
      text-transform: uppercase;
    }

    .stat-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 12px;
    }

    .stat {
      padding: 17px;
      border-radius: var(--radius-lg);
      background: var(--pad-white);
      border: 1px solid rgba(50, 62, 72, 0.12);
    }

    .stat .num {
      display: block;
      font-size: 2.15rem;
      font-weight: 1000;
      line-height: 1;
      letter-spacing: -0.07em;
    }

    .stat .label {
      display: block;
      margin-top: 7px;
      color: rgba(22, 22, 22, 0.58);
      font-weight: 850;
      font-size: 0.82rem;
      text-transform: uppercase;
      letter-spacing: 0.04em;
    }

    .podium {
      display: grid;
      gap: 12px;
      margin-top: 2px;
    }

    .podium-row {
      display: grid;
      grid-template-columns: auto 1fr auto;
      align-items: center;
      gap: 12px;
      padding: 14px;
      border-radius: var(--radius-lg);
      background: var(--pad-dark);
      color: var(--pad-white);
    }

    .podium-row:first-child {
      background: var(--pad-black);
      outline: 3px solid var(--pad-orange);
    }

    .place-dot {
      display: grid;
      place-items: center;
      width: 38px;
      height: 38px;
      border-radius: 50%;
      background: var(--pad-orange);
      color: var(--pad-black);
      font-weight: 1000;
    }

    .podium-name {
      font-weight: 950;
      letter-spacing: -0.03em;
    }

    .podium-meta {
      color: rgba(255, 255, 255, 0.76);
      font-size: 0.86rem;
      font-weight: 750;
    }

    .podium-time {
      font-weight: 1000;
      font-variant-numeric: tabular-nums;
    }

    .controls {
      display: grid;
      grid-template-columns: 1fr auto;
      gap: 14px;
      align-items: center;
      margin: 22px 0;
    }

    .search-wrap {
      position: relative;
    }

    .search-wrap input {
      width: 100%;
      border: 1px solid rgba(50, 62, 72, 0.18);
      border-radius: 999px;
      padding: 15px 18px 15px 46px;
      font: inherit;
      font-weight: 750;
      background: rgba(255, 255, 255, 0.82);
      outline: none;
    }

    .search-wrap span {
      position: absolute;
      left: 18px;
      top: 50%;
      transform: translateY(-50%);
      opacity: 0.52;
      font-weight: 1000;
    }

    .filter-buttons {
      display: flex;
      gap: 9px;
      flex-wrap: wrap;
      justify-content: flex-end;
    }

    button {
      cursor: pointer;
      border: 0;
      font: inherit;
    }

    .filter-button {
      border-radius: 999px;
      padding: 12px 16px;
      background: var(--pad-white);
      color: var(--pad-dark);
      border: 1px solid rgba(50, 62, 72, 0.18);
      font-size: 0.9rem;
      font-weight: 950;
      transition: transform 160ms ease, background 160ms ease, color 160ms ease;
    }

    .filter-button:hover { transform: translateY(-1px); }

    .filter-button.active {
      background: var(--pad-black);
      color: var(--pad-white);
      border-color: var(--pad-black);
    }

    main { padding: 16px 0 70px; }

    .section-card {
      margin-top: 24px;
      background: rgba(255, 255, 255, 0.9);
    }

    .section-heading {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 18px;
      padding: 28px 28px 20px;
      border-bottom: 1px solid rgba(50, 62, 72, 0.12);
    }

    .section-heading p {
      margin: 8px 0 0;
      color: rgba(22, 22, 22, 0.62);
      font-weight: 720;
    }

    .section-count {
      flex: 0 0 auto;
      padding: 10px 14px;
      border-radius: 999px;
      background: rgba(0, 92, 185, 0.16);
      color: #005CB9;
      font-weight: 950;
    }

    .table-wrap {
      overflow-x: auto;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      min-width: 820px;
    }

    th, td {
      padding: 14px 18px;
      text-align: left;
      border-bottom: 1px solid rgba(50, 62, 72, 0.10);
      vertical-align: middle;
    }

    th {
      position: static;
      background: rgba(255, 255, 255, 0.98);
      color: rgba(22, 22, 22, 0.58);
      font-size: 0.76rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      font-weight: 1000;
      box-shadow: inset 0 -1px 0 rgba(50, 62, 72, 0.10);
    }

    td {
      font-weight: 720;
    }

    tr:hover td { background: rgba(0, 92, 185, 0.06); }

    .rank-cell {
      width: 82px;
      font-weight: 1000;
      letter-spacing: -0.05em;
      font-size: 1.3rem;
    }

    .top-rank {
      display: inline-grid;
      place-items: center;
      min-width: 42px;
      height: 42px;
      border-radius: 50%;
      background: var(--pad-orange);
      color: var(--pad-black);
      box-shadow: 0 8px 20px rgba(0, 92, 185, 0.35);
    }

    .name-block strong {
      display: block;
      font-size: 1.02rem;
      letter-spacing: -0.02em;
    }

    .name-block span {
      display: block;
      color: rgba(22, 22, 22, 0.52);
      font-size: 0.86rem;
      margin-top: 2px;
      font-weight: 800;
    }

    .tag {
      display: inline-flex;
      align-items: center;
      width: fit-content;
      border-radius: 999px;
      padding: 6px 10px;
      font-size: 0.78rem;
      font-weight: 950;
      background: rgba(50, 62, 72, 0.09);
      color: var(--pad-dark);
      white-space: nowrap;
    }

    .tag.beginner { background: rgba(0, 92, 185, 0.16); color: #005CB9; }
    .tag.intermediate { background: rgba(50, 62, 72, 0.13); color: var(--pad-dark); }
    .tag.advanced { background: rgba(0, 0, 0, 0.9); color: var(--pad-white); }

    .time-cell,
    .climbs-cell {
      font-variant-numeric: tabular-nums;
      font-weight: 950;
    }

    .finish-status {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      border-radius: 999px;
      padding: 6px 10px;
      font-size: 0.76rem;
      font-weight: 950;
      white-space: nowrap;
    }

    .finish-status.done {
      background: rgba(0, 92, 185, 0.18);
      color: #8e4300;
    }

    .finish-status.open {
      background: rgba(123, 134, 140, 0.16);
      color: var(--pad-dark);
    }

    .fine-print {
      margin: 20px auto 0;
      color: rgba(22, 22, 22, 0.58);
      font-size: 0.92rem;
      line-height: 1.5;
      font-weight: 650;
      text-align: center;
      max-width: 760px;
    }

    .empty-state {
      padding: 32px;
      color: rgba(22, 22, 22, 0.62);
      font-weight: 800;
    }

    @media (max-width: 920px) {
      .hero {
        grid-template-columns: 1fr;
        padding-top: 34px;
      }

      .hero-card { min-height: 0; padding: 30px; }
      .controls { grid-template-columns: 1fr; }
      .filter-buttons { justify-content: flex-start; }
      .section-heading { align-items: flex-start; flex-direction: column; }
    }

    @media (max-width: 620px) {
      .site-shell { width: min(100% - 22px, 1180px); }
      .topbar-inner { align-items: flex-start; flex-direction: column; }
      .nav-links { justify-content: flex-start; }
      .hero-card { padding: 22px; border-radius: 22px; }
      .hero-badge { width: 132px; font-size: 1.08rem; }
      .stat-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>
  <header class="topbar">
    <div class="site-shell topbar-inner">
      <div class="brand-lockup" aria-label="The Pad Climbing">
        <div class="brand-mark">PAD</div>
        <div>The Pad · Santa Barbara</div>
      </div>
      <nav class="nav-links" aria-label="Ranking sections">
        <a href="#overall">Overall</a>
        <a href="#beginner">Beginner</a>
        <a href="#intermediate">Intermediate</a>
        <a href="#advanced">Advanced</a>
      </nav>
    </div>
  </header>

  <section class="site-shell hero" aria-labelledby="page-title">
    <div class="hero-card">
      <div class="hero-content">
        <div class="eyebrow">Final rankings · Santa Barbara</div>
        <h1 id="page-title">Tour de V2</h1>
        <p class="hero-copy">Thirty minutes. Thirty climbs. A whole lot of fun.</p>
      </div>
      <div class="hero-bottom">
        <div class="rule-card">
          <strong>How rankings work:</strong> fastest time wins among full 30-climb finishers. If someone did not complete all 30 climbs, they rank after finishers by climbs completed, then time.
        </div>
        <div class="hero-badge" aria-hidden="true">Final<br />Board</div>
      </div>
    </div>

    <aside class="summary-card" aria-label="Event summary">
      <div>
        <h2>Top of the heap</h2>
        <p class="hero-copy" style="font-size: 1rem; margin-bottom: 0;">Fastest complete scorecards across the whole Tour.</p>
      </div>
      <div class="stat-grid" id="statsGrid"></div>
      <div class="podium" id="podium"></div>
    </aside>
  </section>

  <main class="site-shell">
    <div class="controls" aria-label="Search and filter rankings">
      <label class="search-wrap">
        <span aria-hidden="true">⌕</span>
        <input id="searchInput" type="search" placeholder="Search name, bib, category…" autocomplete="off" />
      </label>
      <div class="filter-buttons" role="group" aria-label="Category filters">
        <button class="filter-button active" data-filter="all">All</button>
        <button class="filter-button" data-filter="Beginner">Beginner</button>
        <button class="filter-button" data-filter="Intermediate">Intermediate</button>
        <button class="filter-button" data-filter="Advanced">Advanced</button>
      </div>
    </div>

    <section class="section-card" id="overall" data-section="all">
      <div class="section-heading">
        <div>
          <h2>Overall ranking</h2>
          <p>Everybody on the same wall-shaped battlefield.</p>
        </div>
        <div class="section-count" id="overallCount"></div>
      </div>
      <div class="table-wrap" id="overallTable"></div>
    </section>

    <section class="section-card" id="beginner" data-section="Beginner">
      <div class="section-heading">
        <div>
          <h2>Beginner</h2>
          <p>V0–V3. Beginner is a category, not a personality.</p>
        </div>
        <div class="section-count" id="beginnerCount"></div>
      </div>
      <div class="table-wrap" id="beginnerTable"></div>
    </section>

    <section class="section-card" id="intermediate" data-section="Intermediate">
      <div class="section-heading">
        <div>
          <h2>Intermediate</h2>
          <p>V4–V6. Just enough confidence to make questionable choices.</p>
        </div>
        <div class="section-count" id="intermediateCount"></div>
      </div>
      <div class="table-wrap" id="intermediateTable"></div>
    </section>

    <section class="section-card" id="advanced" data-section="Advanced">
      <div class="section-heading">
        <div>
          <h2>Advanced</h2>
          <p>V7+. Fingers were harmed in the making of this leaderboard.</p>
        </div>
        <div class="section-count" id="advancedCount"></div>
      </div>
      <div class="table-wrap" id="advancedTable"></div>
    </section>

    <p class="fine-print">Timing note: fastest-time ranking is only applied to scorecards with all 30 climbs completed. Incomplete scorecards are ranked by climbs completed, then time.</p>
  </main>

  <script>
    const rawParticipants = [
      { bib: 41, name: "John Susko", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "8:49" },
      { bib: 37, name: "Luc Tousig", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "8:52" },
      { bib: 14, name: "Troy Kling", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "8:54" },
      { bib: 3, name: "Dylan Gray", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 30, time: "9:20" },
      { bib: 11, name: "Kyle Pobirs", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 30, time: "9:38" },
      { bib: 52, name: "Ryan Bowe", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "9:54" },
      { bib: 23, name: "Benjamin W", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 30, time: "10:32" },
      { bib: 10, name: "Paxton Atla", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "10:37" },
      { bib: 24, name: "Bennet Ma", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 30, time: "11:16" },
      { bib: 25, name: "Parker Cal", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "11:22" },
      { bib: 32, name: "Andrew Br", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "11:42" },
      { bib: 49, name: "Ramon Wa", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "11:52" },
      { bib: 9, name: "Caleb Atla", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "11:54" },
      { bib: 7, name: "Kenzo Buh", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 30, time: "11:58" },
      { bib: 21, name: "Avery Acki", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "12:31" },
      { bib: 2, name: "Dylan Hann", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "12:39" },
      { bib: 29, name: "Z Kling", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "12:58" },
      { bib: 33, name: "Ben Rara", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "13:21" },
      { bib: 36, name: "Rowan De", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "14:16" },
      { bib: 18, name: "Daniel Zam", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "14:19" },
      { bib: 6, name: "Samyak Ja", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "15:18" },
      { bib: 51, name: "Abigail Con", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "15:39" },
      { bib: 48, name: "Helix Mine", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 30, time: "15:41" },
      { bib: 50, name: "Lauren Wo", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "15:48" },
      { bib: 31, name: "Paige Shuk", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "16:02" },
      { bib: 44, name: "James Row", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "16:41" },
      { bib: 16, name: "Gabriela Q", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "16:51" },
      { bib: 27, name: "Alexander", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "17:27" },
      { bib: 60, name: "Cach Holb", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 30, time: "18:13" },
      { bib: 59, name: "Nina Steel", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "19:20" },
      { bib: 34, name: "Luke Obry", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "19:21" },
      { bib: 19, name: "Tom Quise", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "19:48" },
      { bib: 46, name: "Clay Miner", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "19:51" },
      { bib: 55, name: "Ryan Chav", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "19:57" },
      { bib: 58, name: "Euel Pamir", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "23:06" },
      { bib: 30, name: "Sawyer Fle", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "23:18" },
      { bib: 22, name: "Paloma Ca", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 30, time: "23:19" },
      { bib: 54, name: "Ethan Mirb", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "23:34" },
      { bib: 12, name: "Karen Sinc", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "23:44" },
      { bib: 8, name: "Logan McC", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "23:45" },
      { bib: 38, name: "Emily Caug", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "25:28:00" },
      { bib: 13, name: "Taylor Mar", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "26:59:00" },
      { bib: 47, name: "Journey Mi", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 30, time: "28:09:00" },
      { bib: 4, name: "Ellis Gonza", category: "Intermediate (V4–V6)", location: "Santa Barbara", routesCompleted: 30, time: "30:00:00" },
      { bib: 43, name: "Ethan Che", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 29, time: "28:16:00" },
      { bib: 28, name: "Lake Lust", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 28, time: "30:00:00" },
      { bib: 39, name: "Ethan God", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 27, time: "29:27:00" },
      { bib: 40, name: "Tyler Susko", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 27, time: "30:00:00" },
      { bib: 20, name: "Elizabeth N", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 25, time: "22:24" },
      { bib: 1, name: "Sofia Decr", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 25, time: "29:14:00" },
      { bib: 45, name: "Jocelyn Ka", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 22, time: "28:11:00" },
      { bib: 15, name: "Bridget Ge", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 22, time: "29:18:00" },
      { bib: 56, name: "Griffin Eas", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 19, time: "29:43:00" },
      { bib: 26, name: "Kate Taylo", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 14, time: "30:00:00" },
      { bib: 42, name: "Audrey Na", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 9, time: "28:19:00" },
      { bib: 5, name: "Amy Gonza", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 5, time: "30:00:00" },
      { bib: 17, name: "Alexandra", category: "Advanced (V7+)", location: "Santa Barbara", routesCompleted: 0, time: "30:00:00" },
      { bib: 35, name: "Kai McGee", category: "Beginner (V0–V3)", location: "Santa Barbara", routesCompleted: 0, time: "30:00:00" }
    ];

    const MAX_ROUTES = 30;

    const parseTimeToSeconds = (value) => {
      const parts = String(value).split(":").map(Number);
      if (parts.length === 2) return (parts[0] * 60) + parts[1];
      if (parts.length === 3 && parts[2] === 0) return (parts[0] * 60) + parts[1];
      if (parts.length === 3) return (parts[0] * 3600) + (parts[1] * 60) + parts[2];
      return Number.POSITIVE_INFINITY;
    };

    const formatSeconds = (seconds) => {
      const minutes = Math.floor(seconds / 60);
      const remainingSeconds = seconds % 60;
      return `${minutes}:${String(remainingSeconds).padStart(2, "0")}`;
    };

    const categoryKey = (category) => category.split(" ")[0];

    const participants = rawParticipants.map((participant) => ({
      ...participant,
      categoryKey: categoryKey(participant.category),
      seconds: parseTimeToSeconds(participant.time),
      completedAll: participant.routesCompleted === MAX_ROUTES
    }));

    const rankParticipants = (list) => [...list].sort((a, b) => {
      // Complete scorecards are eligible for fastest-time ranking.
      // Incomplete scorecards sit below finishers and are sorted by climbs completed.
      if (a.completedAll !== b.completedAll) return a.completedAll ? -1 : 1;
      if (a.completedAll && b.completedAll) return a.seconds - b.seconds || b.routesCompleted - a.routesCompleted || a.name.localeCompare(b.name);
      return b.routesCompleted - a.routesCompleted || a.seconds - b.seconds || a.name.localeCompare(b.name);
    });

    const getRankedRows = (list) => rankParticipants(list).map((participant, index) => ({
      ...participant,
      rank: index + 1
    }));

    const categoryClass = (key) => key.toLowerCase();

    const renderTable = (mountId, rows) => {
      const mount = document.getElementById(mountId);
      if (!rows.length) {
        mount.innerHTML = `<div class="empty-state">No climbers match that search. Tragic, but fixable.</div>`;
        return;
      }

      mount.innerHTML = `
        <table>
          <thead>
            <tr>
              <th>Rank</th>
              <th>Climber</th>
              <th>Category</th>
              <th>Climbs</th>
              <th>Time</th>
              <th>Status</th>
            </tr>
          </thead>
          <tbody>
            ${rows.map((row) => `
              <tr>
                <td class="rank-cell">${row.rank <= 3 ? `<span class="top-rank">${row.rank}</span>` : row.rank}</td>
                <td>
                  <div class="name-block">
                    <strong>${row.name}</strong>
                    <span>Bib ${row.bib} · ${row.location}</span>
                  </div>
                </td>
                <td><span class="tag ${categoryClass(row.categoryKey)}">${row.category}</span></td>
                <td class="climbs-cell">${row.routesCompleted}/${MAX_ROUTES}</td>
                <td class="time-cell">${formatSeconds(row.seconds)}</td>
                <td>
                  <span class="finish-status ${row.completedAll ? "done" : "open"}">
                    ${row.completedAll ? "✓ Timed finish" : "Climbs ranked"}
                  </span>
                </td>
              </tr>
            `).join("")}
          </tbody>
        </table>
      `;
    };

    const renderStats = () => {
      const finishers = participants.filter((participant) => participant.completedAll).length;
      const totalClimbs = participants.reduce((sum, participant) => sum + participant.routesCompleted, 0);
      const fastest = rankParticipants(participants).find((participant) => participant.completedAll);
      const beginnerWinner = rankParticipants(participants.filter((participant) => participant.categoryKey === "Beginner"))[0];

      document.getElementById("statsGrid").innerHTML = `
        <div class="stat"><span class="num">${participants.length}</span><span class="label">Participants</span></div>
        <div class="stat"><span class="num">${finishers}</span><span class="label">Finished all 30</span></div>
        <div class="stat"><span class="num">${totalClimbs}</span><span class="label">Total climbs</span></div>
        <div class="stat"><span class="num">${formatSeconds(fastest.seconds)}</span><span class="label">Fastest time</span></div>
      `;

      const podiumRows = rankParticipants(participants).filter((participant) => participant.completedAll).slice(0, 3);
      document.getElementById("podium").innerHTML = podiumRows.map((participant, index) => `
        <div class="podium-row">
          <div class="place-dot">${index + 1}</div>
          <div>
            <div class="podium-name">${participant.name}</div>
            <div class="podium-meta">${participant.category} · Bib ${participant.bib}</div>
          </div>
          <div class="podium-time">${formatSeconds(participant.seconds)}</div>
        </div>
      `).join("");
    };

    const renderAll = () => {
      const query = document.getElementById("searchInput").value.trim().toLowerCase();
      const activeFilter = document.querySelector(".filter-button.active").dataset.filter;

      const matchesSearch = (participant) => {
        const haystack = `${participant.name} ${participant.bib} ${participant.category} ${participant.location}`.toLowerCase();
        return haystack.includes(query);
      };

      const filteredParticipants = participants.filter((participant) => {
        const filterMatches = activeFilter === "all" || participant.categoryKey === activeFilter;
        return filterMatches && matchesSearch(participant);
      });

      const visibleSections = document.querySelectorAll("[data-section]");
      visibleSections.forEach((section) => {
        const sectionKey = section.dataset.section;
        section.style.display = activeFilter === "all" || activeFilter === sectionKey ? "block" : "none";
      });

      const overallRows = getRankedRows(filteredParticipants);
      const beginnerRows = getRankedRows(filteredParticipants.filter((participant) => participant.categoryKey === "Beginner"));
      const intermediateRows = getRankedRows(filteredParticipants.filter((participant) => participant.categoryKey === "Intermediate"));
      const advancedRows = getRankedRows(filteredParticipants.filter((participant) => participant.categoryKey === "Advanced"));

      renderTable("overallTable", overallRows);
      renderTable("beginnerTable", beginnerRows);
      renderTable("intermediateTable", intermediateRows);
      renderTable("advancedTable", advancedRows);

      document.getElementById("overallCount").textContent = `${overallRows.length} climbers`;
      document.getElementById("beginnerCount").textContent = `${beginnerRows.length} climbers`;
      document.getElementById("intermediateCount").textContent = `${intermediateRows.length} climbers`;
      document.getElementById("advancedCount").textContent = `${advancedRows.length} climbers`;
    };

    document.getElementById("searchInput").addEventListener("input", renderAll);

    document.querySelectorAll(".filter-button").forEach((button) => {
      button.addEventListener("click", () => {
        document.querySelectorAll(".filter-button").forEach((item) => item.classList.remove("active"));
        button.classList.add("active");
        renderAll();
      });
    });

    renderStats();
    renderAll();
  </script>
</body>
</html>
