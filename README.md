<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Food Vision AI — README</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&family=Lato:wght@300;400;700&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #ffffff;
  --surface: #f8fafc;
  --surface2: #f1f5f9;
  --surface3: #e2e8f0;
  --border: #e2e8f0;
  --border2: #cbd5e1;
  --blue: #2563eb;
  --indigo: #4f46e5;
  --cyan: #0891b2;
  --green: #16a34a;
  --orange: #ea580c;
  --red: #dc2626;
  --yellow: #d97706;
  --purple: #7c3aed;
  --text: #0f172a;
  --text2: #334155;
  --muted: #64748b;
  --light: #94a3b8;
}
*{margin:0;padding:0;box-sizing:border-box;}
body{background:var(--bg);color:var(--text);font-family:'Lato',sans-serif;line-height:1.75;font-size:15px;}

/* ─── TOPBAR ─── */
.topbar{background:var(--blue);color:#fff;padding:10px 40px;display:flex;align-items:center;gap:16px;font-family:'Space Mono',monospace;font-size:12px;letter-spacing:.06em;}
.topbar-dot{width:8px;height:8px;border-radius:50%;background:#60a5fa;}

/* ─── HERO ─── */
.hero{background:linear-gradient(135deg,#1e3a8a 0%,#1d4ed8 40%,#2563eb 70%,#0891b2 100%);color:#fff;padding:72px 40px 60px;text-align:center;position:relative;overflow:hidden;}
.hero::before{content:'';position:absolute;inset:0;background:url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.04'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");}
.hero-emoji{font-size:72px;display:block;margin-bottom:20px;filter:drop-shadow(0 4px 24px rgba(0,0,0,0.3));animation:float 3s ease-in-out infinite;}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-10px)}}
h1{font-family:'Syne',sans-serif;font-size:clamp(40px,7vw,76px);font-weight:800;line-height:1;margin-bottom:12px;text-shadow:0 2px 20px rgba(0,0,0,0.2);}
.hero-tagline{font-family:'Space Mono',monospace;font-size:12px;letter-spacing:.18em;text-transform:uppercase;color:#bfdbfe;margin-bottom:20px;}
.hero-desc{max-width:640px;margin:0 auto 32px;font-size:17px;color:#dbeafe;line-height:1.85;}
.badge-row{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-bottom:32px;}
.badge{display:inline-flex;align-items:center;gap:6px;padding:5px 14px;border-radius:20px;font-family:'Space Mono',monospace;font-size:10px;font-weight:700;letter-spacing:.05em;text-transform:uppercase;border:1.5px solid;backdrop-filter:blur(10px);}
.b-white{border-color:rgba(255,255,255,.5);color:#fff;background:rgba(255,255,255,.12);}
.b-yellow{border-color:#fde68a;color:#fde68a;background:rgba(253,230,138,.1);}
.b-green{border-color:#6ee7b7;color:#6ee7b7;background:rgba(110,231,183,.1);}
.b-pink{border-color:#f9a8d4;color:#f9a8d4;background:rgba(249,168,212,.1);}
.cta-row{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;}
.btn{display:inline-flex;align-items:center;gap:8px;padding:13px 26px;border-radius:8px;font-family:'Syne',sans-serif;font-weight:700;font-size:14px;text-decoration:none;cursor:pointer;border:2px solid;transition:all .2s;}
.btn-white{background:#fff;color:var(--blue);border-color:#fff;}
.btn-white:hover{background:#dbeafe;transform:translateY(-2px);box-shadow:0 8px 24px rgba(0,0,0,.2);}
.btn-outline{background:transparent;color:#fff;border-color:rgba(255,255,255,.5);}
.btn-outline:hover{background:rgba(255,255,255,.1);border-color:#fff;transform:translateY(-2px);}

/* ─── LAYOUT ─── */
.container{max-width:960px;margin:0 auto;padding:0 32px;}

/* ─── SECTIONS ─── */
section{padding:60px 0;border-bottom:1px solid var(--border);}
.section-eyebrow{display:flex;align-items:center;gap:10px;font-family:'Space Mono',monospace;font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:.18em;color:var(--blue);margin-bottom:10px;}
.section-eyebrow::before{content:'';display:block;width:20px;height:2px;background:var(--blue);}
h2{font-family:'Syne',sans-serif;font-size:clamp(24px,4vw,34px);font-weight:800;color:var(--text);margin-bottom:14px;}
h3{font-family:'Syne',sans-serif;font-size:17px;font-weight:700;color:var(--text);margin-bottom:8px;}
h4{font-family:'Syne',sans-serif;font-size:15px;font-weight:700;color:var(--text2);margin-bottom:6px;}
p{color:var(--text2);margin-bottom:12px;}
ul{color:var(--text2);padding-left:20px;}
ul li{margin-bottom:6px;}

/* ─── STATS ─── */
.stats-bar{display:grid;grid-template-columns:repeat(4,1fr);border:1.5px solid var(--border);border-radius:14px;overflow:hidden;background:#fff;box-shadow:0 2px 16px rgba(0,0,0,.06);}
.stat-item{padding:28px 16px;text-align:center;border-right:1px solid var(--border);}
.stat-item:last-child{border-right:none;}
.stat-num{font-family:'Syne',sans-serif;font-size:38px;font-weight:800;color:var(--blue);}
.stat-label{font-size:12px;color:var(--muted);font-family:'Space Mono',monospace;text-transform:uppercase;letter-spacing:.08em;margin-top:4px;}

/* ─── FEATURE GRID ─── */
.feature-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:16px;}
.feature-card{background:#fff;border:1.5px solid var(--border);border-radius:12px;padding:24px;transition:all .2s;position:relative;overflow:hidden;}
.feature-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--blue),var(--cyan));transform:scaleX(0);transition:.3s;transform-origin:left;}
.feature-card:hover{border-color:var(--blue);box-shadow:0 8px 30px rgba(37,99,235,.1);transform:translateY(-3px);}
.feature-card:hover::before{transform:scaleX(1);}
.feature-icon{font-size:28px;margin-bottom:12px;display:block;}
.feature-card p{font-size:13px;margin:0;color:var(--muted);}

/* ─── MODEL CARDS ─── */
.model-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;}
.model-card{background:#fff;border:2px solid var(--border);border-radius:16px;padding:28px 20px;text-align:center;transition:all .3s;position:relative;}
.model-card.custom:hover{border-color:var(--blue);box-shadow:0 12px 40px rgba(37,99,235,.15);}
.model-card.vgg:hover{border-color:var(--purple);box-shadow:0 12px 40px rgba(124,58,237,.15);}
.model-card.resnet:hover{border-color:var(--orange);box-shadow:0 12px 40px rgba(234,88,12,.15);}
.model-card:hover{transform:translateY(-4px);}
.model-icon{width:64px;height:64px;border-radius:16px;margin:0 auto 16px;display:flex;align-items:center;justify-content:center;font-size:28px;border:2px solid;}
.model-card.custom .model-icon{border-color:var(--blue);background:#eff6ff;color:var(--blue);}
.model-card.vgg .model-icon{border-color:var(--purple);background:#f5f3ff;color:var(--purple);}
.model-card.resnet .model-icon{border-color:var(--orange);background:#fff7ed;color:var(--orange);}
.model-card.custom h3{color:var(--blue);}
.model-card.vgg h3{color:var(--purple);}
.model-card.resnet h3{color:var(--orange);}
.model-card p{font-size:13px;color:var(--muted);margin:0 0 14px;}
.model-tag{display:inline-block;padding:4px 10px;border-radius:4px;font-size:11px;font-family:'Space Mono',monospace;border:1.5px solid;}
.model-card.custom .model-tag{border-color:var(--blue);color:var(--blue);background:#eff6ff;}
.model-card.vgg .model-tag{border-color:var(--purple);color:var(--purple);background:#f5f3ff;}
.model-card.resnet .model-tag{border-color:var(--orange);color:var(--orange);background:#fff7ed;}
.model-specs{margin-top:14px;text-align:left;}
.model-spec{display:flex;justify-content:space-between;align-items:center;padding:6px 0;border-bottom:1px solid var(--border);font-size:12px;}
.model-spec:last-child{border-bottom:none;}
.model-spec-key{color:var(--muted);}
.model-spec-val{font-family:'Space Mono',monospace;color:var(--text);font-size:11px;}

/* ─── PREDICTION SHOWCASE ─── */
.prediction-showcase{background:#fff;border:2px solid var(--border);border-radius:20px;overflow:hidden;box-shadow:0 4px 30px rgba(0,0,0,.08);}
.ps-header{padding:16px 24px;border-bottom:1px solid var(--border);display:flex;align-items:center;gap:10px;background:linear-gradient(90deg,#eff6ff,#f0f9ff);}
.ps-dot{width:8px;height:8px;border-radius:50%;background:var(--blue);}
.ps-title{font-family:'Space Mono',monospace;font-size:10px;color:var(--blue);text-transform:uppercase;letter-spacing:.14em;font-weight:700;}
.ps-body{padding:28px 24px;}
.ps-food-name{font-family:'Syne',sans-serif;font-size:38px;font-weight:800;color:var(--text);margin-bottom:6px;}
.ps-model-badge{display:inline-flex;align-items:center;gap:6px;padding:4px 12px;border-radius:6px;font-family:'Space Mono',monospace;font-size:10px;font-weight:700;background:#eff6ff;border:1.5px solid var(--blue);color:var(--blue);margin-bottom:22px;}
.confidence-bar-wrap{margin-bottom:28px;}
.confidence-label{display:flex;justify-content:space-between;margin-bottom:8px;font-size:13px;color:var(--muted);}
.confidence-label span:last-child{color:var(--blue);font-weight:700;font-family:'Space Mono',monospace;}
.confidence-bar{height:10px;background:var(--surface2);border-radius:5px;overflow:hidden;border:1px solid var(--border);}
.confidence-fill{height:100%;border-radius:5px;background:linear-gradient(90deg,var(--blue),var(--cyan));}
.metrics-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin-bottom:24px;}
.metric-card{background:var(--surface);border-radius:12px;padding:20px 12px;text-align:center;border-top:4px solid;}
.metric-card.m1{border-color:var(--blue);}
.metric-card.m2{border-color:var(--purple);}
.metric-card.m3{border-color:var(--yellow);}
.metric-card.m4{border-color:var(--green);}
.metric-val{font-family:'Syne',sans-serif;font-size:28px;font-weight:800;margin-bottom:4px;}
.m1 .metric-val{color:var(--blue);}
.m2 .metric-val{color:var(--purple);}
.m3 .metric-val{color:var(--yellow);}
.m4 .metric-val{color:var(--green);}
.metric-label{font-family:'Space Mono',monospace;font-size:10px;color:var(--muted);text-transform:uppercase;letter-spacing:.1em;}
.metric-icon{font-size:20px;margin-bottom:8px;}
.top5-label{font-family:'Space Mono',monospace;font-size:10px;color:var(--blue);text-transform:uppercase;letter-spacing:.14em;margin-bottom:12px;display:flex;align-items:center;gap:8px;font-weight:700;}
.top5-label::before{content:'';display:block;width:14px;height:2px;background:var(--blue);}
.top5-item{display:flex;align-items:center;gap:12px;padding:10px 0;border-bottom:1px solid var(--border);}
.top5-item:last-child{border-bottom:none;}
.top5-rank{font-family:'Space Mono',monospace;font-size:11px;color:var(--muted);width:24px;flex-shrink:0;}
.top5-rank.r1{color:var(--blue);font-weight:700;}
.top5-food{flex:1;font-size:14px;display:flex;align-items:center;gap:8px;color:var(--text2);}
.top5-bar-wrap{width:120px;}
.top5-bar{height:6px;background:var(--surface2);border-radius:3px;overflow:hidden;}
.top5-bar-fill{height:100%;background:linear-gradient(90deg,var(--blue),var(--cyan));border-radius:3px;}
.top5-pct{font-family:'Space Mono',monospace;font-size:11px;color:var(--blue);width:36px;text-align:right;flex-shrink:0;font-weight:700;}

/* ─── FORMULA BOX ─── */
.formula-section{background:#fff;border:2px solid var(--border);border-radius:16px;overflow:hidden;margin:20px 0;}
.formula-header{background:linear-gradient(90deg,var(--blue),var(--indigo));color:#fff;padding:14px 24px;font-family:'Syne',sans-serif;font-weight:700;font-size:15px;display:flex;align-items:center;gap:10px;}
.formula-body{padding:24px;}
.formula-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;}
.formula-card{background:var(--surface);border:1.5px solid var(--border);border-radius:12px;padding:20px;}
.formula-card h4{color:var(--blue);margin-bottom:10px;font-size:14px;}
.formula-eq{background:#1e293b;color:#e2e8f0;padding:14px 16px;border-radius:8px;font-family:'Space Mono',monospace;font-size:13px;line-height:1.6;margin:10px 0;overflow-x:auto;}
.formula-eq .frac{display:inline-flex;flex-direction:column;align-items:center;vertical-align:middle;margin:0 4px;}
.formula-eq .num{border-bottom:1px solid #94a3b8;padding:0 2px;line-height:1.4;}
.formula-eq .den{padding:0 2px;line-height:1.4;}
.formula-eq .kw{color:#7dd3fc;}
.formula-eq .val{color:#6ee7b7;}
.formula-eq .op{color:#f9a8d4;}
.formula-example{background:#f0fdf4;border:1px solid #bbf7d0;border-radius:8px;padding:12px 14px;margin-top:10px;}
.formula-example-label{font-family:'Space Mono',monospace;font-size:10px;color:var(--green);text-transform:uppercase;letter-spacing:.1em;font-weight:700;margin-bottom:6px;}
.formula-example p{font-size:13px;color:#166534;margin:0;}

/* ─── ARCHITECTURE DEEP DIVE ─── */
.arch-block{background:#fff;border:2px solid var(--border);border-radius:16px;overflow:hidden;margin:20px 0;}
.arch-header{padding:16px 24px;display:flex;align-items:center;gap:12px;border-bottom:1px solid var(--border);}
.arch-icon{width:40px;height:40px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;}
.arch-body{padding:24px;}
.layer-list{display:flex;flex-direction:column;gap:8px;margin:14px 0;}
.layer-item{display:flex;align-items:flex-start;gap:12px;padding:12px 14px;background:var(--surface);border-radius:8px;border-left:3px solid;}
.layer-item.conv{border-color:var(--blue);}
.layer-item.pool{border-color:var(--cyan);}
.layer-item.bn{border-color:var(--green);}
.layer-item.fc{border-color:var(--orange);}
.layer-item.drop{border-color:var(--yellow);}
.layer-item.res{border-color:var(--purple);}
.layer-item.out{border-color:var(--red);}
.layer-num{font-family:'Space Mono',monospace;font-size:10px;color:var(--muted);width:20px;flex-shrink:0;padding-top:2px;}
.layer-name{font-family:'Syne',sans-serif;font-weight:700;font-size:13px;margin-bottom:3px;}
.layer-desc{font-size:12px;color:var(--muted);}
.layer-params{margin-left:auto;font-family:'Space Mono',monospace;font-size:11px;color:var(--blue);flex-shrink:0;white-space:nowrap;}

/* ─── INFO TABLE ─── */
.info-table{width:100%;border-collapse:collapse;margin:14px 0;font-size:13px;}
.info-table th{background:var(--blue);color:#fff;padding:10px 14px;text-align:left;font-family:'Syne',sans-serif;font-weight:700;font-size:12px;}
.info-table td{padding:10px 14px;border-bottom:1px solid var(--border);color:var(--text2);}
.info-table tr:nth-child(even) td{background:var(--surface);}
.info-table td:first-child{font-family:'Space Mono',monospace;font-size:11px;color:var(--text);font-weight:700;}

/* ─── CODE BLOCK ─── */
.code-block{background:#1e293b;border-radius:12px;overflow:hidden;margin:14px 0;border:1.5px solid #334155;}
.code-header{display:flex;align-items:center;justify-content:space-between;padding:10px 16px;background:#0f172a;border-bottom:1px solid #334155;}
.code-dots{display:flex;gap:6px;}
.cd1{width:10px;height:10px;border-radius:50%;background:#f43f5e;}
.cd2{width:10px;height:10px;border-radius:50%;background:#fbbf24;}
.cd3{width:10px;height:10px;border-radius:50%;background:#22c55e;}
.code-lang{font-family:'Space Mono',monospace;font-size:10px;color:#64748b;text-transform:uppercase;letter-spacing:.1em;}
.code-body{padding:18px;font-family:'Space Mono',monospace;font-size:13px;line-height:1.85;overflow-x:auto;color:#e2e8f0;}
.cc{color:#64748b;}
.ck{color:#7dd3fc;}
.cs{color:#fca5a5;}
.cf{color:#86efac;}
.cn{color:#fde68a;}
.cv{color:#c4b5fd;}

/* ─── NUTRITION ─── */
.nutrition-strip{display:grid;grid-template-columns:repeat(5,1fr);gap:12px;margin:20px 0;}
.nut-card{background:#fff;border:2px solid var(--border);border-radius:14px;padding:22px 12px;text-align:center;transition:.2s;}
.nut-card:hover{transform:translateY(-3px);box-shadow:0 8px 24px rgba(0,0,0,.08);}
.nut-icon{font-size:26px;margin-bottom:8px;}
.nut-val{font-family:'Syne',sans-serif;font-size:26px;font-weight:800;margin-bottom:4px;}
.nut-label{font-size:10px;font-family:'Space Mono',monospace;color:var(--muted);text-transform:uppercase;letter-spacing:.08em;}
.nut-card.calories{border-color:var(--orange);}.nut-card.calories .nut-val{color:var(--orange);}
.nut-card.protein{border-color:var(--green);}.nut-card.protein .nut-val{color:var(--green);}
.nut-card.carbs{border-color:var(--blue);}.nut-card.carbs .nut-val{color:var(--blue);}
.nut-card.fats{border-color:var(--red);}.nut-card.fats .nut-val{color:var(--red);}
.nut-card.fiber{border-color:var(--yellow);}.nut-card.fiber .nut-val{color:var(--yellow);}

/* ─── FLOW ─── */
.flow-diagram{display:flex;align-items:center;overflow-x:auto;padding:24px 0;gap:0;}
.flow-step{flex:1;min-width:110px;text-align:center;}
.flow-icon{width:58px;height:58px;border-radius:16px;margin:0 auto 10px;display:flex;align-items:center;justify-content:center;font-size:24px;border:2px solid var(--blue);background:#eff6ff;}
.flow-label{font-size:12px;font-family:'Space Mono',monospace;color:var(--muted);}
.flow-arrow{font-size:22px;color:var(--blue);flex-shrink:0;padding:0 4px;margin-bottom:28px;opacity:.7;}

/* ─── TECH STACK ─── */
.tech-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:16px;}
.tech-group{background:#fff;border:1.5px solid var(--border);border-radius:12px;padding:20px;}
.tech-group-title{font-family:'Space Mono',monospace;font-size:10px;text-transform:uppercase;letter-spacing:.14em;margin-bottom:14px;padding-bottom:10px;border-bottom:1px solid var(--border);font-weight:700;}
.tech-group.frontend .tech-group-title{color:var(--blue);}
.tech-group.backend .tech-group-title{color:var(--purple);}
.tech-group.dl .tech-group-title{color:var(--orange);}
.tech-group.db .tech-group-title{color:var(--green);}
.tech-item{display:flex;align-items:center;gap:10px;padding:8px 0;border-bottom:1px solid var(--surface2);font-size:13px;color:var(--text2);}
.tech-item:last-child{border-bottom:none;}
.tech-item-icon{font-size:18px;width:28px;text-align:center;}

/* ─── INSTALL STEPS ─── */
.install-steps{display:flex;flex-direction:column;gap:18px;}
.install-step{display:flex;gap:20px;align-items:flex-start;}
.step-num{width:36px;height:36px;border-radius:50%;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-family:'Syne',sans-serif;font-weight:800;font-size:14px;border:2px solid var(--blue);color:var(--blue);background:#eff6ff;}
.step-content h3{margin-bottom:6px;font-size:16px;}
.step-content p{font-size:13px;margin-bottom:8px;}

/* ─── ROADMAP ─── */
.roadmap-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;}
.roadmap-item{display:flex;align-items:flex-start;gap:12px;background:#fff;border:1.5px solid var(--border);border-radius:10px;padding:16px;}
.roadmap-icon{font-size:22px;flex-shrink:0;}
.roadmap-item h3{font-size:14px;margin-bottom:4px;}
.roadmap-item p{font-size:12px;margin:0;color:var(--muted);}

/* ─── DEV ─── */
.dev-card{background:linear-gradient(135deg,#eff6ff,#f5f3ff);border:2px solid var(--border);border-radius:20px;padding:36px 32px;display:flex;align-items:center;gap:32px;}
.dev-avatar{width:90px;height:90px;border-radius:50%;flex-shrink:0;border:3px solid var(--blue);background:#dbeafe;display:flex;align-items:center;justify-content:center;font-size:36px;}
.dev-name{font-family:'Syne',sans-serif;font-size:26px;font-weight:800;color:var(--text);margin-bottom:4px;}
.dev-role{font-family:'Space Mono',monospace;font-size:11px;color:var(--blue);text-transform:uppercase;letter-spacing:.12em;margin-bottom:14px;}
.dev-tags{display:flex;gap:8px;flex-wrap:wrap;}
.dev-tag{padding:4px 10px;border-radius:4px;font-size:12px;font-family:'Space Mono',monospace;background:#fff;border:1.5px solid var(--border);color:var(--text2);}

/* ─── CALLOUT ─── */
.callout{padding:16px 20px;border-radius:10px;border-left:4px solid;margin:16px 0;font-size:13px;}
.callout-blue{background:#eff6ff;border-color:var(--blue);color:#1e40af;}
.callout-green{background:#f0fdf4;border-color:var(--green);color:#166534;}
.callout-orange{background:#fff7ed;border-color:var(--orange);color:#9a3412;}
.callout-label{font-family:'Syne',sans-serif;font-weight:700;font-size:13px;margin-bottom:4px;}

/* ─── FOOTER ─── */
.footer{background:var(--text);color:#94a3b8;padding:40px;text-align:center;font-family:'Space Mono',monospace;font-size:12px;letter-spacing:.08em;}
.footer span{color:#60a5fa;}

@media(max-width:700px){
  .stats-bar,.feature-grid,.model-grid,.tech-grid,.roadmap-grid,.formula-grid{grid-template-columns:1fr;}
  .metrics-grid{grid-template-columns:repeat(2,1fr);}
  .nutrition-strip{grid-template-columns:repeat(2,1fr);}
  .dev-card{flex-direction:column;text-align:center;}
  h1{font-size:38px;}
}
</style>
</head>
<body>

<!-- TOPBAR -->
<div class="topbar">
  <div class="topbar-dot"></div>
  Food Vision AI &nbsp;·&nbsp; Deep Learning Food Classification &nbsp;·&nbsp; CNN Architectures
</div>

<!-- HERO -->
<div class="hero">
  <div class="badge-row">
    <span class="badge b-white">🧠 Deep Learning</span>
    <span class="badge b-yellow">👁 Computer Vision</span>
    <span class="badge b-green">🚀 Flask + Redis</span>
    <span class="badge b-pink">📊 TensorFlow · Keras</span>
  </div>
  <span class="hero-emoji">🍱</span>
  <h1>Food Vision AI</h1>
  <p class="hero-desc">A Deep Learning–powered food classification and nutrition analysis system. Upload a food image, choose a CNN architecture, and get real-time predictions with confidence scores, inference metrics, and full nutrition data.</p>
  <div class="cta-row">
    <a href="https://github.com/your-username/food-vision-ai" class="btn btn-white">⭐ Star on GitHub</a>
    <a href="#install" class="btn btn-outline">📦 Installation Guide</a>
    <a href="https://drive.google.com/file/d/12eCgqD2To5Kq2XRIDGBb3OsNbA-MkWSd/view" class="btn btn-outline">📥 ResNet-50 Model</a>
  </div>
</div>

<div class="container">

<!-- ── STATS ── -->
<section>
  <div class="stats-bar">
    <div class="stat-item"><div class="stat-num">34</div><div class="stat-label">Food Classes</div></div>
    <div class="stat-item"><div class="stat-num">3</div><div class="stat-label">CNN Models</div></div>
    <div class="stat-item"><div class="stat-num">256²</div><div class="stat-label">CNN Input Size</div></div>
    <div class="stat-item"><div class="stat-num">⚡</div><div class="stat-label">Real-time Inference</div></div>
  </div>

  <!-- FEATURES -->
  <div class="section-eyebrow">Features</div>
  <h2>What Food Vision AI Does</h2>
  <p>A complete end-to-end pipeline — from image upload to nutrition output — powered by three interchangeable CNN architectures.</p>
  <div class="feature-grid">
    <div class="feature-card"><span class="feature-icon">🔭</span><h3>Real-time Prediction</h3><p>Upload any food image; the selected CNN model instantly classifies it and returns ranked predictions with confidence scores.</p></div>
    <div class="feature-card"><span class="feature-icon">📊</span><h3>Inference Metrics</h3><p>Every prediction exposes Accuracy, Precision, Recall, and F1-Score — so you can evaluate model quality per inference.</p></div>
    <div class="feature-card"><span class="feature-icon">🥗</span><h3>Nutrition Dashboard</h3><p>Redis-backed instant retrieval of Calories, Protein, Carbs, Fats, and Fiber per 100g for every predicted food class.</p></div>
    <div class="feature-card"><span class="feature-icon">🔄</span><h3>Multi-model Selection</h3><p>Switch on the fly between Custom CNN (256×256), VGG-16 (224×224), and ResNet-50 (224×224) without reloading.</p></div>
    <div class="feature-card"><span class="feature-icon">🏆</span><h3>Top-5 Rankings</h3><p>See the top-5 candidate food classes ranked by prediction probability alongside a visual bar chart.</p></div>
    <div class="feature-card"><span class="feature-icon">🎨</span><h3>Modern Responsive UI</h3><p>Dark-accented dashboard with animated confidence bars, metric cards, nutrition tiles, and a class filter panel.</p></div>
  </div>
</section>

<!-- ── PREDICTION RESULT ── -->
<section>
  <div class="section-eyebrow">Model Prediction Results</div>
  <h2>Live Prediction Interface</h2>
  <p>After uploading a food image and selecting a model, the dashboard renders a full prediction result card with all inference metrics, animated confidence visualization, and a top-5 ranking.</p>

  <div class="prediction-showcase">
    <div class="ps-header">
      <div class="ps-dot"></div>
      <div class="ps-title">Prediction Result — Custom CNN</div>
    </div>
    <div class="ps-body">
      <div class="ps-food-name">🌯 Kaathi Rolls</div>
      <div class="ps-model-badge">⚙ Custom CNN &nbsp;·&nbsp; 256 × 256 input</div>

      <div class="confidence-bar-wrap">
        <div class="confidence-label"><span>Confidence Score</span><span>3.0%</span></div>
        <div class="confidence-bar"><div class="confidence-fill" style="width:3%"></div></div>
      </div>

      <div class="top5-label">Inference Metrics</div>
      <div class="metrics-grid">
        <div class="metric-card m1"><div class="metric-icon">🎯</div><div class="metric-val">3.0%</div><div class="metric-label">Accuracy</div></div>
        <div class="metric-card m2"><div class="metric-icon">🔍</div><div class="metric-val">5.4%</div><div class="metric-label">Precision</div></div>
        <div class="metric-card m3"><div class="metric-icon">♻️</div><div class="metric-val">50.9%</div><div class="metric-label">Recall</div></div>
        <div class="metric-card m4"><div class="metric-icon">📈</div><div class="metric-val">9.7%</div><div class="metric-label">F1-Score</div></div>
      </div>

      <div class="top5-label">Top 5 Predictions</div>
      <div class="top5-item"><div class="top5-rank r1">#1</div><div class="top5-food">🌯 kaathi rolls</div><div class="top5-bar-wrap"><div class="top5-bar"><div class="top5-bar-fill" style="width:100%"></div></div></div><div class="top5-pct">3.0%</div></div>
      <div class="top5-item"><div class="top5-rank">#2</div><div class="top5-food">🍚 fried rice</div><div class="top5-bar-wrap"><div class="top5-bar"><div class="top5-bar-fill" style="width:90%"></div></div></div><div class="top5-pct">3.0%</div></div>
      <div class="top5-item"><div class="top5-rank">#3</div><div class="top5-food">🍰 cheesecake</div><div class="top5-bar-wrap"><div class="top5-bar"><div class="top5-bar-fill" style="width:80%"></div></div></div><div class="top5-pct">3.0%</div></div>
      <div class="top5-item"><div class="top5-rank">#4</div><div class="top5-food">🍛 chicken curry</div><div class="top5-bar-wrap"><div class="top5-bar"><div class="top5-bar-fill" style="width:70%"></div></div></div><div class="top5-pct">3.0%</div></div>
      <div class="top5-item"><div class="top5-rank">#5</div><div class="top5-food">🍕 pizza</div><div class="top5-bar-wrap"><div class="top5-bar"><div class="top5-bar-fill" style="width:60%"></div></div></div><div class="top5-pct">3.0%</div></div>
    </div>
  </div>

  <!-- NUTRITION -->
  <div class="section-eyebrow" style="margin-top:36px">Nutrition Per 100g · Redis Cache</div>
  <div class="nutrition-strip">
    <div class="nut-card calories"><div class="nut-icon">🔥</div><div class="nut-val">153</div><div class="nut-label">Calories kcal</div></div>
    <div class="nut-card protein"><div class="nut-icon">💪</div><div class="nut-val">3.2g</div><div class="nut-label">Protein</div></div>
    <div class="nut-card carbs"><div class="nut-icon">🌾</div><div class="nut-val">47.6g</div><div class="nut-label">Carbs</div></div>
    <div class="nut-card fats"><div class="nut-icon">🫙</div><div class="nut-val">0g</div><div class="nut-label">Fats</div></div>
    <div class="nut-card fiber"><div class="nut-icon">🌿</div><div class="nut-val">7g</div><div class="nut-label">Fiber</div></div>
  </div>

  <div class="callout callout-blue">
    <div class="callout-label">💡 How Nutrition is Retrieved</div>
    When a food is predicted, the predicted class name is used as the Redis key. Redis returns a JSON object with per-100g macros in under 1ms — orders of magnitude faster than a SQL query.
    <br><br>
    <strong>Example Redis lookup:</strong><br>
    <code>GET food:kaathi_rolls</code> → <code>{"calories":153,"protein":3.2,"carbs":47.6,"fats":0,"fiber":7}</code>
  </div>
</section>

<!-- ── INFERENCE METRICS & FORMULAS ── -->
<section>
  <div class="section-eyebrow">Evaluation Metrics</div>
  <h2>Inference Metrics — Formulas & Examples</h2>
  <p>After each prediction the system calculates four classification metrics using the confusion matrix values: True Positives (TP), False Positives (FP), True Negatives (TN), and False Negatives (FN).</p>

  <div class="formula-section">
    <div class="formula-header">📐 Confusion Matrix Definitions</div>
    <div class="formula-body">
      <table class="info-table">
        <thead><tr><th>Term</th><th>Symbol</th><th>Meaning</th><th>Example (Food = Pizza)</th></tr></thead>
        <tbody>
          <tr><td>True Positive</td><td>TP</td><td>Model predicted Pizza → actual is Pizza</td><td>Image of pizza → predicted pizza ✅</td></tr>
          <tr><td>False Positive</td><td>FP</td><td>Model predicted Pizza → actual is NOT pizza</td><td>Image of flatbread → predicted pizza ❌</td></tr>
          <tr><td>True Negative</td><td>TN</td><td>Model did NOT predict Pizza → actual is NOT pizza</td><td>Image of sushi → predicted sushi ✅</td></tr>
          <tr><td>False Negative</td><td>FN</td><td>Model did NOT predict Pizza → actual IS pizza</td><td>Image of pizza → predicted pasta ❌</td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="formula-section">
    <div class="formula-header">🧮 Metric Formulas with Worked Examples</div>
    <div class="formula-body">
      <div class="formula-grid">

        <div class="formula-card">
          <h4>🎯 Accuracy</h4>
          <p>Fraction of all predictions that are correct. Works best when classes are balanced.</p>
          <div class="formula-eq">Accuracy = <span class="kw">(TP + TN)</span> / <span class="op">(TP + TN + FP + FN)</span></div>
          <div class="formula-example">
            <div class="formula-example-label">📌 Worked Example</div>
            <p>TP=2, TN=60, FP=18, FN=20 (100 total samples)<br>
            Accuracy = (2+60) / 100 = <strong>62 / 100 = 62%</strong><br>
            → Misleadingly high when classes are imbalanced.</p>
          </div>
          <div class="formula-example" style="background:#fff7ed;border-color:#fed7aa;margin-top:8px;">
            <div class="formula-example-label" style="color:var(--orange)">⚠️ Our Result: 3.0%</div>
            <p style="color:#9a3412;">Very low accuracy → model is predicting incorrectly for this class. Indicates the Custom CNN needs more training data or epochs for kaathi rolls.</p>
          </div>
        </div>

        <div class="formula-card">
          <h4>🔍 Precision</h4>
          <p>Of all times the model said "this is food X", how often was it right? Penalises false positives.</p>
          <div class="formula-eq">Precision = <span class="kw">TP</span> / <span class="op">(TP + FP)</span></div>
          <div class="formula-example">
            <div class="formula-example-label">📌 Worked Example</div>
            <p>TP=5, FP=87 (model predicted kaathi rolls 92 times)<br>
            Precision = 5 / (5+87) = <strong>5 / 92 ≈ 5.4%</strong><br>
            → When model says "kaathi rolls", it's right only 5.4% of the time.</p>
          </div>
          <div class="formula-example" style="background:#fff7ed;border-color:#fed7aa;margin-top:8px;">
            <div class="formula-example-label" style="color:var(--orange)">⚠️ Our Result: 5.4%</div>
            <p style="color:#9a3412;">Too many false positives — model is predicting kaathi rolls for images that aren't kaathi rolls.</p>
          </div>
        </div>

        <div class="formula-card">
          <h4>♻️ Recall (Sensitivity)</h4>
          <p>Of all actual food-X images, how many did the model correctly identify? Penalises false negatives.</p>
          <div class="formula-eq">Recall = <span class="kw">TP</span> / <span class="op">(TP + FN)</span></div>
          <div class="formula-example">
            <div class="formula-example-label">📌 Worked Example</div>
            <p>TP=55, FN=53 (total actual kaathi rolls = 108)<br>
            Recall = 55 / (55+53) = <strong>55 / 108 ≈ 50.9%</strong><br>
            → Model finds ~half of all real kaathi roll images correctly.</p>
          </div>
          <div class="formula-example" style="background:#f0fdf4;border-color:#bbf7d0;margin-top:8px;">
            <div class="formula-example-label">✅ Our Result: 50.9%</div>
            <p style="color:#166534;">Highest metric here — model has reasonable sensitivity, meaning it does detect actual kaathi rolls about half the time despite poor precision.</p>
          </div>
        </div>

        <div class="formula-card">
          <h4>📈 F1-Score</h4>
          <p>Harmonic mean of Precision and Recall. Best single metric when classes are imbalanced.</p>
          <div class="formula-eq">F1 = 2 × <span class="kw">(Precision × Recall)</span> / <span class="op">(Precision + Recall)</span></div>
          <div class="formula-example">
            <div class="formula-example-label">📌 Worked Example</div>
            <p>Precision = 5.4%, Recall = 50.9%<br>
            F1 = 2 × (0.054 × 0.509) / (0.054 + 0.509)<br>
            F1 = 2 × 0.02749 / 0.563 = <strong>0.0977 ≈ 9.7%</strong></p>
          </div>
          <div class="formula-example" style="background:#fff7ed;border-color:#fed7aa;margin-top:8px;">
            <div class="formula-example-label" style="color:var(--orange)">⚠️ Our Result: 9.7%</div>
            <p style="color:#9a3412;">F1 is pulled down severely by low Precision. The harmonic mean punishes extreme imbalance between P and R.</p>
          </div>
        </div>

      </div>

      <div class="callout callout-green" style="margin-top:20px">
        <div class="callout-label">📊 Why Recall (50.9%) is so much higher than Precision (5.4%)?</div>
        The Custom CNN has a tendency to over-predict the kaathi rolls class (high FP). It detects real kaathi rolls adequately (decent TP, low FN → good Recall), but it also fires false alarms on unrelated foods (many FP → poor Precision). Training on a larger, more balanced dataset with data augmentation and class-weighted loss will fix this.
      </div>
    </div>
  </div>

  <!-- Softmax -->
  <div class="formula-section">
    <div class="formula-header">🔢 Softmax — How Confidence Scores Are Computed</div>
    <div class="formula-body">
      <p>The final layer of every model outputs a raw score (logit) for each of the 34 food classes. These logits are converted to probabilities using the <strong>Softmax function</strong>:</p>
      <div class="formula-eq">P(class<span class="kw"> i</span>) = e<sup><span class="val">z_i</span></sup> / Σ<sub>j=1</sub><sup>34</sup> e<sup><span class="val">z_j</span></sup></div>
      <div class="formula-example">
        <div class="formula-example-label">📌 Example with 3 classes (simplified)</div>
        <p>
          Logits: kaathi_rolls=1.2, pizza=1.1, biryani=0.9<br>
          e^1.2=3.32, e^1.1=3.00, e^0.9=2.46 &nbsp;→&nbsp; sum=8.78<br>
          P(kaathi_rolls) = 3.32/8.78 = <strong>37.8%</strong> &nbsp;|&nbsp; P(pizza) = 3.00/8.78 = <strong>34.2%</strong><br>
          All probabilities sum to 1.0 (100%)
        </p>
      </div>
      <p style="margin-top:12px">In our prediction, all top-5 show 3.0% — meaning the model's logits are nearly uniform across all 34 classes, indicating high uncertainty (an underfitted model for this class).</p>
    </div>
  </div>
</section>

<!-- ── CNN ARCHITECTURES ── -->
<section>
  <div class="section-eyebrow">Architectures</div>
  <h2>Model Selection — Deep Dive</h2>
  <p>Three CNN architectures are available. Each is pre-configured with its optimal input resolution and head layer for 34-class food classification.</p>

  <div class="model-grid" style="margin-bottom:32px">
    <div class="model-card custom">
      <div class="model-icon">🧠</div>
      <h3>Custom CNN</h3>
      <p>Lightweight architecture designed from scratch — fast training, low memory footprint.</p>
      <div class="model-tag">256 × 256 RGB</div>
      <div class="model-specs">
        <div class="model-spec"><span class="model-spec-key">Type</span><span class="model-spec-val">From scratch</span></div>
        <div class="model-spec"><span class="model-spec-key">Pretrained</span><span class="model-spec-val">No</span></div>
        <div class="model-spec"><span class="model-spec-key">Input</span><span class="model-spec-val">256×256×3</span></div>
        <div class="model-spec"><span class="model-spec-key">Output</span><span class="model-spec-val">34 classes (Softmax)</span></div>
        <div class="model-spec"><span class="model-spec-key">Optimizer</span><span class="model-spec-val">Adam</span></div>
        <div class="model-spec"><span class="model-spec-key">Loss</span><span class="model-spec-val">Categorical CE</span></div>
      </div>
    </div>
    <div class="model-card vgg">
      <div class="model-icon">🏛</div>
      <h3>VGG-16</h3>
      <p>16-layer deep network with uniform 3×3 convolutions. Fine-tuned from ImageNet weights.</p>
      <div class="model-tag">224 × 224 RGB</div>
      <div class="model-specs">
        <div class="model-spec"><span class="model-spec-key">Type</span><span class="model-spec-val">Transfer Learning</span></div>
        <div class="model-spec"><span class="model-spec-key">Pretrained</span><span class="model-spec-val">ImageNet</span></div>
        <div class="model-spec"><span class="model-spec-key">Input</span><span class="model-spec-val">224×224×3</span></div>
        <div class="model-spec"><span class="model-spec-key">Output</span><span class="model-spec-val">34 classes (Softmax)</span></div>
        <div class="model-spec"><span class="model-spec-key">Parameters</span><span class="model-spec-val">138M (frozen base)</span></div>
        <div class="model-spec"><span class="model-spec-key">Fine-tune layers</span><span class="model-spec-val">FC head only</span></div>
      </div>
    </div>
    <div class="model-card resnet">
      <div class="model-icon">🔗</div>
      <h3>ResNet-50</h3>
      <p>50-layer residual network with identity skip connections. Hosted separately on Drive.</p>
      <div class="model-tag">224 × 224 RGB</div>
      <div class="model-specs">
        <div class="model-spec"><span class="model-spec-key">Type</span><span class="model-spec-val">Transfer Learning</span></div>
        <div class="model-spec"><span class="model-spec-key">Pretrained</span><span class="model-spec-val">ImageNet</span></div>
        <div class="model-spec"><span class="model-spec-key">Input</span><span class="model-spec-val">224×224×3</span></div>
        <div class="model-spec"><span class="model-spec-key">Output</span><span class="model-spec-val">34 classes (Softmax)</span></div>
        <div class="model-spec"><span class="model-spec-key">Parameters</span><span class="model-spec-val">25.6M</span></div>
        <div class="model-spec"><span class="model-spec-key">Key feature</span><span class="model-spec-val">Residual skip blocks</span></div>
      </div>
    </div>
  </div>

  <!-- Custom CNN Architecture -->
  <div class="arch-block">
    <div class="arch-header">
      <div class="arch-icon" style="background:#eff6ff;border:2px solid var(--blue);color:var(--blue);">🧠</div>
      <div><h3 style="margin:0;color:var(--blue)">Custom CNN — Layer-by-Layer Architecture</h3><p style="margin:0;font-size:13px;color:var(--muted)">Trained from scratch · Input: 256×256×3 · Output: 34-class Softmax</p></div>
    </div>
    <div class="arch-body">
      <p>The Custom CNN is a sequential stack of Conv → BatchNorm → ReLU → MaxPool blocks, followed by GlobalAveragePooling and a Dense classification head.</p>
      <div class="layer-list">
        <div class="layer-item conv"><div class="layer-num">L1</div><div><div class="layer-name">Conv2D (32 filters, 3×3) + ReLU</div><div class="layer-desc">Input: 256×256×3 → Output: 256×256×32. Detects low-level edges, corners, color gradients.</div></div><div class="layer-params">32 × 3×3×3 = 864 params</div></div>
        <div class="layer-item bn"><div class="layer-num">L2</div><div><div class="layer-name">BatchNormalization</div><div class="layer-desc">Normalises activations per mini-batch — stabilises training, allows higher learning rates.</div></div><div class="layer-params">128 params</div></div>
        <div class="layer-item pool"><div class="layer-num">L3</div><div><div class="layer-name">MaxPooling2D (2×2, stride 2)</div><div class="layer-desc">Spatial downsampling: 256×256×32 → 128×128×32. Reduces computation, adds translation invariance.</div></div><div class="layer-params">0 params</div></div>
        <div class="layer-item conv"><div class="layer-num">L4</div><div><div class="layer-name">Conv2D (64 filters, 3×3) + ReLU</div><div class="layer-desc">128×128×32 → 128×128×64. Learns mid-level textures (food textures, patterns).</div></div><div class="layer-params">18,432 params</div></div>
        <div class="layer-item bn"><div class="layer-num">L5</div><div><div class="layer-name">BatchNormalization</div><div class="layer-desc">Normalises 64-channel feature maps.</div></div><div class="layer-params">256 params</div></div>
        <div class="layer-item pool"><div class="layer-num">L6</div><div><div class="layer-name">MaxPooling2D (2×2)</div><div class="layer-desc">128×128×64 → 64×64×64.</div></div><div class="layer-params">0 params</div></div>
        <div class="layer-item conv"><div class="layer-num">L7</div><div><div class="layer-name">Conv2D (128 filters, 3×3) + ReLU</div><div class="layer-desc">64×64×64 → 64×64×128. Captures complex food shapes, ingredient arrangements.</div></div><div class="layer-params">73,728 params</div></div>
        <div class="layer-item bn"><div class="layer-num">L8</div><div><div class="layer-name">BatchNormalization + MaxPool</div><div class="layer-desc">64×64×128 → 32×32×128.</div></div><div class="layer-params">512 params</div></div>
        <div class="layer-item drop"><div class="layer-num">L9</div><div><div class="layer-name">Dropout (0.4)</div><div class="layer-desc">Randomly zero 40% of neurons during training — prevents overfitting on small food datasets.</div></div><div class="layer-params">0 params</div></div>
        <div class="layer-item pool"><div class="layer-num">L10</div><div><div class="layer-name">GlobalAveragePooling2D</div><div class="layer-desc">32×32×128 → 128-dimensional vector. Replaces Flatten to reduce parameters and improve generalisation.</div></div><div class="layer-params">0 params</div></div>
        <div class="layer-item fc"><div class="layer-num">L11</div><div><div class="layer-name">Dense (256, ReLU) + Dropout(0.5)</div><div class="layer-desc">Fully-connected classification head. 50% dropout for regularisation.</div></div><div class="layer-params">32,768 params</div></div>
        <div class="layer-item out"><div class="layer-num">L12</div><div><div class="layer-name">Dense (34, Softmax) — Output Layer</div><div class="layer-desc">Outputs probability distribution over all 34 food classes. All values sum to 1.0.</div></div><div class="layer-params">8,704 params</div></div>
      </div>
    </div>
  </div>

  <!-- VGG-16 Architecture -->
  <div class="arch-block" style="margin-top:20px">
    <div class="arch-header">
      <div class="arch-icon" style="background:#f5f3ff;border:2px solid var(--purple);color:var(--purple);">🏛</div>
      <div><h3 style="margin:0;color:var(--purple)">VGG-16 — Architecture & Transfer Learning</h3><p style="margin:0;font-size:13px;color:var(--muted)">ImageNet pretrained · Input: 224×224×3 · Fine-tuned FC head</p></div>
    </div>
    <div class="arch-body">
      <p>VGG-16 uses exclusively 3×3 conv filters in 5 convolutional blocks — a design that achieves depth without parameter explosion. Only the classification head is retrained for our 34-class task.</p>
      <div class="layer-list">
        <div class="layer-item conv"><div class="layer-num">B1</div><div><div class="layer-name">Block 1: Conv2D ×2 (64 filters, 3×3)</div><div class="layer-desc">224×224×3 → 224×224×64. Two conv layers before pooling to build richer feature maps at full resolution.</div></div><div class="layer-params">FROZEN</div></div>
        <div class="layer-item pool"><div class="layer-num"></div><div><div class="layer-name">MaxPool → 112×112×64</div></div></div>
        <div class="layer-item conv"><div class="layer-num">B2</div><div><div class="layer-name">Block 2: Conv2D ×2 (128 filters, 3×3)</div><div class="layer-desc">112×112×64 → 112×112×128. Learns richer texture patterns.</div></div><div class="layer-params">FROZEN</div></div>
        <div class="layer-item pool"><div class="layer-num"></div><div><div class="layer-name">MaxPool → 56×56×128</div></div></div>
        <div class="layer-item conv"><div class="layer-num">B3</div><div><div class="layer-name">Block 3: Conv2D ×3 (256 filters, 3×3)</div><div class="layer-desc">56×56×128 → 56×56×256. Mid-level structural patterns.</div></div><div class="layer-params">FROZEN</div></div>
        <div class="layer-item pool"><div class="layer-num"></div><div><div class="layer-name">MaxPool → 28×28×256</div></div></div>
        <div class="layer-item conv"><div class="layer-num">B4</div><div><div class="layer-name">Block 4: Conv2D ×3 (512 filters, 3×3)</div><div class="layer-desc">28×28×256 → 28×28×512. High-level semantic features.</div></div><div class="layer-params">FROZEN</div></div>
        <div class="layer-item conv"><div class="layer-num">B5</div><div><div class="layer-name">Block 5: Conv2D ×3 (512 filters, 3×3) + MaxPool</div><div class="layer-desc">28×28×512 → 14×14×512 → 7×7×512.</div></div><div class="layer-params">FROZEN</div></div>
        <div class="layer-item fc"><div class="layer-num">FC</div><div><div class="layer-name">Flatten → Dense(256, ReLU) → Dropout(0.5)</div><div class="layer-desc">Custom classification head added on top of frozen VGG-16 base. Only this layer trains.</div></div><div class="layer-params">TRAINABLE</div></div>
        <div class="layer-item out"><div class="layer-num">OUT</div><div><div class="layer-name">Dense(34, Softmax)</div><div class="layer-desc">34-class probability output.</div></div><div class="layer-params">TRAINABLE</div></div>
      </div>
    </div>
  </div>

  <!-- ResNet-50 Architecture -->
  <div class="arch-block" style="margin-top:20px">
    <div class="arch-header">
      <div class="arch-icon" style="background:#fff7ed;border:2px solid var(--orange);color:var(--orange);">🔗</div>
      <div><h3 style="margin:0;color:var(--orange)">ResNet-50 — Residual Skip Connection Architecture</h3><p style="margin:0;font-size:13px;color:var(--muted)">ImageNet pretrained · Input: 224×224×3 · 25.6M parameters · Download from Drive</p></div>
    </div>
    <div class="arch-body">
      <p>ResNet-50 solves the vanishing gradient problem with <strong>identity shortcut connections</strong> (skip connections) that allow gradients to flow directly through the network, enabling much deeper training without degradation.</p>
      <div class="layer-list">
        <div class="layer-item conv"><div class="layer-num">S0</div><div><div class="layer-name">Conv2D (64, 7×7, stride 2) + BN + ReLU</div><div class="layer-desc">224×224×3 → 112×112×64. Initial large-kernel stem layer captures global context.</div></div><div class="layer-params">9,408 params</div></div>
        <div class="layer-item pool"><div class="layer-num"></div><div><div class="layer-name">MaxPool (3×3, stride 2) → 56×56×64</div></div></div>
        <div class="layer-item res"><div class="layer-num">C2</div><div><div class="layer-name">Residual Block ×3 (64 filters) — Stage 2</div><div class="layer-desc">Each block: Conv1×1 → Conv3×3 → Conv1×1 + skip connection. Output: 56×56×256.</div></div><div class="layer-params">215K params</div></div>
        <div class="layer-item res"><div class="layer-num">C3</div><div><div class="layer-name">Residual Block ×4 (128 filters) — Stage 3</div><div class="layer-desc">Stride-2 first block: 56×56×256 → 28×28×512.</div></div><div class="layer-params">1.2M params</div></div>
        <div class="layer-item res"><div class="layer-num">C4</div><div><div class="layer-name">Residual Block ×6 (256 filters) — Stage 4</div><div class="layer-desc">28×28×512 → 14×14×1024.</div></div><div class="layer-params">7.1M params</div></div>
        <div class="layer-item res"><div class="layer-num">C5</div><div><div class="layer-name">Residual Block ×3 (512 filters) — Stage 5</div><div class="layer-desc">14×14×1024 → 7×7×2048.</div></div><div class="layer-params">14.9M params</div></div>
        <div class="layer-item pool"><div class="layer-num"></div><div><div class="layer-name">GlobalAveragePooling2D → 2048-dim vector</div></div></div>
        <div class="layer-item out"><div class="layer-num">OUT</div><div><div class="layer-name">Dense(34, Softmax) — Custom food head</div><div class="layer-desc">Replaces original 1000-class ImageNet head with 34-class food classifier.</div></div><div class="layer-params">TRAINABLE</div></div>
      </div>
      <div class="callout callout-blue" style="margin-top:16px">
        <div class="callout-label">🔗 The Skip Connection Formula</div>
        <strong>H(x) = F(x) + x</strong><br>
        Where F(x) is the learned residual and x is the identity shortcut. If the residual is not needed, F(x)→0 and the layer learns the identity — preventing degradation in deep networks.
      </div>
    </div>
  </div>

  <!-- Model Comparison Table -->
  <h3 style="margin-top:32px">Model Comparison Table</h3>
  <table class="info-table">
    <thead><tr><th>Property</th><th>🧠 Custom CNN</th><th>🏛 VGG-16</th><th>🔗 ResNet-50</th></tr></thead>
    <tbody>
      <tr><td>Input Size</td><td>256×256×3</td><td>224×224×3</td><td>224×224×3</td></tr>
      <tr><td>Pretrained</td><td>No (from scratch)</td><td>Yes (ImageNet)</td><td>Yes (ImageNet)</td></tr>
      <tr><td>Parameters</td><td>~130K (custom)</td><td>138M (frozen base)</td><td>25.6M</td></tr>
      <tr><td>Training Speed</td><td>⚡ Fast</td><td>🐢 Slow (heavy)</td><td>⚡⚡ Fast</td></tr>
      <tr><td>Skip Connections</td><td>No</td><td>No</td><td>Yes (residual)</td></tr>
      <tr><td>Best For</td><td>Quick experiments</td><td>High accuracy (slow)</td><td>Best accuracy+speed</td></tr>
      <tr><td>Model Hosted</td><td>GitHub repo</td><td>GitHub repo</td><td>Google Drive</td></tr>
    </tbody>
  </table>
</section>

<!-- ── HOW IT WORKS ── -->
<section>
  <div class="section-eyebrow">Pipeline</div>
  <h2>End-to-End Prediction Pipeline</h2>
  <div class="flow-diagram">
    <div class="flow-step"><div class="flow-icon">📸</div><div class="flow-label">Upload Image</div></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><div class="flow-icon">🔄</div><div class="flow-label">Preprocess</div></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><div class="flow-icon">🧠</div><div class="flow-label">CNN Inference</div></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><div class="flow-icon">📐</div><div class="flow-label">Softmax Output</div></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><div class="flow-icon">⚡</div><div class="flow-label">Redis Nutrition</div></div>
    <div class="flow-arrow">→</div>
    <div class="flow-step"><div class="flow-icon">📊</div><div class="flow-label">Result Dashboard</div></div>
  </div>

  <table class="info-table" style="margin-top:16px">
    <thead><tr><th>Step</th><th>What Happens</th><th>Tech Used</th></tr></thead>
    <tbody>
      <tr><td>1. Upload</td><td>User drags/drops a JPG, PNG, or WEBP food image</td><td>HTML5 File API, Flask</td></tr>
      <tr><td>2. Preprocess</td><td>Image is resized to model's input size, normalized to [0,1] pixel range, batch dimension added</td><td>OpenCV, NumPy</td></tr>
      <tr><td>3. Inference</td><td>Selected CNN model runs model.predict() on the preprocessed array</td><td>TensorFlow / Keras</td></tr>
      <tr><td>4. Softmax Output</td><td>34 raw logits → 34 probabilities via Softmax. Top-5 are extracted and ranked.</td><td>NumPy argsort</td></tr>
      <tr><td>5. Redis Lookup</td><td>Top-1 class name used as Redis key → nutrition JSON retrieved in &lt;1ms</td><td>Redis, redis-py</td></tr>
      <tr><td>6. Dashboard</td><td>Prediction, confidence, metrics, top-5 rankings, and nutrition rendered to client</td><td>JavaScript, CSS</td></tr>
    </tbody>
  </table>
</section>

<!-- ── TECH STACK ── -->
<section>
  <div class="section-eyebrow">Stack</div>
  <h2>Technologies Used</h2>
  <div class="tech-grid">
    <div class="tech-group frontend">
      <div class="tech-group-title">🎨 Frontend</div>
      <div class="tech-item"><span class="tech-item-icon">🌐</span> HTML5 — structure & upload form</div>
      <div class="tech-item"><span class="tech-item-icon">🎨</span> CSS3 — responsive dark-light UI</div>
      <div class="tech-item"><span class="tech-item-icon">⚡</span> JavaScript — async fetch, bar animation</div>
    </div>
    <div class="tech-group backend">
      <div class="tech-group-title">🖥 Backend</div>
      <div class="tech-item"><span class="tech-item-icon">🐍</span> Python 3.x</div>
      <div class="tech-item"><span class="tech-item-icon">🌶</span> Flask — REST API server</div>
      <div class="tech-item"><span class="tech-item-icon">🔁</span> OpenCV — image preprocessing</div>
    </div>
    <div class="tech-group dl">
      <div class="tech-group-title">🧠 Deep Learning</div>
      <div class="tech-item"><span class="tech-item-icon">🔷</span> TensorFlow 2.x — training & inference</div>
      <div class="tech-item"><span class="tech-item-icon">🔶</span> Keras — model API (Sequential/Functional)</div>
      <div class="tech-item"><span class="tech-item-icon">📦</span> NumPy — array ops & Softmax</div>
    </div>
    <div class="tech-group db">
      <div class="tech-group-title">⚡ Data Store</div>
      <div class="tech-item"><span class="tech-item-icon">🔴</span> Redis — in-memory nutrition KV store</div>
      <div class="tech-item"><span class="tech-item-icon">💾</span> redis-py — Python Redis client</div>
      <div class="tech-item"><span class="tech-item-icon">⚡</span> Sub-millisecond GET lookups</div>
    </div>
  </div>
</section>

<!-- ── INSTALLATION ── -->
<section id="install">
  <div class="section-eyebrow">Setup</div>
  <h2>Installation Guide</h2>
  <div class="install-steps">
    <div class="install-step">
      <div class="step-num">1</div>
      <div class="step-content">
        <h3>Clone the Repository</h3>
        <div class="code-block">
          <div class="code-header"><div class="code-dots"><div class="cd1"></div><div class="cd2"></div><div class="cd3"></div></div><div class="code-lang">bash</div></div>
          <div class="code-body"><span class="ck">git clone</span> <span class="cs">https://github.com/your-username/food-vision-ai.git</span><br><span class="ck">cd</span> food-vision-ai</div>
        </div>
      </div>
    </div>
    <div class="install-step">
      <div class="step-num">2</div>
      <div class="step-content">
        <h3>Create & Activate Virtual Environment</h3>
        <div class="code-block">
          <div class="code-header"><div class="code-dots"><div class="cd1"></div><div class="cd2"></div><div class="cd3"></div></div><div class="code-lang">bash</div></div>
          <div class="code-body"><span class="cc"># Windows</span><br><span class="ck">python -m venv</span> .venv<br>.venv\Scripts\activate<br><br><span class="cc"># Linux / Mac</span><br><span class="ck">python3 -m venv</span> .venv<br><span class="cf">source</span> .venv/bin/activate</div>
        </div>
      </div>
    </div>
    <div class="install-step">
      <div class="step-num">3</div>
      <div class="step-content">
        <h3>Install Python Dependencies</h3>
        <div class="code-block">
          <div class="code-header"><div class="code-dots"><div class="cd1"></div><div class="cd2"></div><div class="cd3"></div></div><div class="code-lang">bash</div></div>
          <div class="code-body"><span class="ck">pip install</span> -r requirements.txt<br><br><span class="cc"># Key packages: tensorflow, flask, opencv-python, redis, numpy, Pillow</span></div>
        </div>
      </div>
    </div>
    <div class="install-step">
      <div class="step-num">4</div>
      <div class="step-content">
        <h3>Install & Start Redis</h3>
        <div class="code-block">
          <div class="code-header"><div class="code-dots"><div class="cd1"></div><div class="cd2"></div><div class="cd3"></div></div><div class="code-lang">bash</div></div>
          <div class="code-body"><span class="cc"># Ubuntu / Debian</span><br><span class="ck">sudo apt install</span> redis-server<br><span class="ck">sudo service</span> redis-server start<br><br><span class="cc"># Mac (Homebrew)</span><br><span class="ck">brew install</span> redis <span class="cf">&amp;&amp;</span> <span class="ck">brew services start</span> redis<br><br><span class="cc"># Windows — download from:</span><br><span class="cs">https://github.com/microsoftarchive/redis/releases</span><br>redis-server</div>
        </div>
      </div>
    </div>
    <div class="install-step">
      <div class="step-num">5</div>
      <div class="step-content">
        <h3>Download ResNet-50 Model (Google Drive)</h3>
        <p>Due to GitHub's 100MB file limit, the trained ResNet-50 model is hosted externally. Download and place it in the project root directory.</p>
        <a href="https://drive.google.com/file/d/12eCgqD2To5Kq2XRIDGBb3OsNbA-MkWSd/view" class="btn btn-white" style="color:var(--blue);border-color:var(--blue);border:2px solid var(--blue);display:inline-flex;margin-top:4px;">📥 Download from Google Drive</a>
      </div>
    </div>
    <div class="install-step">
      <div class="step-num">6</div>
      <div class="step-content">
        <h3>Run the Application</h3>
        <div class="code-block">
          <div class="code-header"><div class="code-dots"><div class="cd1"></div><div class="cd2"></div><div class="cd3"></div></div><div class="code-lang">bash</div></div>
          <div class="code-body"><span class="ck">python</span> app.py<br><br><span class="cc"># Open browser at:</span><br><span class="cs">http://127.0.0.1:5000</span></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── FOOD CLASSES ── -->
<section>
  <div class="section-eyebrow">Dataset</div>
  <h2>34 Supported Food Classes</h2>
  <p>The model is trained to recognise the following food categories. Each class also has a corresponding Redis entry with nutritional data.</p>
  <div style="display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-top:16px;">
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🥔 Baked Potato</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🫓 Chapati</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🌯 Kaathi Rolls</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍚 Fried Rice</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍰 Cheesecake</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍛 Chicken Curry</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍕 Pizza</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍜 Noodles</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍱 Biryani</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🥗 Caesar Salad</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍔 Burger</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🌮 Tacos</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍣 Sushi</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🥞 Pancakes</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">🍦 Ice Cream</div>
    <div style="background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:10px 12px;font-size:13px;color:var(--text2);">+ 19 more classes</div>
  </div>
</section>

<!-- ── ROADMAP ── -->
<section>
  <div class="section-eyebrow">Future Work</div>
  <h2>Roadmap & Planned Improvements</h2>
  <div class="roadmap-grid">
    <div class="roadmap-item"><div class="roadmap-icon">📸</div><div><h3>Live Webcam Prediction</h3><p>Real-time food detection from webcam stream using OpenCV VideoCapture + Flask streaming endpoint.</p></div></div>
    <div class="roadmap-item"><div class="roadmap-icon">📱</div><div><h3>Mobile Application</h3><p>Native iOS/Android app using TensorFlow Lite model conversion for on-device inference.</p></div></div>
    <div class="roadmap-item"><div class="roadmap-icon">🍽</div><div><h3>Multi-food Detection</h3><p>Object detection (YOLO/SSD) to localise and classify multiple food items in a single scene.</p></div></div>
    <div class="roadmap-item"><div class="roadmap-icon">📅</div><div><h3>Calorie Tracking System</h3><p>Daily food diary, calorie summation, and macro-nutrient progress charts per user session.</p></div></div>
    <div class="roadmap-item"><div class="roadmap-icon">🎙</div><div><h3>Voice Assistant Integration</h3><p>Voice-guided queries ("What did I eat today?") using speech-to-text + food diary API.</p></div></div>
    <div class="roadmap-item"><div class="roadmap-icon">☁️</div><div><h3>Cloud Deployment</h3><p>AWS EC2 / GCP Cloud Run with Docker containerisation, load balancing, and CDN for model serving.</p></div></div>
  </div>
</section>

<!-- ── DEVELOPER ── -->
<section>
  <div class="section-eyebrow">Author</div>
  <div class="dev-card">
    <div class="dev-avatar">👩‍💻</div>
    <div>
      <div class="dev-name">Mounika Kusumba</div>
      <div class="dev-role">AI Engineer &amp; Deep Learning Developer</div>
      <div class="dev-tags">
        <span class="dev-tag">🖼 Computer Vision</span>
        <span class="dev-tag">👁 OpenCV</span>
        <span class="dev-tag">🔷 TensorFlow</span>
        <span class="dev-tag">🤖 Deep Learning</span>
        <span class="dev-tag">🧠 Intelligent AI Systems</span>
        <span class="dev-tag">🌶 Flask</span>
        <span class="dev-tag">⚡ Redis</span>
      </div>
    </div>
  </div>
</section>

</div>

<div class="footer">
  Built with ❤️ by <span>Mounika Kusumba</span> &nbsp;·&nbsp; Food Vision AI — Deep Learning Food Classification System
</div>

</body>
</html>
