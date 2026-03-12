<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DP 自由行推荐</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
/* ─── Reset & Variables ─────────────────────────────────────────────── */
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg:       #F0F4F8;
  --surface:  #FFFFFF;
  --surface2: #F7F9FC;
  --border:   #E2E8F0;
  --primary:  #1A56DB;
  --primary-light: #EBF2FF;
  --primary-dark:  #1340A8;
  --accent:   #F97316;
  --accent-light: #FFF3E8;
  --green:    #059669;
  --green-light: #ECFDF5;
  --red:      #DC2626;
  --red-light: #FEF2F2;
  --text1:    #0F172A;
  --text2:    #475569;
  --text3:    #94A3B8;
  --shadow-sm: 0 1px 3px rgba(0,0,0,.08), 0 1px 2px rgba(0,0,0,.05);
  --shadow-md: 0 4px 16px rgba(0,0,0,.10), 0 2px 6px rgba(0,0,0,.06);
  --shadow-lg: 0 12px 40px rgba(0,0,0,.14), 0 4px 12px rgba(0,0,0,.08);
  --r-sm: 10px; --r-md: 16px; --r-lg: 24px;
  --font: 'Noto Sans SC', 'DM Sans', sans-serif;
  --ease-out: cubic-bezier(.22, .68, 0, 1.2);
  --ease-smooth: cubic-bezier(.4, 0, .2, 1);
}

html { font-size: 14px; }
body {
  font-family: var(--font);
  background: var(--bg);
  color: var(--text1);
  min-height: 100vh;
  overflow-x: hidden;
}

/* ─── Layout ────────────────────────────────────────────────────────── */
.app-wrap {
  max-width: 420px;
  margin: 0 auto;
  background: var(--bg);
  min-height: 100vh;
  position: relative;
  box-shadow: 0 0 60px rgba(0,0,0,.12);
}

/* ─── Status bar ─────────────────────────────────────────────────────  */
.status-bar {
  background: #fff;
  padding: 10px 20px 0;
  display: flex; justify-content: space-between; align-items: center;
  font-size: 11px; font-weight: 600; letter-spacing: .3px;
  position: sticky; top: 0; z-index: 100;
}

/* ─── Header / Nav ───────────────────────────────────────────────────  */
.header {
  background: #fff;
  padding: 12px 20px 14px;
  display: flex; align-items: center; gap: 12px;
  border-bottom: 1px solid var(--border);
  position: sticky; top: 32px; z-index: 99;
}
.header-back {
  width: 32px; height: 32px;
  border: none; background: var(--surface2);
  border-radius: 50%; cursor: pointer;
  display: flex; align-items: center; justify-content: center;
  color: var(--text2); font-size: 15px;
  transition: background .2s;
}
.header-back:hover { background: var(--border); }
.header-title { font-size: 16px; font-weight: 700; color: var(--text1); flex: 1; }
.header-share {
  width: 32px; height: 32px;
  border: none; background: none; cursor: pointer;
  color: var(--text2); font-size: 18px;
  display: flex; align-items: center; justify-content: center;
}

