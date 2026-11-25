<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Hanefî Tabakat ve Silsile Şeması — سلسلة فقهاء الحنفية</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=EB+Garamond:ital,wght@0,500;0,700;1,500&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />
  <style>
:root {
  --bg-ui: #f7f4ec;
  --surface: #ffffff;
  --surface-alt: #f1ece0;
  --border: #dcd3be;
  --text: #221a10;
  --text-muted: #6b5d47;
  --accent: #7c5828;
  --accent-hover: #60421b;
  --accent-soft: #f3ead7;
  --danger: #a62626;
  --radius: 8px;
  --shadow: 0 4px 16px rgba(34, 26, 16, 0.08);
}

* {
  box-sizing: border-box;
}

html, body {
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  font-family: 'Inter', 'Segoe UI', system-ui, sans-serif;
  background: var(--bg-ui);
  color: var(--text);
  font-size: 13px;
}

.hidden {
  display: none !important;
}

.app-shell {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
}

/* TOPBAR */
.topbar {
  height: 54px;
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 12px;
  gap: 10px;
  z-index: 30;
  flex-shrink: 0;
}

.topbar-left, .topbar-center, .topbar-right {
  display: flex;
  align-items: center;
  gap: 8px;
}

.topbar-center {
  flex: 1;
  justify-content: center;
  min-width: 0;
}

.brand {
  display: flex;
  flex-direction: column;
  line-height: 1.15;
}

.brand-ar {
  font-family: 'Amiri', 'Traditional Arabic', serif;
  font-size: 16px;
  font-weight: 700;
  color: var(--accent);
}

.brand-tr {
  font-size: 11px;
  font-weight: 600;
  color: var(--text-muted);
}

.icon-btn {
  width: 32px;
  height: 32px;
  border-radius: 7px;
  border: 1px solid var(--border);
  background: var(--surface);
  color: var(--text);
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-size: 15px;
}

.icon-btn:hover {
  background: var(--surface-alt);
}

/* Search */
.search-box {
  position: relative;
  width: 220px;
  max-width: 26vw;
}

.search-box input {
  width: 100%;
  height: 32px;
  padding: 0 10px;
  border-radius: 7px;
  border: 1px solid var(--border);
  background: var(--bg-ui);
  color: var(--text);
  font-size: 12.5px;
  outline: none;
}

.search-box input:focus {
  border-color: var(--accent);
  background: var(--surface);
}

.search-dropdown {
  position: absolute;
  top: 36px;
  left: 0;
  right: 0;
  max-height: 300px;
  overflow-y: auto;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  z-index: 60;
}

.search-item {
  padding: 7px 10px;
  cursor: pointer;
  border-bottom: 1px solid #f2ede2;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 8px;
}

.search-item:hover {
  background: var(--accent-soft);
}

.search-item-names {
  display: flex;
  flex-direction: column;
}

.search-item-ar {
  font-family: 'Amiri', serif;
  font-size: 14px;
  font-weight: 700;
}

.search-item-tr {
  font-size: 11.5px;
  color: var(--text-muted);
}

.search-item-year {
  font-size: 11px;
  font-weight: 700;
  color: var(--accent);
  white-space: nowrap;
}

/* Segmented buttons & selects */
.seg-group {
  display: inline-flex;
  background: var(--surface-alt);
  border: 1px solid var(--border);
  border-radius: 7px;
  padding: 2px;
}

.seg-btn {
  border: none;
  background: transparent;
  padding: 4px 9px;
  border-radius: 5px;
  font-size: 12px;
  font-weight: 600;
  color: var(--text-muted);
  cursor: pointer;
  white-space: nowrap;
}

.seg-btn.active {
  background: var(--surface);
  color: var(--accent);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.08);
}

.top-select, .side-select {
  height: 32px;
  border-radius: 7px;
  border: 1px solid var(--border);
  background: var(--surface);
  color: var(--text);
  padding: 0 8px;
  font-size: 12px;
  font-weight: 500;
  cursor: pointer;
}

.side-select {
  width: 100%;
  margin-top: 4px;
}

.action-btn, .primary-btn, .ghost-btn {
  height: 32px;
  padding: 0 11px;
  border-radius: 7px;
  font-size: 12px;
  font-weight: 600;
  cursor: pointer;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 5px;
  white-space: nowrap;
}

.action-btn {
  border: 1px solid var(--border);
  background: var(--surface);
  color: var(--text);
}

.action-btn:hover {
  background: var(--surface-alt);
}

.action-btn.active {
  background: var(--accent-soft);
  border-color: var(--accent);
  color: var(--accent);
}

.primary-btn {
  border: 1px solid var(--accent);
  background: var(--accent);
  color: #fff;
}

.primary-btn:hover {
  background: var(--accent-hover);
}

.ghost-btn {
  border: 1px solid var(--border);
  background: transparent;
  color: var(--text-muted);
}

.ghost-btn:hover {
  background: var(--surface-alt);
  color: var(--text);
}

.danger-text {
  color: var(--danger) !important;
}

.full-w {
  width: 100%;
}

/* Dropdown */
.dropdown {
  position: relative;
}

.dropdown-menu {
  position: absolute;
  right: 0;
  top: 36px;
  min-width: 230px;
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  padding: 5px;
  z-index: 70;
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.dropdown-menu button {
  text-align: left;
  border: none;
  background: transparent;
  padding: 8px 10px;
  border-radius: 5px;
  font-size: 12.5px;
  font-weight: 500;
  color: var(--text);
  cursor: pointer;
}

.dropdown-menu button:hover {
  background: var(--accent-soft);
  color: var(--accent);
}

.dropdown-menu hr {
  border: none;
  border-top: 1px solid var(--border);
  margin: 4px 0;
}

/* WORKSPACE */
.workspace {
  flex: 1;
  display: flex;
  min-height: 0;
  position: relative;
}

/* SIDEBAR */
.sidebar {
  width: 276px;
  flex-shrink: 0;
  background: var(--surface);
  border-right: 1px solid var(--border);
  overflow-y: auto;
  padding: 12px;
  display: flex;
  flex-direction: column;
  gap: 14px;
  z-index: 20;
}

.sidebar.collapsed {
  display: none;
}

.panel-section {
  border: 1px solid #eae2d1;
  border-radius: var(--radius);
  padding: 10px 11px;
  background: #fcfaf5;
}

.section-header-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.section-title {
  margin: 0 0 8px 0;
  font-size: 11.5px;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  color: var(--accent);
  font-weight: 700;
}

.mini-link {
  border: none;
  background: transparent;
  color: var(--danger);
  font-size: 11px;
  font-weight: 600;
  cursor: pointer;
  margin-bottom: 8px;
}

.toggle-grid {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.toggle-item {
  display: flex;
  align-items: center;
  gap: 8px;
  cursor: pointer;
  font-size: 12.5px;
  color: var(--text);
  user-select: none;
}

.toggle-item input {
  accent-color: var(--accent);
  width: 14px;
  height: 14px;
  cursor: pointer;
}

.soft-hr {
  border: none;
  border-top: 1px dashed var(--border);
  margin: 4px 0;
}

.filter-stack {
  display: flex;
  flex-direction: column;
  gap: 9px;
}

.field-label {
  display: flex;
  flex-direction: column;
  font-size: 11.5px;
  font-weight: 600;
  color: var(--text-muted);
}

.range-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 4px;
}

.dual-range {
  display: flex;
  align-items: center;
  gap: 6px;
}

.dual-range input {
  width: 100%;
  height: 30px;
  border-radius: 6px;
  border: 1px solid var(--border);
  padding: 0 8px;
  font-size: 12px;
}

/* Interactive Literature List */
.literature-list {
  display: flex;
  flex-direction: column;
  gap: 8px;
  max-height: 220px;
  overflow-y: auto;
  padding-right: 2px;
}

.lit-group-title {
  font-size: 11px;
  font-weight: 700;
  color: var(--text-muted);
  margin-bottom: 3px;
}

.lit-items {
  display: flex;
  flex-wrap: wrap;
  gap: 4px;
}

.lit-chip {
  border: 1px solid var(--border);
  background: var(--surface);
  border-radius: 5px;
  padding: 3px 7px;
  font-size: 11px;
  color: var(--text);
  cursor: pointer;
  text-align: left;
}

.lit-chip:hover {
  border-color: var(--accent);
  color: var(--accent);
}

.lit-chip.active {
  background: var(--accent);
  border-color: var(--accent);
  color: #fff;
}

.side-actions {
  display: flex;
  flex-direction: column;
  gap: 7px;
}

.btn-row-2 {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 6px;
}

/* CANVAS VIEWPORT */
.canvas-stage {
  flex: 1;
  position: relative;
  overflow: hidden;
  background: #e9e2d2;
  background-image: radial-gradient(rgba(124, 88, 40, 0.12) 1px, transparent 1px);
  background-size: 20px 20px;
}

.svg-viewport {
  width: 100%;
  height: 100%;
  cursor: grab;
  overflow: hidden;
  position: relative;
}

.svg-viewport.panning {
  cursor: grabbing;
}

.svg-viewport.drag-mode .scholar-node {
  cursor: move !important;
}

.svg-transform {
  transform-origin: 0 0;
  position: absolute;
  top: 0;
  left: 0;
  will-change: transform;
}

.svg-transform svg {
  display: block;
  box-shadow: 0 12px 42px rgba(0, 0, 0, 0.16);
}

/* Floating pills & banners */
.active-banner {
  position: absolute;
  top: 12px;
  left: 50%;
  transform: translateX(-50%);
  background: #2c1f0e;
  color: #fdf8e8;
  padding: 7px 14px;
  border-radius: 20px;
  font-size: 12.5px;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 10px;
  box-shadow: var(--shadow);
  z-index: 25;
}

.banner-close-btn {
  border: none;
  background: rgba(255, 255, 255, 0.18);
  color: #fff;
  width: 22px;
  height: 22px;
  border-radius: 50%;
  cursor: pointer;
}

.exit-poster-btn {
  position: absolute;
  top: 14px;
  right: 16px;
  z-index: 40;
  border: 1px solid var(--border);
  background: rgba(255, 255, 255, 0.94);
  color: var(--text);
  padding: 7px 14px;
  border-radius: 20px;
  font-weight: 700;
  cursor: pointer;
  box-shadow: var(--shadow);
}

.floating-controls {
  position: absolute;
  bottom: 14px;
  left: 16px;
  right: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  pointer-events: none;
  z-index: 25;
}

.stats-pill, .zoom-pill {
  pointer-events: auto;
  background: rgba(255, 255, 255, 0.94);
  border: 1px solid var(--border);
  border-radius: 20px;
  box-shadow: var(--shadow);
  backdrop-filter: blur(6px);
}

.stats-pill {
  padding: 6px 13px;
  font-size: 12px;
  font-weight: 600;
  color: var(--text-muted);
}

.zoom-pill {
  display: inline-flex;
  padding: 2px;
  gap: 2px;
}

.zoom-pill button {
  border: none;
  background: transparent;
  padding: 5px 10px;
  border-radius: 16px;
  font-size: 12px;
  font-weight: 700;
  color: var(--text);
  cursor: pointer;
}

.zoom-pill button:hover {
  background: var(--accent-soft);
  color: var(--accent);
}

/* RIGHT INSPECTOR DRAWER */
.inspector {
  width: 332px;
  flex-shrink: 0;
  background: var(--surface);
  border-left: 1px solid var(--border);
  display: flex;
  flex-direction: column;
  z-index: 25;
  box-shadow: -4px 0 20px rgba(0, 0, 0, 0.06);
}

.inspector-header {
  padding: 14px 14px 10px;
  border-bottom: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 8px;
  background: #fcfaf5;
}

.insp-ar {
  font-family: 'Amiri', serif;
  font-size: 20px;
  font-weight: 700;
  color: var(--accent);
  line-height: 1.25;
}

.insp-tr {
  font-family: 'EB Garamond', serif;
  font-size: 16px;
  font-weight: 700;
  color: var(--text);
}

.inspector-body {
  padding: 12px 14px;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  gap: 12px;
  flex: 1;
}

.insp-badges {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}

.badge-pill {
  font-size: 11px;
  font-weight: 600;
  padding: 3px 8px;
  border-radius: 12px;
  border: 1px solid var(--border);
  background: var(--surface-alt);
}

/* Focus Mode Box */
.focus-box {
  background: #faf5e8;
  border: 1px solid #d6c39c;
  border-radius: var(--radius);
  padding: 10px;
  display: flex;
  flex-direction: column;
  gap: 7px;
}

.focus-box-title {
  font-size: 11.5px;
  font-weight: 700;
  color: var(--accent);
  text-transform: uppercase;
  letter-spacing: 0.03em;
}

.focus-mode-row, .focus-dir-row {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 4px;
}

.f-btn, .f-dir-btn {
  border: 1px solid var(--border);
  background: var(--surface);
  border-radius: 6px;
  padding: 5px 4px;
  font-size: 11px;
  font-weight: 600;
  cursor: pointer;
  color: var(--text);
}

.f-btn.active, .f-dir-btn.active {
  background: var(--accent);
  border-color: var(--accent);
  color: #fff;
}

.focus-counts {
  font-size: 11.5px;
  color: var(--text-muted);
  text-align: center;
}

.insp-details {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.detail-block h4 {
  margin: 0 0 4px 0;
  font-size: 11px;
  text-transform: uppercase;
  color: var(--text-muted);
}

.detail-block p {
  margin: 0;
  font-size: 12.5px;
  line-height: 1.48;
  color: var(--text);
}

.chip-list {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}

.link-chip {
  border: 1px solid var(--border);
  background: var(--bg-ui);
  padding: 4px 8px;
  border-radius: 6px;
  font-size: 11.5px;
  font-weight: 500;
  cursor: pointer;
  color: var(--text);
}

.link-chip:hover {
  border-color: var(--accent);
  background: var(--accent-soft);
  color: var(--accent);
}

.work-tag {
  background: #f2f6fb;
  border: 1px solid #c9d8ec;
  color: #1c3d6e;
  padding: 3px 7px;
  border-radius: 5px;
  font-size: 11.5px;
}

.insp-actions {
  display: grid;
  grid-template-columns: 1fr 1fr auto;
  gap: 6px;
  padding-top: 8px;
  border-top: 1px solid var(--border);
}

/* POSTER FULLSCREEN MODE */
.app-shell.poster-mode .topbar,
.app-shell.poster-mode .sidebar,
.app-shell.poster-mode .inspector {
  display: none !important;
}

/* MODAL */
.modal-backdrop {
  position: fixed;
  inset: 0;
  background: rgba(20, 16, 10, 0.52);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 100;
  padding: 18px;
}

.modal-card {
  width: 720px;
  max-width: 100%;
  max-height: 92vh;
  background: var(--surface);
  border-radius: 12px;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.25);
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.modal-header {
  padding: 14px 18px;
  border-bottom: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #fcfaf5;
}

.modal-header h2 {
  margin: 0;
  font-size: 16px;
  color: var(--accent);
}

.modal-form {
  padding: 16px 18px;
  overflow-y: auto;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.modal-form label {
  display: flex;
  flex-direction: column;
  gap: 4px;
  font-size: 11.5px;
  font-weight: 600;
  color: var(--text-muted);
}

.modal-form input[type="text"],
.modal-form input[type="number"],
.modal-form select,
.modal-form textarea {
  border: 1px solid var(--border);
  border-radius: 6px;
  padding: 7px 9px;
  font-size: 12.5px;
  font-family: inherit;
  color: var(--text);
}

.checkbox-inline {
  flex-direction: row !important;
  align-items: center;
  gap: 8px !important;
  margin-top: 18px;
  cursor: pointer;
}

.form-grid-2 {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px;
}

.form-grid-3 {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 10px;
}

.teacher-picker-wrap {
  border: 1px solid var(--border);
  border-radius: 8px;
  padding: 9px;
  background: #faf8f2;
  display: flex;
  flex-direction: column;
  gap: 7px;
}

.teacher-picker-head {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
  font-size: 11.5px;
  font-weight: 700;
  color: var(--text-muted);
}

.teacher-picker-head input {
  width: 210px;
  padding: 4px 8px !important;
}

.selected-chips {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}

.sel-chip {
  background: var(--accent);
  color: #fff;
  padding: 3px 8px;
  border-radius: 12px;
  font-size: 11px;
  display: inline-flex;
  align-items: center;
  gap: 5px;
}

.sel-chip button {
  border: none;
  background: transparent;
  color: #fff;
  cursor: pointer;
  font-weight: 700;
  padding: 0;
}

.teacher-options {
  max-height: 120px;
  overflow-y: auto;
  display: flex;
  flex-wrap: wrap;
  gap: 4px;
}

.t-opt {
  border: 1px solid var(--border);
  background: var(--surface);
  border-radius: 5px;
  padding: 3px 7px;
  font-size: 11px;
  cursor: pointer;
}

.t-opt:hover {
  border-color: var(--accent);
  color: var(--accent);
}

.modal-footer {
  display: flex;
  justify-content: flex-end;
  gap: 8px;
  padding-top: 8px;
  border-top: 1px solid var(--border);
}

@media (max-width: 1120px) {
  .brand-tr { display: none; }
  .search-box { width: 160px; }
  .sidebar { width: 244px; }
}

</style>
</head>
<body>
  <div id="app" class="app-shell">
    <!-- TOP STUDIO BAR -->
    <header class="topbar" id="topbar">
      <div class="topbar-left">
        <button id="btn-toggle-sidebar" class="icon-btn" title="Paneli Aç/Kapat">☰</button>
        <div class="brand">
          <span class="brand-ar">سلسلة فقهاء الحنفية</span>
          <span class="brand-tr" id="ui-app-title">Hanefî Tabakat ve Silsile Şeması</span>
        </div>
      </div>

      <div class="topbar-center">
        <!-- Search -->
        <div class="search-box">
          <input type="text" id="search-input" autocomplete="off" placeholder="Alim, eser, görev veya yıl ara..." />
          <div id="search-results" class="search-dropdown hidden"></div>
        </div>

        <!-- Language Switcher -->
        <div class="seg-group" id="lang-switch" title="Dil / اللغة">
          <button data-lang="tr" class="seg-btn">TR</button>
          <button data-lang="ar" class="seg-btn">عربي</button>
          <button data-lang="both" class="seg-btn active">AR+TR</button>
        </div>

        <!-- Layout Mode -->
        <div class="seg-group" id="layout-switch">
          <button data-layout="century" class="seg-btn active" id="lbl-layout-century">Yüzyıl Hizalı</button>
          <button data-layout="compact" class="seg-btn" id="lbl-layout-compact">Kompakt Silsile</button>
        </div>

        <!-- Color Mode -->
        <select id="color-mode-select" class="top-select" title="Renklendirme">
          <option value="region">Havzaya Göre</option>
          <option value="tabaka">Tabakaya Göre</option>
          <option value="minimal">Sade Baskı</option>
        </select>

        <!-- Theme -->
        <select id="theme-select" class="top-select" title="Afiş Teması">
          <option value="parchment">Klasik Parşömen</option>
          <option value="printWhite">Matbaa Beyazı</option>
          <option value="night">Sunum (Koyu)</option>
        </select>
      </div>

      <div class="topbar-right">
        <button id="btn-drag-mode" class="action-btn" title="Afiş baskısı öncesi kartları manuel sürükleyerek ince ayar yapın">
          ✥ <span id="lbl-drag-tweak">Kart Taşıma</span>
        </button>
        <button id="btn-poster-mode" class="action-btn" title="Tam Ekran Afiş Önizleme">
          ▣ <span id="lbl-poster-mode">Afiş Önizleme</span>
        </button>
        <div class="dropdown">
          <button id="btn-export-menu" class="primary-btn">⬇ <span id="lbl-export-menu">Dışa Aktar</span></button>
          <div id="export-dropdown" class="dropdown-menu hidden">
            <button data-export="svg" id="lbl-exp-svg">Vektörel Afiş (SVG — Matbaa)</button>
            <button data-export="png2" id="lbl-exp-png2">Yüksek Çözünürlük PNG (2x)</button>
            <button data-export="png3" id="lbl-exp-png3">Ultra Çözünürlük PNG (3x)</button>
            <button data-export="print" id="lbl-exp-print">Yazdır / PDF Afiş</button>
            <hr />
            <button data-export="json" id="lbl-exp-json">Veri Yedeği (JSON)</button>
            <button data-export="csv" id="lbl-exp-csv">Excel Tablosu (CSV)</button>
          </div>
        </div>
      </div>
    </header>

    <!-- MAIN BODY -->
    <div class="workspace">
      <!-- LEFT SIDEBAR -->
      <aside class="sidebar" id="sidebar">
        <!-- Section 1: Card Variable Attributes -->
        <section class="panel-section">
          <h3 class="section-title" id="sec-card-fields">Kartta Gösterilecek Özellikler</h3>
          <div class="toggle-grid">
            <label class="toggle-item"><input type="checkbox" data-field="showHijri" checked /><span id="lbl-f-hijri">Hicrî Vefat Yılı</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showMiladi" /><span id="lbl-f-miladi">Milâdî Vefat Yılı</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showTabaka" /><span id="lbl-f-tabaka">Tabaka Derecesi (İbn Kemal)</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showRegion" /><span id="lbl-f-region">İlmî Havza Etiketi</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showRoles" /><span id="lbl-f-roles">Meşhur Görevleri / Unvanları</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showWorks" /><span id="lbl-f-works">Meşhur Eserleri</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showTags" /><span id="lbl-f-tags">Öne Çıkan Özellikler</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showNonHanafi" checked /><span id="lbl-f-nonhanafi">Gayri-Hanefî İsnad (*)</span></label>
            <hr class="soft-hr" />
            <label class="toggle-item"><input type="checkbox" data-field="showCenturyBands" checked /><span id="lbl-f-bands">Yüzyıl Şeritleri</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showHeader" checked /><span id="lbl-f-header">Afiş Başlığı ve Çerçeve</span></label>
            <label class="toggle-item"><input type="checkbox" data-field="showLegend" checked /><span id="lbl-f-legend">Lejant ve Eserler Kutusu</span></label>
          </div>
        </section>

        <!-- Section 2: Filters -->
        <section class="panel-section">
          <h3 class="section-title" id="sec-filters">Filtreler</h3>
          <div class="filter-stack">
            <label class="field-label">
              <span id="lbl-filter-region">İlmî Havza</span>
              <select id="filter-region" class="side-select"></select>
            </label>
            <label class="field-label">
              <span id="lbl-filter-tabaka">Tabaka (İbn Kemal)</span>
              <select id="filter-tabaka" class="side-select"></select>
            </label>
            <div class="field-label">
              <div class="range-header">
                <span id="lbl-century-range">Yüzyıl Aralığı</span>
                <strong id="century-range-val">1. – 14. yy</strong>
              </div>
              <div class="dual-range">
                <input type="number" id="century-min" min="1" max="15" value="1" />
                <span>—</span>
                <input type="number" id="century-max" min="1" max="15" value="15" />
              </div>
            </div>
          </div>
        </section>

        <!-- Section 3: Interactive Classical Literature -->
        <section class="panel-section">
          <div class="section-header-row">
            <h3 class="section-title" id="sec-books">Temel Eserler (İnteraktif)</h3>
            <button id="btn-clear-book" class="mini-link hidden">Temizle</button>
          </div>
          <div id="literature-list" class="literature-list"></div>
        </section>

        <!-- Section 4: Data Management -->
        <section class="panel-section">
          <h3 class="section-title" id="sec-data">Veri ve Afiş Yönetimi</h3>
          <div class="side-actions">
            <button id="btn-add-scholar" class="primary-btn full-w">+ <span id="lbl-add-scholar">Yeni Alim Ekle</span></button>
            <label class="action-btn full-w file-btn">
              ⬆ <span id="lbl-import-data">JSON / CSV İçe Aktar</span>
              <input type="file" id="import-file-input" accept=".json,.csv" hidden />
            </label>
            <div class="btn-row-2">
              <button id="btn-reset-positions" class="ghost-btn">Yerleşimi Sıfırla</button>
              <button id="btn-reset-data" class="ghost-btn danger-text">Veriyi Sıfırla</button>
            </div>
          </div>
        </section>
      </aside>

      <!-- CENTER CANVAS VIEWPORT -->
      <main class="canvas-stage" id="canvas-stage">
        <!-- Floating Active Mode Banner -->
        <div id="active-banner" class="active-banner hidden">
          <span id="active-banner-text"></span>
          <button id="btn-banner-clear" class="banner-close-btn">✕</button>
        </div>

        <!-- Floating Poster Mode Exit Button -->
        <button id="btn-exit-poster" class="exit-poster-btn hidden">✕ <span id="lbl-exit-poster">Kontrolleri Göster</span></button>

        <!-- Pan & Zoom Container -->
        <div id="svg-viewport" class="svg-viewport">
          <div id="svg-transform" class="svg-transform"></div>
        </div>

        <!-- Bottom Floating Zoom & Stats Controls -->
        <div class="floating-controls" id="floating-controls">
          <div class="stats-pill" id="stats-pill">0 Alim</div>
          <div class="zoom-pill">
            <button id="zoom-out" title="Uzaklaştır">−</button>
            <button id="zoom-fit" title="Afişi Ekrana Sığdır">Sığdır</button>
            <button id="zoom-100" title="%100">100%</button>
            <button id="zoom-in" title="Yakınlaştır">+</button>
          </div>
        </div>
      </main>

      <!-- RIGHT PERSON-FOCUSED INSPECTOR DRAWER -->
      <aside class="inspector hidden" id="inspector">
        <div class="inspector-header">
          <div>
            <div class="insp-ar" id="insp-name-ar"></div>
            <div class="insp-tr" id="insp-name-tr"></div>
          </div>
          <button id="btn-close-inspector" class="icon-btn">✕</button>
        </div>

        <div class="inspector-body">
          <!-- Meta badges -->
          <div class="insp-badges" id="insp-badges"></div>

          <!-- PERSON-FOCUSED MODE BOX -->
          <div class="focus-box">
            <div class="focus-box-title" id="lbl-focus-title">Şahıs Odaklı Mod</div>
            <div class="focus-mode-row">
              <button data-fmode="off" class="f-btn active" id="lbl-f-off">Tam Şema</button>
              <button data-fmode="highlight" class="f-btn" id="lbl-f-highlight">Vurgula</button>
              <button data-fmode="isolate" class="f-btn" id="lbl-f-isolate">İzole Et</button>
            </div>
            <div class="focus-dir-row" id="focus-dir-row">
              <button data-fdir="both" class="f-dir-btn active" id="lbl-d-both">Öncesi + Sonrası</button>
              <button data-fdir="ancestors" class="f-dir-btn" id="lbl-d-anc">Öncesi (Hocalar)</button>
              <button data-fdir="descendants" class="f-dir-btn" id="lbl-d-desc">Sonrası (Talebeler)</button>
            </div>
            <div class="focus-counts" id="focus-counts"></div>
          </div>

          <!-- Details -->
          <div id="insp-details" class="insp-details"></div>

          <!-- Actions -->
          <div class="insp-actions">
            <button id="btn-edit-scholar" class="action-btn">✎ <span id="lbl-edit-scholar">Düzenle</span></button>
            <button id="btn-add-student" class="primary-btn">+ <span id="lbl-add-student">Talebe Ekle</span></button>
            <button id="btn-delete-scholar" class="ghost-btn danger-text">🗑 <span id="lbl-delete-scholar">Sil</span></button>
          </div>
          <button id="btn-copy-embed" class="action-btn full-w">🔗 <span id="lbl-copy-embed">Quartz / Iframe Kodu Kopyala</span></button>
        </div>
      </aside>
    </div>
  </div>

  <!-- ADD / EDIT SCHOLAR MODAL -->
  <div id="scholar-modal" class="modal-backdrop hidden">
    <div class="modal-card">
      <div class="modal-header">
        <h2 id="modal-title">Yeni Alim Ekle</h2>
        <button id="btn-close-modal" class="icon-btn">✕</button>
      </div>
      <form id="scholar-form" class="modal-form">
        <input type="hidden" id="f-id" />
        <div class="form-grid-2">
          <label>
            <span>Türkçe İsim *</span>
            <input type="text" id="f-nameTr" required placeholder="Örn: Muhammed Zâhid el-Kevserî" />
          </label>
          <label>
            <span>Arapça İsim (الاسم بالعربية) *</span>
            <input type="text" id="f-nameAr" dir="rtl" required placeholder="مثال: محمد زاهد الكوثري" />
          </label>
        </div>

        <div class="form-grid-3">
          <label>
            <span>Hicrî Vefat Yılı *</span>
            <input type="number" id="f-deathH" required min="1" max="1500" placeholder="1371" />
          </label>
          <label>
            <span>Milâdî Yıl (Opsiyonel)</span>
            <input type="number" id="f-deathM" min="622" max="2100" placeholder="Otomatik hesaplanır" />
          </label>
          <label>
            <span>İlmî Havza / Bölge</span>
            <select id="f-region"></select>
          </label>
        </div>

        <div class="form-grid-2">
          <label>
            <span>Tabaka Derecesi (İbn Kemal)</span>
            <select id="f-tabaka"></select>
          </label>
          <label class="checkbox-inline">
            <input type="checkbox" id="f-nonHanafi" />
            <span>Gayri-Hanefî İsnad Alimi (*)</span>
          </label>
        </div>

        <!-- Teachers multi-picker -->
        <div class="teacher-picker-wrap">
          <div class="teacher-picker-head">
            <span>Hocaları (Birden fazla seçilebilir)</span>
            <input type="text" id="f-teacher-search" placeholder="Hoca ara..." />
          </div>
          <div id="f-selected-teachers" class="selected-chips"></div>
          <div id="f-teacher-options" class="teacher-options"></div>
        </div>

        <div class="form-grid-2">
          <label>
            <span>Meşhur Görevleri / Unvanları (TR — ; ile ayırın)</span>
            <input type="text" id="f-rolesTr" placeholder="Şeyhülislam; Ders Vekili" />
          </label>
          <label>
            <span>المناصب والألقاب (AR — افصل بـ ;)</span>
            <input type="text" id="f-rolesAr" dir="rtl" placeholder="وكيل الدرس؛ فقيه ومحدث" />
          </label>
        </div>

        <div class="form-grid-2">
          <label>
            <span>Meşhur Eserleri (TR — ; ile ayırın)</span>
            <input type="text" id="f-worksTr" placeholder="Te’nîbü’l-Hatîb; Makâlât" />
          </label>
          <label>
            <span>أشهر المؤلفات (AR — افصل بـ ;)</span>
            <input type="text" id="f-worksAr" dir="rtl" placeholder="تأنيب الخطيب؛ مقالات الكوثري" />
          </label>
        </div>

        <div class="form-grid-2">
          <label>
            <span>Öne Çıkan Özellikler / Etiketler (TR — ;)</span>
            <input type="text" id="f-tagsTr" placeholder="Muhakkik; Hadis ve Fıkıh" />
          </label>
          <label>
            <span>المميزات البارزة (AR — ;)</span>
            <input type="text" id="f-tagsAr" dir="rtl" placeholder="محقق؛ فقه وحديث" />
          </label>
        </div>

        <div class="form-grid-2">
          <label>
            <span>Kısa İlmî Not / Biyografi (TR)</span>
            <textarea id="f-bioTr" rows="2"></textarea>
          </label>
          <label>
            <span>نبذة علمية (AR)</span>
            <textarea id="f-bioAr" dir="rtl" rows="2"></textarea>
          </label>
        </div>

        <div class="modal-footer">
          <button type="button" id="btn-cancel-modal" class="ghost-btn">İptal</button>
          <button type="submit" class="primary-btn">Kaydet ve Şemayı Güncelle</button>
        </div>
      </form>
    </div>
  </div>

  <script>
(function(){
"use strict";
// ===== src/data/taxonomy.js =====
// Taxonomy, Regions, Tabakat (Ibn Kemal), Centuries, Themes, and Bilingual UI strings

const REGIONS = {
  root: {
    id: 'root',
    nameTr: 'Nübüvvet Kaynağı',
    nameAr: 'مصدر النبوة',
    stroke: '#2c2216',
    fill: '#fdf8e8',
    text: '#1f160c',
    arrow: '#8c6d2f',
    laneOrder: 3,
  },
  mekke: {
    id: 'mekke',
    nameTr: 'Mekke-i Mükerreme',
    nameAr: 'مكة المكرمة',
    stroke: '#d49b1a',
    fill: '#fef9e7',
    text: '#6e4e05',
    arrow: '#d49b1a',
    laneOrder: 0,
  },
  medine: {
    id: 'medine',
    nameTr: 'Medine-i Münevvere',
    nameAr: 'المدينة المنورة',
    stroke: '#4b8b3b',
    fill: '#f1f9ee',
    text: '#1f4d15',
    arrow: '#4b8b3b',
    laneOrder: 5,
  },
  kufe: {
    id: 'kufe',
    nameTr: 'Kûfe / Irak',
    nameAr: 'الكوفة والعراق',
    stroke: '#1d4d8f',
    fill: '#eef4fc',
    text: '#0e2d5c',
    arrow: '#2259a3',
    laneOrder: 2,
  },
  maveraunnehir: {
    id: 'maveraunnehir',
    nameTr: 'Mâverâünnehir',
    nameAr: 'ما وراء النهر',
    stroke: '#0d8a96',
    fill: '#ecfafb',
    text: '#074e56',
    arrow: '#0d8a96',
    laneOrder: 4,
  },
  horasan: {
    id: 'horasan',
    nameTr: 'Horasan',
    nameAr: 'خراسان',
    stroke: '#8b2f8b',
    fill: '#faf0fa',
    text: '#541454',
    arrow: '#8b2f8b',
    laneOrder: 6,
  },
  misir: {
    id: 'misir',
    nameTr: 'Mısır ve Şam',
    nameAr: 'مصر والشام',
    stroke: '#c9621e',
    fill: '#fdf4ec',
    text: '#753208',
    arrow: '#c9621e',
    laneOrder: 3,
  },
  rum: {
    id: 'rum',
    nameTr: 'Rum (Anadolu / Osmanlı)',
    nameAr: 'الروم (الدولة العثمانية)',
    stroke: '#7c2929',
    fill: '#fbf0f0',
    text: '#4f1313',
    arrow: '#7c2929',
    laneOrder: 1,
  },
};

// İbn Kemal Paşazade'nin meşhur 7'li Tabakat-ı Fukaha tasnifi (+ Kaynak/Selef için 0)
const TABAKAT = {
  0: {
    id: 0,
    shortTr: 'Selef / İsnad',
    shortAr: 'السلف / الإسناد',
    nameTr: 'Sahabe, Tâbiîn ve İsnad Kaynağı',
    nameAr: 'الصحابة والتابعون ومصادر الإسناد',
    stroke: '#6c5a37',
    fill: '#f7f2e4',
    text: '#43351b',
  },
  1: {
    id: 1,
    shortTr: '1. Tabaka',
    shortAr: 'الطبقة ١',
    nameTr: 'Müctehid fi’ş-Şer‘ (Mutlak Müctehid)',
    nameAr: 'المجتهدون في الشرع',
    stroke: '#8c1d18',
    fill: '#fdeceb',
    text: '#610f0b',
  },
  2: {
    id: 2,
    shortTr: '2. Tabaka',
    shortAr: 'الطبقة ٢',
    nameTr: 'Müctehid fi’l-Mezheb',
    nameAr: 'المجتهدون في المذهب',
    stroke: '#a84b00',
    fill: '#fef2e6',
    text: '#6b2e00',
  },
  3: {
    id: 3,
    shortTr: '3. Tabaka',
    shortAr: 'الطبقة ٣',
    nameTr: 'Müctehid fi’l-Mesâil',
    nameAr: 'المجتهدون في المسائل',
    stroke: '#b08300',
    fill: '#fef9e3',
    text: '#664a00',
  },
  4: {
    id: 4,
    shortTr: '4. Tabaka',
    shortAr: 'الطبقة ٤',
    nameTr: 'Ashâbü’t-Tahrîc',
    nameAr: 'أصحاب التخريج',
    stroke: '#1e7145',
    fill: '#eaf7f0',
    text: '#0e4729',
  },
  5: {
    id: 5,
    shortTr: '5. Tabaka',
    shortAr: 'الطبقة ٥',
    nameTr: 'Ashâbü’t-Tercîh',
    nameAr: 'أصحاب الترجيح',
    stroke: '#0d7387',
    fill: '#e8f7fa',
    text: '#064652',
  },
  6: {
    id: 6,
    shortTr: '6. Tabaka',
    shortAr: 'الطبقة ٦',
    nameTr: 'Ashâbü’t-Temyîz',
    nameAr: 'أصحاب التمييز',
    stroke: '#2c4a9e',
    fill: '#edf1fc',
    text: '#162961',
  },
  7: {
    id: 7,
    shortTr: '7. Tabaka',
    shortAr: 'الطبقة ٧',
    nameTr: 'Mukallidîn / Muhakkikîn',
    nameAr: 'المقلدون والمحققون',
    stroke: '#64388c',
    fill: '#f4eefb',
    text: '#3c1c59',
  },
};

const CENTURY_META = {
  1: { tr: '1. Hicrî Yüzyıl', ar: 'القرن الأول الهجري', subTr: 'Sahabe ve Büyük Tâbiîn', subAr: 'الصحابة وكبار التابعين', miladi: '622 – 719' },
  2: { tr: '2. Hicrî Yüzyıl', ar: 'القرن الثاني الهجري', subTr: 'Kuruluş ve İmamlar Dönemi', subAr: 'عصر التأسيس والأئمة', miladi: '719 – 816' },
  3: { tr: '3. Hicrî Yüzyıl', ar: 'القرن الثالث الهجري', subTr: 'Rivayet ve Yayılma Dönemi', subAr: 'عصر الرواية والانتشار', miladi: '816 – 913' },
  4: { tr: '4. Hicrî Yüzyıl', ar: 'القرن الرابع الهجري', subTr: 'Muhtasarlar ve Ekolleşme', subAr: 'عصر المختصرات والتدوين', miladi: '913 – 1010' },
  5: { tr: '5. Hicrî Yüzyıl', ar: 'القرن الخامس الهجري', subTr: 'Usul ve Büyük Şerhler', subAr: 'عصر الأصول والمبسوطات', miladi: '1010 – 1107' },
  6: { tr: '6. Hicrî Yüzyıl', ar: 'القرن السادس الهجري', subTr: 'Mâverâünnehir Zirvesi (Hidaye)', subAr: 'ذروة ما وراء النهر', miladi: '1107 – 1204' },
  7: { tr: '7. Hicrî Yüzyıl', ar: 'القرن السابع الهجري', subTr: 'Mütûn-ı Erbaa’nın Teşekkülü', subAr: 'تأليف المتون المعتبرة', miladi: '1204 – 1301' },
  8: { tr: '8. Hicrî Yüzyıl', ar: 'القرن الثامن الهجري', subTr: 'Şerh ve Tenkih Dönemi', subAr: 'عصر الشروح والتنقيح', miladi: '1301 – 1398' },
  9: { tr: '9. Hicrî Yüzyıl', ar: 'القرن التاسع الهجري', subTr: 'Osmanlı ve Memluk Havzası', subAr: 'عصر العثمانيين والمماليك', miladi: '1398 – 1495' },
  10: { tr: '10. Hicrî Yüzyıl', ar: 'القرن العاشر الهجري', subTr: 'Meşihat, Fetva ve Tabakat', subAr: 'عصر الفتوى والطبقات', miladi: '1495 – 1592' },
  11: { tr: '11. Hicrî Yüzyıl', ar: 'القرن الحادي عشر الهجري', subTr: 'Haşiye ve Fetva Mecmuaları', subAr: 'عصر الحواشي والفتاوى', miladi: '1592 – 1689' },
  12: { tr: '12. Hicrî Yüzyıl', ar: 'القرن الثاني عشر الهجري', subTr: 'İsnad ve Tahkik Halkası', subAr: 'حلقة الإسناد والتحقيق', miladi: '1689 – 1786' },
  13: { tr: '13. Hicrî Yüzyıl', ar: 'القرن الثالث عشر الهجري', subTr: 'Son Muhakkikler (İbn Âbidîn)', subAr: 'خاتمة المحققين', miladi: '1786 – 1883' },
  14: { tr: '14. Hicrî Yüzyıl', ar: 'القرن الرابع عشر الهجري', subTr: 'Modern Dönem Fakihleri', subAr: 'فقهاء العصر الحديث', miladi: '1883 – 1980' },
  15: { tr: '15. Hicrî Yüzyıl', ar: 'القرن الخامس عشر الهجري', subTr: 'Çağdaş Fakihler', subAr: 'الفقهاء المعاصرون', miladi: '1980 – ...' },
};

const THEMES = {
  parchment: {
    id: 'parchment',
    nameTr: 'Klasik Parşömen',
    nameAr: 'رقّ كلاسيكي',
    bg: '#f5f0e1',
    bgAlt: '#eee7d3',
    bandBorder: '#d9ceb2',
    frameOuter: '#7c6236',
    frameInner: '#bfa46f',
    titleText: '#2c1f0e',
    subtitleText: '#665232',
    bandLabelBg: '#e8dec4',
    bandLabelText: '#3e2e16',
    panelBg: '#faf6eb',
    panelBorder: '#ccb991',
    dimOpacity: 0.14,
  },
  printWhite: {
    id: 'printWhite',
    nameTr: 'Matbaa Beyazı',
    nameAr: 'أبيض للطباعة',
    bg: '#ffffff',
    bgAlt: '#f7f8fa',
    bandBorder: '#d6dce5',
    frameOuter: '#1f2937',
    frameInner: '#94a3b8',
    titleText: '#0f172a',
    subtitleText: '#475569',
    bandLabelBg: '#f1f5f9',
    bandLabelText: '#1e293b',
    panelBg: '#ffffff',
    panelBorder: '#cbd5e1',
    dimOpacity: 0.12,
  },
  night: {
    id: 'night',
    nameTr: 'Sunum (Koyu)',
    nameAr: 'عرض ليلي',
    bg: '#0f172a',
    bgAlt: '#152038',
    bandBorder: '#243454',
    frameOuter: '#c5a059',
    frameInner: '#56688a',
    titleText: '#f8fafc',
    subtitleText: '#cbd5e1',
    bandLabelBg: '#1e293b',
    bandLabelText: '#e2e8f0',
    panelBg: '#162033',
    panelBorder: '#334155',
    dimOpacity: 0.15,
  },
};

const UI_TEXT = {
  tr: {
    appTitle: 'Hanefî Fakihleri Tabakat ve Silsile Şeması',
    posterTitle: 'Hanefî Mezhebi Fakihleri Silsilesi ve Tabakatı',
    posterSubtitle: 'Hicrî Yüzyıllara ve İlmî Havzalara Göre Hoca–Talebe Zinciri',
    searchPlaceholder: 'Alim, eser, görev veya yıl ara...',
    layoutCentury: 'Yüzyıl Hizalı',
    layoutCompact: 'Kompakt Silsile',
    colorRegion: 'Havzaya Göre',
    colorTabaka: 'Tabakaya Göre',
    colorMinimal: 'Sade Baskı',
    posterMode: 'Afiş Önizleme',
    exitPosterMode: 'Kontrolleri Göster',
    dragTweak: 'Kart Taşıma',
    exportMenu: 'Dışa Aktar',
    exportSvg: 'Vektörel Afiş (SVG — Matbaa)',
    exportPng: 'Yüksek Çözünürlük (PNG)',
    exportPrint: 'Yazdır / PDF Afiş',
    exportJson: 'Veri Yedeği (JSON)',
    exportCsv: 'Excel Tablosu (CSV)',
    importData: 'JSON / CSV İçe Aktar',
    addScholar: 'Yeni Alim Ekle',
    resetPositions: 'Yerleşimi Sıfırla',
    resetData: 'Varsayılan Veriye Dön',
    secCardFields: 'Kartta Gösterilecek Özellikler',
    secFilters: 'Filtreler',
    secBooks: 'Temel Eserler (İnteraktif)',
    secData: 'Veri ve Afiş Ayarları',
    fieldHijri: 'Hicrî Vefat Yılı',
    fieldMiladi: 'Milâdî Vefat Yılı',
    fieldTabaka: 'Tabaka Derecesi (İbn Kemal)',
    fieldRegion: 'İlmî Havza Etiketi',
    fieldWorks: 'Meşhur Eserleri',
    fieldRoles: 'Meşhur Görevleri / Unvanları',
    fieldTags: 'Öne Çıkan Özellikler',
    fieldNonHanafi: 'Gayri-Hanefî İsnad Alimleri (*)',
    fieldHeader: 'Afiş Başlığı ve Çerçevesi',
    fieldLegend: 'Lejant ve Eserler Kutusu',
    fieldCenturyBands: 'Yüzyıl Şeritleri ve Zaman Cetveli',
    allRegions: 'Tüm Havzalar',
    allTabakat: 'Tüm Tabakalar',
    centuryRange: 'Yüzyıl Aralığı',
    focusTitle: 'Şahıs Odaklı Mod',
    focusOff: 'Tam Şema',
    focusHighlight: 'Şemada Vurgula',
    focusIsolate: 'Sadece Bu Şahsa İzole Et',
    dirBoth: 'Öncesi ve Sonrası',
    dirAncestors: 'Sadece Öncesi (Hocalar)',
    dirDescendants: 'Sadece Sonrası (Talebeler)',
    teachers: 'Hocaları',
    students: 'Talebeleri',
    works: 'Meşhur Eserleri',
    roles: 'Görevleri / Unvanları',
    tags: 'Öne Çıkan Özellikleri',
    notes: 'İlmî Not / Biyografi',
    editScholar: 'Alimi Düzenle',
    addStudentTo: 'Bu Alime Talebe Ekle',
    deleteScholar: 'Alimi Sil',
    clearFocus: 'Odağı Kaldır',
    nonHanafiNote: '* İlmî ve isnad faydası sebebiyle silsilede zikredilen gayri-Hanefî alimler',
    statsScholars: 'Alim',
    statsEdges: 'Bağlantı',
    statsCenturies: 'Yüzyıl',
    bookActiveHint: 'Seçili eser müellifi ve şarihleri vurgulanıyor',
    clearBook: 'Eser Vurgusunu Kaldır',
  },
  ar: {
    appTitle: 'سلسلة وطبقات فقهاء الحنفية',
    posterTitle: 'سلسلة فقهاء الحنفية وطبقاتهم',
    posterSubtitle: 'مرتبة حسب القرون الهجرية والمدارس العلمية وسلاسل الإسناد',
    searchPlaceholder: 'ابحث عن عالم أو كتاب أو منصب...',
    layoutCentury: 'مرتب بالقرون',
    layoutCompact: 'شجرة مدمجة',
    colorRegion: 'حسب الإقليم',
    colorTabaka: 'حسب الطبقة',
    colorMinimal: 'طباعة بسيطة',
    posterMode: 'معاينة اللوحة',
    exitPosterMode: 'إظهار الأدوات',
    dragTweak: 'تحريك البطاقات',
    exportMenu: 'تصدير',
    exportSvg: 'لوحة متجهة (SVG للطباعة)',
    exportPng: 'صورة عالية الدقة (PNG)',
    exportPrint: 'طباعة / PDF',
    exportJson: 'نسخة بيانات (JSON)',
    exportCsv: 'جدول إكسل (CSV)',
    importData: 'استيراد JSON / CSV',
    addScholar: 'إضافة عالم جديد',
    resetPositions: 'إعادة ضبط المواقع',
    resetData: 'استعادة البيانات الأصلية',
    secCardFields: 'خصائص البطاقة الظاهرة',
    secFilters: 'التصفية',
    secBooks: 'الكتب الأساسية (تفاعلي)',
    secData: 'إدارة البيانات واللوحة',
    fieldHijri: 'سنة الوفاة الهجرية',
    fieldMiladi: 'سنة الوفاة الميلادية',
    fieldTabaka: 'درجة الطبقة (ابن كمال)',
    fieldRegion: 'وسم الإقليم العلمي',
    fieldWorks: 'أشهر المؤلفات',
    fieldRoles: 'أشهر المناصب والألقاب',
    fieldTags: 'المميزات البارزة',
    fieldNonHanafi: 'العلماء من غير الحنفية (*)',
    fieldHeader: 'عنوان اللوحة والإطار',
    fieldLegend: 'دليل الألوان وصندوق الكتب',
    fieldCenturyBands: 'أشرطة القرون والخط الزمني',
    allRegions: 'جميع الأقاليم',
    allTabakat: 'جميع الطبقات',
    centuryRange: 'نطاق القرون',
    focusTitle: 'التركيز على عالم محدد',
    focusOff: 'السلسلة الكاملة',
    focusHighlight: 'تمييز داخل اللوحة',
    focusIsolate: 'عزل هذا العالم فقط',
    dirBoth: 'الشيوخ والتلاميذ معاً',
    dirAncestors: 'الشيوخ فقط (السابقون)',
    dirDescendants: 'التلاميذ فقط (اللاحقون)',
    teachers: 'الشيوخ',
    students: 'التلاميذ',
    works: 'أشهر المؤلفات',
    roles: 'المناصب والألقاب',
    tags: 'المميزات البارزة',
    notes: 'نبذة علمية',
    editScholar: 'تعديل العالم',
    addStudentTo: 'إضافة تلميذ لهذا العالم',
    deleteScholar: 'حذف العالم',
    clearFocus: 'إلغاء التركيز',
    nonHanafiNote: '* العلماء من غير السادة الحنفية المذكورون في السلسلة لفائدتهم العلمية',
    statsScholars: 'عالم',
    statsEdges: 'صلة',
    statsCenturies: 'قرن',
    bookActiveHint: 'يتم تمييز مؤلف الكتاب وشراحه',
    clearBook: 'إلغاء تمييز الكتاب',
  },
};

function toArabicDigits(num) {
  if (num === null || num === undefined || num === '') return '';
  return String(num).replace(/\d/g, (d) => '٠١٢٣٤٥٦٧٨٩'[Number(d)]);
}

function hijriToMiladiApprox(h) {
  if (!h || Number.isNaN(Number(h))) return null;
  return Math.round(Number(h) * 0.970224 + 621.57);
}

function getHijriCentury(deathH) {
  if (!deathH || Number(deathH) <= 100) return 1;
  return Math.ceil(Number(deathH) / 100);
}


// ===== src/data/literature.js =====
// Classical Hanafi Literature Reference (from the uploaded PDF sidebar, made interactive!)

const LITERATURE_GROUPS = [
  {
    id: 'zahir-rivaye',
    titleTr: 'Zâhirü’r-Rivâye (İmam Muhammed)',
    titleAr: 'ظاهر الرواية (محمد الشيباني ١٨٩)',
    items: [
      { id: 'el-asl', nameTr: 'el-Asl (el-Mebsût)', nameAr: 'الأصل', authorId: 'muhammed', relatedIds: ['hakim-sehid', 'serahsi'] },
      { id: 'camius-sagir', nameTr: 'el-Câmiu’s-Sağîr', nameAr: 'الجامع الصغير', authorId: 'muhammed', relatedIds: ['kadihan', 'serahsi', 'sadrussehid'] },
      { id: 'camiul-kebir', nameTr: 'el-Câmiu’l-Kebîr', nameAr: 'الجامع الكبير', authorId: 'muhammed', relatedIds: ['hasiri', 'serahsi', 'cessas'] },
      { id: 'siyerul-kebir', nameTr: 'es-Siyerü’l-Kebîr', nameAr: 'السير الكبير', authorId: 'muhammed', relatedIds: ['serahsi'] },
      { id: 'ez-ziyadat', nameTr: 'ez-Ziyâdât', nameAr: 'الزيادات', authorId: 'muhammed', relatedIds: ['kadihan', 'serahsi'] },
    ],
  },
  {
    id: 'nadir-rivaye',
    titleTr: 'Nâdirü’r-Rivâye',
    titleAr: 'نادر الرواية',
    items: [
      { id: 'nevadir-muhammed', nameTr: 'Harûniyyât, Cürcâniyyât, Keysâniyyât, Rakkıyyât', nameAr: 'هارونيات، جرجانيات، كيسانيات، رقيات', authorId: 'muhammed', relatedIds: ['ebu-suleyman-cuzcani', 'ibn-semaa'] },
      { id: 'kitabul-kesb', nameTr: 'Kitâbü’l-Kesb, el-Âsâr, el-Hucce, el-Muvatta', nameAr: 'كتاب الكسب، الآثار، الحجة، الموطأ', authorId: 'muhammed', relatedIds: ['malik', 'serahsi'] },
      { id: 'ebu-yusuf-works', nameTr: 'el-Emâlî, el-Harâc, İhtilâfu Ebî Hanîfe, er-Red alâ Siyeri’l-Evzâî', nameAr: 'الأمالي، الخراج، اختلاف أبي حنيفة، الرد على سير الأوزاعي', authorId: 'ebu-yusuf', relatedIds: ['ibn-ebi-leyla', 'ebu-hanife'] },
    ],
  },
  {
    id: 'muhtasarlar',
    titleTr: 'Muhtasarlar',
    titleAr: 'المختصرات',
    items: [
      { id: 'muhtasar-tahavi', nameTr: 'Muhtasaru’t-Tahâvî (321)', nameAr: 'مختصر الطحاوي (٣٢١)', authorId: 'tahavi', relatedIds: ['cessas', 'isbicabi'] },
      { id: 'el-kafi', nameTr: 'el-Kâfî — Hâkim eş-Şehîd (334)', nameAr: 'المختصر الكافي — الحاكم الشهيد (٣٣٤)', authorId: 'hakim-sehid', relatedIds: ['serahsi'] },
      { id: 'muhtasar-kerhi', nameTr: 'Muhtasaru’l-Kerhî (340)', nameAr: 'مختصر الكرخي (٣٤٠)', authorId: 'kerhi', relatedIds: ['kuduri', 'cessas'] },
      { id: 'muhtasar-kuduri', nameTr: 'Muhtasaru’l-Kudûrî (428)', nameAr: 'مختصر القدوري (٤٢٨)', authorId: 'kuduri', relatedIds: ['merginani', 'meydani', 'akta'] },
    ],
  },
  {
    id: 'kutub-esasiyye',
    titleTr: 'Kütüb-i Esâsiyye (Temel Eserler)',
    titleAr: 'الكتب الأساسية',
    items: [
      { id: 'el-mebsut', nameTr: 'el-Mebsût — Serahsî (483)', nameAr: 'المبسوط — السرخسي (٤٨٣)', authorId: 'serahsi', relatedIds: ['hakim-sehid', 'muhammed'] },
      { id: 'bedaius-sanai', nameTr: 'Bedâiu’s-Sanâi‘ — Kâsânî (587)', nameAr: 'بدائع الصنائع — الكاساني (٥٨٧)', authorId: 'kasani', relatedIds: ['alaeddin-semerkandi'] },
      { id: 'el-hidaye', nameTr: 'el-Hidâye — Mergînânî (593)', nameAr: 'الهداية — المرغيناني (٥٩٣)', authorId: 'merginani', relatedIds: ['signaki', 'kaki', 'itkani', 'baberti', 'ayni', 'ibn-humam', 'ibn-kemal', 'kadizade'] },
    ],
  },
  {
    id: 'mutun-erbaa',
    titleTr: 'Mütûn-ı Erbaa (Dört Temel Metin)',
    titleAr: 'المتون الأربعة',
    items: [
      { id: 'el-muhtar', nameTr: 'el-Muhtâr — Mevsılî (683)', nameAr: 'المختار — عبد الله الموصلي (٦٨٣)', authorId: 'mevsili', relatedIds: ['hasiri'] },
      { id: 'mecmaul-bahreyn', nameTr: 'Mecmau’l-Bahreyn — İbnü’s-Sââtî (694)', nameAr: 'مجمع البحرين — ابن الساعاتي (٦٩٤)', authorId: 'ibn-saati', relatedIds: ['ayni', 'ibn-melek'] },
      { id: 'kenzud-dekaik', nameTr: 'Kenzü’d-Dekâik — Nesefî (710)', nameAr: 'كنز الدقائق — أبو البركات النسفي (٧١٠)', authorId: 'ebul-berekat-nesefi', relatedIds: ['ayni', 'zeynuddin-ibn-nuceym', 'ibn-selebi', 'siraceddin-ibn-nuceym'] },
      { id: 'vikayetur-rivaye', nameTr: 'Vikâyetü’r-Rivâye — Tâcüşşerîa (709)', nameAr: 'وقاية الرواية — تاج الشريعة (٧٠٩)', authorId: 'tacusseria', relatedIds: ['sadrusseria-sani', 'burhanusseria', 'sadrusseria-evvel'] },
    ],
  },
];


// ===== src/data/scholars.js =====
// Digitized & enriched dataset from "سلسلة فقهاء الحنفية" (PDF)
// Every scholar carries bilingual names, Hijri/Miladi death dates, region (havza),
// Ibn Kemal Tabaka tier, teacher links, roles (görevler), famous works, tags, and brief bio.

const INITIAL_SCHOLARS = [
  // ==================== 1. HİCRÎ YÜZYIL (1–100) ====================
  {
    id: 'muhammad',
    nameAr: 'محمد مصطفى ﷺ',
    nameTr: 'Hz. Muhammed Mustafa (s.a.v.)',
    deathH: 11,
    region: 'root',
    tabaka: 0,
    teachers: [],
    rolesTr: ['Hâtemü’l-Enbiyâ'],
    rolesAr: ['خاتم الأنبياء ﷺ'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Nübüvvet Kaynağı'],
    tagsAr: ['مصدر التشريع'],
    bioTr: 'İslam hukukunun ve tüm fıkıh silsilelerinin nübüvvet kaynağı.',
    bioAr: 'المصدر الأول للتشريع الإسلامي وسند جميع سلاسل الفقهاء.',
  },
  {
    id: 'omer',
    nameAr: 'عمر بن الخطاب',
    nameTr: 'Hz. Ömer b. Hattâb',
    deathH: 23,
    region: 'medine',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['2. Halife', 'Emîrü’l-Mü’minîn'],
    rolesAr: ['ثاني الخلفاء الراشدين'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Sahâbî Fakih'],
    tagsAr: ['فقيه الصحابة'],
    bioTr: 'Re’y ve maslahat merkezli fıkıh geleneğinin en önemli sahabi dayanaklarından.',
    bioAr: 'من أبرز فقهاء الصحابة وأصول مدرسة الرأي.',
  },
  {
    id: 'ibn-mesud',
    nameAr: 'عبد الله بن مسعود',
    nameTr: 'Abdullah b. Mes‘ûd',
    deathH: 32,
    region: 'kufe',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['Kûfe Muallimi ve Kadısı'],
    rolesAr: ['معلم الكوفة وقاضيها'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kûfe Ekolü Kurucusu'],
    tagsAr: ['مؤسس مدرسة الكوفة'],
    bioTr: 'Hz. Ömer tarafından Kûfe’ye gönderilen ve Hanefî fıkhının ana silsilesini oluşturan sahabi.',
    bioAr: 'مؤسس المدرسة الفقهية بالكوفة والمرجع الأول لأهل العراق.',
  },
  {
    id: 'osman',
    nameAr: 'عثمان بن عفان',
    nameTr: 'Hz. Osman b. Affân',
    deathH: 35,
    region: 'medine',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['3. Halife'],
    rolesAr: ['ثالث الخلفاء الراشدين'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Sahâbî Fakih'],
    tagsAr: ['فقيه الصحابة'],
    bioTr: 'Kıraat ve fıkıh isnadında önemli yer tutan sahabi.',
    bioAr: 'من كبار فقهاء الصحابة وأهل القراءة.',
  },
  {
    id: 'ali',
    nameAr: 'علي بن أبي طالب',
    nameTr: 'Hz. Ali b. Ebî Tâlib',
    deathH: 40,
    region: 'kufe',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['4. Halife', 'Akdâ’s-Sahâbe'],
    rolesAr: ['رابع الخلفاء الراشدين'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kûfe Ekolü', 'Kazâ Otoritesi'],
    tagsAr: ['أقضى الصحابة'],
    bioTr: 'Kûfe’yi hilafet merkezi yaparak Irak fıkıh havzasına derin etki eden sahabi.',
    bioAr: 'أقضى الصحابة ومن أبرز مصادر فقه أهل الكوفة.',
  },
  {
    id: 'zeyd',
    nameAr: 'زيد بن ثابت',
    nameTr: 'Zeyd b. Sâbit',
    deathH: 45,
    region: 'medine',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['Vahiy Kâtibi', 'Medine Müftüsü'],
    rolesAr: ['كاتب الوحي ومفتي المدينة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Ferâiz İmamı'],
    tagsAr: ['أفرض الأمة'],
    bioTr: 'Miras hukuku (ferâiz) ve Medine fıkhının önde gelen sahabisi.',
    bioAr: 'أعلم الصحابة بالفرائض ومن أئمة الفتوى بالمدينة.',
  },
  {
    id: 'aise',
    nameAr: 'عائشة بنت أبي بكر',
    nameTr: 'Hz. Âişe',
    deathH: 58,
    region: 'medine',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['Ümmü’l-Mü’minîn', 'Fakîhe'],
    rolesAr: ['أم المؤمنين'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Müksirûn', 'Sahâbî Fakih'],
    tagsAr: ['من المكثرين والفقهاء'],
    bioTr: 'Fıkıh ve hadis rivayetinde Kûfe ve Medine tabiîninin temel hocalarından.',
    bioAr: 'من أعلم الصحابة بالحديث والفقه، أخذ عنها كبار التابعين.',
  },
  {
    id: 'alkame',
    nameAr: 'علقمة بن قيس',
    nameTr: 'Alkame b. Kays',
    deathH: 62,
    region: 'kufe',
    tabaka: 0,
    teachers: ['ibn-mesud', 'omer'],
    rolesTr: ['Kûfe Fakihi'],
    rolesAr: ['فقيه الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Tâbiîn', 'Ashâb-ı İbn Mes‘ûd'],
    tagsAr: ['من كبار التابعين'],
    bioTr: 'İbn Mes‘ûd’un en seçkin talebesi ve İbrahim en-Nehaî’nin dayısı.',
    bioAr: 'أجل أصحاب ابن مسعود وخال إبراهيم النخعي.',
  },
  {
    id: 'mesruk',
    nameAr: 'مسروق بن الأجدع',
    nameTr: 'Mesrûk b. Ecda‘',
    deathH: 63,
    region: 'kufe',
    tabaka: 0,
    teachers: ['ibn-mesud', 'aise', 'omer'],
    rolesTr: ['Kûfe Müftüsü'],
    rolesAr: ['مفتي الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Tâbiîn', 'Ashâb-ı İbn Mes‘ûd'],
    tagsAr: ['من كبار التابعين'],
    bioTr: 'İbn Mes‘ûd ve Hz. Âişe’nin önde gelen talebesi.',
    bioAr: 'من كبار أصحاب ابن مسعود وعائشة رضي الله عنهما.',
  },
  {
    id: 'ibn-abbas',
    nameAr: 'عبد الله بن عباس',
    nameTr: 'Abdullah b. Abbâs',
    deathH: 68,
    region: 'mekke',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['Tercümânü’l-Kur’ân'],
    rolesAr: ['حبر الأمة وترجمان القرآن'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Mekke Ekolü Kurucusu'],
    tagsAr: ['مؤسس مدرسة مكة'],
    bioTr: 'Mekke tefsir ve fıkıh okulunun kurucu sahabisi.',
    bioAr: 'مؤسس مدرسة مكة في التفسير والفقه.',
  },
  {
    id: 'ubeyde',
    nameAr: 'عبيدة السلماني',
    nameTr: 'Ubeyde es-Selmânî',
    deathH: 72,
    region: 'kufe',
    tabaka: 0,
    teachers: ['ali', 'ibn-mesud'],
    rolesTr: ['Kûfe Fakihi'],
    rolesAr: ['فقيه الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Muhadram', 'Tâbiîn'],
    tagsAr: ['مخضرم'],
    bioTr: 'Hz. Ali ve İbn Mes‘ûd’un fıkhını nakleden büyük tabiî.',
    bioAr: 'من كبار فقهاء التابعين بالكوفة، لازم علياً وابن مسعود.',
  },
  {
    id: 'ibn-omer',
    nameAr: 'عبد الله بن عمر',
    nameTr: 'Abdullah b. Ömer',
    deathH: 73,
    region: 'medine',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['Medine Fakihi'],
    rolesAr: ['فقيه المدينة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Müksirûn', 'Medine Ekolü'],
    tagsAr: ['من المكثرين'],
    bioTr: 'Sünnete ittibası ve Medine fıkhındaki merkezi rolüyle tanınan sahabi.',
    bioAr: 'من أئمة الحديث والفقه بالمدينة المنورة.',
  },
  {
    id: 'sulemi',
    nameAr: 'أبو عبد الرحمن السلمي',
    nameTr: 'Ebû Abdurrahman es-Sülemî',
    deathH: 73,
    region: 'kufe',
    tabaka: 0,
    teachers: ['osman', 'zeyd', 'ali'],
    rolesTr: ['Kûfe Baş Mukrii'],
    rolesAr: ['مقرئ الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kıraat Silsilesi'],
    tagsAr: ['سند القراءة'],
    bioTr: 'Kûfe’de kırk yıl Kur’an ve fıkıh okutan büyük tabiî.',
    bioAr: 'مقرئ الكوفة ومحدثها، أخذ عن عثمان وعلي وزيد.',
  },
  {
    id: 'esved',
    nameAr: 'أسود بن يزيد',
    nameTr: 'Esved b. Yezîd en-Nehaî',
    deathH: 75,
    region: 'kufe',
    tabaka: 0,
    teachers: ['ibn-mesud', 'aise'],
    rolesTr: ['Kûfe Fakihi'],
    rolesAr: ['فقيه الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Tâbiîn', 'Ashâb-ı İbn Mes‘ûd'],
    tagsAr: ['من أصحاب ابن مسعود'],
    bioTr: 'İbrahim en-Nehaî’nin dayısı ve Kûfe fıkhının aktarıcılarından.',
    bioAr: 'من كبار أصحاب ابن مسعود وعائشة ومن شيوخ النخعي.',
  },
  {
    id: 'sureyh',
    nameAr: 'قاضي شريح',
    nameTr: 'Kâdı Şüreyh',
    deathH: 80,
    region: 'kufe',
    tabaka: 0,
    teachers: ['omer', 'ali', 'ibn-mesud'],
    rolesTr: ['Kûfe Başkadısı (60 yıl)'],
    rolesAr: ['قاضي الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kazâ Öncüsü'],
    tagsAr: ['أشهر قضاة التابعين'],
    bioTr: 'Hz. Ömer tarafından Kûfe kadılığına tayin edilip uzun yıllar hüküm veren büyük fakih.',
    bioAr: 'ولاه عمر قضاء الكوفة، واشتهر بدقته وعدله في القضاء.',
  },
  {
    id: 'enes',
    nameAr: 'أنس بن مالك',
    nameTr: 'Enes b. Mâlik',
    deathH: 93,
    region: 'medine',
    tabaka: 0,
    teachers: ['muhammad'],
    rolesTr: ['Hâdimü’n-Nebî'],
    rolesAr: ['خادم النبي ﷺ'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Müksirûn'],
    tagsAr: ['من المكثرين'],
    bioTr: 'Hz. Peygamber’e on yıl hizmet eden ve çok sayıda hadis rivayet eden sahabi.',
    bioAr: 'خادم رسول الله ﷺ وأحد المكثرين من الرواية.',
  },
  {
    id: 'said-cubeyr',
    nameAr: 'سعيد بن جبير',
    nameTr: 'Saîd b. Cübeyr',
    deathH: 94,
    region: 'mekke',
    tabaka: 0,
    teachers: ['ibn-abbas'],
    rolesTr: ['Mekke ve Kûfe Fakihi'],
    rolesAr: ['فقيه ومفسر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Tâbiîn', 'Mekke Ekolü'],
    tagsAr: ['من كبار تلاميذ ابن عباس'],
    bioTr: 'İbn Abbâs’ın en önde gelen talebesi.',
    bioAr: 'أجل أصحاب ابن عباس في التفسير والفقه.',
  },
  {
    id: 'nehai',
    nameAr: 'إبراهيم النخعي',
    nameTr: 'İbrâhim en-Nehaî',
    deathH: 96,
    region: 'kufe',
    tabaka: 0,
    teachers: ['alkame', 'esved', 'mesruk', 'ubeyde', 'sureyh'],
    rolesTr: ['Irak Fakihi'],
    rolesAr: ['فقيه العراق'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kûfe Ekolü', 'Hanefî Silsilesi'],
    tagsAr: ['سند الفقه الحنفي'],
    bioTr: 'Kûfe fıkhını sistemleştiren, Hammâd b. Ebî Süleyman’ın hocası büyük tabiî.',
    bioAr: 'فقيه العراق الذي جمع فقه أصحاب ابن مسعود ونقله لحماد.',
  },

  // ==================== 2. HİCRÎ YÜZYIL (101–200) ====================
  {
    id: 'sabi',
    nameAr: 'عامر بن شراحيل الشعبي',
    nameTr: 'Âmir eş-Şa‘bî',
    deathH: 104,
    region: 'kufe',
    tabaka: 0,
    teachers: ['mesruk', 'ubeyde', 'sureyh', 'omer'],
    rolesTr: ['Kûfe Kadısı ve Fakihi'],
    rolesAr: ['فقيه ومحدث الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Tâbiîn'],
    tagsAr: ['من أئمة التابعين'],
    bioTr: 'Ebû Hanîfe’yi ilme teşvik eden büyük tabiîn fakihi ve muhaddisi.',
    bioAr: 'من كبار التابعين، وهو الذي أشار على أبي حنيفة بملازمة العلماء.',
  },
  {
    id: 'ata',
    nameAr: 'عطاء بن أبي رباح',
    nameTr: 'Atâ b. Ebî Rebâh',
    deathH: 114,
    region: 'medine',
    tabaka: 0,
    teachers: ['aise', 'ibn-abbas', 'ibn-omer'],
    rolesTr: ['Mekke Müftüsü'],
    rolesAr: ['مفتي مكة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Hicaz Ekolü'],
    tagsAr: ['إمام أهل مكة'],
    bioTr: 'Ebû Hanîfe’nin hac ziyaretlerinde ilim aldığı büyük Hicaz fakihi.',
    bioAr: 'مفتي أهل مكة وأحد شيوخ الإمام أبي حنيفة في الحجاز.',
  },
  {
    id: 'nafi',
    nameAr: 'نافع مولى ابن عمر',
    nameTr: 'Nâfi‘ Mevlâ İbn Ömer',
    deathH: 117,
    region: 'medine',
    tabaka: 0,
    teachers: ['ibn-omer'],
    rolesTr: ['Medine Muhaddisi'],
    rolesAr: ['محدث المدينة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Silsiletü’z-Zeheb'],
    tagsAr: ['سلسلة الذهب'],
    bioTr: 'İbn Ömer’in ilmini İmam Mâlik ve Ebû Hanîfe’ye aktaran muhaddis.',
    bioAr: 'راوية ابن عمر وشيخ الإمام مالك وأبي حنيفة.',
  },
  {
    id: 'hammad',
    nameAr: 'حماد بن أبي سليمان',
    nameTr: 'Hammâd b. Ebî Süleyman',
    deathH: 120,
    region: 'kufe',
    tabaka: 0,
    teachers: ['nehai', 'sabi'],
    rolesTr: ['Kûfe Ders Halkası Reisi'],
    rolesAr: ['رئيس حلقة الفقه بالكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Ebû Hanîfe’nin Baş Hocası'],
    tagsAr: ['شيخ أبي حنيفة'],
    bioTr: 'Ebû Hanîfe’nin on sekiz yıl boyunca ders halkasına devam ettiği baş hocası.',
    bioAr: 'لازمه الإمام أبو حنيفة ثماني عشرة سنة حتى وفاته.',
  },
  {
    id: 'zuhri',
    nameAr: 'ابن شهاب الزهري',
    nameTr: 'İbn Şihâb ez-Zührî',
    deathH: 124,
    region: 'medine',
    tabaka: 0,
    teachers: ['enes', 'ibn-omer'],
    rolesTr: ['Hadis Tedvin Öncüsü'],
    rolesAr: ['أول من دوّن الحديث'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Medine Ekolü', 'Muhaddis'],
    tagsAr: ['إمام المحدثين'],
    bioTr: 'Hadislerin resmî tedvininde öncü rol oynayan büyük tabiî.',
    bioAr: 'من أئمة الحديث والفقه وأول من دون الحديث بأمر عمر بن عبد العزيز.',
  },
  {
    id: 'asim',
    nameAr: 'عاصم بن بهدلة',
    nameTr: 'Âsım b. Behdele',
    deathH: 127,
    region: 'kufe',
    tabaka: 0,
    teachers: ['sulemi'],
    rolesTr: ['Yedi Kıraat İmamından'],
    rolesAr: ['أحد القراء السبعة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kıraat İmamı'],
    tagsAr: ['إمام القراءة'],
    bioTr: 'Kûfe kıraat imamı ve Ebû Hanîfe’nin kıraat hocası.',
    bioAr: 'أحد القراء السبعة، وروى عنه أبو حنيفة.',
  },
  {
    id: 'ames',
    nameAr: 'سليمان الأعمش',
    nameTr: 'Süleyman el-A‘meş',
    deathH: 148,
    region: 'kufe',
    tabaka: 0,
    teachers: ['said-cubeyr', 'nehai'],
    rolesTr: ['Kûfe Muhaddisi'],
    rolesAr: ['محدث الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Muhaddis', 'Kûfe Ekolü'],
    tagsAr: ['شيخ المحدثين بالكوفة'],
    bioTr: 'Kûfe’nin önde gelen hadis ve kıraat otoritesi.',
    bioAr: 'عالم الكوفة بالحديث والقراءة.',
  },
  {
    id: 'ibn-ebi-leyla',
    nameAr: 'محمد بن عبد الرحمن ابن أبي ليلى',
    nameTr: 'İbn Ebî Leylâ',
    deathH: 148,
    region: 'kufe',
    tabaka: 1,
    teachers: ['ames', 'sabi'],
    rolesTr: ['Kûfe Kadısı (33 yıl)'],
    rolesAr: ['قاضي الكوفة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Müctehid', 'Kûfe Ekolü'],
    tagsAr: ['مجتهد وقاضٍ'],
    bioTr: 'Ebû Yûsuf’un ilk hocası ve Ebû Hanîfe’nin çağdaşı meşhur Kûfe kadısı.',
    bioAr: 'قاضي الكوفة وفقيهها، وأول شيوخ القاضي أبي يوسف.',
  },
  {
    id: 'ibn-cureyc',
    nameAr: 'ابن جريج',
    nameTr: 'İbn Cüreyc',
    deathH: 150,
    region: 'medine',
    tabaka: 0,
    teachers: ['ata'],
    rolesTr: ['Mekke Muhaddisi'],
    rolesAr: ['محدث الحرم'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['İlk Musanniflerden'],
    tagsAr: ['أول من صنف بمكة'],
    bioTr: 'Atâ b. Ebî Rebâh’ın en önemli talebesi ve Hicaz’ın ilk musanniflerinden.',
    bioAr: 'أشهر تلاميذ عطاء وأول من صنف الكتب بالحجاز.',
  },
  {
    id: 'ebu-hanife',
    nameAr: 'أبو حنيفة نعمان بن ثابت',
    nameTr: 'İmâm-ı A‘zam Ebû Hanîfe',
    deathH: 150,
    region: 'kufe',
    tabaka: 1,
    teachers: ['hammad', 'ata', 'nafi', 'sabi', 'asim'],
    rolesTr: ['Mezhep İmamı', 'İmâm-ı A‘zam'],
    rolesAr: ['الإمام الأعظم ومؤسس المذهب'],
    worksTr: ['el-Fıkhü’l-Ekber', 'el-Âlim ve’l-Müteallim', 'el-Müsned'],
    worksAr: ['الفقه الأكبر', 'العالم والمتعلم', 'المسند'],
    tagsTr: ['Kurucu İmam', '1. Tabaka'],
    tagsAr: ['مؤسس المذهب الحنفي'],
    bioTr: 'Hanefî mezhebinin kurucusu, şûra usulüyle fıkhı tedvin eden büyük müçtehit.',
    bioAr: 'مؤسس المذهب الحنفي، واضع أصول الاستنباط ومنهج الشورى الفقهية.',
  },
  {
    id: 'zufer',
    nameAr: 'زفر بن الهذيل',
    nameTr: 'İmam Züfer b. Hüzeyl',
    deathH: 158,
    region: 'kufe',
    tabaka: 2,
    teachers: ['ebu-hanife'],
    rolesTr: ['Basra Kadısı'],
    rolesAr: ['قاضي البصرة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kıyas İmamı', '2. Tabaka'],
    tagsAr: ['أقيس أصحاب أبي حنيفة'],
    bioTr: 'Ebû Hanîfe’nin kıyasta en güçlü talebesi.',
    bioAr: 'من أكبر تلاميذ أبي حنيفة وأقيسهم.',
  },
  {
    id: 'ibn-ebi-zib',
    nameAr: 'ابن أبي الذئب',
    nameTr: 'İbn Ebî’z-Zi’b',
    deathH: 159,
    region: 'medine',
    tabaka: 0,
    teachers: ['nafi', 'zuhri'],
    rolesTr: ['Medine Fakihi'],
    rolesAr: ['فقيه المدينة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Medine Ekolü'],
    tagsAr: ['من فقهاء المدينة'],
    bioTr: 'Medine fıkıh ve hadis geleneğinin önemli temsilcilerinden.',
    bioAr: 'من كبار فقهاء المدينة ومحدثيها.',
  },
  {
    id: 'sufyan-sevri',
    nameAr: 'سفيان الثوري',
    nameTr: 'Süfyân es-Sevrî',
    deathH: 161,
    region: 'kufe',
    tabaka: 1,
    teachers: ['ames', 'hammad', 'ebu-hanife'],
    rolesTr: ['Emîrü’l-Mü’minîn fi’l-Hadîs'],
    rolesAr: ['أمير المؤمنين في الحديث'],
    worksTr: ['el-Câmiu’l-Kebîr', 'Tefsîr'],
    worksAr: ['الجامع الكبير', 'التفسير'],
    tagsTr: ['Müctehid', 'Kûfe Ekolü'],
    tagsAr: ['إمام مجتهد'],
    bioTr: 'Kûfe’nin büyük hadis ve fıkıh imamı.',
    bioAr: 'إمام أهل العراق في الحديث والفقه والزهد.',
  },
  {
    id: 'malik',
    nameAr: 'مالك بن أنس',
    nameTr: 'İmam Mâlik b. Enes',
    deathH: 179,
    region: 'medine',
    tabaka: 1,
    nonHanafi: true,
    teachers: ['nafi', 'zuhri'],
    rolesTr: ['Dârülhicre İmamı'],
    rolesAr: ['إمام دار الهجرة'],
    worksTr: ['el-Muvatta'],
    worksAr: ['الموطأ'],
    tagsTr: ['Mâlikî Mezhebi İmamı'],
    tagsAr: ['مؤسس المذهب المالكي'],
    bioTr: 'Mâlikî mezhebinin kurucusu; İmam Muhammed kendisinden el-Muvatta’ı rivayet etmiştir.',
    bioAr: 'إمام دار الهجرة، روى عنه الإمام محمد بن الحسن الموطأ.',
  },
  {
    id: 'ibn-mubarek',
    nameAr: 'عبد الله بن المبارك',
    nameTr: 'Abdullah b. Mübârek',
    deathH: 181,
    region: 'horasan',
    tabaka: 2,
    teachers: ['ebu-hanife', 'sufyan-sevri', 'malik'],
    rolesTr: ['Horasan İmamı', 'Muhaddis'],
    rolesAr: ['شيخ الإسلام وإمام خراسان'],
    worksTr: ['Kitâbü’z-Zühd', 'Kitâbü’l-Cihâd'],
    worksAr: ['الزهد والرقائق', 'الجهاد'],
    tagsTr: ['Muhaddis', 'Horasan Öncüsü'],
    tagsAr: ['محدث وفقيه'],
    bioTr: 'Ebû Hanîfe’nin hadis ve zühdde zirve olan Horasanlı büyük talebesi.',
    bioAr: 'أحد كبار أصحاب أبي حنيفة، جمع بين الفقه والحديث والزهد.',
  },
  {
    id: 'ebu-yusuf',
    nameAr: 'أبو يوسف يعقوب بن إبراهيم',
    nameTr: 'İmam Ebû Yûsuf',
    deathH: 182,
    region: 'kufe',
    tabaka: 2,
    teachers: ['ebu-hanife', 'ibn-ebi-leyla'],
    rolesTr: ['İlk Kâdılkudât (Başkadı)'],
    rolesAr: ['أول قاضي القضاة في الإسلام'],
    worksTr: ['Kitâbü’l-Harâc', 'el-Âsâr', 'İhtilâfu Ebî Hanîfe'],
    worksAr: ['كتاب الخراج', 'الآثار', 'اختلاف أبي حنيفة'],
    tagsTr: ['İmâmeyn', 'Nâdirü’r-Rivâye'],
    tagsAr: ['الصاحبان', 'نادر الرواية'],
    bioTr: 'Abbâsî Devleti’nin ilk Kâdılkudâtı; Hanefî mezhebinin yargı yoluyla yayılmasını sağlayan imam.',
    bioAr: 'صاحب أبي حنيفة وأول قاضي قضاة، أسهم في انتشار المذهب الحنفي.',
  },
  {
    id: 'muhammed',
    nameAr: 'محمد بن الحسن الشيباني',
    nameTr: 'İmam Muhammed eş-Şeybânî',
    deathH: 189,
    region: 'kufe',
    tabaka: 2,
    teachers: ['ebu-hanife', 'ebu-yusuf', 'malik', 'sufyan-sevri'],
    rolesTr: ['Rakka ve Rey Kadısı', 'Mezhep Müdevvini'],
    rolesAr: ['مدوّن المذهب الحنفي'],
    worksTr: ['el-Asl', 'el-Câmiu’s-Sağîr', 'el-Câmiu’l-Kebîr', 'es-Siyerü’l-Kebîr', 'ez-Ziyâdât'],
    worksAr: ['الأصل', 'الجامع الصغير', 'الجامع الكبير', 'السير الكبير', 'الزيادات'],
    tagsTr: ['İmâmeyn', 'Zâhirü’r-Rivâye Müellifi'],
    tagsAr: ['مؤلف ظاهر الرواية'],
    bioTr: 'Hanefî mezhebinin ana kaynağı olan Zâhirü’r-rivâye eserlerini kaleme alan büyük müçtehit.',
    bioAr: 'مدون المذهب الحنفي ومؤلف كتب ظاهر الرواية الستة.',
  },
  {
    id: 'veki',
    nameAr: 'وكيع بن جراح',
    nameTr: 'Vekî‘ b. Cerrâh',
    deathH: 197,
    region: 'kufe',
    tabaka: 2,
    teachers: ['ibn-ebi-leyla', 'sufyan-sevri', 'ebu-hanife'],
    rolesTr: ['Kûfe Muhaddisi'],
    rolesAr: ['محدث العراق'],
    worksTr: ['ez-Zühd'],
    worksAr: ['الزهد'],
    tagsTr: ['Muhaddis'],
    tagsAr: ['حافظ ومحدث'],
    bioTr: 'Ebû Hanîfe’nin görüşleriyle fetva veren büyük hadis hafızı.',
    bioAr: 'حافظ العراق ومحدثه، وكان يفتي بقول أبي حنيفة.',
  },
  {
    id: 'ebu-suleyman-cuzcani',
    nameAr: 'أبو سليمان الجوزجاني',
    nameTr: 'Ebû Süleyman el-Cüzcânî',
    deathH: 200,
    region: 'horasan',
    tabaka: 3,
    teachers: ['muhammed', 'ebu-yusuf'],
    rolesTr: ['Zâhirü’r-Rivâye Râvisi'],
    rolesAr: ['راوية كتب محمد الشيباني'],
    worksTr: ['Nevâdirü’l-Fetâvâ'],
    worksAr: ['نوادر الفتاوى'],
    tagsTr: ['Horasan Silsilesi'],
    tagsAr: ['سند خراسان وما وراء النهر'],
    bioTr: 'İmam Muhammed’in kitaplarını Horasan ve Mâverâünnehir’e taşıyan temel halka.',
    bioAr: 'أبرز رواة كتب محمد بن الحسن وناقلها إلى خراسان وما وراء النهر.',
  },

  // ==================== 3. HİCRÎ YÜZYIL (201–300) ====================
  {
    id: 'hasan-ziyad',
    nameAr: 'الحسن بن زياد اللؤلؤي',
    nameTr: 'Hasan b. Ziyâd el-Lü’lüî',
    deathH: 204,
    region: 'kufe',
    tabaka: 2,
    teachers: ['ebu-hanife', 'ebu-yusuf', 'zufer'],
    rolesTr: ['Kûfe Kadısı'],
    rolesAr: ['قاضي الكوفة'],
    worksTr: ['Edebü’l-Kâdî', 'el-Mücerred'],
    worksAr: ['أدب القاضي', 'المجرد'],
    tagsTr: ['Ashâbü’l-İmam'],
    tagsAr: ['من كبار أصحاب أبي حنيفة'],
    bioTr: 'Ebû Hanîfe’nin kıdemli talebelerinden ve el-Mücerred müellifi.',
    bioAr: 'من كبار أصحاب أبي حنيفة، ومؤلف كتاب المجرد.',
  },
  {
    id: 'tayalisi',
    nameAr: 'أبو داود الطيالسي',
    nameTr: 'Ebû Dâvûd et-Tayâlisî',
    deathH: 204,
    region: 'kufe',
    tabaka: 0,
    teachers: ['sufyan-sevri'],
    rolesTr: ['Muhaddis'],
    rolesAr: ['محدث البصرة'],
    worksTr: ['el-Müsned'],
    worksAr: ['المسند'],
    tagsTr: ['Muhaddis'],
    tagsAr: ['حافظ'],
    bioTr: 'İlk müsned müelliflerinden büyük hadis alimi.',
    bioAr: 'من أوائل من صنف المسند في الحديث.',
  },
  {
    id: 'vakidi',
    nameAr: 'الواقدي',
    nameTr: 'el-Vâkıdî',
    deathH: 207,
    region: 'medine',
    tabaka: 0,
    teachers: ['ibn-cureyc', 'ibn-ebi-zib', 'malik'],
    rolesTr: ['Bağdat Kadısı', 'Tarihçi'],
    rolesAr: ['قاضي بغداد ومؤرخ'],
    worksTr: ['el-Meğâzî'],
    worksAr: ['المغازي'],
    tagsTr: ['Siyer / Tarih'],
    tagsAr: ['مؤرخ المغازي'],
    bioTr: 'Medine ilmini Bağdat’a taşıyan tarihçi ve kadı.',
    bioAr: 'مؤرخ وقاضٍ روى عن شيوخ المدينة.',
  },
  {
    id: 'ebu-hafs-kebir',
    nameAr: 'أبو حفص الكبير البخاري',
    nameTr: 'Ebû Hafs el-Kebîr el-Buhârî',
    deathH: 217,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['muhammed'],
    rolesTr: ['Buhara Şeyhülislamı'],
    rolesAr: ['فقيه بخارى وإمامها'],
    worksTr: ['el-Ehvâ ve’l-İhtilâf'],
    worksAr: ['الأهواء والاختلاف'],
    tagsTr: ['Buhara Ekolü Kurucusu'],
    tagsAr: ['مؤسس مدرسة بخارى'],
    bioTr: 'Hanefî fıkhını Buhara ve Mâverâünnehir’e yerleştiren kurucu imam.',
    bioAr: 'ناشر المذهب الحنفي في بخارى وما وراء النهر.',
  },
  {
    id: 'isa-eban',
    nameAr: 'عيسى بن أبان',
    nameTr: 'Îsâ b. Ebân',
    deathH: 221,
    region: 'kufe',
    tabaka: 3,
    teachers: ['muhammed'],
    rolesTr: ['Basra Kadısı'],
    rolesAr: ['قاضي البصرة'],
    worksTr: ['Hucetü’s-Sağîr', 'Haberü’l-Vâhid'],
    worksAr: ['الحجج الصغير', 'خبر الواحد'],
    tagsTr: ['Usul Öncüsü'],
    tagsAr: ['من أوائل الأصوليين'],
    bioTr: 'Hanefî fıkıh usulünün erken dönem kurucu isimlerinden.',
    bioAr: 'من أبرز مؤسسي أصول الفقه الحنفي وتلاميذ محمد الشيباني.',
  },
  {
    id: 'kanebi',
    nameAr: 'أبو عبد الرحمن القعنبي',
    nameTr: 'Ebû Abdurrahman el-Ka‘nebî',
    deathH: 221,
    region: 'medine',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['malik'],
    rolesTr: ['Muhaddis'],
    rolesAr: ['راوية الموطأ'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Muvatta Râvisi'],
    tagsAr: ['أثبت رواة الموطأ'],
    bioTr: 'İmam Mâlik’in en güvenilir Muvatta râvisi.',
    bioAr: 'من أثبت رواة الموطأ عن الإمام مالك.',
  },
  {
    id: 'omer-muheyr',
    nameAr: 'عمر بن مهير',
    nameTr: 'Ömer b. Müheyr',
    deathH: 230,
    region: 'kufe',
    tabaka: 3,
    teachers: ['hasan-ziyad'],
    rolesTr: ['Irak Fakihi'],
    rolesAr: ['فقيه عراقي'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Hassâf’ın Babası'],
    tagsAr: ['والد الخصاف'],
    bioTr: 'Hassâf’ın babası ve Hasan b. Ziyâd’ın talebesi.',
    bioAr: 'والد الإمام الخصاف وتلميذ الحسن بن زياد.',
  },
  {
    id: 'ibn-semaa',
    nameAr: 'محمد بن سماعة',
    nameTr: 'Muhammed b. Semâa',
    deathH: 233,
    region: 'kufe',
    tabaka: 3,
    teachers: ['ebu-yusuf', 'muhammed'],
    rolesTr: ['Bağdat Kadısı'],
    rolesAr: ['قاضي بغداد'],
    worksTr: ['Nevâdir', 'Edebü’l-Kâdî'],
    worksAr: ['النوادر', 'أدب القاضي'],
    tagsTr: ['Nâdirü’r-Rivâye Râvisi'],
    tagsAr: ['راوي النوادر'],
    bioTr: 'Ebû Yûsuf ve İmam Muhammed’in önde gelen talebesi ve Bağdat kadısı.',
    bioAr: 'قاضي بغداد وراوية النوادر عن أبي يوسف ومحمد.',
  },
  {
    id: 'yahya-main',
    nameAr: 'يحيى بن معين',
    nameTr: 'Yahyâ b. Maîn',
    deathH: 233,
    region: 'kufe',
    tabaka: 0,
    teachers: ['veki', 'ibn-mubarek'],
    rolesTr: ['Cerh ve Ta‘dîl İmamı'],
    rolesAr: ['إمام الجرح والتعديل'],
    worksTr: ['et-Târîh'],
    worksAr: ['التاريخ'],
    tagsTr: ['Muhaddis'],
    tagsAr: ['إمام الرجال'],
    bioTr: 'Hadis ricâli ilminin zirve ismi; Hanefî fıkhına muhabbetiyle bilinir.',
    bioAr: 'إمام الجرح والتعديل في عصره.',
  },
  {
    id: 'ibn-rahuye',
    nameAr: 'إسحاق بن راهويه',
    nameTr: 'İshak b. Râhûye',
    deathH: 238,
    region: 'horasan',
    tabaka: 0,
    teachers: ['ibn-mubarek', 'veki'],
    rolesTr: ['Horasan Muhaddisi'],
    rolesAr: ['إمام خراسان في الحديث'],
    worksTr: ['el-Müsned'],
    worksAr: ['المسند'],
    tagsTr: ['Muhaddis'],
    tagsAr: ['حافظ ومجتهد'],
    bioTr: 'Horasan hadis ve fıkıh okulunun büyük imamı.',
    bioAr: 'إمام أهل خراسان في الحديث والفقه.',
  },
  {
    id: 'hassaf',
    nameAr: 'أبو بكر الخصاف',
    nameTr: 'Ebû Bekr el-Hassâf',
    deathH: 261,
    region: 'kufe',
    tabaka: 3,
    teachers: ['omer-muheyr', 'tayalisi'],
    rolesTr: ['Vakıf ve Kazâ Hukukçusu'],
    rolesAr: ['فقيه الأوقاف والقضاء'],
    worksTr: ['Ahkâmü’l-Evkâf', 'Edebü’l-Kâdî', 'el-Hiyel'],
    worksAr: ['أحكام الأوقاف', 'أدب القاضي', 'الحيل'],
    tagsTr: ['3. Tabaka', 'Vakıf Hukuku'],
    tagsAr: ['الطبقة الثالثة'],
    bioTr: 'İslam vakıf hukuku ve yargılama usulünün en temel klasik eserlerinin müellifi.',
    bioAr: 'من أئمة الطبقة الثالثة وصاحب أدب القاضي وأحكام الأوقاف.',
  },
  {
    id: 'musa-razi',
    nameAr: 'موسى بن نصر الرازي',
    nameTr: 'Mûsâ b. Nasr er-Râzî',
    deathH: 263,
    region: 'kufe',
    tabaka: 3,
    teachers: ['muhammed'],
    rolesTr: ['Rey Fakihi'],
    rolesAr: ['فقيه الري'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Irak-Rey Halkası'],
    tagsAr: ['تلميذ الشيباني'],
    bioTr: 'İmam Muhammed’in talebesi ve Ebû Ali ed-Dakkâk’ın hocası.',
    bioAr: 'من تلاميذ محمد بن الحسن وشيخ أبي علي الدقاق.',
  },
  {
    id: 'ebu-hafs-sagir',
    nameAr: 'أبو حفص الصغير',
    nameTr: 'Ebû Hafs es-Sağîr',
    deathH: 264,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['ebu-hafs-kebir'],
    rolesTr: ['Buhara Fakihi'],
    rolesAr: ['فقيه بخارى'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Buhara Ekolü'],
    tagsAr: ['مدرسة بخارى'],
    bioTr: 'Ebû Hafs el-Kebîr’in oğlu ve Buhara Hanefî ekolünün ikinci nesil lideri.',
    bioAr: 'ابن أبي حفص الكبير ومواصل مسيرة مدرسة بخارى.',
  },
  {
    id: 'ibn-sucaa',
    nameAr: 'محمد بن شجاع الثلجي',
    nameTr: 'İbn Şücâ‘ es-Selcî',
    deathH: 266,
    region: 'kufe',
    tabaka: 3,
    teachers: ['hasan-ziyad', 'muhammed'],
    rolesTr: ['Irak Fakihi'],
    rolesAr: ['فقيه العراق'],
    worksTr: ['Tashîhu’l-Âsâr'],
    worksAr: ['تصحيح الآثار'],
    tagsTr: ['Irak Ekolü'],
    tagsAr: ['فقيه ومصنف'],
    bioTr: 'Bağdat Hanefîlerinin önemli fakih ve musanniflerinden.',
    bioAr: 'من كبار فقهاء الحنفية ببغداد.',
  },
  {
    id: 'bekr-ammi',
    nameAr: 'بكر بن محمد العمي',
    nameTr: 'Bekr b. Muhammed el-Ammî',
    deathH: 265,
    region: 'kufe',
    tabaka: 3,
    teachers: ['ibn-semaa'],
    rolesTr: ['Basra Fakihi'],
    rolesAr: ['فقيه بصري'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Irak Ekolü'],
    tagsAr: ['حلقة العراق'],
    bioTr: 'İbn Semâa’nın talebesi ve Ebû Hâzım’ın hocası.',
    bioAr: 'تلميذ ابن سماعة وشيخ القاضي أبي حازم.',
  },
  {
    id: 'nusayr-belhi',
    nameAr: 'نصير بن يحيى البلخي',
    nameTr: 'Nusayr b. Yahyâ el-Belhî',
    deathH: 268,
    region: 'horasan',
    tabaka: 3,
    teachers: ['ebu-suleyman-cuzcani'],
    rolesTr: ['Belh Fakihi'],
    rolesAr: ['فقيه بلخ'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Belh Ekolü'],
    tagsAr: ['مدرسة بلخ'],
    bioTr: 'Belh Hanefî okulunun kurucu halkalarından ve Mâtürîdî’nin hocalarından.',
    bioAr: 'من أئمة مدرسة بلخ ومن شيوخ الإمام الماتريدي.',
  },
  {
    id: 'ebu-bekr-cuzcani',
    nameAr: 'أبو بكر الجوزجاني',
    nameTr: 'Ebû Bekr el-Cüzcânî',
    deathH: 275,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['ebu-suleyman-cuzcani'],
    rolesTr: ['Semerkant/Horasan Fakihi'],
    rolesAr: ['فقيه خراسان وما وراء النهر'],
    worksTr: ['el-Fark ve’t-Temyîz'],
    worksAr: ['الفرق والتمييز'],
    tagsTr: ['Mâtürîdî’nin Hocası'],
    tagsAr: ['شيخ الماتريدي'],
    bioTr: 'İmam Mâtürîdî ve Ebû Nasr el-İyâzî’nin hocası.',
    bioAr: 'تلميذ أبي سليمان الجوزجاني وشيخ الماتريدي والعياضي.',
  },
  {
    id: 'muhammed-seleme',
    nameAr: 'محمد بن سلمة البلخي',
    nameTr: 'Muhammed b. Seleme el-Belhî',
    deathH: 278,
    region: 'horasan',
    tabaka: 3,
    teachers: ['ebu-suleyman-cuzcani'],
    rolesTr: ['Belh Fakihi'],
    rolesAr: ['إمام بلخ'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Belh Ekolü'],
    tagsAr: ['مدرسة بلخ'],
    bioTr: 'Belh fıkıh okulunun önde gelen fakihlerinden.',
    bioAr: 'من أئمة الحنفية ببلخ وشيخ أبي بكر الإسكاف.',
  },
  {
    id: 'ebu-ali-dakkak',
    nameAr: 'أبو علي الدقاق',
    nameTr: 'Ebû Ali ed-Dakkâk',
    deathH: 285,
    region: 'kufe',
    tabaka: 3,
    teachers: ['musa-razi'],
    rolesTr: ['Irak Fakihi'],
    rolesAr: ['فقيه عراقي'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Irak Ekolü'],
    tagsAr: ['حلقة العراق'],
    bioTr: 'Berdeî’nin hocası olan Iraklı Hanefî fakihi.',
    bioAr: 'تلميذ موسى بن نصر الرازي وشيخ البردعي.',
  },
  {
    id: 'ebu-hazim',
    nameAr: 'أبو حازم السكوني',
    nameTr: 'Ebû Hâzım es-Sekûnî',
    deathH: 292,
    region: 'kufe',
    tabaka: 3,
    teachers: ['isa-eban', 'bekr-ammi'],
    rolesTr: ['Bağdat ve Kûfe Kadısı'],
    rolesAr: ['قاضي بغداد والكوفة'],
    worksTr: ['Edebü’l-Kâdî'],
    worksAr: ['أدب القاضي'],
    tagsTr: ['Irak Ekolü', 'Tahâvî ve Kerhî’nin Hocası'],
    tagsAr: ['شيخ الطحاوي والكرخي'],
    bioTr: 'İmam Tahâvî ve Ebü’l-Hasan el-Kerhî’nin hocası olan meşhur başkadı.',
    bioAr: 'قاضي القضاة وشيخ الإمامين الطحاوي والكرخي.',
  },

  // ==================== 4. HİCRÎ YÜZYIL (301–400) ====================
  {
    id: 'hasan-sufyan',
    nameAr: 'الحسن بن سفيان النسوي',
    nameTr: 'Hasan b. Süfyân en-Nesevî',
    deathH: 303,
    region: 'horasan',
    tabaka: 0,
    teachers: ['ibn-rahuye'],
    rolesTr: ['Horasan Muhaddisi'],
    rolesAr: ['محدث خراسان'],
    worksTr: ['el-Müsned'],
    worksAr: ['المسند'],
    tagsTr: ['Muhaddis'],
    tagsAr: ['حافظ خراسان'],
    bioTr: 'Hâkim eş-Şehîd’in hadis hocalarından.',
    bioAr: 'حافظ خراسان ومحدثها، أخذ عنه الحاكم الشهيد.',
  },
  {
    id: 'iyazi',
    nameAr: 'أبو نصر العياضي',
    nameTr: 'Ebû Nasr el-İyâzî',
    deathH: 305,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['ebu-bekr-cuzcani'],
    rolesTr: ['Semerkant Şeyhi'],
    rolesAr: ['شيخ سمرقند'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Semerkant Ekolü'],
    tagsAr: ['مدرسة سمرقند'],
    bioTr: 'Semerkant’ta Dârü’l-Cüzcâniyye’nin reisi ve Mâtürîdî’nin hocası.',
    bioAr: 'رئيس دار الجوزجانية بسمرقند وشيخ الإمام الماتريدي.',
  },
  {
    id: 'berdei',
    nameAr: 'أبو سعيد البردعي',
    nameTr: 'Ebû Saîd el-Berdeî',
    deathH: 317,
    region: 'kufe',
    tabaka: 3,
    teachers: ['ebu-ali-dakkak', 'ebu-hazim'],
    rolesTr: ['Bağdat Hanefî Reisi'],
    rolesAr: ['رئيس الحنفية ببغداد'],
    worksTr: ['Mesâilü’l-Hilâf'],
    worksAr: ['مسائل الخلاف'],
    tagsTr: ['Irak Ekolü'],
    tagsAr: ['شيخ الكرخي'],
    bioTr: 'Kerhî ve Debbâs’ın hocası olan Irak Hanefîlerinin reisi.',
    bioAr: 'إمام الحنفية ببغداد وشيخ الكرخي وأبي طاهر الدباس.',
  },
  {
    id: 'tahavi',
    nameAr: 'أبو جعفر الطحاوي',
    nameTr: 'İmam Ebû Ca‘fer et-Tahâvî',
    deathH: 321,
    region: 'misir',
    tabaka: 3,
    teachers: ['ebu-hazim'],
    rolesTr: ['Mısır Hanefî İmamı'],
    rolesAr: ['إمام الحنفية بمصر'],
    worksTr: ['Muhtasaru’t-Tahâvî', 'el-Akîdetü’t-Tahâviyye', 'Şerhu Meâni’l-Âsâr'],
    worksAr: ['مختصر الطحاوي', 'العقيدة الطحاوية', 'شرح معاني الآثار'],
    tagsTr: ['Muhtasar Müellifi', '3. Tabaka', 'Muhaddis'],
    tagsAr: ['صاحب المختصر', 'الطبقة الثالثة'],
    bioTr: 'Hanefî mezhebinin ilk muhtasarını yazan, hadis ve akaidde otorite büyük imam.',
    bioAr: 'إمام مصر وفقيهها ومحدثها، مؤلف المختصر والعقيدة الطحاوية.',
  },
  {
    id: 'ebu-tahir-debbas',
    nameAr: 'أبو طاهر الدباس',
    nameTr: 'Ebû Tâhir ed-Debbâs',
    deathH: 325,
    region: 'kufe',
    tabaka: 4,
    teachers: ['berdei'],
    rolesTr: ['Mâverâünnehir Fakihi'],
    rolesAr: ['فقيه القواعد'],
    worksTr: ['Kavâidü’l-Fıkh (17 Kaide)'],
    worksAr: ['القواعد السبع عشرة'],
    tagsTr: ['Fıkıh Kaideleri Öncüsü'],
    tagsAr: ['مؤسس القواعد الفقهية'],
    bioTr: 'Hanefî fıkhını on yedi temel kaidede toplayan ilk fakih.',
    bioAr: 'أول من جمع الفقه الحنفي في سبع عشرة قاعدة كلية.',
  },
  {
    id: 'ames-ebu-bekr',
    nameAr: 'أبو بكر الأعمش البلخي',
    nameTr: 'Ebû Bekr el-A‘meş el-Belhî',
    deathH: 328,
    region: 'horasan',
    tabaka: 4,
    teachers: ['muhammed-seleme'],
    rolesTr: ['Belh Fakihi'],
    rolesAr: ['فقيه بلخ'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Belh Ekolü'],
    tagsAr: ['مدرسة بلخ'],
    bioTr: 'Ebû Ca‘fer el-Hinduvânî’nin hocalarından Belhli fakih.',
    bioAr: 'من فقهاء بلخ وشيوخ أبي جعفر الهندواني.',
  },
  {
    id: 'maturidi',
    nameAr: 'أبو منصور الماتريدي',
    nameTr: 'İmam Ebû Mansûr el-Mâtürîdî',
    deathH: 333,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['ebu-bekr-cuzcani', 'iyazi', 'nusayr-belhi'],
    rolesTr: ['İmâmü’l-Hüdâ', 'Kelam ve Usul İmamı'],
    rolesAr: ['إمام الهدى ومؤسس الماتريدية'],
    worksTr: ['Kitâbü’t-Tevhîd', 'Te’vîlâtü’l-Kur’ân'],
    worksAr: ['كتاب التوحيد', 'تأويلات القرآن'],
    tagsTr: ['Ehl-i Sünnet Kelam İmamı', 'Semerkant Ekolü'],
    tagsAr: ['إمام أهل السنة'],
    bioTr: 'Ehl-i Sünnet Mâtürîdî kelam ekolünün kurucusu ve Semerkant Hanefî usulünün öncüsü.',
    bioAr: 'إمام أهل السنة والجماعة ومؤسس المدرسة الماتريدية بسمرقند.',
  },
  {
    id: 'iskaf',
    nameAr: 'أبو بكر الإسكاف',
    nameTr: 'Ebû Bekr el-İskâf',
    deathH: 333,
    region: 'horasan',
    tabaka: 4,
    teachers: ['muhammed-seleme'],
    rolesTr: ['Belh Fakihi'],
    rolesAr: ['فقيه بلخ'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Belh Ekolü'],
    tagsAr: ['مدرسة بلخ'],
    bioTr: 'Belh fıkıh okulunda Hinduvânî’nin hocası.',
    bioAr: 'من أئمة بلخ وشيخ أبي جعفر الهندواني.',
  },
  {
    id: 'hakim-sehid',
    nameAr: 'الحاكم الشهيد المروزي',
    nameTr: 'Hâkim eş-Şehîd el-Mervezî',
    deathH: 334,
    region: 'horasan',
    tabaka: 4,
    teachers: ['hasan-sufyan', 'ebu-hafs-sagir'],
    rolesTr: ['Sâmânî Veziri ve Kadısı'],
    rolesAr: ['قاضي مرو ووزير السامانيين'],
    worksTr: ['el-Kâfî', 'el-Müntekâ'],
    worksAr: ['الكافي', 'المنتقى'],
    tagsTr: ['Muhtasar Müellifi', 'Zâhirü’r-Rivâye Cem‘i'],
    tagsAr: ['جامع ظاهر الرواية'],
    bioTr: 'İmam Muhammed’in Zâhirü’r-rivâye eserlerini el-Kâfî’de özetleyen büyük alim.',
    bioAr: 'جمع كتب ظاهر الرواية في مختصره الكافي الذي شرحه السرخسي في المبسوط.',
  },
  {
    id: 'saffar',
    nameAr: 'أبو القاسم الصفار',
    nameTr: 'Ebü’l-Kâsım es-Saffâr',
    deathH: 336,
    region: 'horasan',
    tabaka: 4,
    teachers: ['nusayr-belhi'],
    rolesTr: ['Belh Kadısı'],
    rolesAr: ['قاضي بلخ'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Belh Ekolü'],
    tagsAr: ['مدرسة بلخ'],
    bioTr: 'Belh’te kadılık yapan ve Ebü’l-Leys es-Semerkandî’ye ilim aktaran fakih.',
    bioAr: 'قاضي بلخ ومن شيوخ أبي الليث السمرقندي.',
  },
  {
    id: 'kerhi',
    nameAr: 'أبو الحسن الكرخي',
    nameTr: 'Ebü’l-Hasan el-Kerhî',
    deathH: 340,
    region: 'kufe',
    tabaka: 3,
    teachers: ['berdei', 'ebu-hazim'],
    rolesTr: ['Irak Hanefîleri Reisi'],
    rolesAr: ['رئيس الحنفية بالعراق'],
    worksTr: ['Muhtasaru’l-Kerhî', 'er-Risâle fi’l-Usûl'],
    worksAr: ['مختصر الكرخي', 'الرسالة في الأصول'],
    tagsTr: ['Muhtasar Müellifi', '3. Tabaka', 'Usul'],
    tagsAr: ['صاحب المختصر والأصول'],
    bioTr: 'Irak Hanefî ekolünün zirve ismi; usul risalesi ve muhtasarıyla meşhurdur.',
    bioAr: 'إمام الحنفية بالعراق، صاحب المختصر والرسالة الشهيرة في القواعد.',
  },
  {
    id: 'sebezmuni',
    nameAr: 'عبد الله السبذموني',
    nameTr: 'Abdullah es-Sebezmûnî',
    deathH: 340,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['ebu-hafs-sagir'],
    rolesTr: ['Buhara Fakihi'],
    rolesAr: ['الأستاذ في بخارى'],
    worksTr: ['Keşfü’l-Âsâr'],
    worksAr: ['كشف الآثار'],
    tagsTr: ['Buhara Ekolü'],
    tagsAr: ['مدرسة بخارى'],
    bioTr: '“el-Üstâz” lakabıyla tanınan Buhara Hanefî fakihi.',
    bioAr: 'لُقّب بالأستاذ، ومن أبرز فقهاء بخارى ومحدثيها.',
  },
  {
    id: 'zuccaci',
    nameAr: 'أبو السهل الزجاجي',
    nameTr: 'Ebü’s-Sehl ez-Züccâcî',
    deathH: 351,
    region: 'kufe',
    tabaka: 4,
    teachers: ['kerhi'],
    rolesTr: ['Irak Fakihi'],
    rolesAr: ['فقيه عراقي'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kerhî’nin Talebesi'],
    tagsAr: ['تلميذ الكرخي'],
    bioTr: 'Ebü’l-Hasan el-Kerhî’nin önde gelen talebelerinden.',
    bioAr: 'من كبار تلاميذ أبي الحسن الكرخي.',
  },
  {
    id: 'hinduvani',
    nameAr: 'أبو جعفر الهندواني',
    nameTr: 'Ebû Ca‘fer el-Hinduvânî',
    deathH: 362,
    region: 'horasan',
    tabaka: 4,
    teachers: ['iskaf', 'ames-ebu-bekr'],
    rolesTr: ['Ebû Hanîfe es-Sağîr'],
    rolesAr: ['أبو حنيفة الصغير'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Belh Ekolü'],
    tagsAr: ['مدرسة بلخ'],
    bioTr: 'Derin fıkıh bilgisi sebebiyle “Küçük Ebû Hanîfe” lakabını alan Belh imamı.',
    bioAr: 'لقب بأبي حنيفة الصغير لفقهه ودقته، وهو شيخ أبي الليث السمرقندي.',
  },
  {
    id: 'cessas',
    nameAr: 'أبو بكر الجصاص',
    nameTr: 'Ebû Bekr el-Cessâs',
    deathH: 370,
    region: 'kufe',
    tabaka: 4,
    teachers: ['kerhi'],
    rolesTr: ['Bağdat Hanefîleri Reisi'],
    rolesAr: ['إمام الحنفية ببغداد'],
    worksTr: ['Ahkâmü’l-Kur’ân', 'el-Fusûl fi’l-Usûl', 'Şerhu Muhtasari’t-Tahâvî'],
    worksAr: ['أحكام القرآن', 'الفصول في الأصول', 'شرح مختصر الطحاوي'],
    tagsTr: ['4. Tabaka', 'Usul ve Ahkâm Tefsiri'],
    tagsAr: ['الطبقة الرابعة', 'صاحب أحكام القرآن'],
    bioTr: 'Ashâbü’t-tahrîcin en büyük ismi; el-Fusûl ve Ahkâmü’l-Kur’ân müellifi.',
    bioAr: 'رأس أصحاب التخريج، مؤلف الفصول في الأصول وأحكام القرآن.',
  },
  {
    id: 'ebu-lleys',
    nameAr: 'أبو الليث السمرقندي',
    nameTr: 'Ebü’l-Leys es-Semerkandî',
    deathH: 373,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['hinduvani', 'saffar'],
    rolesTr: ['İmâmü’l-Hüdâ', 'Fakih'],
    rolesAr: ['الفقيه إمام الهدى'],
    worksTr: ['en-Nevâzil', 'Hizânetü’l-Fıkh', 'Tefsîru Ebi’l-Leys'],
    worksAr: ['النوازل', 'خزانة الفقه', 'بحر العلوم'],
    tagsTr: ['Fetva / Nevâzil Öncüsü'],
    tagsAr: ['أول من جمع النوازل'],
    bioTr: 'Fetva ve nevâzil literatürünün kurucularından Semerkantlı büyük fakih.',
    bioAr: 'المعروف بالفقيه، صاحب النوازل وخزانة الفقه وتفسير بحر العلوم.',
  },
  {
    id: 'kelabazi',
    nameAr: 'أبو بكر الكلاباذي',
    nameTr: 'Ebû Bekr el-Kelâbâzî',
    deathH: 380,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['muhammed-fadl'],
    rolesTr: ['Buhara Fakihi ve Mutasavvıf'],
    rolesAr: ['فقيه وصوفي بخارى'],
    worksTr: ['et-Taarruf'],
    worksAr: ['التعرف لمذهب أهل التصوف'],
    tagsTr: ['Buhara Ekolü', 'Tasavvuf'],
    tagsAr: ['فقيه وصوفي'],
    bioTr: 'Hanefî fakihi ve Sünnî tasavvufun klasik eseri et-Taarruf’un müellifi.',
    bioAr: 'فقيه حنفي بخاري ومؤلف كتاب التعرف في التصوف.',
  },
  {
    id: 'muhammed-fadl',
    nameAr: 'محمد بن الفضل البخاري',
    nameTr: 'Muhammed b. Fadl el-Buhârî',
    deathH: 381,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['sebezmuni'],
    rolesTr: ['Buhara İmamı'],
    rolesAr: ['إمام بخارى'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Buhara Ekolü'],
    tagsAr: ['مدرسة بخارى'],
    bioTr: 'Buhara Hanefî geleneğinde Ebû Ali en-Nesefî’nin hocası.',
    bioAr: 'تلميذ السبذموني وشيخ أبي علي النسفي.',
  },
  {
    id: 'ismail-sadik',
    nameAr: 'إسماعيل بن عبد الصادق',
    nameTr: 'İsmâil b. Abdissâdık',
    deathH: 388,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['hinduvani'],
    rolesTr: ['Mâverâünnehir Fakihi'],
    rolesAr: ['فقيه ما وراء النهر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Pezdevî Halkası'],
    tagsAr: ['شيخ البزدوي'],
    bioTr: 'Hinduvânî’nin talebesi ve Ebü’l-Yüsr el-Pezdevî’nin hocalarından.',
    bioAr: 'تلميذ الهندواني وشيخ أبي اليسر البزدوي.',
  },
  {
    id: 'abdulkerim-pezdevi',
    nameAr: 'عبد الكريم البزدوي',
    nameTr: 'Abdülkerîm el-Pezdevî',
    deathH: 390,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['maturidi'],
    rolesTr: ['Nesef Fakihi'],
    rolesAr: ['فقيه نسف'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Pezdevî Ailesinin Dedesi'],
    tagsAr: ['جد البزدويين'],
    bioTr: 'İmam Mâtürîdî’nin talebesi ve Pezdevî kardeşlerin büyük dedesi.',
    bioAr: 'تلميذ الماتريدي وجد الإمامين فخر الإسلام وصدر الإسلام البزدوي.',
  },
  {
    id: 'nevkadi',
    nameAr: 'أبو إسحاق النوقدي',
    nameTr: 'Ebû İshak en-Nevkadî',
    deathH: 392,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['hinduvani'],
    rolesTr: ['Mâverâünnehir Fakihi'],
    rolesAr: ['فقيه ما وراء النهر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Mâverâünnehir'],
    tagsAr: ['ما وراء النهر'],
    bioTr: 'Hinduvânî’nin talebesi ve Seyyârî’nin hocası.',
    bioAr: 'تلميذ أبي جعفر الهندواني وشيخ السياري.',
  },
  {
    id: 'curcani-ebu-abdullah',
    nameAr: 'أبو عبد الله الجرجاني',
    nameTr: 'Ebû Abdullah el-Cürcânî',
    deathH: 398,
    region: 'kufe',
    tabaka: 4,
    teachers: ['cessas'],
    rolesTr: ['Bağdat Fakihi'],
    rolesAr: ['فقيه بغداد'],
    worksTr: ['Tercihü Mezhebi Ebî Hanîfe'],
    worksAr: ['ترجيح مذهب أبي حنيفة'],
    tagsTr: ['Kudûrî’nin Hocası'],
    tagsAr: ['شيخ القدوري'],
    bioTr: 'Cessâs’ın seçkin talebesi ve İmam Kudûrî ile Nâtıfî’nin hocası.',
    bioAr: 'تلميذ الجصاص وشيخ الإمام القدوري والناطفي.',
  },

  // ==================== 5. HİCRÎ YÜZYIL (401–500) ====================
  {
    id: 'harezmi-ebu-bekr',
    nameAr: 'أبو بكر الخوارزمي',
    nameTr: 'Ebû Bekr el-Hârezmî',
    deathH: 403,
    region: 'kufe',
    tabaka: 4,
    teachers: ['cessas'],
    rolesTr: ['Bağdat Müftüsü'],
    rolesAr: ['مفتي بغداد'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Irak Ekolü'],
    tagsAr: ['تلميذ الجصاص'],
    bioTr: 'Bağdat Hanefîlerinin reisi ve Saymerî’nin hocası.',
    bioAr: 'شيخ الحنفية ببغداد وأستاذ أبي عبد الله الصيمري.',
  },
  {
    id: 'usruseni',
    nameAr: 'أبو جعفر الأسروشني',
    nameTr: 'Ebû Ca‘fer el-Üsrûşenî',
    deathH: 404,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['cessas'],
    rolesTr: ['Mâverâünnehir Fakihi'],
    rolesAr: ['فقيه ما وراء النهر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Debûsî’nin Hocası'],
    tagsAr: ['شيخ الدبوسي'],
    bioTr: 'Cessâs’ın ilmini Mâverâünnehir’e ve Debûsî’ye aktaran fakih.',
    bioAr: 'تلميذ الجصاص وشيخ القاضي أبي زيد الدبوسي.',
  },
  {
    id: 'seyyari',
    nameAr: 'السياري',
    nameTr: 'es-Seyyârî',
    deathH: 412,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['nevkadi', 'ebu-lleys'],
    rolesTr: ['Mâverâünnehir Fakihi'],
    rolesAr: ['فقيه ما وراء النهر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Mâverâünnehir'],
    tagsAr: ['ما وراء النهر'],
    bioTr: 'Ebü’l-Leys ve Nevkadî’nin talebesi.',
    bioAr: 'من تلاميذ أبي الليث السمرقندي وأبي إسحاق النوقدي.',
  },
  {
    id: 'ebu-ali-nesefi',
    nameAr: 'أبو علي النسفي',
    nameTr: 'Ebû Ali en-Nesefî',
    deathH: 424,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['muhammed-fadl'],
    rolesTr: ['Buhara Kadısı'],
    rolesAr: ['قاضي بخارى'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Halvânî’nin Hocası'],
    tagsAr: ['شيخ الحلواني'],
    bioTr: 'Şemsüleimme el-Halvânî’nin hocası olan Buhara kadısı.',
    bioAr: 'قاضي بخارى وشيخ شمس الأئمة الحلواني.',
  },
  {
    id: 'kuduri',
    nameAr: 'أبو الحسين القدوري',
    nameTr: 'Ebü’l-Hüseyin el-Kudûrî',
    deathH: 428,
    region: 'kufe',
    tabaka: 5,
    teachers: ['curcani-ebu-abdullah'],
    rolesTr: ['Irak Hanefîleri Reisi'],
    rolesAr: ['رئيس الحنفية بالعراق'],
    worksTr: ['el-Muhtasar (Kudûrî)', 'et-Tecrîd'],
    worksAr: ['مختصر القدوري', 'التجريد'],
    tagsTr: ['Muhtasar Müellifi', '5. Tabaka', 'Ashâbü’t-Tercîh'],
    tagsAr: ['صاحب المختصر', 'الطبقة الخامسة'],
    bioTr: 'Hanefî mezhebinin “el-Kitâb” diye anılan en meşhur muhtasarının müellifi.',
    bioAr: 'رئيس أصحاب الترجيح ومؤلف المختصر الملقب بالكتاب.',
  },
  {
    id: 'debusi',
    nameAr: 'أبو زيد الدبوسي',
    nameTr: 'Ebû Zeyd ed-Debûsî',
    deathH: 430,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['usruseni'],
    rolesTr: ['Hilâf İlmi Kurucusu', 'Kadı'],
    rolesAr: ['مؤسس علم الخلاف'],
    worksTr: ['Takvîmü’l-Edille', 'Te’sîsü’n-Nazar', 'el-Esrâr'],
    worksAr: ['تقويم الأدلة', 'تأسيس النظر', 'الأسرار'],
    tagsTr: ['Hilâf ve Usul Öncüsü', '3. Tabaka'],
    tagsAr: ['مؤسس علم الخلاف والأصول'],
    bioTr: 'Mukayeseli fıkıh (ilm-i hilâf) ve Hanefî fıkıh usulünün kurucu dehası.',
    bioAr: 'أول من وضع علم الخلاف وأبرز أئمة أصول الفقه الحنفي.',
  },
  {
    id: 'mustagfiri',
    nameAr: 'أبو العباس المستغفري',
    nameTr: 'el-Müstağfirî',
    deathH: 432,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['ebu-ali-nesefi'],
    rolesTr: ['Nesef Hatibi ve Muhaddisi'],
    rolesAr: ['خطيب نسف ومحدثها'],
    worksTr: ['Târîhu Semerkand'],
    worksAr: ['تاريخ سمرقند'],
    tagsTr: ['Muhaddis', 'Tarihçi'],
    tagsAr: ['محدث ومؤرخ'],
    bioTr: 'Mâverâünnehir’in büyük hadis ve tarih alimi.',
    bioAr: 'محدث نسف ومؤرخ سمرقند.',
  },
  {
    id: 'saymeri',
    nameAr: 'أبو عبد الله الصيمري',
    nameTr: 'Ebû Abdullah es-Saymerî',
    deathH: 436,
    region: 'kufe',
    tabaka: 4,
    teachers: ['harezmi-ebu-bekr'],
    rolesTr: ['Bağdat Kadısı'],
    rolesAr: ['قاضي الكرخ ببغداد'],
    worksTr: ['Ahbâru Ebî Hanîfe', 'Mesâilü’l-Hilâf'],
    worksAr: ['أخبار أبي حنيفة وأصحابه', 'مسائل الخلاف'],
    tagsTr: ['Tabakat Öncüsü'],
    tagsAr: ['أول من كتب في مناقب الحنفية'],
    bioTr: 'Ebû Hanîfe ve ashabının biyografilerini derleyen ilk tabakat müelliflerinden.',
    bioAr: 'قاضي بغداد ومؤلف أخبار أبي حنيفة وأصحابه.',
  },
  {
    id: 'natifi',
    nameAr: 'أبو العباس الناطفي',
    nameTr: 'Ebü’l-Abbâs en-Nâtıfî',
    deathH: 446,
    region: 'kufe',
    tabaka: 4,
    teachers: ['curcani-ebu-abdullah'],
    rolesTr: ['Rey Fakihi'],
    rolesAr: ['فقيه الري'],
    worksTr: ['el-Ecnâs', 'el-Vâkıât'],
    worksAr: ['الأجناس', 'الواقعات'],
    tagsTr: ['Fetva'],
    tagsAr: ['صاحب الواقعات'],
    bioTr: 'el-Ecnâs ve el-Vâkıât eserleriyle tanınan büyük fakih.',
    bioAr: 'تلميذ الجرجاني وصاحب كتابي الأجناس والواقعات.',
  },
  {
    id: 'halvani',
    nameAr: 'شمس الأئمة الحلواني',
    nameTr: 'Şemsüleimme el-Halvânî',
    deathH: 452,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['ebu-ali-nesefi'],
    rolesTr: ['Buhara Hanefîleri Reisi'],
    rolesAr: ['شمس الأئمة وإمام بخارى'],
    worksTr: ['el-Mebsût', 'en-Nevâdir'],
    worksAr: ['المبسوط', 'النوادر'],
    tagsTr: ['3. Tabaka', 'Buhara Zirvesi'],
    tagsAr: ['الطبقة الثالثة', 'شيخ السرخسي والبزدوي'],
    bioTr: 'Serahsî ve Pezdevî’yi yetiştiren, Mâverâünnehir fıkhının en etkili hocası.',
    bioAr: 'إمام أهل ما وراء النهر وأستاذ السرخسي وفخر الإسلام البزدوي.',
  },
  {
    id: 'sem-ani',
    nameAr: 'أبو منصور السمعاني',
    nameTr: 'Ebû Mansûr es-Sem‘ânî',
    deathH: 460,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['mustagfiri'],
    rolesTr: ['Merv Fakihi'],
    rolesAr: ['فقيه مرو'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Mâverâünnehir'],
    tagsAr: ['ما وراء النهر'],
    bioTr: 'Müstağfirî’nin talebesi ve Ersâbendî’nin hocası.',
    bioAr: 'من تلاميذ المستغفري وشيخ الأرصابندي.',
  },
  {
    id: 'ersabendi',
    nameAr: 'أبو بكر الأرصابندي',
    nameTr: 'Ebû Bekr el-Ersâbendî',
    deathH: 465,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['sem-ani'],
    rolesTr: ['Merv Fakihi'],
    rolesAr: ['فقيه مرو'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Mâverâünnehir'],
    tagsAr: ['ما وراء النهر'],
    bioTr: 'Merv Hanefî ulemasından ve Kirmânî’nin hocası.',
    bioAr: 'من فقهاء مرو وشيخ الإمام الكرماني.',
  },
  {
    id: 'kirmani',
    nameAr: 'ركن الدين الكرماني',
    nameTr: 'Rükneddin el-Kirmânî',
    deathH: 470,
    region: 'maveraunnehir',
    tabaka: 4,
    teachers: ['ersabendi'],
    rolesTr: ['Merv Müftüsü'],
    rolesAr: ['مفتي مرو'],
    worksTr: ['et-Tecrîd'],
    worksAr: ['التجريد'],
    tagsTr: ['Mâverâünnehir'],
    tagsAr: ['فقيه ومفتٍ'],
    bioTr: 'Merv’de fetva makamında bulunmuş büyük Hanefî fakihi.',
    bioAr: 'إمام حنفي بمرو، له مؤلفات وشروح معتبرة.',
  },
  {
    id: 'akta',
    nameAr: 'أبو نصر الأقطع',
    nameTr: 'Ebû Nasr el-Akta‘',
    deathH: 474,
    region: 'kufe',
    tabaka: 5,
    teachers: ['kuduri'],
    rolesTr: ['Bağdat Fakihi'],
    rolesAr: ['فقيه بغداد'],
    worksTr: ['Şerhu Muhtasari’l-Kudûrî'],
    worksAr: ['شرح مختصر القدوري'],
    tagsTr: ['Kudûrî Şârihi'],
    tagsAr: ['شارح القدوري'],
    bioTr: 'Kudûrî’nin talebesi ve Muhtasaru’l-Kudûrî’nin ilk şârihlerinden.',
    bioAr: 'تلميذ القدوري وأحد أوائل شراح مختصره.',
  },
  {
    id: 'damgani',
    nameAr: 'أبو عبد الله الدامغاني الكبير',
    nameTr: 'Ebû Abdullah ed-Dâmegânî el-Kebîr',
    deathH: 478,
    region: 'kufe',
    tabaka: 5,
    teachers: ['saymeri'],
    rolesTr: ['Bağdat Kâdılkudâtı'],
    rolesAr: ['قاضي القضاة ببغداد'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kâdılkudât', 'Irak Ekolü'],
    tagsAr: ['قاضي القضاة'],
    bioTr: 'Abbâsî hilafetinde otuz yıl Kâdılkudâtlık yapan büyük fakih.',
    bioAr: 'قاضي قضاة بغداد ثلاثين سنة وتلميذ الصيمري.',
  },
  {
    id: 'ebul-usr-pezdevi',
    nameAr: 'فخر الإسلام أبو العسر البزدوي',
    nameTr: 'Fahrü’l-İslâm Ebü’l-Usr el-Pezdevî',
    deathH: 482,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['halvani', 'abdulkerim-pezdevi'],
    rolesTr: ['Semerkant Başfakihi'],
    rolesAr: ['فخر الإسلام وإمام ما وراء النهر'],
    worksTr: ['Kenzü’l-Vüsûl (Usûlü’l-Pezdevî)', 'el-Mebsût'],
    worksAr: ['أصول البزدوي', 'المبسوط'],
    tagsTr: ['3. Tabaka', 'Usul Otoritesi'],
    tagsAr: ['الطبقة الثالثة', 'إمام الأصول'],
    bioTr: 'Hanefî fıkıh usulünün en meşhur metni olan Usûlü’l-Pezdevî’nin müellifi.',
    bioAr: 'صاحب كتاب أصول البزدوي (كنز الوصول) الذي عليه مدار علم الأصول الحنفي.',
  },
  {
    id: 'serahsi',
    nameAr: 'شمس الأئمة السرخسي',
    nameTr: 'Şemsüleimme es-Serahsî',
    deathH: 483,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['halvani'],
    rolesTr: ['Şemsüleimme', 'Müçtehid Fakih'],
    rolesAr: ['شمس الأئمة'],
    worksTr: ['el-Mebsût (30 cilt)', 'Usûlü’s-Serahsî', 'Şerhu’s-Siyeri’l-Kebîr'],
    worksAr: ['المبسوط', 'أصول السرخسي', 'شرح السير الكبير'],
    tagsTr: ['Kütüb-i Esâsiyye', '3. Tabaka'],
    tagsAr: ['الكتب الأساسية', 'الطبقة الثالثة'],
    bioTr: 'Özkend zindanında hafızasından 30 ciltlik el-Mebsût’u imla ettiren dev fakih.',
    bioAr: 'أملى كتابه المبسوط من حفظه في سجن أوزجند، وهو من أعظم موسوعات الفقه.',
  },
  {
    id: 'ebul-yusr-pezdevi',
    nameAr: 'صدر الإسلام أبو اليسر البزدوي',
    nameTr: 'Sadrü’l-İslâm Ebü’l-Yüsr el-Pezdevî',
    deathH: 493,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['ismail-sadik', 'abdulkerim-pezdevi'],
    rolesTr: ['Semerkant Kadısı'],
    rolesAr: ['قاضي سمرقند وصدر الإسلام'],
    worksTr: ['Usûlü’d-Dîn', 'el-Mebsût'],
    worksAr: ['أصول الدين', 'المبسوط'],
    tagsTr: ['Kelam ve Fıkıh'],
    tagsAr: ['فقيه ومتكلم'],
    bioTr: 'Fahrü’l-İslâm’ın kardeşi, Necmeddin en-Nesefî ve Alâeddin es-Semerkandî’nin hocası.',
    bioAr: 'أخو فخر الإسلام وشيخ نجم الدين النسفي وعلاء الدين السمرقندي.',
  },

  // ==================== 6. HİCRÎ YÜZYIL (501–600) ====================
  {
    id: 'ozcendi',
    nameAr: 'محمود الأوزجندي',
    nameTr: 'Mahmûd el-Özcendî',
    deathH: 525,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['serahsi'],
    rolesTr: ['Fergana Kadısı'],
    rolesAr: ['قاضي أوزجند'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Kadıhan’ın Dedesi'],
    tagsAr: ['جد قاضي خان'],
    bioTr: 'Serahsî’nin talebesi ve Zahîrüddin el-Mergînânî’nin hocası.',
    bioAr: 'تلميذ السرخسي وجد فخر الدين قاضي خان.',
  },
  {
    id: 'burhaneddin-ibn-maze',
    nameAr: 'برهان الدين ابن مازه الكبير',
    nameTr: 'Burhâneddin İbn Mâze el-Kebîr',
    deathH: 530,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['serahsi'],
    rolesTr: ['Buhara Sadrı (Reisi)'],
    rolesAr: ['صدر بخارى'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Âl-i Burhân Kurucusu'],
    tagsAr: ['جد آل برهان'],
    bioTr: 'Buhara’da asırlarca ilim ve liderlik yürüten Âl-i Burhân ailesinin kurucusu.',
    bioAr: 'مؤسس أسرة آل برهان العلمية في بخارى وتلميذ السرخسي.',
  },
  {
    id: 'sadrussehid',
    nameAr: 'صدر الشهيد حسام الدين ابن مازه',
    nameTr: 'Sadrüşşehîd İbn Mâze',
    deathH: 536,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['burhaneddin-ibn-maze'],
    rolesTr: ['Buhara Sadrı'],
    rolesAr: ['صدر بخارى وشهيدها'],
    worksTr: ['el-Vâkıâtü’l-Hüsâmiyye', 'Şerhu Edebi’l-Kâdî'],
    worksAr: ['الواقعات الحسامية', 'شرح أدب القاضي'],
    tagsTr: ['Fetva', 'Mergînânî’nin Hocası'],
    tagsAr: ['شيخ المرغيناني'],
    bioTr: 'Katvan savaşında şehit düşen, Mergînânî ve Kadıhan’ın hocası büyük fakih.',
    bioAr: 'من كبار فقهاء آل برهان، وأستاذ المرغيناني وقاضي خان.',
  },
  {
    id: 'necmeddin-nesefi',
    nameAr: 'نجم الدين عمر النسفي',
    nameTr: 'Necmeddin Ömer en-Nesefî',
    deathH: 537,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['ebul-yusr-pezdevi'],
    rolesTr: ['Semerkant Müftüsü'],
    rolesAr: ['مفتي الثقلين'],
    worksTr: ['el-Akâidü’n-Nesefiyye', 'Tılbetü’t-Talebe', 'el-Manzûme'],
    worksAr: ['العقائد النسفية', 'طلبة الطلبة', 'المنظومة في الخلاف'],
    tagsTr: ['Akaid', 'Hilâf', 'Mergînânî’nin Hocası'],
    tagsAr: ['صاحب العقائد النسفية'],
    bioTr: 'Medreselerde asırlarca okutulan Akâidü’n-Nesefî’nin müellifi ve Mergînânî’nin hocası.',
    bioAr: 'مؤلف العقائد النسفية والمنظومة في الخلاف وشيخ المرغيناني.',
  },
  {
    id: 'alaeddin-semerkandi',
    nameAr: 'علاء الدين السمرقندي',
    nameTr: 'Alâeddin es-Semerkandî',
    deathH: 539,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['ebul-usr-pezdevi', 'ebul-yusr-pezdevi'],
    rolesTr: ['Semerkant Fakihi'],
    rolesAr: ['إمام سمرقند'],
    worksTr: ['Tuhfetü’l-Fukahâ', 'Mîzânü’l-Usûl'],
    worksAr: ['تحفة الفقهاء', 'ميزان الأصول'],
    tagsTr: ['Kâsânî’nin Hocası', 'Usul'],
    tagsAr: ['صاحب التحفة وميزان الأصول'],
    bioTr: 'Bedâiu’s-Sanâi‘in ana metni olan Tuhfetü’l-Fukahâ’nın müellifi ve Kâsânî’nin kayınpederi.',
    bioAr: 'مؤلف تحفة الفقهاء وميزان الأصول، وشيخ الكاساني.',
  },
  {
    id: 'sadrussaid',
    nameAr: 'صدر السعيد تاج الدين ابن مازه',
    nameTr: 'Sadrüssaîd İbn Mâze',
    deathH: 550,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['burhaneddin-ibn-maze'],
    rolesTr: ['Buhara Sadrı'],
    rolesAr: ['صدر بخارى'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Âl-i Burhân'],
    tagsAr: ['آل برهان'],
    bioTr: 'Sadrüşşehîd’in kardeşi ve Mergînânî’nin hocalarından.',
    bioAr: 'أخو صدر الشهيد ومن شيوخ برهان الدين المرغيناني.',
  },
  {
    id: 'bendenici',
    nameAr: 'البندنيجي',
    nameTr: 'el-Bendenîcî',
    deathH: 555,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['alaeddin-semerkandi'],
    rolesTr: ['Fakih'],
    rolesAr: ['فقيه'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Semerkant Ekolü'],
    tagsAr: ['تلميذ السمرقندي'],
    bioTr: 'Alâeddin es-Semerkandî’nin önde gelen talebelerinden.',
    bioAr: 'من تلاميذ علاء الدين السمرقندي.',
  },
  {
    id: 'zahiruddin-merginani',
    nameAr: 'ظهير الدين المرغيناني',
    nameTr: 'Zahîrüddin el-Mergînânî',
    deathH: 560,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['ozcendi'],
    rolesTr: ['Muhtesib ve Müftü'],
    rolesAr: ['مفتي فرغانة'],
    worksTr: ['el-Fetâva’z-Zahîriyye'],
    worksAr: ['الفتاوى الظهيرية'],
    tagsTr: ['Fetva'],
    tagsAr: ['صاحب الظهيرية'],
    bioTr: 'Kadıhan’ın hocası ve Fetâvâ-yı Zahîriyye müellifi.',
    bioAr: 'شيخ قاضي خان ومؤلف الفتاوى الظهيرية.',
  },
  {
    id: 'kasani',
    nameAr: 'علاء الدين الكاساني',
    nameTr: 'Alâeddin el-Kâsânî',
    deathH: 587,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['alaeddin-semerkandi'],
    rolesTr: ['Melikü’l-Ulemâ', 'Halep Başmüderrisi'],
    rolesAr: ['ملك العلماء ومدرس الحلاوية بحلب'],
    worksTr: ['Bedâiu’s-Sanâi‘'],
    worksAr: ['بدائع الصنائع في ترتيب الشرائع'],
    tagsTr: ['Kütüb-i Esâsiyye', '5. Tabaka'],
    tagsAr: ['الكتب الأساسية', 'ملك العلماء'],
    bioTr: 'Sistematik fıkıh şaheseri Bedâiu’s-Sanâi‘in müellifi “Melikü’l-Ulemâ”.',
    bioAr: 'صاحب بدائع الصنائع، أعظم كتب الفقه الحنفي ترتيباً وتحقيقاً.',
  },
  {
    id: 'kadihan',
    nameAr: 'فخر الدين قاضي خان',
    nameTr: 'Fahreddin Kâdîhân',
    deathH: 592,
    region: 'maveraunnehir',
    tabaka: 3,
    teachers: ['zahiruddin-merginani', 'sadrussehid'],
    rolesTr: ['Fergana Müftüsü'],
    rolesAr: ['مفتي ما وراء النهر'],
    worksTr: ['Fetâvâ Kâdîhân', 'Şerhu’l-Câmii’s-Sağîr'],
    worksAr: ['فتاوى قاضي خان', 'شرح الجامع الصغير'],
    tagsTr: ['3. Tabaka', 'Fetva Otoritesi'],
    tagsAr: ['الطبقة الثالثة', 'صاحب الفتاوى الخانية'],
    bioTr: 'Hanefî mezhebinde fetva ve tercih otoritesi; İbn Kemal’e göre 3. tabakadandır.',
    bioAr: 'مرجع الفتوى في المذهب الحنفي، وصاحب الفتاوى الخانية.',
  },
  {
    id: 'merginani',
    nameAr: 'برهان الدين المرغيناني',
    nameTr: 'Burhâneddin el-Mergînânî',
    deathH: 593,
    region: 'maveraunnehir',
    tabaka: 5,
    teachers: ['necmeddin-nesefi', 'sadrussehid', 'sadrussaid', 'alaeddin-semerkandi'],
    rolesTr: ['Şeyhülislam', 'Müctehid-i Müreccih'],
    rolesAr: ['صاحب الهداية وشيخ الإسلام'],
    worksTr: ['el-Hidâye', 'Bidâyetü’l-Mübtedî', 'et-Tecnîs'],
    worksAr: ['الهداية', 'بداية المبتدي', 'التجنيس والمزيد'],
    tagsTr: ['Kütüb-i Esâsiyye', '5. Tabaka'],
    tagsAr: ['الكتب الأساسية', 'الطبقة الخامسة'],
    bioTr: 'Hanefî fıkhının medreselerde en çok okutulan ve şerh edilen eseri el-Hidâye’nin müellifi.',
    bioAr: 'صاحب كتاب الهداية، أشهر وأهم كتب الفقه الحنفي على الإطلاق.',
  },

  // ==================== 7. HİCRÎ YÜZYIL (601–700) ====================
  {
    id: 'hilati',
    nameAr: 'محمد الخلاطي',
    nameTr: 'Muhammed el-Hilâtî',
    deathH: 602,
    region: 'misir',
    tabaka: 6,
    teachers: ['kadihan'],
    rolesTr: ['Mısır Fakihi'],
    rolesAr: ['فقيه بمصر'],
    worksTr: ['Telhîsu’l-Câmii’l-Kebîr'],
    worksAr: ['تلخيص الجامع الكبير'],
    tagsTr: ['Mısır Halkası'],
    tagsAr: ['حلقة مصر'],
    bioTr: 'Mısır Hanefî silsilesinde Sürûcî’nin hocası.',
    bioAr: 'من فقهاء الحنفية وشيخ شمس الدين السروجي.',
  },
  {
    id: 'zernuci',
    nameAr: 'برهان الدين الزرنوجي',
    nameTr: 'Burhâneddin ez-Zernûcî',
    deathH: 620,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['merginani'],
    rolesTr: ['Eğitimci ve Fakih'],
    rolesAr: ['فقيه ومربٍّ'],
    worksTr: ['Ta‘lîmü’l-Müteallim'],
    worksAr: ['تعليم المتعلم طريق التعلم'],
    tagsTr: ['Mergînânî’nin Talebesi'],
    tagsAr: ['صاحب تعليم المتعلم'],
    bioTr: 'İslam eğitim klasiği Ta‘lîmü’l-Müteallim’in müellifi ve Mergînânî’nin talebesi.',
    bioAr: 'تلميذ المرغيناني ومؤلف الكتاب التربوي الشهير تعليم المتعلم.',
  },
  {
    id: 'sadrusseria-evvel',
    nameAr: 'صدر الشريعة الأول',
    nameTr: 'Sadrüşşerîa el-Evvel',
    deathH: 630,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['merginani'],
    rolesTr: ['Buhara Fakihi'],
    rolesAr: ['صدر الشريعة الأكبر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Mahbûbî Ailesi'],
    tagsAr: ['أسرة المحبوبي'],
    bioTr: 'Tâcüşşerîa ve Burhânüşşerîa’nın babası, Sadrüşşerîa es-Sânî’nin dedesi.',
    bioAr: 'رأس أسرة المحبوبي العلمية ببخارى ووالد تاج الشريعة.',
  },
  {
    id: 'hasiri',
    nameAr: 'محمود بن أحمد الحصيري',
    nameTr: 'Mahmûd b. Ahmed el-Hasîrî',
    deathH: 639,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['kadihan'],
    rolesTr: ['Şam Nûriyye Başmüderrisi'],
    rolesAr: ['شيخ الحنفية بالشام'],
    worksTr: ['et-Tahrîr fi Şerhi’l-Câmii’l-Kebîr'],
    worksAr: ['التحرير في شرح الجامع الكبير'],
    tagsTr: ['Mevsılî’nin Hocası'],
    tagsAr: ['شيخ الموصلي'],
    bioTr: 'Kadıhan’ın ilmini Şam’a taşıyan ve Mevsılî’yi yetiştiren büyük fakih.',
    bioAr: 'نقل فقه ما وراء النهر إلى دمشق، وهو شيخ صاحب المختار.',
  },
  {
    id: 'kerderi',
    nameAr: 'شمس الأئمة محمد الكردري',
    nameTr: 'Şemsüleimme Muhammed el-Kerderî',
    deathH: 642,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['merginani', 'kadihan'],
    rolesTr: ['Buhara ve Semerkant Üstadı'],
    rolesAr: ['شمس الأئمة الكردري'],
    worksTr: ['er-Red ve’l-İntisâr'],
    worksAr: ['الرد والانتصار لأبي حنيفة'],
    tagsTr: ['Nesefî’nin Hocası'],
    tagsAr: ['شيخ أبي البركات النسفي'],
    bioTr: 'Moğol istilası sonrası Mâverâünnehir fıkıh silsilesini ayakta tutan büyük hoca.',
    bioAr: 'أحيا المذهب الحنفي بعد الفتنة التترية، وهو شيخ أبي البركات النسفي.',
  },
  {
    id: 'meymergi',
    nameAr: 'محمد الميمرغي',
    nameTr: 'Muhammed el-Meymergî',
    deathH: 675,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['kerderi'],
    rolesTr: ['Mâverâünnehir Fakihi'],
    rolesAr: ['فقيه ما وراء النهر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Buhârî’nin Hocası'],
    tagsAr: ['شيخ عبد العزيز البخاري'],
    bioTr: 'Kerderî’nin talebesi ve Abdülaziz el-Buhârî’nin hocası.',
    bioAr: 'تلميذ الكردري وشيخ عبد العزيز البخاري.',
  },
  {
    id: 'mevsili',
    nameAr: 'عبد الله بن محمود الموصلي',
    nameTr: 'Abdullah b. Mahmûd el-Mevsılî',
    deathH: 683,
    region: 'kufe',
    tabaka: 6,
    teachers: ['hasiri'],
    rolesTr: ['Kûfe Kadısı', 'Bağdat Müderrisi'],
    rolesAr: ['قاضي الكوفة ومؤلف المختار'],
    worksTr: ['el-Muhtâr', 'el-İhtiyâr li-Ta‘lîli’l-Muhtâr'],
    worksAr: ['المختار للفتوى', 'الاختيار لتعليل المختار'],
    tagsTr: ['Mütûn-ı Erbaa', '6. Tabaka'],
    tagsAr: ['المتون الأربعة', 'الطبقة السادسة'],
    bioTr: 'Mütûn-ı Erbaa’dan el-Muhtâr ve şerhi el-İhtiyâr’ın müellifi.',
    bioAr: 'مؤلف المختار أحد المتون الأربعة وشرحه الاختيار.',
  },
  {
    id: 'habbazi',
    nameAr: 'عمر بن محمد الخبازي',
    nameTr: 'Ömer b. Muhammed el-Habbâzî',
    deathH: 691,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['kerderi'],
    rolesTr: ['Şam Müderrisi'],
    rolesAr: ['شيخ الحنفية بدمشق'],
    worksTr: ['el-Muğnî fî Usûli’l-Fıkh'],
    worksAr: ['المغني في أصول الفقه'],
    tagsTr: ['Usul'],
    tagsAr: ['صاحب المغني في الأصول'],
    bioTr: 'Usulde el-Muğnî eseriyle meşhur Mâverâünnehir asıllı fakih.',
    bioAr: 'صاحب كتاب المغني في أصول الفقه.',
  },
  {
    id: 'ibn-saati',
    nameAr: 'مظفر الدين ابن الساعاتي',
    nameTr: 'Muzafferüddin İbnü’s-Sââtî',
    deathH: 694,
    region: 'kufe',
    tabaka: 6,
    teachers: ['kerderi'],
    rolesTr: ['Bağdat Müstansıriyye Müderrisi'],
    rolesAr: ['مدرس المستنصرية ببغداد'],
    worksTr: ['Mecmau’l-Bahreyn', 'Bedîu’n-Nizâm'],
    worksAr: ['مجمع البحرين', 'بديع النظام'],
    tagsTr: ['Mütûn-ı Erbaa', '6. Tabaka', 'Usul'],
    tagsAr: ['المتون الأربعة', 'الطبقة السادسة'],
    bioTr: 'Mütûn-ı Erbaa’dan Mecmau’l-Bahreyn ve usulde Bedîu’n-Nizâm’ın müellifi.',
    bioAr: 'مؤلف مجمع البحرين أحد المتون الأربعة وبديع النظام في الأصول.',
  },

  // ==================== 8. HİCRÎ YÜZYIL (701–800) ====================
  {
    id: 'tacusseria',
    nameAr: 'تاج الشريعة المحبوبي',
    nameTr: 'Tâcüşşerîa el-Mahbûbî',
    deathH: 709,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['sadrusseria-evvel'],
    rolesTr: ['Buhara Müftüsü'],
    rolesAr: ['تاج الشريعة'],
    worksTr: ['Vikâyetü’r-Rivâye'],
    worksAr: ['وقاية الرواية في مسائل الهداية'],
    tagsTr: ['Mütûn-ı Erbaa', '6. Tabaka'],
    tagsAr: ['المتون الأربعة', 'الطبقة السادسة'],
    bioTr: 'el-Hidâye’yi özetleyen ve Mütûn-ı Erbaa’dan sayılan el-Vikâye’nin müellifi.',
    bioAr: 'مؤلف وقاية الرواية لخص فيه الهداية لحفيده صدر الشريعة الثاني.',
  },
  {
    id: 'ebul-berekat-nesefi',
    nameAr: 'أبو البركات حافظ الدين النسفي',
    nameTr: 'Ebü’l-Berekât en-Nesefî',
    deathH: 710,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['kerderi'],
    rolesTr: ['İmam, Müfessir, Usulcü'],
    rolesAr: ['حافظ الدين النسفي'],
    worksTr: ['Kenzü’d-Dekâik', 'el-Menâr', 'Medârikü’t-Tenzîl'],
    worksAr: ['كنز الدقائق', 'المنار في الأصول', 'مدارك التنزيل'],
    tagsTr: ['Mütûn-ı Erbaa', '6. Tabaka', 'Usul ve Tefsir'],
    tagsAr: ['المتون الأربعة', 'صاحب الكنز والمنار'],
    bioTr: 'Mütûn-ı Erbaa’nın en meşhuru Kenzü’d-Dekâik ile el-Menâr ve Medârik tefsirinin müellifi.',
    bioAr: 'صاحب كنز الدقائق والمنار في الأصول وتفسير المدارك.',
  },
  {
    id: 'suruci',
    nameAr: 'شمس الدين السروجي',
    nameTr: 'Şemseddin es-Sürûcî',
    deathH: 710,
    region: 'misir',
    tabaka: 6,
    teachers: ['hilati'],
    rolesTr: ['Mısır Hanefî Kâdılkudâtı'],
    rolesAr: ['قاضي قضاة الحنفية بمصر'],
    worksTr: ['el-Gâye fî Şerhi’l-Hidâye'],
    worksAr: ['الغاية في شرح الهداية'],
    tagsTr: ['Hidâye Şârihi', 'Kâdılkudât'],
    tagsAr: ['قاضي القضاة وشارح الهداية'],
    bioTr: 'el-Hidâye üzerine el-Gâye şerhini yazan Mısır Hanefî başkadısı.',
    bioAr: 'قاضي القضاة بمصر وشارح الهداية في كتابه الغاية.',
  },
  {
    id: 'signaki',
    nameAr: 'حسام الدين السغناقي',
    nameTr: 'Hüsâmeddin es-Sıgnâkî',
    deathH: 714,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['ebul-berekat-nesefi'],
    rolesTr: ['Bağdat ve Halep Müderrisi'],
    rolesAr: ['شارح الهداية والبزدوي'],
    worksTr: ['en-Nihâye fî Şerhi’l-Hidâye', 'el-Kâfî fî Şerhi’l-Pezdevî'],
    worksAr: ['النهاية في شرح الهداية', 'الكافي في شرح أصول البزدوي'],
    tagsTr: ['Hidâye Şârihi', 'Usul'],
    tagsAr: ['شارح الهداية'],
    bioTr: 'el-Hidâye’ye ilk kapsamlı şerhlerden en-Nihâye’yi yazan büyük fakih.',
    bioAr: 'صاحب النهاية في شرح الهداية والكافي في شرح أصول البزدوي.',
  },
  {
    id: 'abdulaziz-buhari',
    nameAr: 'علاء الدين عبد العزيز البخاري',
    nameTr: 'Alâeddin Abdülaziz el-Buhârî',
    deathH: 730,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['meymergi', 'ebul-berekat-nesefi'],
    rolesTr: ['Buhara Müderrisi', 'Usulcü'],
    rolesAr: ['محقق الأصول ببخارى'],
    worksTr: ['Keşfü’l-Esrâr (Pezdevî Şerhi)', 'et-Tahkîk'],
    worksAr: ['كشف الأسرار شرح أصول البزدوي', 'التحقيق'],
    tagsTr: ['Usul Şârihi', '6. Tabaka'],
    tagsAr: ['صاحب كشف الأسرار'],
    bioTr: 'Usûlü’l-Pezdevî’nin en meşhur şerhi Keşfü’l-Esrâr’ın müellifi.',
    bioAr: 'صاحب كشف الأسرار أعظم شروح أصول البزدوي.',
  },
  {
    id: 'burhanusseria',
    nameAr: 'برهان الشريعة المحبوبي',
    nameTr: 'Burhânüşşerîa el-Mahbûbî',
    deathH: 730,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['sadrusseria-evvel'],
    rolesTr: ['Buhara Fakihi'],
    rolesAr: ['برهان الشريعة'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Mahbûbî Ailesi'],
    tagsAr: ['أسرة المحبوبي'],
    bioTr: 'Sadrüşşerîa el-Evvel’in oğlu ve Sadrüşşerîa es-Sânî’nin hocası.',
    bioAr: 'أخو تاج الشريعة وأستاذ صدر الشريعة الثاني.',
  },
  {
    id: 'sadrusseria-sani',
    nameAr: 'صدر الشريعة الثاني عبيد الله',
    nameTr: 'Sadrüşşerîa es-Sânî',
    deathH: 747,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['tacusseria', 'burhanusseria'],
    rolesTr: ['Fakih, Usulcü, Mütekellim'],
    rolesAr: ['صدر الشريعة الأصغر'],
    worksTr: ['Şerhu’l-Vikâye', 'en-Nukâye', 'et-Tenkîh ve’t-Tavzîh'],
    worksAr: ['شرح الوقاية', 'النقاية', 'التنقيح والتوضيح'],
    tagsTr: ['6. Tabaka', 'Memzûc Usul Öncüsü'],
    tagsAr: ['الطبقة السادسة', 'صاحب التنقيح والتوضيح'],
    bioTr: 'Vikâye şerhi ve Tenkîh/Tavzîh ile Hanefî fıkıh ve usulünde çığır açan alim.',
    bioAr: 'صاحب شرح الوقاية والتوضيح، جدد في أصول الفقه الحنفي.',
  },
  {
    id: 'zehebi',
    nameAr: 'شمس الدين الذهبي',
    nameTr: 'Şemseddin ez-Zehebî',
    deathH: 748,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: [],
    rolesTr: ['Hâfız ve Tarihçi'],
    rolesAr: ['مؤرخ الإسلام وحافظه'],
    worksTr: ['Siyeru A‘lâmi’n-Nübelâ', 'Târîhu’l-İslâm'],
    worksAr: ['سير أعلام النبلاء', 'تاريخ الإسلام'],
    tagsTr: ['Muhaddis', 'Tarihçi'],
    tagsAr: ['حافظ ومؤرخ'],
    bioTr: 'İslam tarihçiliği ve hadis ricâlinde otorite; İbn Receb’in hocası.',
    bioAr: 'مؤرخ الإسلام وحافظه، وشيخ ابن رجب.',
  },
  {
    id: 'kaki',
    nameAr: 'قوام الدين الكاكي',
    nameTr: 'Kıvâmüddin el-Kâkî',
    deathH: 749,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['signaki'],
    rolesTr: ['Kahire Müderrisi'],
    rolesAr: ['شارح الهداية بمصر'],
    worksTr: ['Mi‘râcü’d-Dirâye (Hidâye Şerhi)'],
    worksAr: ['معراج الدراية في شرح الهداية'],
    tagsTr: ['Hidâye Şârihi', 'Bâbertî’nin Hocası'],
    tagsAr: ['شارح الهداية وشيخ البابرتي'],
    bioTr: 'el-Hidâye’yi şerh eden ve Ekmelüddin el-Bâbertî’yi yetiştiren fakih.',
    bioAr: 'تلميذ السغناقي وشيخ البابرتي، مؤلف معراج الدراية.',
  },
  {
    id: 'ibn-turkmani',
    nameAr: 'علاء الدين ابن التركماني',
    nameTr: 'Alâeddin İbnü’t-Türkmânî',
    deathH: 750,
    region: 'misir',
    tabaka: 6,
    teachers: ['suruci'],
    rolesTr: ['Mısır Hanefî Kâdılkudâtı'],
    rolesAr: ['قاضي القضاة بمصر'],
    worksTr: ['el-Cevherü’n-Nakî'],
    worksAr: ['الجوهر النقي على سنن البيهقي'],
    tagsTr: ['Hadis ve Fıkıh', 'Kâdılkudât'],
    tagsAr: ['فقيه ومحدث'],
    bioTr: 'Beyhakî’nin Sünen’ine Hanefî delilleriyle yazdığı el-Cevherü’n-Nakî ile tanınan başkadı.',
    bioAr: 'قاضي القضاة بمصر ومؤلف الجوهر النقي في الذب عن مذهب الحنفية.',
  },
  {
    id: 'ibn-fasih',
    nameAr: 'فخر الدين ابن الفصيح',
    nameTr: 'Fahreddin İbnü’l-Fasîh',
    deathH: 755,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['signaki', 'ebul-berekat-nesefi'],
    rolesTr: ['Şam Müderrisi'],
    rolesAr: ['فقيه ومدرس بدمشق'],
    worksTr: ['el-Müstahsen'],
    worksAr: ['المستحسن في شرح الكنز'],
    tagsTr: ['Kenz Şârihi'],
    tagsAr: ['شارح الكنز'],
    bioTr: 'Nesefî ve Sıgnâkî’nin talebesi, Şam Hanefî müderrisi.',
    bioAr: 'تلميذ النسفي والسغناقي ومدرس الحنفية بالشام.',
  },
  {
    id: 'itkani',
    nameAr: 'قوام الدين الإتقاني',
    nameTr: 'Kıvâmüddin el-İtkânî',
    deathH: 758,
    region: 'maveraunnehir',
    tabaka: 6,
    teachers: ['signaki'],
    rolesTr: ['Kahire Şeyhûniyye Şeyhi'],
    rolesAr: ['شيخ الشيخونية بالقاهرة'],
    worksTr: ['Gâyetü’l-Beyân (Hidâye Şerhi)'],
    worksAr: ['غاية البيان في شرح الهداية'],
    tagsTr: ['Hidâye Şârihi'],
    tagsAr: ['شارح الهداية'],
    bioTr: 'Türkistan’dan Kahire’ye gelip büyük Hidâye şerhi Gâyetü’l-Beyân’ı yazan fakih.',
    bioAr: 'صاحب غاية البيان في شرح الهداية وتلميذ السغناقي.',
  },
  {
    id: 'ibn-vehban',
    nameAr: 'أمين الدين ابن وهبان',
    nameTr: 'Emînüddin İbn Vehbân',
    deathH: 768,
    region: 'misir',
    tabaka: 6,
    teachers: ['ibn-fasih'],
    rolesTr: ['Şam Kadısı'],
    rolesAr: ['قاضي دمشق'],
    worksTr: ['el-Manzûmetü’l-Vehbâniyye'],
    worksAr: ['المنظومة الوهبانية'],
    tagsTr: ['Manzum Fıkıh'],
    tagsAr: ['صاحب الوهبانية'],
    bioTr: 'Meşhur Vehbâniyye fıkıh manzumesinin müellifi.',
    bioAr: 'قاضي دمشق وصاحب المنظومة الوهبانية الشهيرة.',
  },
  {
    id: 'baberti',
    nameAr: 'أكمل الدين البابرتي',
    nameTr: 'Ekmelüddin el-Bâbertî',
    deathH: 786,
    region: 'misir',
    tabaka: 6,
    teachers: ['kaki', 'abdulaziz-buhari'],
    rolesTr: ['Kahire Şeyhûniyye Başmüderrisi'],
    rolesAr: ['شيخ الحنفية بمصر'],
    worksTr: ['el-İnâye fî Şerhi’l-Hidâye', 'et-Takrîr'],
    worksAr: ['العناية في شرح الهداية', 'التقرير شرح أصول البزدوي'],
    tagsTr: ['Hidâye Şârihi', 'Osmanlı Ulemasının Hocası'],
    tagsAr: ['شارح الهداية وشيخ علماء الروم'],
    bioTr: 'Bayburtlu büyük alim; Molla Fenârî, Seyyid Şerîf ve Simâvî’nin hocası.',
    bioAr: 'صاحب العناية في شرح الهداية، وأستاذ ملا فناري والسيد الشريف الجرجاني.',
  },
  {
    id: 'ibn-receb',
    nameAr: 'ابن رجب الحنبلي',
    nameTr: 'İbn Receb el-Hanbelî',
    deathH: 795,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['zehebi'],
    rolesTr: ['Hâfız ve Fakih'],
    rolesAr: ['حافظ وفقيه'],
    worksTr: ['Câmiu’l-Ulûm ve’l-Hikem', 'el-Kavâid'],
    worksAr: ['جامع العلوم والحكم', 'القواعد الفقهية'],
    tagsTr: ['Muhaddis', 'Kavâid'],
    tagsAr: ['حافظ ومحدث'],
    bioTr: 'Hadis ve fıkıh kaideleriyle tanınan büyük Hanbelî alimi.',
    bioAr: 'الإمام الحافظ الفقيه، تلميذ الذهبي وشيخ ابن اللحام.',
  },

  // ==================== 9. HİCRÎ YÜZYIL (801–900) ====================
  {
    id: 'ibn-lehham',
    nameAr: 'ابن اللحام',
    nameTr: 'İbnü’l-Lehhâm',
    deathH: 803,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['ibn-receb'],
    rolesTr: ['Usulcü'],
    rolesAr: ['أصولي وفقيه'],
    worksTr: ['el-Kavâid ve’l-Fevâidü’l-Usûliyye'],
    worksAr: ['القواعد والفوائد الأصولية'],
    tagsTr: ['Usul'],
    tagsAr: ['أصولي'],
    bioTr: 'İbn Receb’in talebesi, usul alimi.',
    bioAr: 'تلميذ ابن رجب ومؤلف القواعد الأصولية.',
  },
  {
    id: 'iraki',
    nameAr: 'زين الدين العراقي',
    nameTr: 'Zeynüddin el-Irâkî',
    deathH: 806,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['ibn-turkmani'],
    rolesTr: ['Hâfızü’l-Asr'],
    rolesAr: ['حافظ العصر'],
    worksTr: ['Elfiyyetü’l-Irâkî', 'el-Muğnî an Hamli’l-Esfâr'],
    worksAr: ['ألفية العراقي', 'المغني عن حمل الأسفار'],
    tagsTr: ['Muhaddis', 'Aynî’nin Hocası'],
    tagsAr: ['شيخ المحدثين'],
    bioTr: 'Bedreddin el-Aynî’nin hadis hocası olan büyük muhaddis.',
    bioAr: 'حافظ العصر وشيخ بدر الدين العيني في الحديث.',
  },
  {
    id: 'ebul-velid-ibn-sihne',
    nameAr: 'أبو الوليد ابن الشحنة',
    nameTr: 'Ebü’l-Velîd İbnü’ş-Şıhne',
    deathH: 815,
    region: 'misir',
    tabaka: 6,
    teachers: ['itkani', 'baberti'],
    rolesTr: ['Halep ve Şam Kâdılkudâtı'],
    rolesAr: ['قاضي حلب ودمشق'],
    worksTr: ['Lisânü’l-Hükkâm'],
    worksAr: ['لسان الحكام'],
    tagsTr: ['Kâdılkudât', 'İbnü’l-Hümâm’ın Hocası'],
    tagsAr: ['شيخ ابن الهمام'],
    bioTr: 'Halep başkadısı, tarihçi ve İbnü’l-Hümâm’ın hocası.',
    bioAr: 'قاضي حلب، مؤلف لسان الحكام وشيخ الكمال ابن الهمام.',
  },
  {
    id: 'seyyid-serif',
    nameAr: 'السيد الشريف الجرجاني',
    nameTr: 'Seyyid Şerîf el-Cürcânî',
    deathH: 816,
    region: 'rum',
    tabaka: 6,
    teachers: ['baberti'],
    rolesTr: ['Şîraz ve Semerkant Başmüderrisi'],
    rolesAr: ['سلطان المحققين'],
    worksTr: ['et-Ta‘rîfât', 'Şerhu’l-Mevâkıf', 'Hâşiye ale’l-Hidâye'],
    worksAr: ['التعريفات', 'شرح المواقف', 'حاشية على الهداية'],
    tagsTr: ['Muhakkik', 'Kelam ve Usul'],
    tagsAr: ['محقق وشارح'],
    bioTr: 'Bâbertî’nin talebesi, kelam, usul ve mantıkta Osmanlı medreselerine yön veren muhakkik.',
    bioAr: 'تلميذ البابرتي، صاحب التعريفات وشرح المواقف.',
  },
  {
    id: 'simavi',
    nameAr: 'بدر الدين السماوي',
    nameTr: 'Şeyh Bedreddin es-Simâvî',
    deathH: 823,
    region: 'rum',
    tabaka: 6,
    teachers: ['baberti'],
    rolesTr: ['Kazasker', 'Fakih'],
    rolesAr: ['قاضي العسكر وفقيه'],
    worksTr: ['Câmiu’l-Fusûleyn', 'Letâifü’l-İşârât', 'et-Teshîl'],
    worksAr: ['جامع الفصولين', 'لطائف الإشارات', 'التسهيل'],
    tagsTr: ['Kazâ Hukuku', 'Osmanlı Havzası'],
    tagsAr: ['صاحب جامع الفصولين'],
    bioTr: 'Bâbertî’nin talebesi; kazâ hukukunda Câmiu’l-Fusûleyn’in müellifi.',
    bioAr: 'تلميذ البابرتي ومؤلف جامع الفصولين المعتمد عند القضاة.',
  },
  {
    id: 'kariul-hidaye',
    nameAr: 'سراج الدين قارئ الهداية',
    nameTr: 'Sirâceddin Kâriü’l-Hidâye',
    deathH: 829,
    region: 'misir',
    tabaka: 6,
    teachers: ['baberti'],
    rolesTr: ['Mısır Hanefî Müftüsü'],
    rolesAr: ['مفتي الحنفية بمصر'],
    worksTr: ['Fetâvâ Kâriü’l-Hidâye'],
    worksAr: ['فتاوى قارئ الهداية'],
    tagsTr: ['İbnü’l-Hümâm’ın Hocası'],
    tagsAr: ['شيخ ابن الهمام'],
    bioTr: 'Kemâleddin İbnü’l-Hümâm’ın baş fıkıh hocası.',
    bioAr: 'تلميذ البابرتي والشيخ الأكبر لكمال الدين ابن الهمام.',
  },
  {
    id: 'molla-fenari',
    nameAr: 'شمس الدين ملا فناري',
    nameTr: 'Molla Fenârî',
    deathH: 834,
    region: 'rum',
    tabaka: 6,
    teachers: ['baberti'],
    rolesTr: ['İlk Osmanlı Şeyhülislamı', 'Bursa Kadısı'],
    rolesAr: ['أول شيخ إسلام في الدولة العثمانية'],
    worksTr: ['Fusûlü’l-Bedâyi‘', 'Aynü’l-A‘yân'],
    worksAr: ['فصول البدائع في أصول الشرائع', 'عين الأعيان'],
    tagsTr: ['İlk Şeyhülislam', 'Osmanlı Ekolü Kurucusu', 'Usul'],
    tagsAr: ['مؤسس المدرسة العثمانية'],
    bioTr: 'Osmanlı Devleti’nin ilk Şeyhülislamı; Bâbertî’nin ilmini Anadolu’ya taşıyan kurucu alim.',
    bioAr: 'أول شيخ إسلام في الدولة العثمانية وصاحب فصول البدائع.',
  },
  {
    id: 'ibn-hatib-nasiriyye',
    nameAr: 'ابن خطيب الناصرية',
    nameTr: 'İbn Hatîb en-Nâsıriyye',
    deathH: 843,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['ebul-velid-ibn-sihne'],
    rolesTr: ['Halep Kadısı'],
    rolesAr: ['قاضي حلب'],
    worksTr: ['ed-Dürrü’l-Müntehab'],
    worksAr: ['الدر المنتخب في تاريخ حلب'],
    tagsTr: ['Tarihçi'],
    tagsAr: ['مؤرخ وقاضٍ'],
    bioTr: 'Halep kadısı ve tarihçisi.',
    bioAr: 'قاضي حلب ومؤرخها.',
  },
  {
    id: 'ayni',
    nameAr: 'بدر الدين العيني',
    nameTr: 'Bedreddin el-Aynî',
    deathH: 855,
    region: 'misir',
    tabaka: 6,
    teachers: ['iraki', 'ibn-turkmani'],
    rolesTr: ['Mısır Hanefî Kâdılkudâtı'],
    rolesAr: ['قاضي القضاة بمصر'],
    worksTr: ['el-Binâye (Hidâye Şerhi)', 'Umdetü’l-Kârî', 'Remzü’l-Hakâik'],
    worksAr: ['البناية شرح الهداية', 'عمدة القاري', 'رمز الحقائق'],
    tagsTr: ['Hidâye ve Kenz Şârihi', 'Buhârî Şârihi', 'Kâdılkudât'],
    tagsAr: ['شارح الهداية والبخاري'],
    bioTr: 'Gaziantepli büyük alim; Buhârî, Hidâye ve Kenz şerhleriyle meşhurdur.',
    bioAr: 'الإمام الحافظ الفقيه، شارح البخاري والهداية وكنز الدقائق.',
  },
  {
    id: 'ibn-humam',
    nameAr: 'كمال الدين ابن الهمام',
    nameTr: 'Kemâleddin İbnü’l-Hümâm',
    deathH: 861,
    region: 'misir',
    tabaka: 5,
    teachers: ['kariul-hidaye', 'ebul-velid-ibn-sihne'],
    rolesTr: ['Şeyhûniyye Başmüderrisi', 'Muhakkik'],
    rolesAr: ['المحقّق على الإطلاق'],
    worksTr: ['Fethu’l-Kadîr (Hidâye Şerhi)', 'et-Tahrîr', 'el-Müsâyere'],
    worksAr: ['فتح القدير', 'التحرير في الأصول', 'المسايرة'],
    tagsTr: ['Hidâye Şârihi', 'Muhakkik', 'Usul'],
    tagsAr: ['صاحب فتح القدير والتحرير'],
    bioTr: '“el-Muhakkik” unvanıyla anılan, Fethu’l-Kadîr ve et-Tahrîr’in müellifi büyük müçtehit-muhakkik.',
    bioAr: 'المحقق على الإطلاق، مؤلف فتح القدير في شرح الهداية والتحرير في الأصول.',
  },
  {
    id: 'molla-yegan',
    nameAr: 'ملا يكان (محمد بن أرمغان)',
    nameTr: 'Molla Yegân',
    deathH: 865,
    region: 'rum',
    tabaka: 6,
    teachers: ['molla-fenari'],
    rolesTr: ['Osmanlı Şeyhülislamı', 'Bursa Kadısı'],
    rolesAr: ['شيخ الإسلام العثماني'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['Şeyhülislam', 'Osmanlı Ekolü'],
    tagsAr: ['شيخ الإسلام'],
    bioTr: 'Molla Fenârî’nin halefi; Hızır Bey ve Molla Hüsrev’in hocası.',
    bioAr: 'خليفة ملا فناري وأستاذ خضر بك وملا خسرو.',
  },
  {
    id: 'hizir-bey',
    nameAr: 'خضر بك',
    nameTr: 'Hızır Bey',
    deathH: 865,
    region: 'rum',
    tabaka: 6,
    teachers: ['molla-yegan'],
    rolesTr: ['İlk İstanbul Kadısı'],
    rolesAr: ['أول قاضٍ لإسطنبول'],
    worksTr: ['el-Kasîdetü’n-Nûniyye'],
    worksAr: ['القصيدة النونية في العقائد'],
    tagsTr: ['İstanbul’un İlk Kadısı', 'Kelam'],
    tagsAr: ['أول قاضٍ للقسطنطينية'],
    bioTr: 'Fetih sonrası Fatih Sultan Mehmed tarafından tayin edilen ilk İstanbul kadısı.',
    bioAr: 'أول قاضٍ لإسطنبول بعد الفتح، وصاحب النونية في العقائد.',
  },
  {
    id: 'munavi',
    nameAr: 'يحيى بن محمد المناوي',
    nameTr: 'Yahyâ b. Muhammed el-Münâvî',
    deathH: 871,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['ibn-humam'],
    rolesTr: ['Mısır Şâfiî Başkadısı'],
    rolesAr: ['قاضي قضاة الشافعية بمصر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['حلقة إسناد'],
    bioTr: 'Süyûtî, Sehâvî ve Zekeriyyâ el-Ensârî’nin hocalarından.',
    bioAr: 'من شيوخ السيوطي والسخاوي وزكريا الأنصاري.',
  },
  {
    id: 'necmeddin-kadi-aclun',
    nameAr: 'نجم الدين ابن قاضي عجلون',
    nameTr: 'Necmeddin İbn Kâdî Aclûn',
    deathH: 876,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['ibn-hatib-nasiriyye', 'ibn-humam'],
    rolesTr: ['Şam Müderrisi'],
    rolesAr: ['شيخ الشام'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['حلقة إسناد'],
    bioTr: 'Şam ulemasından ve Takıyyüddin İbn Kâdî Aclûn’un kardeşi/hocası.',
    bioAr: 'من كبار علماء دمشق.',
  },
  {
    id: 'ibn-kutluboga',
    nameAr: 'قاسم ابن قطلوبغا',
    nameTr: 'Kâsım İbn Kutluboğa',
    deathH: 879,
    region: 'misir',
    tabaka: 6,
    teachers: ['ibn-humam'],
    rolesTr: ['Muhaddis ve Fakih'],
    rolesAr: ['الإمام الفقيه المحدث'],
    worksTr: ['Tâcü’t-Terâcim', 'et-Tashîh ve’t-Tercîh'],
    worksAr: ['تاج التراجم في طبقات الحنفية', 'التصحيح والترجيح على القدوري'],
    tagsTr: ['Tabakat Müellifi', 'Tercîh'],
    tagsAr: ['مؤلف تاج التراجم'],
    bioTr: 'Hanefî tabakat klasiği Tâcü’t-Terâcim’in müellifi ve İbnü’l-Hümâm’ın baş talebesi.',
    bioAr: 'أبرز تلاميذ ابن الهمام ومؤلف تاج التراجم في طبقات الحنفية.',
  },
  {
    id: 'molla-husrev',
    nameAr: 'ملا خسرو (محمد بن فرامرز)',
    nameTr: 'Molla Hüsrev',
    deathH: 885,
    region: 'rum',
    tabaka: 6,
    teachers: ['molla-yegan', 'molla-fenari'],
    rolesTr: ['Osmanlı Şeyhülislamı', 'Kazasker'],
    rolesAr: ['شيخ الإسلام العثماني'],
    worksTr: ['Dürerü’l-Hükkâm (Gurer Şerhi)', 'Mir’âtü’l-Usûl'],
    worksAr: ['درر الحكام شرح غرر الأحكام', 'مرآة الأصول'],
    tagsTr: ['Şeyhülislam', 'Osmanlı Medrese Metni', 'Usul'],
    tagsAr: ['صاحب الدرر ومرآة الأصول'],
    bioTr: 'Fatih’in “zamanın Ebû Hanîfe’si” dediği, Dürer ve Mir’ât müellifi Osmanlı Şeyhülislamı.',
    bioAr: 'شيخ الإسلام في عهد السلطان الفاتح، صاحب درر الحكام ومرآة الأصول.',
  },
  {
    id: 'hocazade',
    nameAr: 'مصلح الدين خواجه زاده',
    nameTr: 'Hocazâde Muslihuddin',
    deathH: 893,
    region: 'rum',
    tabaka: 6,
    teachers: ['hizir-bey'],
    rolesTr: ['Kazasker', 'İstanbul ve Bursa Kadısı'],
    rolesAr: ['قاضي العسكر بإسطنبول'],
    worksTr: ['Tehâfütü’l-Felâsife'],
    worksAr: ['تهافت الفلاسفة'],
    tagsTr: ['Kelam / Felsefe', 'Osmanlı Ekolü'],
    tagsAr: ['متكلم وفيلسوف'],
    bioTr: 'Fatih devrinin büyük kelamcı ve fakihi; İbn Kemal’in hocalarından.',
    bioAr: 'تلميذ خضر بك وصاحب كتاب التهافت ومن شيوخ ابن كمال.',
  },

  // ==================== 10. HİCRÎ YÜZYIL (901–1000) ====================
  {
    id: 'kesteli',
    nameAr: 'مصلح الدين القسطلاني (كستلي)',
    nameTr: 'Molla Kestelî',
    deathH: 901,
    region: 'rum',
    tabaka: 6,
    teachers: ['hizir-bey'],
    rolesTr: ['Rumeli ve Anadolu Kazaskeri'],
    rolesAr: ['قاضي العسكر'],
    worksTr: ['Hâşiye alâ Şerhi’l-Akâid'],
    worksAr: ['حاشية على شرح العقائد النسفية'],
    tagsTr: ['Kelam', 'Osmanlı Ekolü'],
    tagsAr: ['صاحب حاشية الكستلي'],
    bioTr: 'Şerhu’l-Akâid haşiyesiyle meşhur Osmanlı kazaskeri.',
    bioAr: 'قاضي العسكر وصاحب الحاشية الشهيرة على شرح العقائد.',
  },
  {
    id: 'sehavi',
    nameAr: 'شمس الدين السخاوي',
    nameTr: 'Şemseddin es-Sehâvî',
    deathH: 902,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['munavi', 'ibn-humam'],
    rolesTr: ['Hâfız ve Tarihçi'],
    rolesAr: ['الحافظ المؤرخ'],
    worksTr: ['ed-Dav’ü’l-Lâmi‘', 'Fethu’l-Muğîs'],
    worksAr: ['الضوء اللامع', 'فتح المغيث'],
    tagsTr: ['Muhaddis', 'Biyografi'],
    tagsAr: ['حافظ ومؤرخ'],
    bioTr: 'Hadis usulü ve 9. yüzyıl biyografilerinin büyük hafızı.',
    bioAr: 'الحافظ المؤرخ، صاحب الضوء اللامع وفتح المغيث.',
  },
  {
    id: 'suyuti',
    nameAr: 'جلال الدين السيوطي',
    nameTr: 'Celâleddin es-Süyûtî',
    deathH: 911,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['munavi', 'ibn-kutluboga'],
    rolesTr: ['Müsennif-i Mısır'],
    rolesAr: ['الحافظ الموسوعي'],
    worksTr: ['el-Eşbâh ve’n-Nezâir', 'el-İtkân'],
    worksAr: ['الأشباه والنظائر', 'الإتقان في علوم القرآن'],
    tagsTr: ['Çok Yönlü Alim', 'İsnad'],
    tagsAr: ['عالم موسوعي'],
    bioTr: 'İbn Tolun ve Bedreddin el-Gazzî’ye isnad aktaran büyük Şâfiî ansiklopedist alim.',
    bioAr: 'العالم الموسوعي، أخذ عنه ابن طولون وبدر الدين الغزي.',
  },
  {
    id: 'zekeriya-ensari',
    nameAr: 'زكريا الأنصاري',
    nameTr: 'Zekeriyyâ el-Ensârî',
    deathH: 926,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['ibn-humam', 'munavi'],
    rolesTr: ['Şeyhülislam-ı Mısır'],
    rolesAr: ['شيخ الإسلام بمصر'],
    worksTr: ['Fethu’l-Vehhâb'],
    worksAr: ['فتح الوهاب'],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['شيخ الإسلام'],
    bioTr: 'Mısır-Şam hadis ve fıkıh isnadında kilit rol oynayan Şâfiî Şeyhülislamı.',
    bioAr: 'شيخ الإسلام بمصر وحلقة وصل رئيسية في الإسناد العلمي.',
  },
  {
    id: 'takiyyuddin-aclun',
    nameAr: 'تقي الدين ابن قاضي عجلون',
    nameTr: 'Takıyyüddin İbn Kâdî Aclûn',
    deathH: 928,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['necmeddin-kadi-aclun'],
    rolesTr: ['Şam Şeyhülislamı'],
    rolesAr: ['شيخ الإسلام بدمشق'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['حلقة إسناد'],
    bioTr: 'Şam’da İbn Tolun ve İbn Sultân’ın hocası.',
    bioAr: 'شيخ الإسلام بالشام وأستاذ ابن طولون وابن سلطان.',
  },
  {
    id: 'ibn-kemal',
    nameAr: 'أحمد ابن كمال (باشا زاده)',
    nameTr: 'İbn Kemal Paşazâde',
    deathH: 940,
    region: 'rum',
    tabaka: 6,
    teachers: ['molla-husrev', 'hocazade', 'kesteli'],
    rolesTr: ['Osmanlı Şeyhülislamı', 'Müftiyyü’s-Sekaleyn'],
    rolesAr: ['شيخ الإسلام ومفتي الثقلين'],
    worksTr: ['Tabakâtü’l-Fukahâ', 'el-Îzâh', 'Tağyîrü’t-Tenkîh'],
    worksAr: ['طبقات الفقهاء', 'الإيضاح في شرح الإصلاح', 'تغيير التنقيح'],
    tagsTr: ['Şeyhülislam', '7’li Tabakat Tasnifi', 'Hidâye Şârihi'],
    tagsAr: ['واضع تقسيم الطبقات السبع'],
    bioTr: 'Hanefî fakihlerinin meşhur 7’li tabakat tasnifini ortaya koyan Osmanlı Şeyhülislamı.',
    bioAr: 'شيخ الإسلام العثماني وصاحب الرسالة الشهيرة في طبقات الفقهاء السبع.',
  },
  {
    id: 'sadi-celebi',
    nameAr: 'سعدي جلبي',
    nameTr: 'Sa‘dî Çelebi',
    deathH: 945,
    region: 'rum',
    tabaka: 6,
    teachers: ['molla-husrev'],
    rolesTr: ['Osmanlı Şeyhülislamı'],
    rolesAr: ['شيخ الإسلام العثماني'],
    worksTr: ['Hâşiye ale’l-İnâye (Sa‘dî Çelebi Haşiyesi)'],
    worksAr: ['حاشية على العناية شرح الهداية'],
    tagsTr: ['Şeyhülislam', 'Hidâye Haşiyesi'],
    tagsAr: ['شيخ الإسلام ومحشّي الهداية'],
    bioTr: 'Bâbertî’nin el-İnâye şerhine yazdığı kıymetli haşiyeyle tanınan Şeyhülislam.',
    bioAr: 'شيخ الإسلام وصاحب الحاشية المطبوعة مع فتح القدير والعناية.',
  },
  {
    id: 'ibn-selebi',
    nameAr: 'شهاب الدين أحمد ابن الشلبي',
    nameTr: 'Şihâbeddin İbnü’ş-Şelebî',
    deathH: 947,
    region: 'misir',
    tabaka: 6,
    teachers: ['ibn-kutluboga'],
    rolesTr: ['Mısır Hanefî Müftüsü'],
    rolesAr: ['مفتي الحنفية بمصر'],
    worksTr: ['Hâşiye alâ Tebyîni’l-Hakâik'],
    worksAr: ['حاشية على تبيين الحقائق للزيلعي'],
    tagsTr: ['İbn Nüceym’in Hocası', 'Kenz Haşiyesi'],
    tagsAr: ['شيخ ابن نجيم'],
    bioTr: 'Zeylaî’nin Kenz şerhine yazdığı haşiyeyle meşhur, Zeynüddin İbn Nüceym’in hocası.',
    bioAr: 'صاحب الحاشية على الزيلعي وشيخ زين الدين ابن نجيم.',
  },
  {
    id: 'ibn-sultan',
    nameAr: 'محمد بن سلطان الدمشقي',
    nameTr: 'İbn Sultân ed-Dımaşkî',
    deathH: 950,
    region: 'misir',
    tabaka: 6,
    teachers: ['takiyyuddin-aclun'],
    rolesTr: ['Şam Hanefî Müftüsü'],
    rolesAr: ['مفتي الحنفية بدمشق'],
    worksTr: ['Fetâvâ İbn Sultân'],
    worksAr: ['الفتاوى'],
    tagsTr: ['Şam Havzası'],
    tagsAr: ['مفتي الشام'],
    bioTr: '10. yüzyılda Şam Hanefîlerinin önde gelen müftüsü.',
    bioAr: 'مفتي الحنفية بدمشق وتلميذ ابن قاضي عجلون.',
  },
  {
    id: 'ibn-tolun',
    nameAr: 'شمس الدين ابن طولون',
    nameTr: 'Şemseddin İbn Tolun',
    deathH: 953,
    region: 'misir',
    tabaka: 6,
    teachers: ['suyuti', 'takiyyuddin-aclun'],
    rolesTr: ['Şam Tarihçisi ve Fakihi'],
    rolesAr: ['مؤرخ الشام وفقيهها'],
    worksTr: ['el-Gurefü’l-Aliyye fî Terâcimi’l-Hanefiyye'],
    worksAr: ['الغرف العلية في تراجم متأخري الحنفية'],
    tagsTr: ['Tabakat Müellifi', 'Tarihçi'],
    tagsAr: ['مؤرخ ومصنف طبقات'],
    bioTr: 'Çok velud Şamlı Hanefî fakihi ve tarihçisi.',
    bioAr: 'المؤرخ الفقيه الحنفي، صاحب الغرف العلية في طبقات الحنفية.',
  },
  {
    id: 'sihabeddin-remli',
    nameAr: 'شهاب الدين الرملي',
    nameTr: 'Şihâbeddin er-Remlî',
    deathH: 957,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['zekeriya-ensari'],
    rolesTr: ['Mısır Şâfiî Müftüsü'],
    rolesAr: ['مفتي الديار المصرية'],
    worksTr: ['Fetâva’r-Remlî'],
    worksAr: ['فتاوى الرملي'],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['حلقة إسناد'],
    bioTr: 'Zekeriyyâ el-Ensârî’nin talebesi ve Şemseddin er-Remlî’nin babası.',
    bioAr: 'تلميذ زكريا الأنصاري ووالد شمس الدين الرملي.',
  },
  {
    id: 'seriyyuddin-sihne',
    nameAr: 'سري الدين ابن الشحنة',
    nameTr: 'Seriyyüddin İbnü’ş-Şıhne',
    deathH: 961,
    region: 'misir',
    tabaka: 6,
    teachers: ['ibn-kutluboga'],
    rolesTr: ['Kahire Hanefî Başkadısı'],
    rolesAr: ['قاضي الحنفية بمصر'],
    worksTr: ['Şerhu’l-Vehbâniyye'],
    worksAr: ['شرح المنظومة الوهبانية'],
    tagsTr: ['İbn Nüceym’in Hocası'],
    tagsAr: ['شيخ ابن نجيم'],
    bioTr: 'Vehbâniyye şerhiyle tanınan, İbn Nüceym’in hocalarından.',
    bioAr: 'قاضي مصر وشارح الوهبانية ومن شيوخ ابن نجيم.',
  },
  {
    id: 'zeynuddin-ibn-nuceym',
    nameAr: 'زين الدين ابن نجيم',
    nameTr: 'Zeynüddin İbn Nüceym',
    deathH: 970,
    region: 'misir',
    tabaka: 6,
    teachers: ['ibn-selebi', 'seriyyuddin-sihne'],
    rolesTr: ['Mısır Hanefîleri Reisi'],
    rolesAr: ['إمام الحنفية بمصر في عصره'],
    worksTr: ['el-Eşbâh ve’n-Nezâir', 'el-Bahrü’r-Râik (Kenz Şerhi)'],
    worksAr: ['الأشباه والنظائر', 'البحر الرائق شرح كنز الدقائق'],
    tagsTr: ['Kavâid Otoritesi', 'Kenz Şârihi', '6. Tabaka'],
    tagsAr: ['صاحب الأشباه والبحر الرائق'],
    bioTr: 'Mecelle’nin temel kaynağı olan el-Eşbâh ve’n-Nezâir ile el-Bahrü’r-Râik’in müellifi.',
    bioAr: 'صاحب الأشباه والنظائر والبحر الرائق، من أعظم فقهاء الحنفية المتأخرين.',
  },
  {
    id: 'ebussuud',
    nameAr: 'أبو السعود أفندي',
    nameTr: 'Ebüssuûd Efendi',
    deathH: 982,
    region: 'rum',
    tabaka: 6,
    teachers: ['ibn-kemal', 'sadi-celebi'],
    rolesTr: ['Osmanlı Şeyhülislamı (30 yıl)', 'Muallim-i Sânî'],
    rolesAr: ['شيخ الإسلام العثماني (٣٠ سنة)'],
    worksTr: ['İrşâdü’l-Akli’s-Selîm (Tefsir)', 'Ma‘rûzât', 'Fetâvâ'],
    worksAr: ['إرشاد العقل السليم', 'المعروضات', 'الفتاوى'],
    tagsTr: ['Şeyhülislam', 'Müfessir', 'Osmanlı Hukuku'],
    tagsAr: ['شيخ الإسلام والمفسر'],
    bioTr: 'Kanunî devrinde Osmanlı hukukunu ve fetva geleneğini zirveye taşıyan büyük Şeyhülislam.',
    bioAr: 'شيخ الإسلام في عهد السلطان سليمان القانوني وصاحب التفسير الشهير.',
  },
  {
    id: 'bedreddin-gazzi',
    nameAr: 'بدر الدين الغزي',
    nameTr: 'Bedreddin el-Gazzî',
    deathH: 984,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['zekeriya-ensari', 'suyuti'],
    rolesTr: ['Şam Şâfiî Müftüsü'],
    rolesAr: ['مفتي الشام'],
    worksTr: ['el-Mütâli‘u’l-Bedriyye'],
    worksAr: ['المطالع البدرية'],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['حلقة إسناد'],
    bioTr: 'Şam’da Süyûtî ve Zekeriyyâ el-Ensârî’nin ilmini aktaran alim.',
    bioAr: 'عالم الشام ومفتيها، ووالد نجم الدين الغزي.',
  },
  {
    id: 'kadizade',
    nameAr: 'قاضي زاده شمس الدين أحمد',
    nameTr: 'Kâdızâde Şemseddin Ahmed',
    deathH: 988,
    region: 'rum',
    tabaka: 6,
    teachers: ['ebussuud', 'sadi-celebi'],
    rolesTr: ['Osmanlı Şeyhülislamı'],
    rolesAr: ['شيخ الإسلام العثماني'],
    worksTr: ['Netâicü’l-Efkâr (Tekmile-i Fethu’l-Kadîr)'],
    worksAr: ['نتائج الأفكار تكملة فتح القدير'],
    tagsTr: ['Şeyhülislam', 'Hidâye Şârihi'],
    tagsAr: ['مكمل فتح القدير'],
    bioTr: 'İbnü’l-Hümâm’ın yarım kalan Fethu’l-Kadîr şerhini tamamlayan Osmanlı Şeyhülislamı.',
    bioAr: 'شيخ الإسلام العثماني الذي أكمل فتح القدير بكتابه نتائج الأفكار.',
  },

  // ==================== 11. HİCRÎ YÜZYIL (1001–1100) ====================
  {
    id: 'nuruddin-ibn-ganim',
    nameAr: 'نور الدين ابن غانم المقدسي',
    nameTr: 'Nûreddin İbn Gânim el-Makdisî',
    deathH: 1004,
    region: 'misir',
    tabaka: 6,
    teachers: ['zeynuddin-ibn-nuceym', 'sihabeddin-remli'],
    rolesTr: ['Kudüs ve Kahire Hanefî Şeyhi'],
    rolesAr: ['شيخ الحنفية بمصر والقدس'],
    worksTr: ['Nûrü’l-Ayn fî Islâhi Câmii’l-Fusûleyn'],
    worksAr: ['نور العين في إصلاح جامع الفصولين'],
    tagsTr: ['Şürünbülâlî’nin Hocası'],
    tagsAr: ['شيخ الشرنبلالي'],
    bioTr: 'Zeynüddin İbn Nüceym’in talebesi ve Hasan eş-Şürünbülâlî’nin hocası.',
    bioAr: 'تلميذ ابن نجيم وشيخ حسن الشرنبلالي.',
  },
  {
    id: 'semseddin-remli',
    nameAr: 'شمس الدين الرملي',
    nameTr: 'Şemseddin er-Remlî',
    deathH: 1004,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['sihabeddin-remli'],
    rolesTr: ['Şâfiî es-Sağîr'],
    rolesAr: ['الشافعي الصغير'],
    worksTr: ['Nihâyetü’l-Muhtâc'],
    worksAr: ['نهاية المحتاج'],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['الشافعي الصغير'],
    bioTr: 'Mısır’ın büyük Şâfiî imamı ve Şinnavî’nin hocası.',
    bioAr: 'الملقب بالشافعي الصغير وشيخ الشنواني.',
  },
  {
    id: 'siraceddin-ibn-nuceym',
    nameAr: 'سراج الدين عمر ابن نجيم',
    nameTr: 'Sirâceddin İbn Nüceym',
    deathH: 1005,
    region: 'misir',
    tabaka: 6,
    teachers: ['zeynuddin-ibn-nuceym'],
    rolesTr: ['Mısır Hanefî Fakihi'],
    rolesAr: ['فقيه الحنفية بمصر'],
    worksTr: ['en-Nehrü’l-Fâik (Kenz Şerhi)'],
    worksAr: ['النهر الفائق شرح كنز الدقائق'],
    tagsTr: ['Kenz Şârihi', 'Hayreddin er-Remlî’nin Hocası'],
    tagsAr: ['صاحب النهر الفائق'],
    bioTr: 'Zeynüddin İbn Nüceym’in kardeşi ve en-Nehrü’l-Fâik müellifi.',
    bioAr: 'أخو زين الدين ابن نجيم وصاحب النهر الفائق.',
  },
  {
    id: 'sinnavi',
    nameAr: 'أبو بكر الشنواني',
    nameTr: 'Ebû Bekr eş-Şinnavî',
    deathH: 1019,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['semseddin-remli'],
    rolesTr: ['Ezher Alimi'],
    rolesAr: ['عالم الأزهر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['حلقة إسناد'],
    bioTr: 'Hayreddin er-Remlî’nin Ezher’deki hocalarından.',
    bioAr: 'من شيوخ خير الدين الرملي بالأزهر.',
  },
  {
    id: 'necmeddin-gazzi',
    nameAr: 'نجم الدين الغزي',
    nameTr: 'Necmeddin el-Gazzî',
    deathH: 1061,
    region: 'misir',
    tabaka: 0,
    nonHanafi: true,
    teachers: ['bedreddin-gazzi'],
    rolesTr: ['Şam Tarihçisi ve Muhaddisi'],
    rolesAr: ['مؤرخ الشام ومحدثها'],
    worksTr: ['el-Kevâkibü’s-Sâire'],
    worksAr: ['الكواكب السائرة بأعيان المائة العاشرة'],
    tagsTr: ['Tarihçi', 'Haskefî’nin Hocası'],
    tagsAr: ['مؤرخ ومحدث'],
    bioTr: 'Haskefî ve Nâblusî’ye hadis ve icazet veren Şamlı büyük tarihçi.',
    bioAr: 'مؤرخ الشام، أخذ عنه الحصكفي وإسماعيل النابلسي.',
  },
  {
    id: 'ismail-nablusi',
    nameAr: 'إسماعيل النابلسي',
    nameTr: 'İsmâil en-Nâblusî',
    deathH: 1062,
    region: 'misir',
    tabaka: 6,
    teachers: ['necmeddin-gazzi', 'nuruddin-ibn-ganim'],
    rolesTr: ['Şam Hanefî Fakihi'],
    rolesAr: ['فقيه الحنفية بدمشق'],
    worksTr: ['el-İhkâm Şerhu Düreri’l-Hükkâm'],
    worksAr: ['الإحكام شرح درر الحكام'],
    tagsTr: ['Dürer Şârihi'],
    tagsAr: ['شارح الدرر'],
    bioTr: 'Molla Hüsrev’in Dürer’ine kapsamlı şerh yazan Şamlı fakih.',
    bioAr: 'صاحب الإحكام في شرح درر الحكام لملا خسرو.',
  },
  {
    id: 'surunbulali',
    nameAr: 'حسن الشرنبلالي',
    nameTr: 'Hasan eş-Şürünbülâlî',
    deathH: 1069,
    region: 'misir',
    tabaka: 6,
    teachers: ['nuruddin-ibn-ganim'],
    rolesTr: ['Ezher Hanefî Başmüderrisi'],
    rolesAr: ['شيخ الحنفية بالأزهر'],
    worksTr: ['Nûrü’l-Îzâh', 'Merâkı’l-Felâh', 'Gunyetü Zevi’l-Ahkâm'],
    worksAr: ['نور الإيضاح', 'مراقي الفلاح', 'غنية ذوي الأحكام'],
    tagsTr: ['İbadet Fıkhı Klasiği', 'Dürer Haşiyesi'],
    tagsAr: ['صاحب نور الإيضاح ومراقي الفلاح'],
    bioTr: 'Nûrü’l-Îzâh ve Merâkı’l-Felâh eserleriyle ibadet fıkhında meşhur Ezher alimi.',
    bioAr: 'شيخ الحنفية بالأزهر ومؤلف نور الإيضاح ومراقي الفلاح.',
  },
  {
    id: 'hayreddin-remli',
    nameAr: 'خير الدين بن أحمد الرملي',
    nameTr: 'Hayreddin er-Remlî',
    deathH: 1081,
    region: 'misir',
    tabaka: 6,
    teachers: ['sinnavi', 'siraceddin-ibn-nuceym'],
    rolesTr: ['Filistin / Şam Müftüsü'],
    rolesAr: ['مفتي الحنفية بفلسطين والشام'],
    worksTr: ['el-Fetâva’l-Hayriyye'],
    worksAr: ['الفتاوى الخيرية لنفع البرية'],
    tagsTr: ['Fetva Otoritesi', 'Haskefî’nin Hocası'],
    tagsAr: ['صاحب الفتاوى الخيرية'],
    bioTr: 'Osmanlı dönemi Şam-Filistin havzasının en etkili Hanefî müftüsü; Haskefî’nin hocası.',
    bioAr: 'مرجع الفتوى في عصره وشيخ علاء الدين الحصكفي.',
  },
  {
    id: 'haskefi',
    nameAr: 'علاء الدين الحصكفي',
    nameTr: 'Alâeddin el-Haskefî',
    deathH: 1088,
    region: 'misir',
    tabaka: 6,
    teachers: ['hayreddin-remli', 'necmeddin-gazzi'],
    rolesTr: ['Şam Hanefî Müftüsü'],
    rolesAr: ['مفتي الحنفية بدمشق'],
    worksTr: ['ed-Dürrü’l-Muhtâr', 'ed-Dürrü’l-Müntekâ'],
    worksAr: ['الدر المختار شرح تنوير الأبصار', 'الدر المنتقى'],
    tagsTr: ['ed-Dürrü’l-Muhtâr Müellifi'],
    tagsAr: ['صاحب الدر المختار'],
    bioTr: 'İbn Âbidîn’in Reddü’l-Muhtâr ile haşiye yazdığı ed-Dürrü’l-Muhtâr’ın müellifi.',
    bioAr: 'مفتي دمشق ومؤلف الدر المختار الذي وضع عليه ابن عابدين حاشيته الشهيرة.',
  },

  // ==================== 12. HİCRÎ YÜZYIL (1101–1200) ====================
  {
    id: 'hasan-surunbulali',
    nameAr: 'حسن بن حسن الشرنبلالي',
    nameTr: 'Hasan b. Hasan eş-Şürünbülâlî',
    deathH: 1123,
    region: 'misir',
    tabaka: 7,
    teachers: ['surunbulali'],
    rolesTr: ['Ezher Müderrisi'],
    rolesAr: ['مدرس بالأزهر'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['İsnad Halkası'],
    tagsAr: ['حلقة إسناد'],
    bioTr: 'Hasan eş-Şürünbülâlî’nin oğlu ve Cebertî’nin hocası.',
    bioAr: 'ابن الإمام الشرنبلالي وشيخ حسن الجبرتي.',
  },
  {
    id: 'ceberti',
    nameAr: 'حسن بن إبراهيم الجبرتي',
    nameTr: 'Hasan b. İbrâhim el-Cebertî',
    deathH: 1188,
    region: 'misir',
    tabaka: 7,
    teachers: ['hasan-surunbulali'],
    rolesTr: ['Ezher Hanefî Şeyhi'],
    rolesAr: ['شيخ الحنفية بمصر'],
    worksTr: ['el-İkdü’s-Semîn'],
    worksAr: ['العقد الثمين'],
    tagsTr: ['Zebîdî’nin Hocası'],
    tagsAr: ['شيخ الزبيدي'],
    bioTr: 'Murtazâ ez-Zebîdî’nin fıkıh hocası ve tarihçi Cebertî’nin babası.',
    bioAr: 'شيخ الحنفية بمصر وأستاذ محمد مرتضى الزبيدي.',
  },

  // ==================== 13. HİCRÎ YÜZYIL (1201–1300) ====================
  {
    id: 'zebidi',
    nameAr: 'محمد مرتضى الزبيدي',
    nameTr: 'Muhammed Murtazâ ez-Zebîdî',
    deathH: 1205,
    region: 'misir',
    tabaka: 6,
    teachers: ['ceberti', 'ismail-nablusi'],
    rolesTr: ['Lügavî, Muhaddis ve Fakih'],
    rolesAr: ['علامة العصر'],
    worksTr: ['Tâcü’l-Arûs', 'İthâfü’s-Sâdeti’l-Müttakîn', 'Ukûdü’l-Cevâhiri’l-Münîfe'],
    worksAr: ['تاج العروس', 'إتحاف السادة المتقين', 'عقود الجواهر المنيفة'],
    tagsTr: ['Hadis ve Fıkıh', 'İsnad'],
    tagsAr: ['صاحب تاج العروس وعقود الجواهر'],
    bioTr: 'Ebû Hanîfe’nin hadis delillerini Ukûdü’l-Cevâhir’de toplayan dev ansiklopedist alim.',
    bioAr: 'صاحب تاج العروس وعقود الجواهر المنيفة في أدلة مذهب أبي حنيفة.',
  },
  {
    id: 'akkad',
    nameAr: 'محمد شاكر العقاد',
    nameTr: 'Muhammed Şâkir el-Akkâd',
    deathH: 1222,
    region: 'misir',
    tabaka: 7,
    teachers: ['zebidi'],
    rolesTr: ['Şam Hanefî Üstadı'],
    rolesAr: ['شيخ ابن عابدين'],
    worksTr: [],
    worksAr: [],
    tagsTr: ['İbn Âbidîn’in Baş Hocası'],
    tagsAr: ['شيخ ابن عابدين الأكبر'],
    bioTr: 'İbn Âbidîn’i Hanefî fıkhına yönlendiren ve yetiştiren Şamlı baş hocası.',
    bioAr: 'الشيخ الأكبر لابن عابدين وهو الذي وجهه للتعمق في المذهب الحنفي.',
  },
  {
    id: 'ibn-abidin',
    nameAr: 'محمد أمين ابن عابدين',
    nameTr: 'Muhammed Emîn İbn Âbidîn',
    deathH: 1252,
    region: 'misir',
    tabaka: 6,
    teachers: ['akkad', 'haskefi'],
    rolesTr: ['Hâtimetü’l-Muhakkikîn', 'Şam Fetva Emini'],
    rolesAr: ['خاتمة المحققين وأمين الفتوى بدمشق'],
    worksTr: ['Reddü’l-Muhtâr (İbn Âbidîn Haşiyesi)', 'Ukûdü Resmi’l-Müftî', 'el-Ukûdü’d-Dürriyye'],
    worksAr: ['رد المحتار على الدر المختار', 'عقود رسم المفتي', 'العقود الدرية'],
    tagsTr: ['Hâtimetü’l-Muhakkikîn', 'Fetva Usulü'],
    tagsAr: ['صاحب الحاشية الشهيرة'],
    bioTr: 'Son dönem Hanefî fıkhının en büyük muhakkiki; Reddü’l-Muhtâr ve Resmi’l-Müftî müellifi.',
    bioAr: 'خاتمة المحققين في المذهب الحنفي، وصاحب حاشية رد المحتار المعتمدة للفتوى.',
  },
  {
    id: 'meydani',
    nameAr: 'عبد الغني الغنيمي الميداني',
    nameTr: 'Abdülganî el-Meydânî',
    deathH: 1298,
    region: 'misir',
    tabaka: 7,
    teachers: ['ibn-abidin'],
    rolesTr: ['Şam Hanefî Üstadı'],
    rolesAr: ['شيخ الحنفية بالشام'],
    worksTr: ['el-Lübâb fî Şerhi’l-Kitâb', 'Şerhu’l-Akîdeti’t-Tahâviyye'],
    worksAr: ['اللباب في شرح الكتاب', 'شرح العقيدة الطحاوية'],
    tagsTr: ['Kudûrî Şârihi', 'İbn Âbidîn’in Talebesi'],
    tagsAr: ['صاحب اللباب'],
    bioTr: 'İbn Âbidîn’in en seçkin talebesi ve el-Lübâb (Kudûrî şerhi) müellifi.',
    bioAr: 'تلميذ ابن عابدين ومؤلف اللباب في شرح مختصر القدوري.',
  },
];


// ===== src/engine/layout.js =====
// Century-Aligned & Compact Silsile Layout Engine with Crossing Minimization and Person-Focus Subgraph


function buildAdjacency(scholars) {
  const byId = new Map();
  const childrenMap = new Map();
  const parentsMap = new Map();

  for (const s of scholars) {
    byId.set(s.id, s);
    childrenMap.set(s.id, []);
    parentsMap.set(s.id, []);
  }

  for (const s of scholars) {
    const teachers = Array.isArray(s.teachers) ? s.teachers : [];
    for (const tId of teachers) {
      if (byId.has(tId) && tId !== s.id) {
        parentsMap.get(s.id).push(tId);
        childrenMap.get(tId).push(s.id);
      }
    }
  }

  return { byId, childrenMap, parentsMap };
}

function computeLineage(scholars, targetId, direction = 'both') {
  const { byId, childrenMap, parentsMap } = buildAdjacency(scholars);
  const ancestors = new Set();
  const descendants = new Set();

  if (!targetId || !byId.has(targetId)) {
    return { activeSet: null, ancestors, descendants, directTeachers: [], directStudents: [] };
  }

  // BFS Upwards (Teachers / Ancestors)
  const upQueue = [...(parentsMap.get(targetId) || [])];
  while (upQueue.length > 0) {
    const curr = upQueue.shift();
    if (!ancestors.has(curr) && curr !== targetId) {
      ancestors.add(curr);
      for (const p of parentsMap.get(curr) || []) {
        if (!ancestors.has(p)) upQueue.push(p);
      }
    }
  }

  // BFS Downwards (Students / Descendants)
  const downQueue = [...(childrenMap.get(targetId) || [])];
  while (downQueue.length > 0) {
    const curr = downQueue.shift();
    if (!descendants.has(curr) && curr !== targetId) {
      descendants.add(curr);
      for (const ch of childrenMap.get(curr) || []) {
        if (!descendants.has(ch)) downQueue.push(ch);
      }
    }
  }

  const activeSet = new Set([targetId]);
  if (direction === 'both' || direction === 'ancestors') {
    for (const a of ancestors) activeSet.add(a);
  }
  if (direction === 'both' || direction === 'descendants') {
    for (const d of descendants) activeSet.add(d);
  }

  return {
    activeSet,
    ancestors,
    descendants,
    directTeachers: (parentsMap.get(targetId) || []).map((id) => byId.get(id)).filter(Boolean),
    directStudents: (childrenMap.get(targetId) || []).map((id) => byId.get(id)).filter(Boolean),
  };
}

function estimateCardSize(scholar, options) {
  const {
    lang = 'both',
    showTabaka = false,
    showRegion = false,
    showWorks = false,
    showRoles = false,
    showTags = false,
  } = options;

  const isRoot = scholar.id === 'muhammad';
  const baseWidth = lang === 'both' || showWorks || showRoles ? 196 : 168;
  const width = isRoot ? Math.max(baseWidth + 36, 234) : baseWidth;

  let height = 14; // top & bottom padding
  if (lang === 'both') {
    height += 36; // Arabic + Turkish name
  } else {
    height += 26; // single language name
  }

  if (options.showHijri || options.showMiladi) {
    height += 14;
  }
  if (showTabaka && scholar.tabaka > 0) {
    height += 18;
  }
  if (showRegion && scholar.region !== 'root') {
    height += 14;
  }
  if (showRoles && ((scholar.rolesTr && scholar.rolesTr.length) || (scholar.rolesAr && scholar.rolesAr.length))) {
    height += 16;
  }
  if (showWorks && ((scholar.worksTr && scholar.worksTr.length) || (scholar.worksAr && scholar.worksAr.length))) {
    const count = Math.min(2, Math.max(scholar.worksTr?.length || 0, scholar.worksAr?.length || 0));
    height += 10 + count * 13;
  }
  if (showTags && ((scholar.tagsTr && scholar.tagsTr.length) || (scholar.tagsAr && scholar.tagsAr.length))) {
    height += 16;
  }

  return { width, height: Math.max(height, 54) };
}

function computePosterLayout(allScholars, state) {
  const {
    lang = 'both',
    layoutMode = 'century',
    showNonHanafi = true,
    regionFilter = 'all',
    tabakaFilter = 'all',
    centuryMin = 1,
    centuryMax = 15,
    focusId = null,
    focusMode = 'off', // 'off' | 'highlight' | 'isolate'
    focusDirection = 'both',
    showHeader = true,
    showLegend = true,
    showCenturyBands = true,
    customOffsets = {},
  } = state;

  const lineage = computeLineage(allScholars, focusId, focusDirection);

  // 1. Filter visible scholars
  let visibleScholars = allScholars.filter((s) => {
    if (!showNonHanafi && s.nonHanafi) return false;
    if (focusMode === 'isolate' && lineage.activeSet) {
      return lineage.activeSet.has(s.id);
    }
    const c = getHijriCentury(s.deathH);
    if (c < centuryMin || c > centuryMax) return false;
    if (regionFilter !== 'all' && s.region !== regionFilter && s.id !== 'muhammad') return false;
    if (tabakaFilter !== 'all' && String(s.tabaka) !== String(tabakaFilter)) return false;
    return true;
  });

  if (visibleScholars.length === 0) {
    return {
      nodes: [],
      edges: [],
      bands: [],
      width: 1400,
      height: 800,
      headerHeight: 0,
      footerY: 700,
      footerHeight: 0,
      timelineWidth: 0,
      timelineSide: lang === 'ar' ? 'right' : 'left',
      lineage,
    };
  }

  const { byId, parentsMap, childrenMap } = buildAdjacency(visibleScholars);

  // 2. Card sizing
  const sizeMap = new Map();
  let maxCardW = 182;
  for (const s of visibleScholars) {
    const sz = estimateCardSize(s, state);
    sizeMap.set(s.id, sz);
    if (sz.width > maxCardW) maxCardW = sz.width;
  }

  const gapX = 20;
  const gapY = 30;
  const maxNodesPerRow = visibleScholars.length > 60 ? 15 : 8;
  const timelineSide = lang === 'ar' ? 'right' : 'left';
  const hasTimeline = layoutMode === 'century' && showCenturyBands;
  const timelineWidth = hasTimeline ? 190 : 0;
  const frameMargin = 44;
  const headerHeight = showHeader ? (focusMode === 'isolate' && focusId ? 170 : 138) : 26;

  // 3. Row grouping: either Century-Aligned or Compact Silsile
  const rows = []; // { century, subTier, nodes: Scholar[] }
  const centuryRowRanges = new Map(); // century -> { startIdx, endIdx }

  if (layoutMode === 'century') {
    const byCentury = new Map();
    for (const s of visibleScholars) {
      const c = getHijriCentury(s.deathH);
      if (!byCentury.has(c)) byCentury.set(c, []);
      byCentury.get(c).push(s);
    }

    const sortedCenturies = [...byCentury.keys()].sort((a, b) => a - b);

    for (const c of sortedCenturies) {
      const group = byCentury.get(c);
      const groupIds = new Set(group.map((s) => s.id));

      // Intra-century topological depth (longest path from teachers in SAME century)
      const subRank = new Map();
      const visiting = new Set();

      const getRank = (id) => {
        if (subRank.has(id)) return subRank.get(id);
        if (visiting.has(id)) return 0; // cycle guard
        visiting.add(id);
        let r = 0;
        for (const pId of parentsMap.get(id) || []) {
          if (groupIds.has(pId)) {
            r = Math.max(r, getRank(pId) + 1);
          }
        }
        visiting.delete(id);
        subRank.set(id, r);
        return r;
      };

      for (const s of group) {
        if (s.id === 'muhammad') {
          subRank.set(s.id, 0);
        } else {
          getRank(s.id);
        }
      }

      // Group into tiers by subRank
      const tierMap = new Map();
      for (const s of group) {
        const r = subRank.get(s.id) || 0;
        if (!tierMap.has(r)) tierMap.set(r, []);
        tierMap.get(r).push(s);
      }

      const startIdx = rows.length;
      const tierKeys = [...tierMap.keys()].sort((a, b) => a - b);

      for (const tk of tierKeys) {
        let tierNodes = tierMap.get(tk);
        // Sort by deathH first so if we split an overcrowded tier, earlier scholars stay higher!
        tierNodes.sort((a, b) => (a.deathH || 0) - (b.deathH || 0));

        if (tierNodes.length <= maxNodesPerRow) {
          rows.push({ century: c, subTier: tk, nodes: tierNodes });
        } else {
          // Split chronologically into balanced sub-rows
          const chunks = Math.ceil(tierNodes.length / maxNodesPerRow);
          const perChunk = Math.ceil(tierNodes.length / chunks);
          for (let i = 0; i < tierNodes.length; i += perChunk) {
            rows.push({ century: c, subTier: tk + i * 0.01, nodes: tierNodes.slice(i, i + perChunk) });
          }
        }
      }

      centuryRowRanges.set(c, { startIdx, endIdx: rows.length - 1 });
    }
  } else {
    // Compact Silsile Mode: global topological depth
    const depthMap = new Map();
    const visiting = new Set();

    const getDepth = (id) => {
      if (depthMap.has(id)) return depthMap.get(id);
      if (visiting.has(id)) return 0;
      visiting.add(id);
      let d = 0;
      for (const pId of parentsMap.get(id) || []) {
        d = Math.max(d, getDepth(pId) + 1);
      }
      visiting.delete(id);
      depthMap.set(id, d);
      return d;
    };

    for (const s of visibleScholars) getDepth(s.id);

    const byDepth = new Map();
    for (const s of visibleScholars) {
      const d = depthMap.get(s.id) || 0;
      if (!byDepth.has(d)) byDepth.set(d, []);
      byDepth.get(d).push(s);
    }

    for (const d of [...byDepth.keys()].sort((a, b) => a - b)) {
      const tierNodes = byDepth.get(d).sort((a, b) => (a.deathH || 0) - (b.deathH || 0));
      if (tierNodes.length <= maxNodesPerRow) {
        rows.push({ century: null, subTier: d, nodes: tierNodes });
      } else {
        const chunks = Math.ceil(tierNodes.length / maxNodesPerRow);
        const perChunk = Math.ceil(tierNodes.length / chunks);
        for (let i = 0; i < tierNodes.length; i += perChunk) {
          rows.push({ century: null, subTier: d + i * 0.01, nodes: tierNodes.slice(i, i + perChunk) });
        }
      }
    }
  }

  // 4. Horizontal Ordering (Regional Lane Seed + Multi-Pass Barycenter Crossing Minimization)
  const regionLane = (s) => {
    const base = REGIONS[s.region]?.laneOrder ?? 3;
    return lang === 'ar' ? 6 - base : base;
  };

  // Seed initial horizontal positions
  const orderScore = new Map();
  for (const row of rows) {
    row.nodes.sort((a, b) => {
      const la = regionLane(a);
      const lb = regionLane(b);
      if (la !== lb) return la - lb;
      return (a.deathH || 0) - (b.deathH || 0);
    });
    const n = row.nodes.length;
    row.nodes.forEach((s, idx) => {
      const norm = n === 1 ? 0.5 : idx / (n - 1);
      orderScore.set(s.id, norm);
    });
  }

  // 4 top-down & bottom-up barycenter passes
  for (let pass = 0; pass < 4; pass++) {
    // Top-down
    for (let r = 1; r < rows.length; r++) {
      const row = rows[r];
      const scored = row.nodes.map((s) => {
        const ps = parentsMap.get(s.id) || [];
        const laneNorm = regionLane(s) / 6;
        if (ps.length === 0) return { s, score: laneNorm };
        const avgParent = ps.reduce((acc, pid) => acc + (orderScore.get(pid) ?? laneNorm), 0) / ps.length;
        return { s, score: avgParent * 0.78 + laneNorm * 0.22 };
      });
      scored.sort((a, b) => a.score - b.score);
      row.nodes = scored.map((x) => x.s);
      const n = row.nodes.length;
      row.nodes.forEach((s, idx) => orderScore.set(s.id, n === 1 ? 0.5 : idx / (n - 1)));
    }

    // Bottom-up
    for (let r = rows.length - 2; r >= 0; r--) {
      const row = rows[r];
      const scored = row.nodes.map((s) => {
        const ch = childrenMap.get(s.id) || [];
        const laneNorm = regionLane(s) / 6;
        const curr = orderScore.get(s.id) ?? laneNorm;
        if (ch.length === 0) return { s, score: curr };
        const avgChild = ch.reduce((acc, cid) => acc + (orderScore.get(cid) ?? curr), 0) / ch.length;
        return { s, score: curr * 0.55 + avgChild * 0.35 + laneNorm * 0.1 };
      });
      scored.sort((a, b) => a.score - b.score);
      row.nodes = scored.map((x) => x.s);
      const n = row.nodes.length;
      row.nodes.forEach((s, idx) => orderScore.set(s.id, n === 1 ? 0.5 : idx / (n - 1)));
    }
  }

  // 5. Compute Canvas Width & X/Y Coordinates
  let widestRowPx = 0;
  for (const row of rows) {
    const w = row.nodes.reduce((sum, s) => sum + sizeMap.get(s.id).width, 0) + Math.max(0, row.nodes.length - 1) * gapX;
    if (w > widestRowPx) widestRowPx = w;
  }

  const contentMinWidth = showLegend ? 1320 : 960;
  const contentWidth = Math.max(widestRowPx + 120, contentMinWidth);
  const totalWidth = frameMargin * 2 + timelineWidth + contentWidth;
  const contentLeft = frameMargin + (timelineSide === 'left' ? timelineWidth : 0);
  const contentCenterX = contentLeft + contentWidth / 2;

  const bandPadTop = 18;
  const bandPadBottom = 18;
  const rowMetrics = rows.map((row) => {
    const maxH = row.nodes.reduce((m, s) => Math.max(m, sizeMap.get(s.id).height), 54);
    return { maxH };
  });

  let cursorY = frameMargin + headerHeight;
  const bands = [];
  const nodePositions = new Map();

  if (layoutMode === 'century') {
    const sortedCenturies = [...centuryRowRanges.keys()].sort((a, b) => a - b);
    for (const c of sortedCenturies) {
      const { startIdx, endIdx } = centuryRowRanges.get(c);
      const yStart = cursorY;
      cursorY += bandPadTop;

      for (let r = startIdx; r <= endIdx; r++) {
        const row = rows[r];
        const rowH = rowMetrics[r].maxH;
        placeRowNodes(row.nodes, cursorY, rowH, contentCenterX, gapX, sizeMap, customOffsets, nodePositions);
        cursorY += rowH + (r < endIdx ? gapY : 0);
      }

      cursorY += bandPadBottom;
      const yEnd = cursorY;
      const count = rows.slice(startIdx, endIdx + 1).reduce((acc, r) => acc + r.nodes.length, 0);
      bands.push({
        century: c,
        yStart,
        yEnd,
        height: yEnd - yStart,
        count,
        meta: CENTURY_META[c] || {
          tr: `${c}. Hicrî Yüzyıl`,
          ar: `القرن ${c} الهجري`,
          subTr: '',
          subAr: '',
          miladi: '',
        },
      });
    }
  } else {
    cursorY += 20;
    for (let r = 0; r < rows.length; r++) {
      const row = rows[r];
      const rowH = rowMetrics[r].maxH;
      placeRowNodes(row.nodes, cursorY, rowH, contentCenterX, gapX, sizeMap, customOffsets, nodePositions);
      cursorY += rowH + (r < rows.length - 1 ? gapY : 0);
    }
    cursorY += 28;
  }

  // Refine X positions gently toward parents inside each row while preventing overlaps
  for (let iter = 0; iter < 2; iter++) {
    for (const row of rows) {
      if (row.nodes.length >= maxNodesPerRow || row.nodes.length === 1) continue;
      // Only relax if the row isn't full
      const desired = row.nodes.map((s) => {
        const pos = nodePositions.get(s.id);
        const off = customOffsets[s.id];
        if (off && (off.dx || off.dy)) return { s, pos, targetCx: pos.cx, locked: true };
        const ps = (parentsMap.get(s.id) || []).filter((pid) => nodePositions.has(pid));
        if (ps.length === 0) return { s, pos, targetCx: pos.cx, locked: false };
        const avgCx = ps.reduce((sum, pid) => sum + nodePositions.get(pid).cx, 0) / ps.length;
        return { s, pos, targetCx: pos.cx * 0.45 + avgCx * 0.55, locked: false };
      });

      // Left-to-right collision resolution
      const leftBound = contentLeft + 44;
      const rightBound = contentLeft + contentWidth - 44;
      for (let i = 0; i < desired.length; i++) {
        const item = desired[i];
        if (item.locked) continue;
        let cx = Math.max(leftBound + item.pos.w / 2, Math.min(rightBound - item.pos.w / 2, item.targetCx));
        if (i > 0) {
          const prev = desired[i - 1];
          const minCx = prev.pos.cx + prev.pos.w / 2 + gapX + item.pos.w / 2;
          if (cx < minCx) cx = minCx;
        }
        item.pos.cx = cx;
        item.pos.x = cx - item.pos.w / 2;
      }

      // Right-to-left clamp if overflowed right edge
      for (let i = desired.length - 1; i >= 0; i--) {
        const item = desired[i];
        if (item.locked) continue;
        if (item.pos.cx + item.pos.w / 2 > rightBound) {
          item.pos.cx = rightBound - item.pos.w / 2;
          item.pos.x = item.pos.cx - item.pos.w / 2;
        }
        if (i < desired.length - 1) {
          const next = desired[i + 1];
          const maxCx = next.pos.cx - next.pos.w / 2 - gapX - item.pos.w / 2;
          if (item.pos.cx > maxCx) {
            item.pos.cx = maxCx;
            item.pos.x = item.pos.cx - item.pos.w / 2;
          }
        }
      }
    }
  }

  // 6. Build Edges with spread ports
  const outgoingByNode = new Map();
  const incomingByNode = new Map();
  const rawEdges = [];

  for (const s of visibleScholars) {
    for (const tId of parentsMap.get(s.id) || []) {
      if (nodePositions.has(tId) && nodePositions.has(s.id)) {
        rawEdges.push({ from: tId, to: s.id });
        if (!outgoingByNode.has(tId)) outgoingByNode.set(tId, []);
        outgoingByNode.get(tId).push(s.id);
        if (!incomingByNode.has(s.id)) incomingByNode.set(s.id, []);
        incomingByNode.get(s.id).push(tId);
      }
    }
  }

  // Sort ports left-to-right to avoid needless crossings near box edges
  for (const [id, list] of outgoingByNode.entries()) {
    list.sort((a, b) => nodePositions.get(a).cx - nodePositions.get(b).cx);
  }
  for (const [id, list] of incomingByNode.entries()) {
    list.sort((a, b) => nodePositions.get(a).cx - nodePositions.get(b).cx);
  }

  const edges = rawEdges.map((e) => {
    const fromPos = nodePositions.get(e.from);
    const toPos = nodePositions.get(e.to);
    const outList = outgoingByNode.get(e.from) || [e.to];
    const inList = incomingByNode.get(e.to) || [e.from];
    const outIdx = outList.indexOf(e.to);
    const inIdx = inList.indexOf(e.from);

    const spreadOut = outList.length > 1 ? ((outIdx / (outList.length - 1)) - 0.5) * Math.min(fromPos.w * 0.55, 70) : 0;
    const spreadIn = inList.length > 1 ? ((inIdx / (inList.length - 1)) - 0.5) * Math.min(toPos.w * 0.55, 70) : 0;

    return {
      id: `${e.from}__${e.to}`,
      from: e.from,
      to: e.to,
      fromScholar: byId.get(e.from),
      toScholar: byId.get(e.to),
      x1: fromPos.cx + spreadOut,
      y1: fromPos.y + fromPos.h,
      x2: toPos.cx + spreadIn,
      y2: toPos.y,
    };
  });

  // 7. Footer Legend & Classical Literature Box
  const footerY = cursorY + 22;
  const footerHeight = showLegend ? 310 : 48;
  const totalHeight = footerY + footerHeight + frameMargin;

  const nodes = visibleScholars.map((s) => ({
    scholar: s,
    ...nodePositions.get(s.id),
  }));

  return {
    nodes,
    edges,
    bands,
    width: totalWidth,
    height: totalHeight,
    frameMargin,
    headerHeight,
    contentLeft,
    contentWidth,
    timelineWidth,
    timelineSide,
    footerY,
    footerHeight,
    lineage,
  };
}

function placeRowNodes(rowNodes, yTop, rowH, centerX, gapX, sizeMap, customOffsets, outMap) {
  const totalW = rowNodes.reduce((sum, s) => sum + sizeMap.get(s.id).width, 0) + Math.max(0, rowNodes.length - 1) * gapX;
  let x = centerX - totalW / 2;

  for (const s of rowNodes) {
    const { width: w, height: h } = sizeMap.get(s.id);
    const off = customOffsets[s.id] || { dx: 0, dy: 0 };
    const nx = x + (off.dx || 0);
    const ny = yTop + (rowH - h) / 2 + (off.dy || 0);
    outMap.set(s.id, {
      x: nx,
      y: ny,
      w,
      h,
      cx: nx + w / 2,
      cy: ny + h / 2,
    });
    x += w + gapX;
  }
}


// ===== src/engine/svgRenderer.js =====
// Pure Vector SVG Poster Renderer (Print-shop & Illustrator/CorelDRAW compatible)



function esc(str) {
  return String(str ?? '')
    .replace(/&/g, '&amp;')
    .replace(/</g, '&lt;')
    .replace(/>/g, '&gt;')
    .replace(/"/g, '&quot;');
}

function wrapText(text, maxChars) {
  if (!text) return [];
  const words = String(text).trim().split(/\s+/);
  const lines = [];
  let line = '';
  for (const w of words) {
    if (!line) {
      line = w;
    } else if ((line + ' ' + w).length <= maxChars) {
      line += ' ' + w;
    } else {
      lines.push(line);
      line = w;
    }
  }
  if (line) lines.push(line);
  return lines;
}

function getCardPalette(scholar, colorMode, theme) {
  if (colorMode === 'minimal') {
    const dark = theme.id === 'night';
    return {
      stroke: dark ? '#94a3b8' : '#334155',
      fill: dark ? '#1e293b' : '#ffffff',
      text: dark ? '#f1f5f9' : '#0f172a',
      arrow: dark ? '#64748b' : '#475569',
    };
  }
  if (colorMode === 'tabaka') {
    const t = TABAKAT[scholar.tabaka] || TABAKAT[0];
    if (theme.id === 'night') {
      return { stroke: t.stroke, fill: '#18243a', text: '#f1f5f9', arrow: t.stroke };
    }
    return { stroke: t.stroke, fill: t.fill, text: t.text, arrow: t.stroke };
  }
  const r = REGIONS[scholar.region] || REGIONS.kufe;
  if (theme.id === 'night') {
    return { stroke: r.stroke, fill: '#18243a', text: '#f1f5f9', arrow: r.arrow };
  }
  return { stroke: r.stroke, fill: r.fill, text: r.text, arrow: r.arrow };
}

function renderCornerOrnament(cx, cy, color) {
  // Subtle 8-pointed Islamic star (Rub el Hizb) ornament for poster corners
  return `
    <g transform="translate(${cx},${cy})" opacity="0.65">
      <rect x="-9" y="-9" width="18" height="18" fill="none" stroke="${color}" stroke-width="1.3"/>
      <rect x="-9" y="-9" width="18" height="18" transform="rotate(45)" fill="none" stroke="${color}" stroke-width="1.3"/>
      <circle cx="0" cy="0" r="3" fill="${color}"/>
    </g>
  `;
}

function renderPosterSVG(layout, state, activeBook = null) {
  const {
    lang = 'both',
    colorMode = 'region',
    themeId = 'parchment',
    selectedId = null,
    focusId = null,
    focusMode = 'off',
    showHeader = true,
    showLegend = true,
    showCenturyBands = true,
    showHijri = true,
    showMiladi = false,
    showTabaka = false,
    showRegion = false,
    showWorks = false,
    showRoles = false,
    showTags = false,
  } = state;

  const theme = THEMES[themeId] || THEMES.parchment;
  const { width, height, frameMargin, headerHeight, contentLeft, contentWidth, timelineWidth, timelineSide, bands, nodes, edges, footerY, footerHeight, lineage } = layout;

  // Determine highlight sets (from Person Focus OR Interactive Book selection)
  let highlightSet = null;
  if (focusMode === 'highlight' && focusId && lineage.activeSet) {
    highlightSet = lineage.activeSet;
  } else if (activeBook) {
    highlightSet = new Set([activeBook.authorId, ...(activeBook.relatedIds || [])]);
  }

  const fontAr = "'Amiri', 'Noto Naskh Arabic', 'Traditional Arabic', 'Sakkal Majalla', serif";
  const fontTr = "'EB Garamond', 'Inter', 'Segoe UI', Georgia, serif";
  const fontUi = "'Inter', 'Segoe UI', system-ui, sans-serif";

  const parts = [];

  parts.push(`<svg xmlns="http://www.w3.org/2000/svg" id="poster-svg" viewBox="0 0 ${Math.ceil(width)} ${Math.ceil(height)}" width="${Math.ceil(width)}" height="${Math.ceil(height)}">`);

  // Defs & embedded styles (so exported standalone SVG looks identical everywhere)
  parts.push(`
    <defs>
      <style>
        .f-ar { font-family: ${fontAr}; }
        .f-tr { font-family: ${fontTr}; }
        .f-ui { font-family: ${fontUi}; }
        .scholar-node { cursor: pointer; transition: opacity 0.18s ease; }
        .scholar-node:hover .card-bg { filter: brightness(0.97); }
      </style>
      <filter id="card-shadow" x="-6%" y="-6%" width="112%" height="118%">
        <feDropShadow dx="0" dy="2" stdDeviation="2.2" flood-color="#000000" flood-opacity="${theme.id === 'night' ? '0.38' : '0.10'}"/>
      </filter>
    </defs>
  `);

  // 1. Background
  parts.push(`<rect x="0" y="0" width="${width}" height="${height}" fill="${theme.bg}"/>`);

  // 2. Ornamental Poster Frame
  if (showHeader) {
    const f1 = 18;
    const f2 = 26;
    parts.push(`<rect x="${f1}" y="${f1}" width="${width - f1 * 2}" height="${height - f1 * 2}" rx="6" fill="none" stroke="${theme.frameOuter}" stroke-width="2.6"/>`);
    parts.push(`<rect x="${f2}" y="${f2}" width="${width - f2 * 2}" height="${height - f2 * 2}" rx="3" fill="none" stroke="${theme.frameInner}" stroke-width="1"/>`);
    parts.push(renderCornerOrnament(f2 + 12, f2 + 12, theme.frameOuter));
    parts.push(renderCornerOrnament(width - f2 - 12, f2 + 12, theme.frameOuter));
    parts.push(renderCornerOrnament(f2 + 12, height - f2 - 12, theme.frameOuter));
    parts.push(renderCornerOrnament(width - f2 - 12, height - f2 - 12, theme.frameOuter));
  }

  // 3. Century Bands & Timeline Column
  if (bands.length > 0 && showCenturyBands) {
    const bandX = frameMargin;
    const bandW = width - frameMargin * 2;
    const tlX = timelineSide === 'left' ? frameMargin : width - frameMargin - timelineWidth;

    parts.push(`<g class="century-bands">`);
    bands.forEach((b, idx) => {
      const fill = idx % 2 === 0 ? theme.bg : theme.bgAlt;
      parts.push(`<rect x="${bandX}" y="${b.yStart}" width="${bandW}" height="${b.height}" fill="${fill}" stroke="${theme.bandBorder}" stroke-width="0.9"/>`);

      // Timeline label box
      parts.push(`<rect x="${tlX}" y="${b.yStart}" width="${timelineWidth}" height="${b.height}" fill="${theme.bandLabelBg}" opacity="0.72" stroke="${theme.bandBorder}" stroke-width="0.9"/>`);

      const midY = b.yStart + b.height / 2;
      const centerX = tlX + timelineWidth / 2;

      if (lang === 'ar') {
        parts.push(`<text x="${centerX}" y="${midY - 12}" text-anchor="middle" class="f-ar" font-size="18" font-weight="700" fill="${theme.bandLabelText}">${esc(b.meta.ar)}</text>`);
        if (b.meta.subAr) {
          parts.push(`<text x="${centerX}" y="${midY + 9}" text-anchor="middle" class="f-ar" font-size="13" fill="${theme.subtitleText}">${esc(b.meta.subAr)}</text>`);
        }
        if (b.meta.miladi) {
          parts.push(`<text x="${centerX}" y="${midY + 26}" text-anchor="middle" class="f-ui" font-size="11" fill="${theme.subtitleText}" opacity="0.8">م ${esc(b.meta.miladi)}</text>`);
        }
      } else if (lang === 'tr') {
        parts.push(`<text x="${centerX}" y="${midY - 12}" text-anchor="middle" class="f-tr" font-size="16" font-weight="700" fill="${theme.bandLabelText}">${esc(b.meta.tr)}</text>`);
        if (b.meta.subTr) {
          parts.push(`<text x="${centerX}" y="${midY + 8}" text-anchor="middle" class="f-ui" font-size="11" fill="${theme.subtitleText}">${esc(b.meta.subTr)}</text>`);
        }
        if (b.meta.miladi) {
          parts.push(`<text x="${centerX}" y="${midY + 25}" text-anchor="middle" class="f-ui" font-size="10.5" fill="${theme.subtitleText}" opacity="0.8">M. ${esc(b.meta.miladi)}</text>`);
        }
      } else {
        // Bilingual timeline badge
        parts.push(`<text x="${centerX}" y="${midY - 18}" text-anchor="middle" class="f-ar" font-size="16" font-weight="700" fill="${theme.bandLabelText}">${esc(b.meta.ar)}</text>`);
        parts.push(`<text x="${centerX}" y="${midY + 1}" text-anchor="middle" class="f-tr" font-size="13.5" font-weight="700" fill="${theme.bandLabelText}">${esc(b.meta.tr)}</text>`);
        if (b.meta.subTr) {
          parts.push(`<text x="${centerX}" y="${midY + 17}" text-anchor="middle" class="f-ui" font-size="10" fill="${theme.subtitleText}">${esc(b.meta.subTr)}</text>`);
        }
        if (b.meta.miladi) {
          parts.push(`<text x="${centerX}" y="${midY + 32}" text-anchor="middle" class="f-ui" font-size="10" fill="${theme.subtitleText}" opacity="0.78">M. ${esc(b.meta.miladi)}</text>`);
        }
      }
    });
    parts.push(`</g>`);
  }

  // 4. Poster Header Title Cartouche
  if (showHeader) {
    const cx = width / 2;
    const topY = frameMargin + 10;
    const focusScholar = focusId ? nodes.find((n) => n.scholar.id === focusId)?.scholar : null;

    parts.push(`<g class="poster-header">`);
    if (lang === 'ar') {
      parts.push(`<text x="${cx}" y="${topY + 46}" text-anchor="middle" class="f-ar" font-size="44" font-weight="700" fill="${theme.titleText}">${esc(UI_TEXT.ar.posterTitle)}</text>`);
      parts.push(`<text x="${cx}" y="${topY + 78}" text-anchor="middle" class="f-ar" font-size="19" fill="${theme.subtitleText}">${esc(UI_TEXT.ar.posterSubtitle)}</text>`);
    } else if (lang === 'tr') {
      parts.push(`<text x="${cx}" y="${topY + 44}" text-anchor="middle" class="f-tr" font-size="36" font-weight="700" fill="${theme.titleText}">${esc(UI_TEXT.tr.posterTitle)}</text>`);
      parts.push(`<text x="${cx}" y="${topY + 74}" text-anchor="middle" class="f-ui" font-size="15" fill="${theme.subtitleText}">${esc(UI_TEXT.tr.posterSubtitle)}</text>`);
    } else {
      parts.push(`<text x="${cx}" y="${topY + 40}" text-anchor="middle" class="f-ar" font-size="40" font-weight="700" fill="${theme.titleText}">${esc(UI_TEXT.ar.posterTitle)}</text>`);
      parts.push(`<text x="${cx}" y="${topY + 74}" text-anchor="middle" class="f-tr" font-size="23" font-weight="700" fill="${theme.titleText}">${esc(UI_TEXT.tr.posterTitle)}</text>`);
      parts.push(`<text x="${cx}" y="${topY + 98}" text-anchor="middle" class="f-ui" font-size="13" fill="${theme.subtitleText}">${esc(UI_TEXT.tr.posterSubtitle)}</text>`);
    }

    // Decorative divider under header
    const divY = topY + (lang === 'both' ? 114 : 96);
    parts.push(`<line x1="${cx - 260}" y1="${divY}" x2="${cx + 260}" y2="${divY}" stroke="${theme.frameInner}" stroke-width="1.3"/>`);
    parts.push(`<circle cx="${cx}" cy="${divY}" r="4" fill="${theme.frameOuter}"/>`);

    if (focusMode === 'isolate' && focusScholar) {
      const labelTr = `Şahıs Odaklı Silsile: ${focusScholar.nameTr} (${focusScholar.deathH})`;
      const labelAr = `سلسلة العالم: ${focusScholar.nameAr} (${toArabicDigits(focusScholar.deathH)})`;
      const bannerText = lang === 'ar' ? labelAr : lang === 'tr' ? labelTr : `${labelAr}  •  ${labelTr}`;
      parts.push(`<rect x="${cx - 310}" y="${divY + 12}" width="620" height="30" rx="15" fill="${theme.bandLabelBg}" stroke="${theme.frameOuter}" stroke-width="1"/>`);
      parts.push(`<text x="${cx}" y="${divY + 32}" text-anchor="middle" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="13.5" font-weight="600" fill="${theme.titleText}">${esc(bannerText)}</text>`);
    }
    parts.push(`</g>`);
  }

  // 5. Edges (Smooth Cubic Bezier Curves + crisp vector arrowheads)
  // Render dimmed edges first, then highlighted edges on top!
  const sortedEdges = [...edges].sort((a, b) => {
    const aActive = !highlightSet || (highlightSet.has(a.from) && highlightSet.has(a.to));
    const bActive = !highlightSet || (highlightSet.has(b.from) && highlightSet.has(b.to));
    return Number(aActive) - Number(bActive);
  });

  parts.push(`<g class="silsile-edges">`);
  for (const e of sortedEdges) {
    const pal = getCardPalette(e.fromScholar, colorMode, theme);
    const isEdgeActive = !highlightSet || (highlightSet.has(e.from) && highlightSet.has(e.to));
    const opacity = isEdgeActive ? (highlightSet ? 0.95 : 0.72) : theme.dimOpacity * 0.75;
    const strokeW = isEdgeActive && highlightSet ? 2.4 : 1.55;

    const dy = e.y2 - e.y1;
    const ctrlOffset = Math.max(26, Math.min(Math.abs(dy) * 0.52, 130));
    const c1y = e.y1 + ctrlOffset;
    const c2y = e.y2 - ctrlOffset;
    const tipY = e.y2 - 2;

    const pathD = `M ${e.x1.toFixed(1)} ${e.y1.toFixed(1)} C ${e.x1.toFixed(1)} ${c1y.toFixed(1)}, ${e.x2.toFixed(1)} ${c2y.toFixed(1)}, ${e.x2.toFixed(1)} ${(tipY - 5).toFixed(1)}`;
    parts.push(`<path d="${pathD}" fill="none" stroke="${pal.arrow}" stroke-width="${strokeW}" opacity="${opacity}" stroke-linecap="round"/>`);

    // Vector arrowhead pointing down at (e.x2, tipY)
    const ax = e.x2;
    const ay = tipY;
    parts.push(`<polygon points="${ax.toFixed(1)},${ay.toFixed(1)} ${(ax - 4).toFixed(1)},${(ay - 7.5).toFixed(1)} ${(ax + 4).toFixed(1)},${(ay - 7.5).toFixed(1)}" fill="${pal.arrow}" opacity="${opacity}"/>`);
  }
  parts.push(`</g>`);

  // 6. Scholar Cards
  parts.push(`<g class="silsile-nodes">`);
  for (const item of nodes) {
    const s = item.scholar;
    const { x, y, w, h, cx } = item;
    const pal = getCardPalette(s, colorMode, theme);
    const isRoot = s.id === 'muhammad';
    const isSelected = s.id === selectedId || s.id === focusId;
    const isActive = !highlightSet || highlightSet.has(s.id);
    const opacity = isActive ? 1 : theme.dimOpacity;

    const strokeW = isSelected ? 3.2 : isRoot ? 2.8 : 1.8;
    const rx = isRoot ? 16 : 9;

    parts.push(`<g class="scholar-node" data-id="${esc(s.id)}" opacity="${opacity}">`);

    // Selection glow ring
    if (isSelected) {
      parts.push(`<rect x="${x - 4}" y="${y - 4}" width="${w + 8}" height="${h + 8}" rx="${rx + 3}" fill="none" stroke="${pal.stroke}" stroke-width="2" stroke-dasharray="5 3" opacity="0.85"/>`);
    }

    // Card background
    parts.push(`<rect class="card-bg" x="${x}" y="${y}" width="${w}" height="${h}" rx="${rx}" fill="${pal.fill}" stroke="${pal.stroke}" stroke-width="${strokeW}" filter="url(#card-shadow)"/>`);

    // Top color accent bar on root or Tabaka mode
    if (isRoot) {
      parts.push(`<rect x="${x + 4}" y="${y + 4}" width="${w - 8}" height="${h - 8}" rx="${rx - 3}" fill="none" stroke="${theme.frameInner}" stroke-width="0.9"/>`);
    }

    // Non-Hanafi asterisk badge (*)
    if (s.nonHanafi) {
      const starX = lang === 'ar' ? x + 13 : x + w - 13;
      parts.push(`<circle cx="${starX}" cy="${y + 13}" r="8" fill="${pal.stroke}" opacity="0.16"/>`);
      parts.push(`<text x="${starX}" y="${y + 17.5}" text-anchor="middle" class="f-ui" font-size="14" font-weight="700" fill="${pal.stroke}">*</text>`);
    }

    // Card content layout (vertical stack inside box)
    let ty = y + 16;

    // Name(s)
    if (lang === 'ar') {
      const arLines = wrapText(s.nameAr, 23).slice(0, 2);
      arLines.forEach((ln, idx) => {
        parts.push(`<text x="${cx}" y="${ty + idx * 15}" text-anchor="middle" class="f-ar" font-size="${isRoot ? 16.5 : 14.5}" font-weight="700" fill="${pal.text}">${esc(ln)}</text>`);
      });
      ty += arLines.length * 15 + 1;
    } else if (lang === 'tr') {
      const trLines = wrapText(s.nameTr, 23).slice(0, 2);
      trLines.forEach((ln, idx) => {
        parts.push(`<text x="${cx}" y="${ty + idx * 13.5}" text-anchor="middle" class="f-tr" font-size="${isRoot ? 14.5 : 13}" font-weight="700" fill="${pal.text}">${esc(ln)}</text>`);
      });
      ty += trLines.length * 13.5 + 2;
    } else {
      // Bilingual: Arabic on top, Turkish right below
      const arShort = s.nameAr.length > 27 ? s.nameAr.slice(0, 26) + '…' : s.nameAr;
      const trShort = s.nameTr.length > 28 ? s.nameTr.slice(0, 27) + '…' : s.nameTr;
      parts.push(`<text x="${cx}" y="${ty}" text-anchor="middle" class="f-ar" font-size="${isRoot ? 16 : 14}" font-weight="700" fill="${pal.text}">${esc(arShort)}</text>`);
      ty += 16;
      parts.push(`<text x="${cx}" y="${ty}" text-anchor="middle" class="f-tr" font-size="${isRoot ? 12.5 : 11.5}" font-weight="600" fill="${pal.text}" opacity="0.9">${esc(trShort)}</text>`);
      ty += 14;
    }

    // Death Year(s)
    if (showHijri || showMiladi) {
      const mYear = s.deathM || hijriToMiladiApprox(s.deathH);
      const dateParts = [];
      if (showHijri && s.deathH) {
        dateParts.push(lang === 'ar' ? `ت ${toArabicDigits(s.deathH)} هـ` : `v. ${s.deathH}`);
      }
      if (showMiladi && mYear) {
        dateParts.push(lang === 'ar' ? `${toArabicDigits(mYear)} م` : `m. ${mYear}`);
      }
      if (dateParts.length > 0) {
        parts.push(`<text x="${cx}" y="${ty + 1}" text-anchor="middle" class="f-ui" font-size="10" font-weight="600" fill="${pal.stroke}">(${esc(dateParts.join(' / '))})</text>`);
        ty += 14;
      }
    }

    // Tabaka Badge
    if (showTabaka && s.tabaka > 0) {
      const tb = TABAKAT[s.tabaka];
      if (tb) {
        const label = lang === 'ar' ? tb.shortAr : tb.shortTr;
        const bw = Math.min(w - 20, 120);
        parts.push(`<rect x="${cx - bw / 2}" y="${ty - 9}" width="${bw}" height="14" rx="7" fill="${tb.stroke}" opacity="0.14" stroke="${tb.stroke}" stroke-width="0.7"/>`);
        parts.push(`<text x="${cx}" y="${ty + 1.5}" text-anchor="middle" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="9" font-weight="700" fill="${theme.id === 'night' ? '#e2e8f0' : tb.text}">${esc(label)}</text>`);
        ty += 17;
      }
    }

    // Region Micro-Label
    if (showRegion && s.region !== 'root') {
      const reg = REGIONS[s.region];
      if (reg) {
        const rLabel = lang === 'ar' ? reg.nameAr : reg.nameTr;
        parts.push(`<text x="${cx}" y="${ty}" text-anchor="middle" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="9" fill="${pal.stroke}" opacity="0.9">● ${esc(rLabel)}</text>`);
        ty += 13.5;
      }
    }

    // Roles / Famous Offices
    if (showRoles) {
      const roleArr = lang === 'ar' ? (s.rolesAr?.length ? s.rolesAr : s.rolesTr) : (s.rolesTr?.length ? s.rolesTr : s.rolesAr);
      if (roleArr && roleArr.length > 0) {
        const txt = roleArr[0].length > 26 ? roleArr[0].slice(0, 25) + '…' : roleArr[0];
        parts.push(`<text x="${cx}" y="${ty + 1}" text-anchor="middle" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="9" font-style="italic" fill="${pal.text}" opacity="0.82">${esc(txt)}</text>`);
        ty += 14.5;
      }
    }

    // Famous Works
    if (showWorks) {
      const worksArr = lang === 'ar' ? (s.worksAr?.length ? s.worksAr : s.worksTr) : (s.worksTr?.length ? s.worksTr : s.worksAr);
      if (worksArr && worksArr.length > 0) {
        parts.push(`<line x1="${x + 14}" y1="${ty - 6}" x2="${x + w - 14}" y2="${ty - 6}" stroke="${pal.stroke}" stroke-width="0.6" opacity="0.35"/>`);
        worksArr.slice(0, 2).forEach((wk) => {
          const shortWk = wk.length > 27 ? wk.slice(0, 26) + '…' : wk;
          parts.push(`<text x="${cx}" y="${ty + 4}" text-anchor="middle" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="9" fill="${pal.text}" opacity="0.88">▪ ${esc(shortWk)}</text>`);
          ty += 13;
        });
        ty += 3;
      }
    }

    // Tags / Key Features
    if (showTags) {
      const tagsArr = lang === 'ar' ? (s.tagsAr?.length ? s.tagsAr : s.tagsTr) : (s.tagsTr?.length ? s.tagsTr : s.tagsAr);
      if (tagsArr && tagsArr.length > 0) {
        const tagTxt = tagsArr.slice(0, 2).join(' · ');
        const shortTag = tagTxt.length > 27 ? tagTxt.slice(0, 26) + '…' : tagTxt;
        parts.push(`<text x="${cx}" y="${ty + 2}" text-anchor="middle" class="f-ui" font-size="8.5" font-weight="600" fill="${pal.stroke}" opacity="0.85"># ${esc(shortTag)}</text>`);
      }
    }

    parts.push(`</g>`);
  }
  parts.push(`</g>`);

  // 7. Bottom Poster Legend & Classical Literature Panel
  if (showLegend) {
    const px = frameMargin;
    const pw = width - frameMargin * 2;
    const py = footerY;
    const ph = footerHeight - 16;

    parts.push(`<g class="poster-footer">`);
    parts.push(`<rect x="${px}" y="${py}" width="${pw}" height="${ph}" rx="10" fill="${theme.panelBg}" stroke="${theme.panelBorder}" stroke-width="1.3"/>`);

    // Left Column: Color Legend (25% width)
    const legendW = Math.min(340, pw * 0.25);
    const legX = lang === 'ar' ? px + pw - legendW + 18 : px + 22;
    let ly = py + 28;

    const legTitle = colorMode === 'tabaka'
      ? (lang === 'ar' ? 'طبقات الفقهاء (ابن كمال باشا)' : 'Tabakât-ı Fukahâ (İbn Kemal)')
      : (lang === 'ar' ? 'الأقاليم والمدارس العلمية' : 'İlmî Havzalar / Bölgeler');

    parts.push(`<text x="${legX}" y="${ly}" class="${lang === 'ar' ? 'f-ar' : 'f-tr'}" font-size="16" font-weight="700" fill="${theme.titleText}">${esc(legTitle)}</text>`);
    ly += 22;

    if (colorMode === 'tabaka') {
      Object.values(TABAKAT).filter((t) => t.id > 0).forEach((t) => {
        parts.push(`<rect x="${legX}" y="${ly - 10}" width="14" height="11" rx="3" fill="${t.fill}" stroke="${t.stroke}" stroke-width="1.5"/>`);
        const lbl = lang === 'ar' ? `${t.shortAr}: ${t.nameAr}` : `${t.shortTr}: ${t.nameTr}`;
        parts.push(`<text x="${legX + 20}" y="${ly}" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="11" fill="${theme.titleText}">${esc(lbl)}</text>`);
        ly += 21;
      });
    } else {
      Object.values(REGIONS).filter((r) => r.id !== 'root').forEach((r) => {
        parts.push(`<circle cx="${legX + 6}" cy="${ly - 4}" r="5.5" fill="${r.stroke}"/>`);
        const lbl = lang === 'ar' ? r.nameAr : lang === 'tr' ? r.nameTr : `${r.nameTr} (${r.nameAr})`;
        parts.push(`<text x="${legX + 18}" y="${ly}" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="12" fill="${theme.titleText}">${esc(lbl)}</text>`);
        ly += 23;
      });
    }

    // Non-Hanafi footnote
    ly += 8;
    const noteText = lang === 'ar' ? UI_TEXT.ar.nonHanafiNote : UI_TEXT.tr.nonHanafiNote;
    wrapText(noteText, 40).forEach((ln) => {
      parts.push(`<text x="${legX}" y="${ly}" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="10.5" fill="${theme.subtitleText}">${esc(ln)}</text>`);
      ly += 15;
    });

    // Vertical divider
    const divX = lang === 'ar' ? px + pw - legendW - 6 : px + legendW + 10;
    parts.push(`<line x1="${divX}" y1="${py + 18}" x2="${divX}" y2="${py + ph - 18}" stroke="${theme.panelBorder}" stroke-width="1"/>`);

    // Right Area: 5 Columns of Classical Hanafi Literature (from the PDF!)
    const litStartX = lang === 'ar' ? px + 22 : divX + 20;
    const litTotalW = pw - legendW - 46;
    const colW = litTotalW / LITERATURE_GROUPS.length;

    LITERATURE_GROUPS.forEach((grp, gIdx) => {
      const gx = litStartX + gIdx * colW;
      let gy = py + 28;
      const gTitle = lang === 'ar' ? grp.titleAr : grp.titleTr;
      parts.push(`<text x="${gx}" y="${gy}" class="${lang === 'ar' ? 'f-ar' : 'f-tr'}" font-size="13.5" font-weight="700" fill="${theme.frameOuter}">${esc(gTitle)}</text>`);
      parts.push(`<line x1="${gx}" y1="${gy + 6}" x2="${gx + colW - 18}" y2="${gy + 6}" stroke="${theme.panelBorder}" stroke-width="0.9"/>`);
      gy += 24;

      grp.items.forEach((bk) => {
        const bText = lang === 'ar' ? bk.nameAr : bk.nameTr;
        const isBookSelected = activeBook && activeBook.id === bk.id;
        wrapText(`• ${bText}`, Math.max(22, Math.floor((colW - 16) / 6.2))).slice(0, 3).forEach((ln) => {
          parts.push(`<text x="${gx}" y="${gy}" class="${lang === 'ar' ? 'f-ar' : 'f-ui'}" font-size="11" font-weight="${isBookSelected ? '700' : '400'}" fill="${isBookSelected ? theme.frameOuter : theme.titleText}">${esc(ln)}</text>`);
          gy += 16;
        });
        gy += 5;
      });
    });

    parts.push(`</g>`);
  }

  parts.push(`</svg>`);
  return parts.join('\n');
}


// ===== src/engine/exporter.js =====
// Export & Import Utilities: Vector SVG (Print-Shop Ready), High-Res PNG, Print/PDF, JSON, Excel CSV


function triggerDownload(blob, filename) {
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = filename;
  document.body.appendChild(a);
  a.click();
  setTimeout(() => {
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
  }, 300);
}

function exportPosterSVG(svgString, filename = 'hanefi-tabakat-afis.svg') {
  const standalone = `<?xml version="1.0" encoding="UTF-8" standalone="no"?>\n${svgString}`;
  const blob = new Blob([standalone], { type: 'image/svg+xml;charset=utf-8' });
  triggerDownload(blob, filename);
}

function exportPosterPNG(svgString, width, height, scale = 2, filename = 'hanefi-tabakat-afis.png') {
  return new Promise((resolve, reject) => {
    // Clamp max canvas pixels for browser safety (~16384px max dimension)
    const maxDim = Math.max(width, height);
    const safeScale = Math.min(scale, Math.floor(14000 / maxDim) || 1);

    const canvas = document.createElement('canvas');
    canvas.width = Math.ceil(width * safeScale);
    canvas.height = Math.ceil(height * safeScale);
    const ctx = canvas.getContext('2d');

    const img = new Image();
    const svgBlob = new Blob([svgString], { type: 'image/svg+xml;charset=utf-8' });
    const url = URL.createObjectURL(svgBlob);

    img.onload = () => {
      ctx.scale(safeScale, safeScale);
      ctx.drawImage(img, 0, 0);
      URL.revokeObjectURL(url);
      canvas.toBlob((pngBlob) => {
        if (!pngBlob) return reject(new Error('PNG oluşturulamadı.'));
        triggerDownload(pngBlob, filename);
        resolve();
      }, 'image/png');
    };
    img.onerror = (err) => {
      URL.revokeObjectURL(url);
      reject(err);
    };
    img.src = url;
  });
}

function printPosterPDF(svgString, title = 'Hanefî Tabakat Şeması') {
  const win = window.open('', '_blank');
  if (!win) {
    alert('Tarayıcı açılır pencereyi engelledi. Lütfen bu sayfa için açılır pencerelere izin verin veya SVG dışa aktarımı kullanın.');
    return;
  }
  win.document.write(`<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8"/>
  <title>${title}</title>
  <link rel="preconnect" href="https://fonts.googleapis.com"/>
  <link href="https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=EB+Garamond:wght@500;700&family=Inter:wght@400;600;700&display=swap" rel="stylesheet"/>
  <style>
    @page { margin: 8mm; }
    * { box-sizing: border-box; }
    html, body { margin: 0; padding: 0; background: #fff; width: 100%; height: 100%; }
    .wrap { display: flex; justify-content: center; align-items: flex-start; width: 100%; }
    svg { width: 100%; height: auto; max-width: 100%; display: block; }
  </style>
</head>
<body>
  <div class="wrap">${svgString}</div>
  <script>
    window.onload = function() { setTimeout(function() { window.print(); }, 500); };
  <\/script>
</body>
</html>`);
  win.document.close();
}

function exportScholarsJSON(scholars, filename = 'hanefi-tabakat-verisi.json') {
  const blob = new Blob([JSON.stringify(scholars, null, 2)], { type: 'application/json;charset=utf-8' });
  triggerDownload(blob, filename);
}

function csvEscape(val) {
  const s = String(val ?? '');
  if (/[",\n\r;]/.test(s)) {
    return `"${s.replace(/"/g, '""')}"`;
  }
  return s;
}

function exportScholarsCSV(scholars, filename = 'hanefi-tabakat-excel.csv') {
  const headers = [
    'id', 'nameTr', 'nameAr', 'deathH', 'deathM', 'region', 'tabaka',
    'nonHanafi', 'teachers', 'rolesTr', 'rolesAr', 'worksTr', 'worksAr',
    'tagsTr', 'tagsAr', 'bioTr', 'bioAr',
  ];

  const lines = [headers.join(',')];
  for (const s of scholars) {
    const row = [
      s.id,
      s.nameTr,
      s.nameAr,
      s.deathH ?? '',
      s.deathM ?? hijriToMiladiApprox(s.deathH) ?? '',
      s.region,
      s.tabaka ?? 0,
      s.nonHanafi ? 'true' : 'false',
      (s.teachers || []).join(';'),
      (s.rolesTr || []).join(';'),
      (s.rolesAr || []).join(';'),
      (s.worksTr || []).join(';'),
      (s.worksAr || []).join(';'),
      (s.tagsTr || []).join(';'),
      (s.tagsAr || []).join(';'),
      s.bioTr || '',
      s.bioAr || '',
    ].map(csvEscape);
    lines.push(row.join(','));
  }

  // UTF-8 BOM so Microsoft Excel opens Arabic & Turkish flawlessly
  const blob = new Blob(['\uFEFF' + lines.join('\r\n')], { type: 'text/csv;charset=utf-8' });
  triggerDownload(blob, filename);
}

function parseCSVLine(line) {
  const res = [];
  let cur = '';
  let inQuotes = false;
  for (let i = 0; i < line.length; i++) {
    const ch = line[i];
    if (inQuotes) {
      if (ch === '"' && line[i + 1] === '"') {
        cur += '"';
        i++;
      } else if (ch === '"') {
        inQuotes = false;
      } else {
        cur += ch;
      }
    } else if (ch === '"') {
      inQuotes = true;
    } else if (ch === ',') {
      res.push(cur);
      cur = '';
    } else {
      cur += ch;
    }
  }
  res.push(cur);
  return res;
}

function parseImportedFile(text, filename = '') {
  const clean = text.replace(/^\uFEFF/, '').trim();
  if (filename.toLowerCase().endsWith('.json') || clean.startsWith('[')) {
    const parsed = JSON.parse(clean);
    if (!Array.isArray(parsed)) throw new Error('JSON dosyası bir alim dizisi olmalıdır.');
    return parsed.map(normalizeScholar);
  }

  // CSV parse
  const lines = clean.split(/\r?\n/).filter((l) => l.trim().length > 0);
  if (lines.length < 2) throw new Error('CSV dosyası boş veya geçersiz.');
  const headers = parseCSVLine(lines[0]).map((h) => h.trim());
  const out = [];

  for (let i = 1; i < lines.length; i++) {
    const cols = parseCSVLine(lines[i]);
    const obj = {};
    headers.forEach((h, idx) => {
      obj[h] = cols[idx] ?? '';
    });
    out.push(normalizeScholar(obj));
  }
  return out;
}

function splitList(val) {
  if (Array.isArray(val)) return val.map((x) => String(x).trim()).filter(Boolean);
  if (!val) return [];
  return String(val).split(/[;|]/).map((x) => x.trim()).filter(Boolean);
}

function normalizeScholar(raw) {
  const id = String(raw.id || '').trim() || `scholar-${Date.now()}-${Math.random().toString(36).slice(2, 6)}`;
  return {
    id,
    nameTr: String(raw.nameTr || raw.nameAr || id).trim(),
    nameAr: String(raw.nameAr || raw.nameTr || id).trim(),
    deathH: raw.deathH ? Number(raw.deathH) : 100,
    deathM: raw.deathM ? Number(raw.deathM) : undefined,
    region: String(raw.region || 'kufe').trim(),
    tabaka: raw.tabaka !== undefined && raw.tabaka !== '' ? Number(raw.tabaka) : 6,
    nonHanafi: raw.nonHanafi === true || String(raw.nonHanafi).toLowerCase() === 'true',
    teachers: splitList(raw.teachers),
    rolesTr: splitList(raw.rolesTr),
    rolesAr: splitList(raw.rolesAr),
    worksTr: splitList(raw.worksTr),
    worksAr: splitList(raw.worksAr),
    tagsTr: splitList(raw.tagsTr),
    tagsAr: splitList(raw.tagsAr),
    bioTr: String(raw.bioTr || '').trim(),
    bioAr: String(raw.bioAr || '').trim(),
  };
}


// ===== src/ui/app.js =====
// Interactive Application Controller for Hanefî Tabakat & Silsile Studio







const STORAGE_SCHOLARS_KEY = 'hanefi_tabakat_scholars_v1';
const STORAGE_OFFSETS_KEY = 'hanefi_tabakat_offsets_v1';

// Load persisted scholars or default digitized PDF set
function loadScholars() {
  try {
    const raw = localStorage.getItem(STORAGE_SCHOLARS_KEY);
    if (raw) {
      const parsed = JSON.parse(raw);
      if (Array.isArray(parsed) && parsed.length > 0) return parsed;
    }
  } catch (_) {}
  return structuredClone(INITIAL_SCHOLARS);
}

function loadOffsets() {
  try {
    const raw = localStorage.getItem(STORAGE_OFFSETS_KEY);
    if (raw) return JSON.parse(raw) || {};
  } catch (_) {}
  return {};
}

const state = {
  scholars: loadScholars(),
  customOffsets: loadOffsets(),
  lang: 'both', // 'tr' | 'ar' | 'both'
  layoutMode: 'century', // 'century' | 'compact'
  colorMode: 'region', // 'region' | 'tabaka' | 'minimal'
  themeId: 'parchment', // 'parchment' | 'printWhite' | 'night'

  // Variable card & poster fields
  showHijri: true,
  showMiladi: false,
  showTabaka: false,
  showRegion: false,
  showRoles: false,
  showWorks: false,
  showTags: false,
  showNonHanafi: true,
  showCenturyBands: true,
  showHeader: true,
  showLegend: true,

  // Filters
  regionFilter: 'all',
  tabakaFilter: 'all',
  centuryMin: 1,
  centuryMax: 15,

  // Interactive focus & selection
  selectedId: null,
  focusId: null,
  focusMode: 'off', // 'off' | 'highlight' | 'isolate'
  focusDirection: 'both', // 'both' | 'ancestors' | 'descendants'
  activeBookId: null,
  dragMode: false,
  posterMode: false,

  // Pan & Zoom
  panX: 24,
  panY: 16,
  zoom: 0.45,
};

let currentLayout = null;
let currentSvgString = '';
let modalSelectedTeachers = [];

// DOM refs
const $ = (id) => document.getElementById(id);
const appEl = $('app');
const sidebarEl = $('sidebar');
const inspectorEl = $('inspector');
const viewportEl = $('svg-viewport');
const transformEl = $('svg-transform');

function saveScholars() {
  try {
    localStorage.setItem(STORAGE_SCHOLARS_KEY, JSON.stringify(state.scholars));
  } catch (_) {}
}

function saveOffsets() {
  try {
    localStorage.setItem(STORAGE_OFFSETS_KEY, JSON.stringify(state.customOffsets));
  } catch (_) {}
}

function getActiveBook() {
  if (!state.activeBookId) return null;
  for (const grp of LITERATURE_GROUPS) {
    const found = grp.items.find((i) => i.id === state.activeBookId);
    if (found) return found;
  }
  return null;
}

function getUiLang() {
  return state.lang === 'ar' ? 'ar' : 'tr';
}

function applyUILanguage() {
  const t = UI_TEXT[getUiLang()];
  document.documentElement.lang = getUiLang();
  $('ui-app-title').textContent = t.appTitle;
  $('search-input').placeholder = t.searchPlaceholder;
  $('lbl-layout-century').textContent = t.layoutCentury;
  $('lbl-layout-compact').textContent = t.layoutCompact;
  $('lbl-drag-tweak').textContent = t.dragTweak;
  $('lbl-poster-mode').textContent = t.posterMode;
  $('lbl-exit-poster').textContent = t.exitPosterMode;
  $('lbl-export-menu').textContent = t.exportMenu;
  $('lbl-exp-svg').textContent = t.exportSvg;
  $('lbl-exp-print').textContent = t.exportPrint;
  $('lbl-exp-json').textContent = t.exportJson;
  $('lbl-exp-csv').textContent = t.exportCsv;
  $('sec-card-fields').textContent = t.secCardFields;
  $('sec-filters').textContent = t.secFilters;
  $('sec-books').textContent = t.secBooks;
  $('sec-data').textContent = t.secData;
  $('lbl-f-hijri').textContent = t.fieldHijri;
  $('lbl-f-miladi').textContent = t.fieldMiladi;
  $('lbl-f-tabaka').textContent = t.fieldTabaka;
  $('lbl-f-region').textContent = t.fieldRegion;
  $('lbl-f-roles').textContent = t.fieldRoles;
  $('lbl-f-works').textContent = t.fieldWorks;
  $('lbl-f-tags').textContent = t.fieldTags;
  $('lbl-f-nonhanafi').textContent = t.fieldNonHanafi;
  $('lbl-f-bands').textContent = t.fieldCenturyBands;
  $('lbl-f-header').textContent = t.fieldHeader;
  $('lbl-f-legend').textContent = t.fieldLegend;
  $('lbl-century-range').textContent = t.centuryRange;
  $('lbl-add-scholar').textContent = t.addScholar;
  $('lbl-import-data').textContent = t.importData;
  $('lbl-focus-title').textContent = t.focusTitle;
  $('lbl-f-off').textContent = t.focusOff;
  $('lbl-f-highlight').textContent = t.focusHighlight;
  $('lbl-f-isolate').textContent = t.focusIsolate;
  $('lbl-d-both').textContent = t.dirBoth;
  $('lbl-d-anc').textContent = t.dirAncestors;
  $('lbl-d-desc').textContent = t.dirDescendants;
  $('lbl-edit-scholar').textContent = t.editScholar;
  $('lbl-add-student').textContent = t.addStudentTo;
  $('lbl-delete-scholar').textContent = t.deleteScholar;

  // Color mode select labels
  const cm = $('color-mode-select');
  cm.options[0].textContent = t.colorRegion;
  cm.options[1].textContent = t.colorTabaka;
  cm.options[2].textContent = t.colorMinimal;

  populateFilterSelects();
  renderLiteratureSidebar();
}

function populateFilterSelects() {
  const isAr = state.lang === 'ar';
  const t = UI_TEXT[getUiLang()];

  const regSel = $('filter-region');
  const prevReg = state.regionFilter;
  regSel.innerHTML = `<option value="all">${t.allRegions}</option>`;
  Object.values(REGIONS).filter((r) => r.id !== 'root').forEach((r) => {
    const opt = document.createElement('option');
    opt.value = r.id;
    opt.textContent = isAr ? r.nameAr : state.lang === 'both' ? `${r.nameTr} (${r.nameAr})` : r.nameTr;
    regSel.appendChild(opt);
  });
  regSel.value = prevReg;

  const tabSel = $('filter-tabaka');
  const prevTab = state.tabakaFilter;
  tabSel.innerHTML = `<option value="all">${t.allTabakat}</option>`;
  Object.values(TABAKAT).forEach((tb) => {
    const opt = document.createElement('option');
    opt.value = String(tb.id);
    opt.textContent = isAr ? `${tb.shortAr} — ${tb.nameAr}` : `${tb.shortTr} — ${tb.nameTr}`;
    tabSel.appendChild(opt);
  });
  tabSel.value = prevTab;
}

function renderLiteratureSidebar() {
  const isAr = state.lang === 'ar';
  const listEl = $('literature-list');
  listEl.innerHTML = '';

  LITERATURE_GROUPS.forEach((grp) => {
    const wrap = document.createElement('div');
    const title = document.createElement('div');
    title.className = 'lit-group-title';
    title.textContent = isAr ? grp.titleAr : grp.titleTr;
    wrap.appendChild(title);

    const itemsDiv = document.createElement('div');
    itemsDiv.className = 'lit-items';
    grp.items.forEach((bk) => {
      const btn = document.createElement('button');
      btn.className = `lit-chip ${state.activeBookId === bk.id ? 'active' : ''}`;
      btn.textContent = isAr ? bk.nameAr : bk.nameTr;
      btn.addEventListener('click', () => {
        if (state.activeBookId === bk.id) {
          state.activeBookId = null;
        } else {
          state.activeBookId = bk.id;
          state.focusMode = 'off';
        }
        renderLiteratureSidebar();
        renderPoster();
      });
      itemsDiv.appendChild(btn);
    });
    wrap.appendChild(itemsDiv);
    listEl.appendChild(wrap);
  });

  $('btn-clear-book').classList.toggle('hidden', !state.activeBookId);
}

function renderPoster(shouldFit = false) {
  const activeBook = getActiveBook();
  currentLayout = computePosterLayout(state.scholars, state);
  currentSvgString = renderPosterSVG(currentLayout, state, activeBook);

  transformEl.innerHTML = currentSvgString;
  bindSvgNodeEvents();
  updateStatsAndBanner();

  if (shouldFit) {
    fitPosterToViewport();
  } else {
    applyTransform();
  }

  if (state.selectedId) {
    renderInspector(state.selectedId);
  }
}

function updateStatsAndBanner() {
  const t = UI_TEXT[getUiLang()];
  const cCount = currentLayout.bands.length;
  const statsParts = [
    `${currentLayout.nodes.length} ${t.statsScholars}`,
    `${currentLayout.edges.length} ${t.statsEdges}`,
  ];
  if (cCount > 0) statsParts.push(`${cCount} ${t.statsCenturies}`);
  $('stats-pill').textContent = statsParts.join(' · ');

  const banner = $('active-banner');
  const bannerTxt = $('active-banner-text');

  if (state.focusMode !== 'off' && state.focusId) {
    const sc = state.scholars.find((s) => s.id === state.focusId);
    if (sc) {
      const modeLbl = state.focusMode === 'isolate' ? t.focusIsolate : t.focusHighlight;
      const dirLbl = state.focusDirection === 'ancestors' ? t.dirAncestors : state.focusDirection === 'descendants' ? t.dirDescendants : t.dirBoth;
      const name = state.lang === 'ar' ? sc.nameAr : sc.nameTr;
      bannerTxt.textContent = `${modeLbl}: ${name} (${dirLbl})`;
      banner.classList.remove('hidden');
      return;
    }
  }

  const activeBook = getActiveBook();
  if (activeBook) {
    const bkName = state.lang === 'ar' ? activeBook.nameAr : activeBook.nameTr;
    bannerTxt.textContent = `${t.bookActiveHint}: ${bkName}`;
    banner.classList.remove('hidden');
    return;
  }

  if (state.dragMode) {
    bannerTxt.textContent = state.lang === 'ar'
      ? 'وضع تحريك البطاقات مفعل: اسحب أي بطاقة لضبط موقعها في اللوحة'
      : 'Kart Taşıma Modu Aktif: Baskı öncesi herhangi bir alim kartını sürükleyip ince ayar yapabilirsiniz.';
    banner.classList.remove('hidden');
    return;
  }

  banner.classList.add('hidden');
}

function applyTransform() {
  transformEl.style.transform = `translate(${state.panX}px, ${state.panY}px) scale(${state.zoom})`;
}

function fitPosterToViewport() {
  if (!currentLayout) return;
  const rect = viewportEl.getBoundingClientRect();
  if (!rect.width || !rect.height) return;
  const pad = 28;
  const scaleX = (rect.width - pad * 2) / currentLayout.width;
  const scaleY = (rect.height - pad * 2) / currentLayout.height;
  // For very tall wall posters, prefer fitting width cleanly (so it's immediately legible) unless it's a compact isolated tree
  const fitAll = Math.min(scaleX, scaleY);
  const fitW = scaleX * 0.96;
  state.zoom = currentLayout.height > currentLayout.width * 1.65 ? Math.max(fitAll, Math.min(fitW, 0.72)) : Math.min(fitAll, 1.05);
  state.zoom = Math.max(0.15, Math.min(state.zoom, 1.4));
  state.panX = Math.max(pad, (rect.width - currentLayout.width * state.zoom) / 2);
  state.panY = pad;
  applyTransform();
}

function centerOnScholar(id) {
  if (!currentLayout) return;
  const node = currentLayout.nodes.find((n) => n.scholar.id === id);
  if (!node) return;
  const rect = viewportEl.getBoundingClientRect();
  state.zoom = Math.max(state.zoom, 0.85);
  state.panX = rect.width / 2 - node.cx * state.zoom;
  state.panY = rect.height / 2 - node.cy * state.zoom;
  applyTransform();
}

// Node clicks + optional drag-tweak for poster fine-tuning
function bindSvgNodeEvents() {
  const nodeEls = transformEl.querySelectorAll('.scholar-node');
  nodeEls.forEach((el) => {
    const id = el.getAttribute('data-id');

    el.addEventListener('click', (ev) => {
      if (el.dataset.dragged === '1') {
        el.dataset.dragged = '0';
        return;
      }
      ev.stopPropagation();
      selectScholar(id);
    });

    el.addEventListener('mousedown', (ev) => {
      if (!state.dragMode || ev.button !== 0) return;
      ev.stopPropagation();
      ev.preventDefault();
      const startX = ev.clientX;
      const startY = ev.clientY;
      const prevOff = state.customOffsets[id] || { dx: 0, dy: 0 };
      let moved = false;

      const onMove = (mEv) => {
        const dx = (mEv.clientX - startX) / state.zoom;
        const dy = (mEv.clientY - startY) / state.zoom;
        if (Math.abs(dx) > 2 || Math.abs(dy) > 2) moved = true;
        state.customOffsets[id] = { dx: prevOff.dx + dx, dy: prevOff.dy + dy };
        el.setAttribute('transform', `translate(${dx}, ${dy})`);
      };

      const onUp = () => {
        window.removeEventListener('mousemove', onMove);
        window.removeEventListener('mouseup', onUp);
        if (moved) {
          el.dataset.dragged = '1';
          saveOffsets();
          renderPoster(false);
        }
      };

      window.addEventListener('mousemove', onMove);
      window.addEventListener('mouseup', onUp);
    });
  });
}

function selectScholar(id, jump = false) {
  state.selectedId = id;
  if (state.focusMode !== 'off') {
    state.focusId = id;
  }
  renderInspector(id);
  renderPoster(false);
  if (jump) centerOnScholar(id);
}

function renderInspector(id) {
  const s = state.scholars.find((x) => x.id === id);
  if (!s) {
    inspectorEl.classList.add('hidden');
    return;
  }
  inspectorEl.classList.remove('hidden');

  const isAr = state.lang === 'ar';
  const t = UI_TEXT[getUiLang()];
  const reg = REGIONS[s.region] || REGIONS.kufe;
  const tb = TABAKAT[s.tabaka] || TABAKAT[0];
  const mYear = s.deathM || hijriToMiladiApprox(s.deathH);

  $('insp-name-ar').textContent = s.nameAr;
  $('insp-name-tr').textContent = s.nameTr;

  // Badges
  const badgesEl = $('insp-badges');
  badgesEl.innerHTML = '';
  const addBadge = (text, border, bg, color) => {
    const sp = document.createElement('span');
    sp.className = 'badge-pill';
    sp.textContent = text;
    if (border) sp.style.borderColor = border;
    if (bg) sp.style.background = bg;
    if (color) sp.style.color = color;
    badgesEl.appendChild(sp);
  };

  addBadge(isAr ? `ت ${toArabicDigits(s.deathH)} هـ / ${toArabicDigits(mYear)} م` : `v. H. ${s.deathH} / M. ${mYear}`);
  addBadge(isAr ? reg.nameAr : reg.nameTr, reg.stroke, reg.fill, reg.text);
  if (s.tabaka > 0) {
    addBadge(isAr ? `${tb.shortAr}: ${tb.nameAr}` : `${tb.shortTr}: ${tb.nameTr}`, tb.stroke, tb.fill, tb.text);
  }
  if (s.nonHanafi) {
    addBadge(isAr ? '* إسناد غير حنفي' : '* Gayri-Hanefî İsnad', '#94a3b8', '#f1f5f9', '#334155');
  }

  // Focus mode buttons state
  const isFocusedHere = state.focusId === id && state.focusMode !== 'off';
  const effectiveMode = isFocusedHere ? state.focusMode : 'off';
  document.querySelectorAll('.f-btn').forEach((btn) => {
    btn.classList.toggle('active', btn.dataset.fmode === effectiveMode);
  });
  document.querySelectorAll('.f-dir-btn').forEach((btn) => {
    btn.classList.toggle('active', btn.dataset.fdir === state.focusDirection);
  });

  const lin = computeLineage(state.scholars, id, 'both');
  $('focus-counts').textContent = isAr
    ? `${toArabicDigits(lin.ancestors.size)} شيخ في السلسلة العليا  •  ${toArabicDigits(lin.descendants.size)} تلميذ في السلسلة السفلى`
    : `Öncesi: ${lin.ancestors.size} alim (hoca zinciri)  •  Sonrası: ${lin.descendants.size} alim (talebe zinciri)`;

  // Detail blocks
  const det = $('insp-details');
  det.innerHTML = '';

  const addBlock = (heading, contentEl) => {
    const blk = document.createElement('div');
    blk.className = 'detail-block';
    const h = document.createElement('h4');
    h.textContent = heading;
    blk.appendChild(h);
    blk.appendChild(contentEl);
    det.appendChild(blk);
  };

  const roles = isAr ? (s.rolesAr?.length ? s.rolesAr : s.rolesTr) : (s.rolesTr?.length ? s.rolesTr : s.rolesAr);
  if (roles && roles.length) {
    const div = document.createElement('div');
    div.className = 'chip-list';
    roles.forEach((r) => {
      const sp = document.createElement('span');
      sp.className = 'badge-pill';
      sp.textContent = r;
      div.appendChild(sp);
    });
    addBlock(t.roles, div);
  }

  const works = isAr ? (s.worksAr?.length ? s.worksAr : s.worksTr) : (s.worksTr?.length ? s.worksTr : s.worksAr);
  if (works && works.length) {
    const div = document.createElement('div');
    div.className = 'chip-list';
    works.forEach((w) => {
      const sp = document.createElement('span');
      sp.className = 'work-tag';
      sp.textContent = w;
      div.appendChild(sp);
    });
    addBlock(t.works, div);
  }

  const tags = isAr ? (s.tagsAr?.length ? s.tagsAr : s.tagsTr) : (s.tagsTr?.length ? s.tagsTr : s.tagsAr);
  if (tags && tags.length) {
    const div = document.createElement('div');
    div.className = 'chip-list';
    tags.forEach((tg) => {
      const sp = document.createElement('span');
      sp.className = 'badge-pill';
      sp.textContent = `# ${tg}`;
      div.appendChild(sp);
    });
    addBlock(t.tags, div);
  }

  const bio = isAr ? (s.bioAr || s.bioTr) : (s.bioTr || s.bioAr);
  if (bio) {
    const p = document.createElement('p');
    p.textContent = bio;
    if (isAr) p.dir = 'rtl';
    addBlock(t.notes, p);
  }

  // Direct Teachers
  if (lin.directTeachers.length > 0) {
    const div = document.createElement('div');
    div.className = 'chip-list';
    lin.directTeachers.forEach((tc) => {
      const btn = document.createElement('button');
      btn.className = 'link-chip';
      btn.textContent = isAr ? `${tc.nameAr} (${toArabicDigits(tc.deathH)})` : `${tc.nameTr} (${tc.deathH})`;
      btn.addEventListener('click', () => selectScholar(tc.id, true));
      div.appendChild(btn);
    });
    addBlock(`${t.teachers} (${lin.directTeachers.length})`, div);
  }

  // Direct Students
  if (lin.directStudents.length > 0) {
    const div = document.createElement('div');
    div.className = 'chip-list';
    lin.directStudents.forEach((st) => {
      const btn = document.createElement('button');
      btn.className = 'link-chip';
      btn.textContent = isAr ? `${st.nameAr} (${toArabicDigits(st.deathH)})` : `${st.nameTr} (${st.deathH})`;
      btn.addEventListener('click', () => selectScholar(st.id, true));
      div.appendChild(btn);
    });
    addBlock(`${t.students} (${lin.directStudents.length})`, div);
  }
}

// ==================== ADD / EDIT SCHOLAR MODAL ====================
function openScholarModal(editScholar = null, prefillTeacherId = null) {
  const modal = $('scholar-modal');
  modal.classList.remove('hidden');

  // Populate region & tabaka selects inside modal
  const regSel = $('f-region');
  regSel.innerHTML = '';
  Object.values(REGIONS).forEach((r) => {
    const opt = document.createElement('option');
    opt.value = r.id;
    opt.textContent = `${r.nameTr} (${r.nameAr})`;
    regSel.appendChild(opt);
  });

  const tabSel = $('f-tabaka');
  tabSel.innerHTML = '';
  Object.values(TABAKAT).forEach((tb) => {
    const opt = document.createElement('option');
    opt.value = String(tb.id);
    opt.textContent = `${tb.shortTr} — ${tb.nameTr}`;
    tabSel.appendChild(opt);
  });

  if (editScholar) {
    $('modal-title').textContent = `Alimi Düzenle: ${editScholar.nameTr}`;
    $('f-id').value = editScholar.id;
    $('f-nameTr').value = editScholar.nameTr || '';
    $('f-nameAr').value = editScholar.nameAr || '';
    $('f-deathH').value = editScholar.deathH || '';
    $('f-deathM').value = editScholar.deathM || '';
    $('f-region').value = editScholar.region || 'kufe';
    $('f-tabaka').value = String(editScholar.tabaka ?? 6);
    $('f-nonHanafi').checked = Boolean(editScholar.nonHanafi);
    $('f-rolesTr').value = (editScholar.rolesTr || []).join('; ');
    $('f-rolesAr').value = (editScholar.rolesAr || []).join('; ');
    $('f-worksTr').value = (editScholar.worksTr || []).join('; ');
    $('f-worksAr').value = (editScholar.worksAr || []).join('; ');
    $('f-tagsTr').value = (editScholar.tagsTr || []).join('; ');
    $('f-tagsAr').value = (editScholar.tagsAr || []).join('; ');
    $('f-bioTr').value = editScholar.bioTr || '';
    $('f-bioAr').value = editScholar.bioAr || '';
    modalSelectedTeachers = [...(editScholar.teachers || [])];
  } else {
    $('modal-title').textContent = 'Yeni Alim Ekle';
    $('scholar-form').reset();
    $('f-id').value = '';
    $('f-region').value = 'rum';
    $('f-tabaka').value = '6';
    modalSelectedTeachers = prefillTeacherId ? [prefillTeacherId] : [];
    if (prefillTeacherId) {
      const tObj = state.scholars.find((x) => x.id === prefillTeacherId);
      if (tObj) {
        $('f-region').value = tObj.region === 'root' ? 'kufe' : tObj.region;
        $('f-deathH').value = (tObj.deathH || 100) + 35;
      }
    }
  }

  $('f-teacher-search').value = '';
  renderModalTeacherPicker();
}

function renderModalTeacherPicker() {
  const editId = $('f-id').value;
  const query = $('f-teacher-search').value.trim().toLowerCase();

  const selDiv = $('f-selected-teachers');
  selDiv.innerHTML = '';
  modalSelectedTeachers.forEach((tid) => {
    const sc = state.scholars.find((x) => x.id === tid);
    if (!sc) return;
    const chip = document.createElement('span');
    chip.className = 'sel-chip';
    chip.innerHTML = `${sc.nameTr} (${sc.deathH}) <button type="button" data-rm="${tid}">×</button>`;
    chip.querySelector('button').addEventListener('click', () => {
      modalSelectedTeachers = modalSelectedTeachers.filter((x) => x !== tid);
      renderModalTeacherPicker();
    });
    selDiv.appendChild(chip);
  });

  const optDiv = $('f-teacher-options');
  optDiv.innerHTML = '';
  const candidates = state.scholars
    .filter((s) => s.id !== editId && !modalSelectedTeachers.includes(s.id))
    .filter((s) => !query || s.nameTr.toLowerCase().includes(query) || s.nameAr.includes(query) || String(s.deathH).includes(query))
    .sort((a, b) => (a.deathH || 0) - (b.deathH || 0))
    .slice(0, 36);

  candidates.forEach((s) => {
    const btn = document.createElement('button');
    btn.type = 'button';
    btn.className = 't-opt';
    btn.textContent = `+ ${s.nameTr} (${s.deathH})`;
    btn.addEventListener('click', () => {
      modalSelectedTeachers.push(s.id);
      renderModalTeacherPicker();
    });
    optDiv.appendChild(btn);
  });
}

function splitSemi(str) {
  return String(str || '').split(/[;|]/).map((s) => s.trim()).filter(Boolean);
}

// ==================== EVENT WIRING ====================
function initEvents() {
  // Sidebar toggle
  $('btn-toggle-sidebar').addEventListener('click', () => {
    sidebarEl.classList.toggle('collapsed');
  });

  // Language switcher
  $('lang-switch').addEventListener('click', (ev) => {
    const btn = ev.target.closest('[data-lang]');
    if (!btn) return;
    state.lang = btn.dataset.lang;
    $('lang-switch').querySelectorAll('.seg-btn').forEach((b) => b.classList.toggle('active', b === btn));
    applyUILanguage();
    renderPoster(false);
  });

  // Layout switcher
  $('layout-switch').addEventListener('click', (ev) => {
    const btn = ev.target.closest('[data-layout]');
    if (!btn) return;
    state.layoutMode = btn.dataset.layout;
    $('layout-switch').querySelectorAll('.seg-btn').forEach((b) => b.classList.toggle('active', b === btn));
    renderPoster(true);
  });

  // Color mode & Theme
  $('color-mode-select').addEventListener('change', (ev) => {
    state.colorMode = ev.target.value;
    renderPoster(false);
  });

  $('theme-select').addEventListener('change', (ev) => {
    state.themeId = ev.target.value;
    renderPoster(false);
  });

  // Variable card field checkboxes
  document.querySelectorAll('[data-field]').forEach((cb) => {
    cb.addEventListener('change', () => {
      state[cb.dataset.field] = cb.checked;
      renderPoster(false);
    });
  });

  // Filters
  $('filter-region').addEventListener('change', (ev) => {
    state.regionFilter = ev.target.value;
    renderPoster(true);
  });

  $('filter-tabaka').addEventListener('change', (ev) => {
    state.tabakaFilter = ev.target.value;
    renderPoster(true);
  });

  const onCenturyChange = () => {
    const cMin = Math.max(1, Math.min(15, Number($('century-min').value) || 1));
    const cMax = Math.max(cMin, Math.min(15, Number($('century-max').value) || 15));
    state.centuryMin = cMin;
    state.centuryMax = cMax;
    $('century-range-val').textContent = `${cMin}. – ${cMax}. yy`;
    renderPoster(true);
  };
  $('century-min').addEventListener('change', onCenturyChange);
  $('century-max').addEventListener('change', onCenturyChange);

  $('btn-clear-book').addEventListener('click', () => {
    state.activeBookId = null;
    renderLiteratureSidebar();
    renderPoster(false);
  });

  // Search
  const searchInput = $('search-input');
  const searchDrop = $('search-results');

  searchInput.addEventListener('input', () => {
    const q = searchInput.value.trim().toLowerCase();
    if (!q) {
      searchDrop.classList.add('hidden');
      return;
    }
    const matches = state.scholars.filter((s) => {
      const blob = [
        s.nameTr, s.nameAr, String(s.deathH || ''),
        ...(s.worksTr || []), ...(s.worksAr || []),
        ...(s.rolesTr || []), ...(s.rolesAr || []),
        ...(s.tagsTr || []), ...(s.tagsAr || []),
      ].join(' ').toLowerCase();
      return blob.includes(q);
    }).slice(0, 14);

    searchDrop.innerHTML = '';
    if (matches.length === 0) {
      searchDrop.innerHTML = `<div class="search-item"><span class="search-item-tr">Sonuç bulunamadı</span></div>`;
    } else {
      matches.forEach((m) => {
        const div = document.createElement('div');
        div.className = 'search-item';
        div.innerHTML = `
          <div class="search-item-names">
            <span class="search-item-ar">${m.nameAr}</span>
            <span class="search-item-tr">${m.nameTr}</span>
          </div>
          <span class="search-item-year">v. ${m.deathH}</span>
        `;
        div.addEventListener('click', () => {
          searchDrop.classList.add('hidden');
          searchInput.value = '';
          selectScholar(m.id, true);
        });
        searchDrop.appendChild(div);
      });
    }
    searchDrop.classList.remove('hidden');
  });

  document.addEventListener('click', (ev) => {
    if (!ev.target.closest('.search-box')) searchDrop.classList.add('hidden');
    if (!ev.target.closest('.dropdown')) $('export-dropdown').classList.add('hidden');
  });

  // Drag Tweak Mode
  $('btn-drag-mode').addEventListener('click', () => {
    state.dragMode = !state.dragMode;
    $('btn-drag-mode').classList.toggle('active', state.dragMode);
    viewportEl.classList.toggle('drag-mode', state.dragMode);
    updateStatsAndBanner();
  });

  // Fullscreen Poster Mode
  const setPosterMode = (on) => {
    state.posterMode = on;
    appEl.classList.toggle('poster-mode', on);
    $('btn-exit-poster').classList.toggle('hidden', !on);
    setTimeout(() => fitPosterToViewport(), 40);
  };
  $('btn-poster-mode').addEventListener('click', () => setPosterMode(true));
  $('btn-exit-poster').addEventListener('click', () => setPosterMode(false));
  window.addEventListener('keydown', (ev) => {
    if (ev.key === 'Escape' && state.posterMode) setPosterMode(false);
  });

  // Export Menu
  $('btn-export-menu').addEventListener('click', (ev) => {
    ev.stopPropagation();
    $('export-dropdown').classList.toggle('hidden');
  });

  $('export-dropdown').addEventListener('click', async (ev) => {
    const btn = ev.target.closest('[data-export]');
    if (!btn) return;
    $('export-dropdown').classList.add('hidden');
    const type = btn.dataset.export;
    const suffix = state.focusMode === 'isolate' && state.focusId ? `-${state.focusId}` : '';

    if (type === 'svg') {
      exportPosterSVG(currentSvgString, `hanefi-tabakat-afis${suffix}.svg`);
    } else if (type === 'png2') {
      await exportPosterPNG(currentSvgString, currentLayout.width, currentLayout.height, 2, `hanefi-tabakat-afis${suffix}-2x.png`);
    } else if (type === 'png3') {
      await exportPosterPNG(currentSvgString, currentLayout.width, currentLayout.height, 3, `hanefi-tabakat-afis${suffix}-3x.png`);
    } else if (type === 'print') {
      printPosterPDF(currentSvgString);
    } else if (type === 'json') {
      exportScholarsJSON(state.scholars);
    } else if (type === 'csv') {
      exportScholarsCSV(state.scholars);
    }
  });

  // Active Banner clear
  $('btn-banner-clear').addEventListener('click', () => {
    if (state.focusMode !== 'off') {
      state.focusMode = 'off';
      state.focusId = null;
      renderPoster(true);
    } else if (state.activeBookId) {
      state.activeBookId = null;
      renderLiteratureSidebar();
      renderPoster(false);
    } else if (state.dragMode) {
      state.dragMode = false;
      $('btn-drag-mode').classList.remove('active');
      viewportEl.classList.remove('drag-mode');
      updateStatsAndBanner();
    }
  });

  // Inspector controls
  $('btn-close-inspector').addEventListener('click', () => {
    state.selectedId = null;
    inspectorEl.classList.add('hidden');
    renderPoster(false);
  });

  document.querySelectorAll('.f-btn').forEach((btn) => {
    btn.addEventListener('click', () => {
      if (!state.selectedId) return;
      const mode = btn.dataset.fmode;
      state.focusMode = mode;
      state.focusId = mode === 'off' ? null : state.selectedId;
      state.activeBookId = null;
      renderLiteratureSidebar();
      renderPoster(mode === 'isolate');
    });
  });

  document.querySelectorAll('.f-dir-btn').forEach((btn) => {
    btn.addEventListener('click', () => {
      if (!state.selectedId) return;
      state.focusDirection = btn.dataset.fdir;
      if (state.focusMode === 'off') {
        state.focusMode = 'highlight';
        state.focusId = state.selectedId;
      }
      renderPoster(state.focusMode === 'isolate');
    });
  });

  $('btn-edit-scholar').addEventListener('click', () => {
    const sc = state.scholars.find((x) => x.id === state.selectedId);
    if (sc) openScholarModal(sc);
  });

  $('btn-add-student').addEventListener('click', () => {
    if (state.selectedId) openScholarModal(null, state.selectedId);
  });

  $('btn-delete-scholar').addEventListener('click', () => {
    const sc = state.scholars.find((x) => x.id === state.selectedId);
    if (!sc) return;
    if (!confirm(`"${sc.nameTr}" kaydını silmek istediğinize emin misiniz?`)) return;
    state.scholars = state.scholars
      .filter((x) => x.id !== sc.id)
      .map((x) => ({ ...x, teachers: (x.teachers || []).filter((t) => t !== sc.id) }));
    state.selectedId = null;
    if (state.focusId === sc.id) {
      state.focusId = null;
      state.focusMode = 'off';
    }
    inspectorEl.classList.add('hidden');
    saveScholars();
    renderPoster(false);
  });

  $('btn-copy-embed').addEventListener('click', async () => {
    if (!state.selectedId) return;
    const mode = state.focusId === state.selectedId && state.focusMode !== 'off' ? state.focusMode : 'isolate';
    const dir = state.focusDirection || 'both';
    const snippet = `<iframe src="/static/tabakat/index.html?focus=${encodeURIComponent(state.selectedId)}&mode=${mode}&dir=${dir}&lang=${state.lang}&embed=1" style="width:100%; height:82vh; border:1px solid #d9ceb2; border-radius:10px;" loading="lazy"></iframe>`;
    try {
      await navigator.clipboard.writeText(snippet);
      const lbl = $('lbl-copy-embed');
      const prev = lbl.textContent;
      lbl.textContent = 'Kopyalandı!';
      setTimeout(() => { lbl.textContent = prev; }, 1600);
    } catch (_) {
      window.prompt('Quartz / Obsidian notunuza yapıştırın:', snippet);
    }
  });

  // Sidebar Data buttons
  $('btn-add-scholar').addEventListener('click', () => openScholarModal(null, null));

  $('import-file-input').addEventListener('change', (ev) => {
    const file = ev.target.files?.[0];
    if (!file) return;
    const reader = new FileReader();
    reader.onload = () => {
      try {
        const imported = parseImportedFile(String(reader.result || ''), file.name);
        if (imported.length === 0) throw new Error('Kayıt bulunamadı.');
        state.scholars = imported;
        state.selectedId = null;
        state.focusId = null;
        state.focusMode = 'off';
        inspectorEl.classList.add('hidden');
        saveScholars();
        renderPoster(true);
        alert(`${imported.length} alim başarıyla içe aktarıldı.`);
      } catch (err) {
        alert(`İçe aktarma hatası: ${err.message}`);
      }
      ev.target.value = '';
    };
    reader.readAsText(file, 'UTF-8');
  });

  $('btn-reset-positions').addEventListener('click', () => {
    state.customOffsets = {};
    saveOffsets();
    renderPoster(true);
  });

  $('btn-reset-data').addEventListener('click', () => {
    if (!confirm('Tüm eklediğiniz değişiklikler silinip PDF’deki orijinal alim listesine dönülsün mü?')) return;
    state.scholars = structuredClone(INITIAL_SCHOLARS);
    state.customOffsets = {};
    state.selectedId = null;
    state.focusId = null;
    state.focusMode = 'off';
    inspectorEl.classList.add('hidden');
    saveScholars();
    saveOffsets();
    renderPoster(true);
  });

  // Modal Form events
  const closeModal = () => $('scholar-modal').classList.add('hidden');
  $('btn-close-modal').addEventListener('click', closeModal);
  $('btn-cancel-modal').addEventListener('click', closeModal);
  $('f-teacher-search').addEventListener('input', renderModalTeacherPicker);

  $('scholar-form').addEventListener('submit', (ev) => {
    ev.preventDefault();
    const editId = $('f-id').value.trim();
    const nameTr = $('f-nameTr').value.trim();
    const nameAr = $('f-nameAr').value.trim();
    const deathH = Number($('f-deathH').value);
    const deathMRaw = $('f-deathM').value.trim();

    const record = {
      id: editId || `${nameTr.toLowerCase().replace(/[^a-z0-9]+/g, '-').replace(/^-|-$/g, '')}-${Date.now().toString(36).slice(-4)}`,
      nameTr,
      nameAr,
      deathH,
      deathM: deathMRaw ? Number(deathMRaw) : undefined,
      region: $('f-region').value,
      tabaka: Number($('f-tabaka').value),
      nonHanafi: $('f-nonHanafi').checked,
      teachers: [...modalSelectedTeachers],
      rolesTr: splitSemi($('f-rolesTr').value),
      rolesAr: splitSemi($('f-rolesAr').value),
      worksTr: splitSemi($('f-worksTr').value),
      worksAr: splitSemi($('f-worksAr').value),
      tagsTr: splitSemi($('f-tagsTr').value),
      tagsAr: splitSemi($('f-tagsAr').value),
      bioTr: $('f-bioTr').value.trim(),
      bioAr: $('f-bioAr').value.trim(),
    };

    if (editId) {
      const idx = state.scholars.findIndex((s) => s.id === editId);
      if (idx >= 0) state.scholars[idx] = record;
    } else {
      state.scholars.push(record);
    }

    saveScholars();
    closeModal();
    selectScholar(record.id, true);
  });

  // Pan & Zoom controls
  let isPanning = false;
  let panStartX = 0;
  let panStartY = 0;

  viewportEl.addEventListener('mousedown', (ev) => {
    if (ev.button !== 0) return;
    if (state.dragMode && ev.target.closest('.scholar-node')) return;
    isPanning = true;
    panStartX = ev.clientX - state.panX;
    panStartY = ev.clientY - state.panY;
    viewportEl.classList.add('panning');
  });

  window.addEventListener('mousemove', (ev) => {
    if (!isPanning) return;
    state.panX = ev.clientX - panStartX;
    state.panY = ev.clientY - panStartY;
    applyTransform();
  });

  window.addEventListener('mouseup', () => {
    if (isPanning) {
      isPanning = false;
      viewportEl.classList.remove('panning');
    }
  });

  viewportEl.addEventListener('wheel', (ev) => {
    ev.preventDefault();
    const rect = viewportEl.getBoundingClientRect();
    const mx = ev.clientX - rect.left;
    const my = ev.clientY - rect.top;
    const factor = ev.deltaY < 0 ? 1.12 : 0.89;
    const nextZoom = Math.max(0.12, Math.min(2.6, state.zoom * factor));
    const ratio = nextZoom / state.zoom;
    state.panX = mx - (mx - state.panX) * ratio;
    state.panY = my - (my - state.panY) * ratio;
    state.zoom = nextZoom;
    applyTransform();
  }, { passive: false });

  $('zoom-in').addEventListener('click', () => {
    state.zoom = Math.min(2.6, state.zoom * 1.2);
    applyTransform();
  });
  $('zoom-out').addEventListener('click', () => {
    state.zoom = Math.max(0.12, state.zoom / 1.2);
    applyTransform();
  });
  $('zoom-100').addEventListener('click', () => {
    state.zoom = 1;
    applyTransform();
  });
  $('zoom-fit').addEventListener('click', fitPosterToViewport);
}

let embedHideInspectorOnLoad = false;

function applyUrlParams() {
  const params = new URLSearchParams(window.location.search);
  const lang = params.get('lang');
  if (lang && ['tr', 'ar', 'both'].includes(lang)) {
    state.lang = lang;
    $('lang-switch').querySelectorAll('.seg-btn').forEach((b) => b.classList.toggle('active', b.dataset.lang === lang));
  }

  const layout = params.get('layout');
  if (layout && ['century', 'compact'].includes(layout)) {
    state.layoutMode = layout;
    $('layout-switch').querySelectorAll('.seg-btn').forEach((b) => b.classList.toggle('active', b.dataset.layout === layout));
  }

  const color = params.get('color');
  if (color && ['region', 'tabaka', 'minimal'].includes(color)) {
    state.colorMode = color;
    $('color-mode-select').value = color;
  }

  const theme = params.get('theme');
  if (theme && ['parchment', 'printWhite', 'night'].includes(theme)) {
    state.themeId = theme;
    $('theme-select').value = theme;
  }

  const dir = params.get('dir');
  if (dir && ['both', 'ancestors', 'descendants'].includes(dir)) {
    state.focusDirection = dir;
  }

  const focus = params.get('focus');
  if (focus && state.scholars.some((s) => s.id === focus)) {
    const mode = params.get('mode');
    state.selectedId = focus;
    state.focusId = focus;
    state.focusMode = ['off', 'highlight', 'isolate'].includes(mode) ? mode : 'isolate';
  }

  const embed = params.get('embed');
  if (embed === '1' || embed === 'true') {
    sidebarEl.classList.add('collapsed');
    embedHideInspectorOnLoad = true;
  }
}

// Bootstrap
applyUrlParams();
applyUILanguage();
initEvents();
renderPoster(true);
if (embedHideInspectorOnLoad) {
  inspectorEl.classList.add('hidden');
}

})();
</script>
</body>
</html>