/* ─── Trip Info Banner ───────────────────────────────────────────────  */
.trip-banner {
  background: linear-gradient(135deg, #1A56DB 0%, #1340A8 50%, #0D2E8A 100%);
  padding: 20px;
  color: #fff;
  position: relative;
  overflow: hidden;
}
.trip-banner::before {
  content: '';
  position: absolute; inset: 0;
  background: url("data:image/svg+xml,%3Csvg width='100' height='100' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Ccircle cx='80' cy='20' r='40' fill='rgba(255,255,255,.04)'/%3E%3Ccircle cx='10' cy='80' r='30' fill='rgba(255,255,255,.03)'/%3E%3C/svg%3E");
  pointer-events: none;
}
.route-row {
  display: flex; align-items: center; gap: 10px; margin-bottom: 14px;
}
.city { font-size: 26px; font-weight: 700; letter-spacing: -.5px; }
.route-arrow {
  flex: 1; display: flex; flex-direction: column; align-items: center; gap: 2px;
}
.route-line {
  width: 100%; height: 1px;
  background: linear-gradient(90deg, rgba(255,255,255,.3), rgba(255,255,255,.7), rgba(255,255,255,.3));
  position: relative;
}
.route-plane {
  font-size: 16px; margin-top: -8px;
  animation: fly 3s ease-in-out infinite;
}
@keyframes fly {
  0%, 100% { transform: translateX(-4px); }
  50% { transform: translateX(4px); }
}
.trip-meta {
  display: flex; gap: 16px; flex-wrap: wrap;
}
.meta-chip {
  background: rgba(255,255,255,.15);
  border: 1px solid rgba(255,255,255,.2);
  border-radius: 20px; padding: 4px 12px;
  font-size: 12px; font-weight: 500;
  backdrop-filter: blur(8px);
}

/* ─── States wrapper ─────────────────────────────────────────────────  */
.states { position: relative; }
.state { display: none; }
.state.active { display: block; }

/* ─── SKELETON STATE ─────────────────────────────────────────────────  */
#state-skeleton { padding: 16px; }
.skeleton-label {
  display: flex; align-items: center; gap: 8px;
  padding: 12px 0 10px;
  font-size: 12px; font-weight: 600;
  color: var(--text3); letter-spacing: .5px; text-transform: uppercase;
}
.skeleton-label .dot {
  width: 6px; height: 6px; border-radius: 50%;
  background: var(--primary);
  animation: pulse-dot 1.2s ease-in-out infinite;
}
.skeleton-label .dot:nth-child(2) { animation-delay: .2s; }
.skeleton-label .dot:nth-child(3) { animation-delay: .4s; }
@keyframes pulse-dot {
  0%, 100% { opacity: .3; transform: scale(.8); }
  50% { opacity: 1; transform: scale(1); }
}
.skeleton-card {
  background: var(--surface);
  border-radius: var(--r-md);
  padding: 16px;
  margin-bottom: 12px;
  box-shadow: var(--shadow-sm);
  overflow: hidden;
}
.skel {
  background: linear-gradient(90deg, #E2E8F0 25%, #F1F5F9 50%, #E2E8F0 75%);
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
  border-radius: 6px;
}
@keyframes shimmer {
  0% { background-position: 200% center; }
  100% { background-position: -200% center; }
}
.skel-row { display: flex; gap: 10px; align-items: center; margin-bottom: 10px; }
.skel-circle { border-radius: 50% !important; flex-shrink: 0; }
.skel-h { height: 14px; }
.skel-h-lg { height: 20px; }
.skel-h-sm { height: 10px; }

/* ─── Partial Load Banner ────────────────────────────────────────────  */
.partial-banner {
  background: var(--primary-light);
  border: 1px solid rgba(26,86,219,.2);
  border-radius: var(--r-sm);
  padding: 10px 14px;
  margin-bottom: 12px;
  display: flex; align-items: center; gap: 10px;
  font-size: 12px; color: var(--primary);
  font-weight: 500;
}
.partial-spinner {
  width: 14px; height: 14px;
  border: 2px solid rgba(26,86,219,.3);
  border-top-color: var(--primary);
  border-radius: 50%;
  animation: spin .7s linear infinite;
  flex-shrink: 0;
}
@keyframes spin { to { transform: rotate(360deg); } }

/* ─── FLIGHT PARTIAL (loaded first) ─────────────────────────────────  */
#state-partial { padding: 16px; }
.section-header {
  display: flex; align-items: center; justify-content: space-between;
  margin-bottom: 12px;
}
.section-title {
  font-size: 13px; font-weight: 700; color: var(--text1);
  display: flex; align-items: center; gap: 6px;
}
.section-title .icon { font-size: 16px; }
.tag-new {
  background: var(--green); color: #fff;
  font-size: 10px; font-weight: 700; padding: 2px 6px;
  border-radius: 4px; letter-spacing: .3px;
}

/* ─── Flight Card ────────────────────────────────────────────────────  */
.flight-card {
  background: var(--surface);
  border-radius: var(--r-md);
  border: 1.5px solid var(--border);
  overflow: hidden;
  margin-bottom: 10px;
  box-shadow: var(--shadow-sm);
  opacity: 0; transform: translateY(12px);
  animation: card-in .45s var(--ease-out) forwards;
}
@keyframes card-in {
  to { opacity: 1; transform: translateY(0); }
}
.flight-card:nth-child(2) { animation-delay: .08s; }
.flight-direction-bar {
  background: var(--surface2);
  padding: 6px 14px;
  font-size: 11px; font-weight: 600; color: var(--text3);
  letter-spacing: .4px; text-transform: uppercase;
  border-bottom: 1px solid var(--border);
  display: flex; align-items: center; gap: 6px;
}
.flight-main {
  padding: 14px;
  display: flex; align-items: center; gap: 0;
}
.flight-time-block { text-align: center; min-width: 64px; }
.flight-time { font-size: 22px; font-weight: 700; color: var(--text1); letter-spacing: -.5px; }
.flight-airport { font-size: 11px; color: var(--text3); margin-top: 2px; }
.flight-middle {
  flex: 1; display: flex; flex-direction: column; align-items: center;
  padding: 0 10px; gap: 2px;
}
.flight-duration { font-size: 11px; color: var(--text3); font-weight: 500; }
.flight-path {
  width: 100%; display: flex; align-items: center; gap: 4px;
}
.path-line { flex: 1; height: 1px; background: var(--border); }
.path-dot { width: 5px; height: 5px; border-radius: 50%; background: var(--primary); flex-shrink: 0; }
.flight-type { font-size: 11px; color: var(--primary); font-weight: 600; }
.flight-footer {
  padding: 10px 14px;
  border-top: 1px solid var(--border);
  display: flex; align-items: center; justify-content: space-between;
}
.airline-info { display: flex; align-items: center; gap: 6px; }
.airline-logo {
  width: 20px; height: 20px; border-radius: 4px;
  background: var(--primary); color: #fff;
  font-size: 10px; font-weight: 700;
  display: flex; align-items: center; justify-content: center;
}
.airline-name { font-size: 12px; color: var(--text2); }
.flight-price { font-size: 15px; font-weight: 700; color: var(--accent); }
.flight-price span { font-size: 11px; font-weight: 400; color: var(--text3); }

/* ─── Loading Hotel ──────────────────────────────────────────────────  */
.loading-section {
  background: var(--surface);
  border-radius: var(--r-md);
  border: 1.5px dashed var(--border);
  padding: 20px 16px;
  text-align: center; margin-bottom: 10px;
}
.loading-section .loading-icon { font-size: 28px; margin-bottom: 8px; }
.loading-section p { font-size: 12px; color: var(--text3); }

/* ─── FULL RESULT STATE ──────────────────────────────────────────────  */
#state-result { padding: 16px; }

/* Recommendation reason card */
.reason-card {
  background: linear-gradient(135deg, #F0F7FF, #E8F4E8);
  border: 1px solid rgba(26,86,219,.15);
  border-radius: var(--r-md);
  padding: 14px 16px;
  margin-bottom: 16px;
  opacity: 0; transform: translateY(8px);
  animation: card-in .5s var(--ease-out) .1s forwards;
}
.reason-label {
  font-size: 11px; font-weight: 700; color: var(--primary);
  letter-spacing: .5px; text-transform: uppercase;
  margin-bottom: 6px; display: flex; align-items: center; gap: 5px;
}
.reason-text { font-size: 13px; color: var(--text1); line-height: 1.6; font-weight: 400; }

/* Package summary bar */
.package-bar {
  background: var(--surface);
  border-radius: var(--r-md);
  border: 1.5px solid var(--primary);
  padding: 14px 16px;
  margin-bottom: 12px;
  display: flex; align-items: center; justify-content: space-between;
  box-shadow: 0 0 0 4px var(--primary-light);
  opacity: 0; animation: card-in .5s var(--ease-out) .15s forwards;
}
.pkg-label { font-size: 12px; color: var(--text2); margin-bottom: 2px; }
.pkg-total { font-size: 24px; font-weight: 800; color: var(--accent); letter-spacing: -.5px; }
.pkg-total sub { font-size: 13px; font-weight: 500; color: var(--text3); vertical-align: baseline; }
.pkg-per { font-size: 11px; color: var(--text3); margin-top: 2px; }
.pkg-badge {
  background: var(--accent); color: #fff;
  font-size: 11px; font-weight: 700;
  padding: 4px 10px; border-radius: 20px;
  white-space: nowrap;
}

/* Result section */
.result-section {
  margin-bottom: 12px;
  opacity: 0; transform: translateY(10px);
}
.result-section:nth-child(2) { animation: card-in .5s var(--ease-out) .2s forwards; }
.result-section:nth-child(3) { animation: card-in .5s var(--ease-out) .28s forwards; }
.result-section:nth-child(4) { animation: card-in .5s var(--ease-out) .35s forwards; }

.section-label {
  font-size: 12px; font-weight: 700; color: var(--text2);
  margin-bottom: 8px; display: flex; align-items: center; gap: 6px;
  letter-spacing: .3px;
}
.section-label::before {
  content: ''; width: 3px; height: 14px;
  background: var(--primary); border-radius: 2px;
}

/* Hotel Card */
.hotel-card {
  background: var(--surface);
  border-radius: var(--r-md);
  border: 1.5px solid var(--border);
  overflow: hidden;
  box-shadow: var(--shadow-sm);
}
.hotel-img {
  width: 100%; height: 140px;
  background: linear-gradient(135deg, #1A56DB 0%, #7C3AED 100%);
  position: relative; overflow: hidden;
  display: flex; align-items: center; justify-content: center;
}
.hotel-img-placeholder { font-size: 48px; opacity: .4; }
.hotel-rating-badge {
  position: absolute; top: 10px; right: 10px;
  background: rgba(0,0,0,.55); backdrop-filter: blur(8px);
  color: #fff; border-radius: 8px; padding: 4px 8px;
  font-size: 12px; font-weight: 600;
  display: flex; align-items: center; gap: 4px;
}
.hotel-img-tag {
  position: absolute; bottom: 10px; left: 10px;
  background: rgba(5,150,105,.9); color: #fff;
  font-size: 10px; font-weight: 700;
  padding: 3px 8px; border-radius: 4px;
}
.hotel-body { padding: 14px; }
.hotel-name { font-size: 15px; font-weight: 700; margin-bottom: 6px; }
.hotel-tags { display: flex; flex-wrap: wrap; gap: 5px; margin-bottom: 10px; }
.hotel-tag {
  background: var(--surface2); border: 1px solid var(--border);
  border-radius: 4px; padding: 2px 8px;
  font-size: 11px; color: var(--text2);
}
.hotel-tag.highlight { background: var(--green-light); border-color: rgba(5,150,105,.2); color: var(--green); }
.hotel-price-row {
  display: flex; align-items: baseline; justify-content: space-between;
  border-top: 1px solid var(--border); padding-top: 10px;
}
.hotel-price { font-size: 18px; font-weight: 800; color: var(--accent); }
.hotel-price sub { font-size: 11px; font-weight: 400; color: var(--text3); vertical-align: baseline; }
.hotel-nights { font-size: 12px; color: var(--text3); }

/* ─── Action Buttons ─────────────────────────────────────────────────  */
.action-area {
  padding: 16px;
  background: var(--surface);
  border-top: 1px solid var(--border);
  position: sticky; bottom: 0; z-index: 90;
  box-shadow: 0 -8px 24px rgba(0,0,0,.08);
}
.btn-primary {
  width: 100%; padding: 15px;
  background: var(--primary);
  color: #fff; font-family: var(--font);
  font-size: 15px; font-weight: 700;
  border: none; border-radius: var(--r-md);
  cursor: pointer; letter-spacing: .2px;
  transition: background .2s, transform .12s, box-shadow .2s;
  position: relative; overflow: hidden;
}
.btn-primary::after {
  content: '';
  position: absolute; inset: 0;
  background: linear-gradient(135deg, rgba(255,255,255,.12), transparent);
  pointer-events: none;
}
.btn-primary:hover { background: var(--primary-dark); box-shadow: 0 4px 16px rgba(26,86,219,.4); }
.btn-primary:active { transform: scale(.98); }

.btn-row { display: flex; gap: 8px; margin-top: 8px; }
.btn-secondary {
  flex: 1; padding: 11px 8px;
  background: var(--surface);
  color: var(--primary);
  font-family: var(--font); font-size: 13px; font-weight: 600;
  border: 1.5px solid var(--primary);
  border-radius: var(--r-sm);
  cursor: pointer;
  transition: background .2s, transform .12s;
  white-space: nowrap;
}
.btn-secondary:hover { background: var(--primary-light); }
.btn-secondary:active { transform: scale(.97); }
.btn-secondary.warn { color: var(--text2); border-color: var(--border); }
.btn-secondary.warn:hover { background: var(--surface2); }

/* ─── REFRESH STATE ──────────────────────────────────────────────────  */
#state-reco { padding: 16px; }
.reco-header {
  background: var(--accent-light);
  border: 1px solid rgba(249,115,22,.2);
  border-radius: var(--r-md); padding: 14px 16px;
  margin-bottom: 16px;
  display: flex; align-items: flex-start; gap: 10px;
}
.reco-icon { font-size: 20px; flex-shrink: 0; }
.reco-header p { font-size: 13px; color: var(--text1); line-height: 1.5; }
.reco-header strong { color: var(--accent); }

.option-cards { display: flex; flex-direction: column; gap: 10px; margin-bottom: 12px; }
.option-card {
  background: var(--surface);
  border-radius: var(--r-md);
  border: 2px solid var(--border);
  padding: 14px;
  cursor: pointer;
  transition: border-color .2s, box-shadow .2s, transform .15s;
  position: relative; overflow: hidden;
}
.option-card:hover {
  border-color: var(--primary);
  box-shadow: 0 0 0 4px var(--primary-light);
  transform: translateY(-1px);
}
.option-card.selected {
  border-color: var(--primary);
  background: var(--primary-light);
}
.option-card.selected::before {
  content: '✓';
  position: absolute; top: 10px; right: 12px;
  width: 20px; height: 20px;
  background: var(--primary); color: #fff;
  border-radius: 50%; font-size: 11px; font-weight: 700;
  display: flex; align-items: center; justify-content: center;
}
.option-num {
  font-size: 10px; font-weight: 700; color: var(--primary);
  letter-spacing: .5px; text-transform: uppercase; margin-bottom: 6px;
}
.option-title { font-size: 14px; font-weight: 700; margin-bottom: 4px; }
.option-sub { font-size: 12px; color: var(--text2); line-height: 1.5; }
.option-price { font-size: 16px; font-weight: 800; color: var(--accent); margin-top: 6px; }

/* ─── NO RESULT STATE ────────────────────────────────────────────────  */
#state-empty { padding: 24px 16px; text-align: center; }
.empty-icon { font-size: 56px; margin-bottom: 16px; }
.empty-title { font-size: 17px; font-weight: 700; margin-bottom: 8px; }
.empty-sub { font-size: 13px; color: var(--text2); line-height: 1.6; margin-bottom: 20px; }
.alt-cards { display: flex; flex-direction: column; gap: 10px; text-align: left; margin-bottom: 16px; }
.alt-card {
  background: var(--surface); border-radius: var(--r-md);
  border: 1.5px solid var(--border);
  padding: 14px 16px;
  display: flex; align-items: center; justify-content: space-between;
  cursor: pointer; transition: border-color .2s, transform .15s;
}
.alt-card:hover { border-color: var(--primary); transform: translateX(3px); }
.alt-left .alt-date { font-size: 11px; color: var(--text3); margin-bottom: 3px; }
.alt-left .alt-route { font-size: 14px; font-weight: 700; }
.alt-price { font-size: 16px; font-weight: 800; color: var(--accent); }
.btn-outline {
  width: 100%; padding: 13px;
  background: none; border: 1.5px solid var(--border);
  border-radius: var(--r-md);
  color: var(--text2); font-family: var(--font);
  font-size: 14px; font-weight: 600;
  cursor: pointer; transition: border-color .2s, color .2s;
  margin-bottom: 8px;
}
.btn-outline:hover { border-color: var(--primary); color: var(--primary); }

/* ─── ORDER STATE ────────────────────────────────────────────────────  */
#state-order { padding: 0; }
.order-header {
  background: var(--green);
  padding: 20px;
  text-align: center;
  color: #fff;
}
.order-checkmark {
  width: 56px; height: 56px;
  background: rgba(255,255,255,.2);
  border-radius: 50%; margin: 0 auto 12px;
  display: flex; align-items: center; justify-content: center;
  font-size: 28px;
  animation: pop .4s var(--ease-out);
}
@keyframes pop {
  0% { transform: scale(0); opacity: 0; }
  70% { transform: scale(1.15); }
  100% { transform: scale(1); opacity: 1; }
}
.order-header h2 { font-size: 18px; font-weight: 700; margin-bottom: 4px; }
.order-header p { font-size: 13px; opacity: .85; }
.order-body { padding: 16px; }
.order-row {
  display: flex; justify-content: space-between; align-items: center;
  padding: 12px 0; border-bottom: 1px solid var(--border);
}
.order-row:last-child { border-bottom: none; }
.order-key { font-size: 13px; color: var(--text2); }
.order-val { font-size: 13px; font-weight: 600; text-align: right; }
.order-total .order-key { font-size: 14px; font-weight: 700; color: var(--text1); }
.order-total .order-val { font-size: 20px; font-weight: 800; color: var(--accent); }

/* ─── Toast ──────────────────────────────────────────────────────────  */
.toast {
  position: fixed; bottom: 90px; left: 50%; transform: translateX(-50%) translateY(20px);
  background: rgba(15,23,42,.88); color: #fff;
  padding: 10px 18px; border-radius: 20px;
  font-size: 13px; font-weight: 500;
  backdrop-filter: blur(12px);
  pointer-events: none; opacity: 0;
  transition: opacity .25s, transform .25s var(--ease-out);
  white-space: nowrap; z-index: 999;
}
.toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

/* ─── Progress Steps ─────────────────────────────────────────────────  */
.progress-bar {
  background: #fff;
  padding: 10px 20px;
  display: flex; align-items: center; gap: 0;
  border-bottom: 1px solid var(--border);
}
.step-item {
  display: flex; flex-direction: column; align-items: center; gap: 3px;
  flex: 1;
}
.step-dot {
  width: 24px; height: 24px; border-radius: 50%;
  background: var(--border); color: var(--text3);
  font-size: 11px; font-weight: 700;
  display: flex; align-items: center; justify-content: center;
  transition: background .3s, color .3s;
}
.step-dot.active { background: var(--primary); color: #fff; }
.step-dot.done { background: var(--green); color: #fff; }
.step-label { font-size: 10px; color: var(--text3); font-weight: 500; }
.step-label.active { color: var(--primary); font-weight: 600; }
.step-connector { flex: 1; height: 1px; background: var(--border); margin-bottom: 14px; }
.step-connector.done { background: var(--green); }

/* ─── Slide Transition ───────────────────────────────────────────────  */
.state { animation: none; }
.state.slide-in {
  animation: slide-in .35s var(--ease-smooth) forwards;
}
@keyframes slide-in {
  from { opacity: 0; transform: translateX(24px); }
  to   { opacity: 1; transform: translateX(0); }
}

/* ─── Ripple ─────────────────────────────────────────────────────────  */
.btn-primary, .btn-secondary, .option-card, .alt-card {
  -webkit-tap-highlight-color: transparent;
}

/* ─── Scrollbar ──────────────────────────────────────────────────────  */
::-webkit-scrollbar { width: 4px; }
::-webkit-scrollbar-track { background: transparent; }
::-webkit-scrollbar-thumb { background: var(--border); border-radius: 2px; }

/* ─── Utilities ──────────────────────────────────────────────────────  */
.mt-8 { margin-top: 8px; }
.text-green { color: var(--green); }
.text-accent { color: var(--accent); }
.text-sm { font-size: 12px; color: var(--text2); }
.flex-between { display: flex; align-items: center; justify-content: space-between; }
</style>
</head>
<body>
<div class="app-wrap">

  <!-- Status Bar -->
  <div class="status-bar">
    <span>9:41</span>
    <span>📶 🔋</span>
  </div>

  <!-- Header -->
  <div class="header">
    <button class="header-back" onclick="goBack()">←</button>
    <div class="header-title" id="header-title">为你匹配方案</div>
    <button class="header-share">⋯</button>
  </div>

  <!-- Progress Steps -->
  <div class="progress-bar" id="progress-bar">
    <div class="step-item">
      <div class="step-dot done" id="step1">✓</div>
      <div class="step-label">意图识别</div>
    </div>
    <div class="step-connector done" id="conn1"></div>
    <div class="step-item">
      <div class="step-dot active" id="step2">2</div>
      <div class="step-label active" id="steplabel2">推荐方案</div>
    </div>
    <div class="step-connector" id="conn2"></div>
    <div class="step-item">
      <div class="step-dot" id="step3">3</div>
      <div class="step-label" id="steplabel3">确认订单</div>
    </div>
    <div class="step-connector" id="conn3"></div>
    <div class="step-item">
      <div class="step-dot" id="step4">4</div>
      <div class="step-label" id="steplabel4">提交</div>
    </div>
  </div>

  <!-- Trip Banner -->
  <div class="trip-banner">
    <div class="route-row">
      <div class="city">上海</div>
      <div class="route-arrow">
        <div class="route-plane">✈️</div>
        <div class="route-line"></div>
      </div>
      <div class="city">三亚</div>
    </div>
    <div class="trip-meta">
      <div class="meta-chip">3月20日出发</div>
      <div class="meta-chip">往返 4天</div>
      <div class="meta-chip">2位成人</div>
      <div class="meta-chip">性价比优先</div>
    </div>
  </div>

  <!-- ═══════ STATE: SKELETON ════════════════════════════════════════ -->
  <div class="states">
    <div class="state active" id="state-skeleton">
      <div style="padding:16px">
        <div class="skeleton-label">
          <div class="dot"></div><div class="dot"></div><div class="dot"></div>
          正在为你匹配最优机酒方案
        </div>
        <!-- flight skel -->
        <div class="skeleton-card">
          <div class="skel-row" style="margin-bottom:14px">
            <div class="skel skel-circle" style="width:28px;height:28px"></div>
            <div class="skel skel-h" style="width:40%"></div>
            <div class="skel skel-h-sm" style="width:20%;margin-left:auto"></div>
          </div>
          <div style="display:flex;gap:8px;align-items:center;margin-bottom:12px">
            <div style="flex:1">
              <div class="skel skel-h-lg" style="width:55%;margin-bottom:6px"></div>
              <div class="skel skel-h-sm" style="width:35%"></div>
            </div>
            <div style="flex:.6;text-align:center">
              <div class="skel skel-h-sm" style="width:60%;margin:0 auto 6px"></div>
              <div class="skel skel-h-sm" style="width:80%;margin:0 auto"></div>
            </div>
            <div style="flex:1;text-align:right">
              <div class="skel skel-h-lg" style="width:55%;margin-left:auto;margin-bottom:6px"></div>
              <div class="skel skel-h-sm" style="width:35%;margin-left:auto"></div>
            </div>
          </div>
          <div class="skel skel-h-sm" style="width:30%"></div>
        </div>
        <!-- hotel skel -->
        <div class="skeleton-card">
          <div class="skel" style="height:100px;margin-bottom:12px;border-radius:8px"></div>
          <div class="skel skel-h" style="width:60%;margin-bottom:8px"></div>
          <div style="display:flex;gap:6px;margin-bottom:10px">
            <div class="skel skel-h-sm" style="width:22%"></div>
            <div class="skel skel-h-sm" style="width:22%"></div>
            <div class="skel skel-h-sm" style="width:22%"></div>
          </div>
          <div class="skel skel-h" style="width:35%"></div>
        </div>
      </div>
      <div class="action-area">
        <div class="skel" style="height:48px;border-radius:14px;margin-bottom:8px"></div>
        <div style="display:flex;gap:8px">
          <div class="skel" style="height:42px;flex:1;border-radius:10px"></div>
          <div class="skel" style="height:42px;flex:1;border-radius:10px"></div>
        </div>
      </div>
    </div>

    <!-- ═══════ STATE: PARTIAL (flight loaded, hotel loading) ══════ -->
    <div class="state" id="state-partial">
      <div class="partial-banner">
        <div class="partial-spinner"></div>
        酒店方案加载中，已为你展示机票结果
      </div>
      <div class="section-header">
        <div class="section-title"><span class="icon">✈️</span> 机票方案 <span class="tag-new">已就绪</span></div>
      </div>
      <!-- Outbound -->
      <div class="flight-card">
        <div class="flight-direction-bar">🛫 去程</div>
        <div class="flight-main">
          <div class="flight-time-block">
            <div class="flight-time">07:30</div>
            <div class="flight-airport">SHA 虹桥</div>
          </div>
          <div class="flight-middle">
            <div class="flight-duration">3h 15m</div>
            <div class="flight-path">
              <div class="path-dot"></div>
              <div class="path-line"></div>
              <div class="path-dot"></div>
            </div>
            <div class="flight-type">直飞</div>
          </div>
          <div class="flight-time-block">
            <div class="flight-time">10:45</div>
            <div class="flight-airport">SYX 凤凰</div>
          </div>
        </div>
        <div class="flight-footer">
          <div class="airline-info">
            <div class="airline-logo">东</div>
            <div class="airline-name">东方航空 MU5675 · 经济舱</div>
          </div>
          <div class="flight-price">¥680<span>/人</span></div>
        </div>
      </div>
      <!-- Return -->
      <div class="flight-card">
        <div class="flight-direction-bar">🛬 返程</div>
        <div class="flight-main">
          <div class="flight-time-block">
            <div class="flight-time">15:20</div>
            <div class="flight-airport">SYX 凤凰</div>
          </div>
          <div class="flight-middle">
            <div class="flight-duration">3h 35m</div>
            <div class="flight-path">
              <div class="path-dot"></div>
              <div class="path-line"></div>
              <div class="path-dot"></div>
            </div>
            <div class="flight-type">经停厦门</div>
          </div>
          <div class="flight-time-block">
            <div class="flight-time">18:55</div>
            <div class="flight-airport">PVG 浦东</div>
          </div>
        </div>
        <div class="flight-footer">
          <div class="airline-info">
            <div class="airline-logo" style="background:#1340A8">厦</div>
            <div class="airline-name">厦门航空 MF8013 · 经济舱</div>
          </div>
          <div class="flight-price">¥590<span>/人</span></div>
        </div>
      </div>
      <!-- Hotel loading -->
      <div class="section-header" style="margin-top:6px">
        <div class="section-title"><span class="icon">🏨</span> 酒店方案</div>
      </div>
      <div class="loading-section">
        <div class="loading-icon">🏨</div>
        <div class="partial-spinner" style="margin:0 auto 8px"></div>
        <p>正在为你查找三亚最优酒店…</p>
      </div>
      <div class="action-area">
        <div class="skel" style="height:48px;border-radius:14px;margin-bottom:8px;opacity:.4"></div>
        <p style="text-align:center;font-size:12px;color:var(--text3);margin-top:4px">等待酒店结果后可预订</p>
      </div>
    </div>

    <!-- ═══════ STATE: FULL RESULT ══════════════════════════════════ -->
    <div class="state" id="state-result">
      <!-- Reason -->
      <div class="reason-card">
        <div class="reason-label">✦ 推荐理由</div>
        <div class="reason-text">直飞去程 + 性价比酒店全程，机酒合计最优；三亚湾步行即达海边，单人大床房避免双床房浪费。</div>
      </div>
      <!-- Package total -->
      <div class="package-bar">
        <div>
          <div class="pkg-label">机票 + 酒店 合计</div>
          <div class="pkg-total">¥3,550<sub> 起</sub></div>
          <div class="pkg-per">人均 ¥1,775</div>
        </div>
        <div class="pkg-badge">💰 性价比最优</div>
      </div>
      <!-- Flights -->
      <div class="result-section">
        <div class="section-label">机票方案</div>
        <div class="flight-card" style="opacity:1;transform:none">
          <div class="flight-direction-bar">🛫 去程 · 3月20日</div>
          <div class="flight-main">
            <div class="flight-time-block">
              <div class="flight-time">07:30</div>
              <div class="flight-airport">SHA 虹桥</div>
            </div>
            <div class="flight-middle">
              <div class="flight-duration">3h 15m</div>
              <div class="flight-path">
                <div class="path-dot"></div>
                <div class="path-line"></div>
                <div class="path-dot"></div>
              </div>
              <div class="flight-type">直飞</div>
            </div>
            <div class="flight-time-block">
              <div class="flight-time">10:45</div>
              <div class="flight-airport">SYX 凤凰</div>
            </div>
          </div>
          <div class="flight-footer">
            <div class="airline-info">
              <div class="airline-logo">东</div>
              <div class="airline-name">东方航空 MU5675 · 经济舱</div>
            </div>
            <div class="flight-price">¥680<span>/人</span></div>
          </div>
        </div>
        <div class="flight-card" style="opacity:1;transform:none;margin-top:8px">
          <div class="flight-direction-bar">🛬 返程 · 3月23日</div>
          <div class="flight-main">
            <div class="flight-time-block">
              <div class="flight-time">15:20</div>
              <div class="flight-airport">SYX 凤凰</div>
            </div>
            <div class="flight-middle">
              <div class="flight-duration">3h 35m</div>
              <div class="flight-path">
                <div class="path-dot"></div>
                <div class="path-line"></div>
                <div class="path-dot"></div>
              </div>
              <div class="flight-type">经停厦门</div>
            </div>
            <div class="flight-time-block">
              <div class="flight-time">18:55</div>
              <div class="flight-airport">PVG 浦东</div>
            </div>
          </div>
          <div class="flight-footer">
            <div class="airline-info">
              <div class="airline-logo" style="background:#1340A8">厦</div>
              <div class="airline-name">厦门航空 MF8013 · 经济舱</div>
            </div>
            <div class="flight-price">¥590<span>/人</span></div>
          </div>
        </div>
      </div>
      <!-- Hotel -->
      <div class="result-section">
        <div class="section-label">酒店方案</div>
        <div class="hotel-card">
          <div class="hotel-img">
            <div class="hotel-img-placeholder">🏖️</div>
            <div class="hotel-rating-badge">⭐ 4.6</div>
            <div class="hotel-img-tag">✓ 含双早</div>
          </div>
          <div class="hotel-body">
            <div class="hotel-name">三亚湾海景精品酒店</div>
            <div class="hotel-tags">
              <span class="hotel-tag highlight">距海边 200m</span>
              <span class="hotel-tag highlight">含双早</span>
              <span class="hotel-tag">大床房</span>
              <span class="hotel-tag">免费停车</span>
              <span class="hotel-tag">4.6分</span>
            </div>
            <div class="hotel-price-row">
              <div>
                <div class="hotel-price">¥380<sub>/晚</sub></div>
                <div class="hotel-nights">3月20–23日 共3晚</div>
              </div>
              <div style="text-align:right">
                <div style="font-size:13px;color:var(--text2)">小计</div>
                <div style="font-size:16px;font-weight:800;color:var(--text1)">¥1,140</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="action-area">
        <button class="btn-primary" onclick="goToOrder()">立即预订 · ¥3,550</button>
        <div class="btn-row">
          <button class="btn-secondary" onclick="goReco('hotel')">🔄 换个酒店</button>
          <button class="btn-secondary" onclick="goReco('flight')">✈️ 换个机票</button>
          <button class="btn-secondary warn" onclick="goReco('all')">重新推荐</button>
        </div>
      </div>
    </div>

    <!-- ═══════ STATE: RECO (换一换) ══════════════════════════════ -->
    <div class="state" id="state-reco">
      <div class="reco-header">
        <div class="reco-icon">🔄</div>
        <div>
          <p id="reco-title"><strong>已为你重新推荐酒店</strong>，以下是 2 个新方案（机票保持不变）</p>
        </div>
      </div>

      <div class="section-label" style="padding:0 0 8px">选择你满意的方案</div>

      <div class="option-cards">
        <div class="option-card" id="opt1" onclick="selectOption(1)">
          <div class="option-num">方案 A</div>
          <div class="option-title">三亚湾 XX 海景大酒店</div>
          <div class="option-sub">⭐ 4.7 · 距海边 50m · 含双早 · 大床房<br>步行即达海边，五星设施，度假氛围极佳</div>
          <div class="option-price">¥520/晚 · 小计 ¥1,560</div>
        </div>
        <div class="option-card" id="opt2" onclick="selectOption(2)">
          <div class="option-num">方案 B</div>
          <div class="option-title">海棠湾 XX 精品度假酒店</div>
          <div class="option-sub">⭐ 4.5 · 距海边 300m · 含双早 · 大床房<br>性价比更高，近免税城，购物方便</div>
          <div class="option-price">¥420/晚 · 小计 ¥1,260</div>
        </div>
      </div>

      <div style="padding:0">
        <div class="flight-card" style="opacity:1;transform:none;margin-bottom:12px">
          <div class="flight-direction-bar" style="background:var(--green-light);color:var(--green)">✓ 机票保持不变</div>
          <div class="flight-main">
            <div class="flight-time-block">
              <div class="flight-time" style="font-size:18px">07:30</div>
              <div class="flight-airport">SHA 虹桥</div>
            </div>
            <div class="flight-middle">
              <div class="flight-duration">去 3h15m / 返 3h35m</div>
              <div class="flight-path">
                <div class="path-dot"></div>
                <div class="path-line"></div>
                <div class="path-dot"></div>
              </div>
              <div class="flight-type">MU5675 / MF8013</div>
            </div>
            <div class="flight-time-block">
              <div class="flight-time" style="font-size:18px">10:45</div>
              <div class="flight-airport">SYX 凤凰</div>
            </div>
          </div>
          <div class="flight-footer">
            <span class="text-sm">机票合计</span>
            <div class="flight-price">¥2,540<span> 2人</span></div>
          </div>
        </div>
      </div>

      <div class="action-area">
        <button class="btn-primary" id="reco-confirm" onclick="confirmReco()" disabled style="opacity:.45">
          请先选择一个方案
        </button>
        <div class="btn-row">
          <button class="btn-secondary warn" onclick="giveUp()">放弃，联系定制师</button>
          <button class="btn-secondary" onclick="backToResult()">← 返回上个方案</button>
        </div>
      </div>
    </div>

    <!-- ═══════ STATE: NO RESULT ════════════════════════════════════ -->
    <div class="state" id="state-empty">
      <div class="empty-icon">🔍</div>
      <div class="empty-title">未找到3月13日的机酒资源</div>
      <div class="empty-sub">成都 → 拉萨 该日期暂无可用舱位，<br>为你推荐相近日期的替代方案</div>
      <div class="alt-cards">
        <div class="alt-card" onclick="showToast('已为你加载3月15日方案')">
          <div class="alt-left">
            <div class="alt-date">3月15日（后天）出发</div>
            <div class="alt-route">成都 → 拉萨 · 往返4天</div>
          </div>
          <div class="alt-price">¥5,480<span style="font-size:11px;color:var(--text3)"> 起</span></div>
        </div>
        <div class="alt-card" onclick="showToast('已为你加载3月16日方案')">
          <div class="alt-left">
            <div class="alt-date">3月16日（大后天）出发</div>
            <div class="alt-route">成都 → 拉萨 · 往返4天</div>
          </div>
          <div class="alt-price">¥4,880<span style="font-size:11px;color:var(--text3)"> 起</span></div>
        </div>
      </div>
      <button class="btn-outline" onclick="showToast('已为你重新搜索')">📅 选择其他出发日期</button>
      <button class="btn-outline" onclick="showToast('正在连接定制师…')">👨‍💼 联系专属定制师</button>
    </div>

    <!-- ═══════ STATE: ORDER ═════════════════════════════════════════ -->
    <div class="state" id="state-order">
      <div class="order-header">
        <div class="order-checkmark">✓</div>
        <h2>方案确认</h2>
        <p>请核对以下行程信息，确认无误后提交</p>
      </div>
      <div class="order-body">
        <div class="order-row">
          <div class="order-key">出发城市</div>
          <div class="order-val">上海</div>
        </div>
        <div class="order-row">
          <div class="order-key">目的地</div>
          <div class="order-val">三亚</div>
        </div>
        <div class="order-row">
          <div class="order-key">去程航班</div>
          <div class="order-val">MU5675 · 3月20日 07:30</div>
        </div>
        <div class="order-row">
          <div class="order-key">返程航班</div>
          <div class="order-val">MF8013 · 3月23日 15:20</div>
        </div>
        <div class="order-row">
          <div class="order-key">酒店</div>
          <div class="order-val">三亚湾海景精品酒店<br><span class="text-sm">3月20–23日 · 3晚 · 大床房</span></div>
        </div>
        <div class="order-row">
          <div class="order-key">出行人数</div>
          <div class="order-val">成人 × 2</div>
        </div>
        <div class="order-row order-total">
          <div class="order-key">合计总价</div>
          <div class="order-val">¥3,550</div>
        </div>
      </div>
      <div class="action-area">
        <button class="btn-primary" onclick="submitOrder()">确认，填写乘客信息 →</button>
        <div class="btn-row">
          <button class="btn-secondary warn" onclick="backToResult()">← 修改方案</button>
        </div>
      </div>
    </div>

  </div><!-- /.states -->
</div><!-- /.app-wrap -->

<div class="toast" id="toast"></div>

<script>
// ─── State machine ────────────────────────────────────────────────────────
let currentState = 'skeleton';
let recoCount = 0;
let selectedOption = null;

const states = ['skeleton','partial','result','reco','empty','order'];

function showState(name, slideIn = true) {
  states.forEach(s => {
    const el = document.getElementById('state-' + s);
    el.classList.remove('active', 'slide-in');
  });
  const el = document.getElementById('state-' + name);
  el.classList.add('active');
  if (slideIn) el.classList.add('slide-in');
  currentState = name;
  updateHeader(name);
  updateProgress(name);
  // Scroll to top
  el.scrollIntoView({ behavior: 'smooth', block: 'start' });
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function updateHeader(state) {
  const titles = {
    skeleton: '为你匹配方案',
    partial:  '机票已就绪 · 酒店加载中',
    result:   '推荐方案',
    reco:     '重新推荐',
    empty:    '暂无结果',
    order:    '确认订单',
  };
  document.getElementById('header-title').textContent = titles[state] || '';
}

function updateProgress(state) {
  const stepMap = { skeleton:2, partial:2, result:2, reco:2, empty:2, order:3 };
  const active = stepMap[state] || 2;
  for (let i = 1; i <= 4; i++) {
    const dot = document.getElementById('step' + i);
    const lbl = document.getElementById('steplabel' + i);
    dot.classList.remove('active','done');
    if (lbl) lbl.classList.remove('active');
    if (i < active) { dot.classList.add('done'); dot.textContent = '✓'; }
    else if (i === active) {
      dot.classList.add('active');
      dot.textContent = i;
      if (lbl) lbl.classList.add('active');
    } else { dot.textContent = i; }
  }
  for (let i = 1; i <= 3; i++) {
    const conn = document.getElementById('conn' + i);
    if (conn) {
      conn.classList.toggle('done', i < active);
    }
  }
}

// ─── Demo flow ─────────────────────────────────────────────────────────────
function startDemo() {
  showState('skeleton', false);
  // After 1.8s → partial (flight loaded)
  setTimeout(() => showState('partial'), 1800);
  // After 3.4s → full result
  setTimeout(() => showState('result'), 3400);
}

function goToOrder() {
  showState('order');
}

function goReco(type) {
  recoCount++;
  selectedOption = null;
  const confirmBtn = document.getElementById('reco-confirm');
  confirmBtn.disabled = true;
  confirmBtn.style.opacity = '.45';
  confirmBtn.textContent = '请先选择一个方案';
  // reset selection
  document.getElementById('opt1').classList.remove('selected');
  document.getElementById('opt2').classList.remove('selected');

  const titles = {
    hotel: '<strong>已为你重新推荐酒店</strong>，以下是 2 个新方案（机票保持不变）',
    flight: '<strong>已为你重新推荐机票</strong>，以下是 2 个新方案（酒店保持不变）',
    all:  '<strong>已为你全量重新推荐</strong>，以下是全新机酒组合方案',
  };
  document.getElementById('reco-title').innerHTML = titles[type] || titles.all;

  if (recoCount > 2) {
    showToast('已达推荐上限，为你转接定制师');
    setTimeout(() => {
      showToast('定制师接入中…');
    }, 1500);
    return;
  }
  showState('reco');
}

function selectOption(num) {
  selectedOption = num;
  document.getElementById('opt1').classList.toggle('selected', num === 1);
  document.getElementById('opt2').classList.toggle('selected', num === 2);
  const confirmBtn = document.getElementById('reco-confirm');
  confirmBtn.disabled = false;
  confirmBtn.style.opacity = '1';
  const prices = { 1: '¥4,100', 2: '¥3,800' };
  confirmBtn.textContent = `确认选择方案 ${num === 1 ? 'A' : 'B'} · ${prices[num]}`;
}

function confirmReco() {
  if (!selectedOption) return;
  showToast('方案已更新 ✓');
  setTimeout(() => showState('result'), 600);
}

function backToResult() {
  showState('result');
}

function giveUp() {
  showToast('正在为你连接专属定制师…');
}

function submitOrder() {
  showToast('订单已提交，正在占座…');
  updateProgress('submit');
  // Simulate success
  setTimeout(() => showToast('✅ 出票成功！订单已生成'), 2000);
}

function goBack() {
  const backMap = { result:'skeleton', reco:'result', order:'result', empty:'skeleton', partial:'skeleton' };
  const target = backMap[currentState];
  if (target) showState(target);
}

// ─── Toast ────────────────────────────────────────────────────────────────
let toastTimer;
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => t.classList.remove('show'), 2500);
}

// ─── Demo buttons ─────────────────────────────────────────────────────────
// Add demo nav bar
const demoBar = document.createElement('div');
demoBar.style.cssText = `
  position: fixed; bottom: 0; left: 50%; transform: translateX(-50%);
  width: 420px; background: rgba(15,23,42,.92); backdrop-filter:blur(12px);
  padding: 10px 16px; display:flex; gap:6px; flex-wrap:wrap;
  z-index: 1000; border-top: 1px solid rgba(255,255,255,.1);
`;
const demos = [
  ['🦴 骨架屏', () => showState('skeleton',false)],
  ['✈️ 机票先到', () => showState('partial')],
  ['🎯 完整方案', () => showState('result')],
  ['🔄 重新推荐', () => goReco('hotel')],
  ['😶 无结果', () => showState('empty')],
  ['📋 确认订单', () => showState('order')],
];
demos.forEach(([label, fn]) => {
  const btn = document.createElement('button');
  btn.textContent = label;
  btn.style.cssText = `
    flex:1; min-width:80px; padding:7px 4px;
    background:rgba(255,255,255,.1); border:1px solid rgba(255,255,255,.15);
    color:#fff; border-radius:8px; font-size:11px; cursor:pointer;
    font-family:var(--font); transition:background .2s;
  `;
  btn.addEventListener('mouseenter', () => btn.style.background = 'rgba(255,255,255,.2)');
  btn.addEventListener('mouseleave', () => btn.style.background = 'rgba(255,255,255,.1)');
  btn.addEventListener('click', fn);
  demoBar.appendChild(btn);
});
document.body.appendChild(demoBar);

// ─── Boot ─────────────────────────────────────────────────────────────────
startDemo();
</script>
</body>
</html>
