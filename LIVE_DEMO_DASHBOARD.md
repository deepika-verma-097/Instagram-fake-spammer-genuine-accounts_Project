[instagram_dashboard (3).html](https://github.com/user-attachments/files/25658010/instagram_dashboard.3.html)# 🚀 Live Demo

You can view the live dashboard here:

👉 [Click Here to Open Dashboard](file:///C:/Users/FRRO/Downloads/instagram_dashboard%20(3).html)
[<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>INSTA·SCAN — Fake Account Intelligence</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;500;600;700&family=Exo+2:wght@300;400;600;800;900&display=swap" rel="stylesheet">
<style>
*{margin:0;padding:0;box-sizing:border-box;}

:root{
  --bg:#060818;
  --surface:#0c1128;
  --surface2:#111830;
  --border:#1e2d5a;
  --border2:#2a3d7a;
  --pink:#f0366a;
  --cyan:#06d6f5;
  --green:#05e89a;
  --yellow:#ffd166;
  --purple:#9b72ff;
  --text:#f0f4ff;
  --sub:#9ab0d8;
  --dim:#4a5f8a;
}

html,body{width:100vw;height:100vh;overflow:hidden;background:var(--bg);color:var(--text);font-family:'Rajdhani',sans-serif;}

/* ── ANIMATED BACKGROUND ── */
.bg-mesh{
  position:fixed;inset:0;z-index:0;
  background:
    radial-gradient(ellipse 600px 400px at 85% 5%,rgba(240,54,106,0.12) 0%,transparent 70%),
    radial-gradient(ellipse 500px 400px at 10% 90%,rgba(6,214,245,0.1) 0%,transparent 70%),
    radial-gradient(ellipse 300px 300px at 55% 50%,rgba(155,114,255,0.06) 0%,transparent 70%);
  pointer-events:none;
}
.grid-lines{
  position:fixed;inset:0;z-index:0;
  background-image:
    linear-gradient(rgba(6,214,245,0.03) 1px,transparent 1px),
    linear-gradient(90deg,rgba(6,214,245,0.03) 1px,transparent 1px);
  background-size:44px 44px;
  pointer-events:none;
}
/* Slow rotating gradient ring */
.ring{
  position:fixed;width:900px;height:900px;border-radius:50%;
  border:1px solid rgba(6,214,245,0.05);
  top:50%;left:50%;transform:translate(-50%,-50%);
  animation:spin 40s linear infinite;pointer-events:none;z-index:0;
}
.ring2{
  position:fixed;width:650px;height:650px;border-radius:50%;
  border:1px solid rgba(240,54,106,0.04);
  top:50%;left:50%;transform:translate(-50%,-50%);
  animation:spin 28s linear infinite reverse;pointer-events:none;z-index:0;
}
@keyframes spin{to{transform:translate(-50%,-50%) rotate(360deg);}}

/* Scan line */
.scanline{
  position:fixed;left:0;right:0;height:180px;
  background:linear-gradient(180deg,transparent,rgba(6,214,245,0.025),transparent);
  pointer-events:none;z-index:1;animation:scanDrop 7s ease-in-out infinite;
}
@keyframes scanDrop{0%{top:-180px}100%{top:100vh}}

/* ── SHELL ── */
.shell{
  position:relative;z-index:2;
  width:100vw;height:100vh;
  display:grid;
  grid-template-rows:64px 1fr;
  padding:10px 12px;gap:8px;
}

/* ── HEADER ── */
header{
  display:grid;
  grid-template-columns:auto 1fr auto;
  align-items:center;gap:20px;
  padding:0 18px;
  background:linear-gradient(135deg,rgba(12,17,40,0.95),rgba(17,24,48,0.9));
  border:1px solid var(--border2);
  border-radius:10px;
  position:relative;overflow:hidden;
  box-shadow:0 0 30px rgba(6,214,245,0.08), inset 0 1px 0 rgba(255,255,255,0.05);
}
header::before{
  content:'';position:absolute;inset:0;
  background:linear-gradient(90deg,transparent 0%,rgba(6,214,245,0.04) 50%,transparent 100%);
  animation:hSweep 4s ease-in-out infinite;
}
@keyframes hSweep{0%,100%{transform:translateX(-100%)}50%{transform:translateX(100%)}}
header::after{
  content:'';position:absolute;bottom:0;left:5%;right:5%;height:1px;
  background:linear-gradient(90deg,transparent,var(--cyan),transparent);
  opacity:0.3;
}

.logo-block{display:flex;align-items:center;gap:12px;}
.logo-icon{
  width:36px;height:36px;border-radius:8px;
  background:linear-gradient(135deg,rgba(240,54,106,0.3),rgba(6,214,245,0.3));
  border:1px solid rgba(6,214,245,0.4);
  display:flex;align-items:center;justify-content:center;font-size:16px;
  box-shadow:0 0 15px rgba(6,214,245,0.2);
}
.logo-text{
  font-family:'Exo 2',sans-serif;font-size:22px;font-weight:900;
  letter-spacing:0.12em;
  background:linear-gradient(90deg,var(--cyan),#a0f0ff);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  filter:drop-shadow(0 0 12px rgba(6,214,245,0.5));
}
.logo-text span{
  background:linear-gradient(90deg,var(--pink),#ff8ab0);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;
  filter:drop-shadow(0 0 12px rgba(240,54,106,0.5));
}

.h-center{display:flex;flex-direction:column;align-items:center;gap:3px;}
.h-title{font-family:'Exo 2',sans-serif;font-size:11px;font-weight:600;letter-spacing:0.25em;color:var(--sub);text-transform:uppercase;}
.h-desc{font-size:11px;color:var(--dim);letter-spacing:0.05em;}

.h-right{display:flex;gap:10px;align-items:center;}
.badge{
  display:flex;align-items:center;gap:7px;
  padding:6px 14px;border-radius:6px;
  font-family:'Exo 2',sans-serif;font-size:11px;font-weight:700;letter-spacing:0.08em;
  border:1px solid;text-transform:uppercase;
}
.badge-dot{width:6px;height:6px;border-radius:50%;animation:pulse 1.6s ease-in-out infinite;}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1)}50%{opacity:0.4;transform:scale(0.7)}}
.bg{border-color:rgba(5,232,154,0.4);color:var(--green);background:rgba(5,232,154,0.08);}
.bg .badge-dot{background:var(--green);box-shadow:0 0 6px var(--green);}
.bc{border-color:rgba(6,214,245,0.4);color:var(--cyan);background:rgba(6,214,245,0.08);}
.bc .badge-dot{background:var(--cyan);box-shadow:0 0 6px var(--cyan);}
.bp{border-color:rgba(240,54,106,0.4);color:var(--pink);background:rgba(240,54,106,0.08);}
.bp .badge-dot{background:var(--pink);box-shadow:0 0 6px var(--pink);}

/* ── MAIN GRID ── */
.main{
  display:grid;
  grid-template-columns:210px 1fr 1fr 190px;
  grid-template-rows:1fr 1fr;
  gap:8px;
}

/* ── PANEL BASE ── */
.panel{
  background:linear-gradient(135deg,rgba(12,17,40,0.98),rgba(11,16,38,0.95));
  border:1px solid var(--border);
  border-radius:10px;
  padding:14px 16px;
  position:relative;overflow:hidden;
  transition:border-color 0.3s,box-shadow 0.3s;
  box-shadow:0 4px 24px rgba(0,0,0,0.3);
}
.panel:hover{
  border-color:rgba(6,214,245,0.35);
  box-shadow:0 4px 32px rgba(6,214,245,0.1),0 0 0 1px rgba(6,214,245,0.05);
}
/* Corner accents */
.panel::before{
  content:'';position:absolute;top:0;left:0;
  width:24px;height:24px;
  border-top:2px solid rgba(6,214,245,0.5);
  border-left:2px solid rgba(6,214,245,0.5);
  border-radius:10px 0 0 0;
}
.panel::after{
  content:'';position:absolute;bottom:0;right:0;
  width:24px;height:24px;
  border-bottom:2px solid rgba(240,54,106,0.35);
  border-right:2px solid rgba(240,54,106,0.35);
  border-radius:0 0 10px 0;
}

/* ── PANEL TITLE ── */
.ptitle{
  font-family:'Exo 2',sans-serif;
  font-size:11px;font-weight:700;
  letter-spacing:0.2em;text-transform:uppercase;
  color:var(--sub);
  margin-bottom:10px;
  display:flex;align-items:center;gap:7px;
}
.ptitle-dot{width:5px;height:5px;border-radius:50%;background:var(--cyan);box-shadow:0 0 8px var(--cyan);}

/* ── KPI COLUMN ── */
.p-kpi{grid-column:1;grid-row:1/3;display:flex;flex-direction:column;gap:6px;}

.kblock{
  flex:1;
  border-radius:8px;
  border:1px solid var(--border);
  padding:10px 13px;
  display:flex;flex-direction:column;justify-content:center;
  position:relative;overflow:hidden;
  background:rgba(255,255,255,0.02);
  transition:border-color 0.3s;
}
.kblock:hover{border-color:rgba(6,214,245,0.3);}
.kblock::before{
  content:'';position:absolute;left:0;top:15%;bottom:15%;
  width:3px;border-radius:0 2px 2px 0;
}
.kblock.kc::before{background:linear-gradient(180deg,var(--cyan),rgba(6,214,245,0.3));box-shadow:0 0 10px rgba(6,214,245,0.4);}
.kblock.kp::before{background:linear-gradient(180deg,var(--pink),rgba(240,54,106,0.3));box-shadow:0 0 10px rgba(240,54,106,0.4);}
.kblock.kg::before{background:linear-gradient(180deg,var(--green),rgba(5,232,154,0.3));box-shadow:0 0 10px rgba(5,232,154,0.4);}
.kblock.ky::before{background:linear-gradient(180deg,var(--yellow),rgba(255,209,102,0.3));box-shadow:0 0 10px rgba(255,209,102,0.3);}
.kblock.kpu::before{background:linear-gradient(180deg,var(--purple),rgba(155,114,255,0.3));box-shadow:0 0 10px rgba(155,114,255,0.4);}

.klabel{font-family:'Exo 2',sans-serif;font-size:10px;font-weight:600;letter-spacing:0.14em;color:var(--sub);text-transform:uppercase;margin-bottom:4px;}
.kvalue{font-family:'Exo 2',sans-serif;font-size:28px;font-weight:900;line-height:1;letter-spacing:-0.02em;}
.kvalue.kc{color:var(--cyan);text-shadow:0 0 16px rgba(6,214,245,0.55);}
.kvalue.kp{color:var(--pink);text-shadow:0 0 16px rgba(240,54,106,0.55);}
.kvalue.kg{color:var(--green);text-shadow:0 0 16px rgba(5,232,154,0.55);}
.kvalue.ky{color:var(--yellow);text-shadow:0 0 12px rgba(255,209,102,0.45);}
.kvalue.kpu{color:var(--purple);text-shadow:0 0 14px rgba(155,114,255,0.5);}
.ksub{font-family:'Rajdhani',sans-serif;font-size:11px;color:var(--dim);margin-top:3px;letter-spacing:0.03em;}

/* Confusion matrix */
.cmat{display:grid;grid-template-columns:1fr 1fr;gap:4px;margin-top:6px;}
.cm{background:rgba(255,255,255,0.03);border:1px solid var(--border);border-radius:5px;padding:5px 4px;text-align:center;}
.cm-v{font-family:'Exo 2',sans-serif;font-size:15px;font-weight:800;line-height:1;}
.cm-l{font-size:9px;color:var(--dim);text-transform:uppercase;letter-spacing:0.06em;margin-top:2px;}

/* ── PIE PANEL ── */
.p-pie{grid-column:2;grid-row:1;}
.pie-wrap{display:flex;align-items:center;gap:20px;height:calc(100% - 28px);}
.pie-leg{display:flex;flex-direction:column;gap:10px;flex:1;}
.pie-item{padding:8px 10px;border-radius:6px;border:1px solid var(--border);}
.pie-item.pi-p{border-color:rgba(240,54,106,0.3);background:rgba(240,54,106,0.05);}
.pie-item.pi-g{border-color:rgba(5,232,154,0.3);background:rgba(5,232,154,0.05);}
.pi-pct{font-family:'Exo 2',sans-serif;font-size:26px;font-weight:900;line-height:1;}
.pi-p .pi-pct{color:var(--pink);text-shadow:0 0 14px rgba(240,54,106,0.5);}
.pi-g .pi-pct{color:var(--green);text-shadow:0 0 14px rgba(5,232,154,0.5);}
.pi-lbl{font-family:'Exo 2',sans-serif;font-size:10px;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;}
.pi-p .pi-lbl{color:rgba(240,54,106,0.8);}
.pi-g .pi-lbl{color:rgba(5,232,154,0.8);}
.pi-ct{font-size:11px;color:var(--dim);margin-top:1px;}
.pie-note{
  margin-top:6px;padding:7px 10px;
  background:rgba(6,214,245,0.05);
  border:1px solid rgba(6,214,245,0.15);
  border-radius:6px;font-size:11px;color:var(--sub);line-height:1.5;
}

/* ── SCATTER PANEL ── */
.p-scatter{grid-column:3;grid-row:1;}
.scatter-legend{display:flex;gap:16px;margin-top:6px;}
.sleg{display:flex;align-items:center;gap:5px;font-size:11px;color:var(--sub);}
.sleg-dot{width:9px;height:9px;border-radius:50%;}

/* ── FEATURE IMPORTANCE ── */
.p-feat{grid-column:4;grid-row:1/3;display:flex;flex-direction:column;}
.feat-list{display:flex;flex-direction:column;gap:7px;flex:1;justify-content:space-around;overflow:hidden;}
.feat-row{display:flex;flex-direction:column;gap:3px;}
.feat-meta{display:flex;justify-content:space-between;align-items:center;}
.feat-name{font-family:'Rajdhani',sans-serif;font-size:12px;font-weight:600;color:var(--text);letter-spacing:0.03em;}
.feat-pct{font-family:'Exo 2',sans-serif;font-size:11px;font-weight:800;}
.feat-track{height:6px;background:rgba(255,255,255,0.05);border-radius:3px;overflow:hidden;}
.feat-fill{height:100%;border-radius:3px;width:0;transition:width 2s cubic-bezier(0.16,1,0.3,1);}

/* ── PRIVATE PANEL ── */
.p-private{grid-column:2;grid-row:2;}

/* ── PROFILE PIC PANEL ── */
.p-profpic{grid-column:3;grid-row:2;}
.pp-list{display:flex;flex-direction:column;gap:8px;height:calc(100% - 28px);justify-content:center;}
.pp-row{display:flex;flex-direction:column;gap:4px;}
.pp-lbl{display:flex;justify-content:space-between;align-items:center;}
.pp-lname{font-size:12px;color:var(--sub);font-weight:600;}
.pp-val{font-family:'Exo 2',sans-serif;font-size:12px;font-weight:700;color:var(--text);}
.pp-track{height:9px;background:rgba(255,255,255,0.05);border-radius:5px;overflow:hidden;}
.pp-fill{height:100%;border-radius:5px;width:0;transition:width 1.5s cubic-bezier(0.16,1,0.3,1);}
.pp-stats{display:grid;grid-template-columns:1fr 1fr;gap:7px;margin-top:8px;}
.pp-stat{border-radius:7px;padding:8px 10px;text-align:center;border:1px solid;}
.pp-stat.ps-p{border-color:rgba(240,54,106,0.35);background:rgba(240,54,106,0.07);}
.pp-stat.ps-g{border-color:rgba(5,232,154,0.3);background:rgba(5,232,154,0.06);}
.pp-sv{font-family:'Exo 2',sans-serif;font-size:18px;font-weight:900;line-height:1;}
.ps-p .pp-sv{color:var(--pink);text-shadow:0 0 10px rgba(240,54,106,0.4);}
.ps-g .pp-sv{color:var(--green);text-shadow:0 0 10px rgba(5,232,154,0.4);}
.pp-sl{font-size:10px;color:var(--dim);text-transform:uppercase;letter-spacing:0.07em;margin-top:3px;}
.pp-insight{
  margin-top:6px;padding:7px 10px;
  background:rgba(240,54,106,0.05);
  border:1px solid rgba(240,54,106,0.2);
  border-radius:6px;font-size:11px;color:var(--sub);line-height:1.5;
}
.pp-insight span{color:var(--pink);font-weight:700;}

/* ── TOOLTIP ── */
#tt{
  position:fixed;z-index:9999;pointer-events:none;
  background:rgba(11,16,38,0.97);
  border:1px solid var(--border2);
  border-radius:7px;padding:7px 13px;
  font-family:'Rajdhani',sans-serif;font-size:13px;font-weight:600;
  color:var(--text);white-space:nowrap;
  box-shadow:0 4px 20px rgba(0,0,0,0.5);
  opacity:0;transition:opacity 0.15s;
}
#tt.on{opacity:1;}

/* Entrance animations */
@keyframes fadeSlideUp{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}
.panel{animation:fadeSlideUp 0.5s ease both;}
.p-kpi{animation-delay:0.05s;}
.p-pie{animation-delay:0.12s;}
.p-scatter{animation-delay:0.19s;}
.p-feat{animation-delay:0.26s;}
.p-private{animation-delay:0.33s;}
.p-profpic{animation-delay:0.4s;}
</style>
</head>
<body>

<div class="bg-mesh"></div>
<div class="grid-lines"></div>
<div class="ring"></div>
<div class="ring2"></div>
<div class="scanline"></div>

<div class="shell">

  <!-- HEADER -->
  <header>
    <div class="logo-block">
      <div class="logo-icon">📡</div>
      <div class="logo-text">INSTA<span>·</span>SCAN</div>
    </div>
    <div class="h-center">
      <div class="h-title">Fake Account Intelligence System</div>
      <div class="h-desc">Machine Learning · Decision Tree Classifier · Instagram Dataset 2019</div>
    </div>
    <div class="h-right">
      <div class="badge bg"><div class="badge-dot"></div>MODEL LIVE</div>
      <div class="badge bc"><div class="badge-dot"></div>696 ACCOUNTS</div>
      <div class="badge bp"><div class="badge-dot"></div>94.2% ACCURACY</div>
    </div>
  </header>

  <!-- MAIN GRID -->
  <div class="main">

    <!-- KPI COLUMN -->
    <div class="panel p-kpi">
      <div class="ptitle"><div class="ptitle-dot"></div>System Metrics</div>

      <div class="kblock kc">
        <div class="klabel">Total Accounts</div>
        <div class="kvalue kc" data-t="696">0</div>
        <div class="ksub">Train (576) + Test (120)</div>
      </div>
      <div class="kblock kp">
        <div class="klabel">Fake / Spam</div>
        <div class="kvalue kp" data-t="348">0</div>
        <div class="ksub">50.0% of full dataset</div>
      </div>
      <div class="kblock kg">
        <div class="klabel">Genuine</div>
        <div class="kvalue kg" data-t="348">0</div>
        <div class="ksub">50.0% of full dataset</div>
      </div>
      <div class="kblock ky">
        <div class="klabel">Model Accuracy</div>
        <div class="kvalue ky" style="font-size:22px;">94.2%</div>
        <div class="ksub">F1 Score: 0.94 · Precision: 0.95</div>
      </div>
      <div class="kblock kpu" style="flex:0.85;">
        <div class="klabel">Confusion Matrix</div>
        <div class="cmat">
          <div class="cm"><div class="cm-v" style="color:var(--green);">57</div><div class="cm-l">True Gen.</div></div>
          <div class="cm"><div class="cm-v" style="color:var(--pink);">3</div><div class="cm-l">False Fake</div></div>
          <div class="cm"><div class="cm-v" style="color:var(--yellow);">4</div><div class="cm-l">Missed</div></div>
          <div class="cm"><div class="cm-v" style="color:var(--green);">56</div><div class="cm-l">True Fake</div></div>
        </div>
      </div>
    </div>

    <!-- PIE CHART -->
    <div class="panel p-pie">
      <div class="ptitle"><div class="ptitle-dot"></div>Fake vs Genuine Distribution</div>
      <div class="pie-wrap">
        <canvas id="pieC" width="140" height="140" style="flex-shrink:0;"></canvas>
        <div class="pie-leg">
          <div class="pie-item pi-p">
            <div class="pi-pct">50%</div>
            <div class="pi-lbl">⬡ Fake / Spam</div>
            <div class="pi-ct">348 accounts detected</div>
          </div>
          <div class="pie-item pi-g">
            <div class="pi-pct">50%</div>
            <div class="pi-lbl">⬡ Genuine</div>
            <div class="pi-ct">348 accounts verified</div>
          </div>
          <div class="pie-note">Perfectly balanced dataset —<br>no class bias in training signal.</div>
        </div>
      </div>
    </div>

    <!-- SCATTER -->
    <div class="panel p-scatter">
      <div class="ptitle"><div class="ptitle-dot"></div>Followers Count vs Account Type</div>
      <canvas id="scatterC" style="width:100%;height:calc(100% - 50px);display:block;"></canvas>
      <div class="scatter-legend">
        <div class="sleg"><div class="sleg-dot" style="background:var(--green);box-shadow:0 0 5px var(--green);"></div>Genuine Account</div>
        <div class="sleg"><div class="sleg-dot" style="background:var(--pink);box-shadow:0 0 5px var(--pink);"></div>Fake Account</div>
        <div style="margin-left:auto;font-size:10px;color:var(--dim);">Hover dots to inspect</div>
      </div>
    </div>

    <!-- FEATURE IMPORTANCE -->
    <div class="panel p-feat">
      <div class="ptitle"><div class="ptitle-dot"></div>Feature Importance</div>
      <div class="feat-list" id="featList"></div>
    </div>

    <!-- PRIVATE BAR -->
    <div class="panel p-private">
      <div class="ptitle"><div class="ptitle-dot"></div>Private vs Public — Fake Distribution</div>
      <canvas id="privateC" style="width:100%;height:calc(100% - 34px);display:block;"></canvas>
    </div>

    <!-- PROFILE PIC -->
    <div class="panel p-profpic">
      <div class="ptitle"><div class="ptitle-dot"></div>Profile Picture Signal</div>
      <div class="pp-list">
        <div class="pp-row">
          <div class="pp-lbl"><span class="pp-lname">Has Pic · Genuine</span><span class="pp-val">346 / 99.4%</span></div>
          <div class="pp-track"><div class="pp-fill" style="background:linear-gradient(90deg,#05e89a,#00c97a);" data-w="99.4"></div></div>
        </div>
        <div class="pp-row">
          <div class="pp-lbl"><span class="pp-lname">Has Pic · Fake</span><span class="pp-val">149 / 42.8%</span></div>
          <div class="pp-track"><div class="pp-fill" style="background:linear-gradient(90deg,#f0366a,#ff7096);" data-w="42.8"></div></div>
        </div>
        <div class="pp-row">
          <div class="pp-lbl"><span class="pp-lname">No Pic · Fake</span><span class="pp-val">199 / 57.2%</span></div>
          <div class="pp-track"><div class="pp-fill" style="background:linear-gradient(90deg,#f0366a,#ff8c42);" data-w="57.2"></div></div>
        </div>
        <div class="pp-row">
          <div class="pp-lbl"><span class="pp-lname">No Pic · Genuine</span><span class="pp-val">2 / 0.6%</span></div>
          <div class="pp-track"><div class="pp-fill" style="background:var(--green);opacity:0.5;" data-w="0.6"></div></div>
        </div>
        <div class="pp-stats">
          <div class="pp-stat ps-p">
            <div class="pp-sv">57.2%</div>
            <div class="pp-sl">Fake · No Pic</div>
          </div>
          <div class="pp-stat ps-g">
            <div class="pp-sv">99.4%</div>
            <div class="pp-sl">Genuine · Has Pic</div>
          </div>
        </div>
        <div class="pp-insight"><span>KEY SIGNAL:</span> Absence of profile picture is a strong fake predictor.</div>
      </div>
    </div>

  </div><!-- end .main -->
</div><!-- end .shell -->

<div id="tt"></div>

<script>
// ── COUNT-UP ──
document.querySelectorAll('[data-t]').forEach((el,i)=>{
  const target=+el.dataset.t,dur=1400+i*200;
  let s=null;
  const step=ts=>{if(!s)s=ts;const p=Math.min((ts-s)/dur,1);const e=1-Math.pow(1-p,3);el.textContent=Math.floor(e*target);if(p<1)requestAnimationFrame(step);else el.textContent=target;};
  setTimeout(()=>requestAnimationFrame(step),200+i*100);
});

// ── PIE CHART ──
(function(){
  const c=document.getElementById('pieC'),ctx=c.getContext('2d');
  const cx=70,cy=70,ro=60,ri=36;
  const segs=[
    {a:Math.PI,color:'#f0366a',glow:'rgba(240,54,106,0.7)'},
    {a:Math.PI,color:'#05e89a',glow:'rgba(5,232,154,0.6)'},
  ];
  let angle=-Math.PI/2;
  const gap=0.04;
  segs.forEach(s=>{
    const ea=angle+s.a-gap;
    // Glow layer
    ctx.save();ctx.shadowColor=s.glow;ctx.shadowBlur=20;
    ctx.beginPath();ctx.moveTo(cx,cy);ctx.arc(cx,cy,ro,angle,ea);ctx.closePath();
    ctx.fillStyle=s.color;ctx.globalAlpha=0.9;ctx.fill();
    ctx.restore();ctx.globalAlpha=1;
    angle=ea+gap;
  });
  // Donut
  ctx.beginPath();ctx.arc(cx,cy,ri,0,Math.PI*2);
  const grad=ctx.createRadialGradient(cx,cy,0,cx,cy,ri);
  grad.addColorStop(0,'#0f1830');grad.addColorStop(1,'#0c1128');
  ctx.fillStyle=grad;ctx.fill();
  // Center ring
  ctx.beginPath();ctx.arc(cx,cy,ri,0,Math.PI*2);
  ctx.strokeStyle='rgba(6,214,245,0.2)';ctx.lineWidth=1.5;ctx.stroke();
  // Center text
  ctx.fillStyle='#06d6f5';ctx.font='bold 15px Exo 2,sans-serif';
  ctx.textAlign='center';ctx.textBaseline='middle';
  ctx.shadowColor='rgba(6,214,245,0.8)';ctx.shadowBlur=12;
  ctx.fillText('696',cx,cy-6);ctx.shadowBlur=0;
  ctx.fillStyle='#4a5f8a';ctx.font='9px Rajdhani,sans-serif';
  ctx.fillText('ACCOUNTS',cx,cy+8);
})();

// ── SCATTER ──
(function(){
  const canvas=document.getElementById('scatterC');
  const tt=document.getElementById('tt');
  function draw(){
    const W=canvas.offsetWidth,H=canvas.offsetHeight;
    if(!W||!H)return;
    canvas.width=W;canvas.height=H;
    const ctx=canvas.getContext('2d');
    const PL=46,PR=10,PT=8,PB=8;
    const pW=W-PL-PR,pH=H-PT-PB,maxF=8000;
    let seed=42;
    const rnd=()=>{seed=(seed*1664525+1013904223)%4294967296;return seed/4294967296;};
    const raw=[
      [1000,0],[2740,0],[159,0],[414,0],[800,0],[7000,0],[700,0],[1200,0],[5000,0],[950,0],
      [328,0],[4890,0],[225,0],[450,0],[1100,0],[670,0],[380,0],[2100,0],[990,0],[760,0],
      [310,0],[88,0],[540,0],[1890,0],[3200,0],[320,0],[710,0],[180,0],[930,0],[460,0],
      [280,0],[3800,0],[620,0],[1400,0],[790,0],[510,0],[2900,0],[660,0],[850,0],[1700,0],
      [1500,0],[560,0],[430,0],[2300,0],[370,0],[680,0],[1100,0],[840,0],[490,0],[2600,0],
      [10,1],[25,1],[8,1],[50,1],[15,1],[30,1],[12,1],[45,1],[20,1],[35,1],
      [5,1],[18,1],[60,1],[3,1],[22,1],[40,1],[7,1],[55,1],[28,1],[16,1],
      [1200,1],[900,1],[500,1],[300,1],[2500,1],[1800,1],[600,1],[400,1],[1500,1],[3000,1],
      [150,1],[200,1],[80,1],[350,1],[700,1],[1100,1],[450,1],[250,1],[650,1],[180,1],
      [75,1],[120,1],[550,1],[800,1],[1000,1],[420,1],[90,1],[280,1],[370,1],[130,1],
    ];
    // Grid lines
    for(let i=0;i<=4;i++){
      const x=PL+(i/4)*pW;
      ctx.strokeStyle='rgba(30,45,90,0.8)';ctx.lineWidth=1;
      ctx.beginPath();ctx.moveTo(x,PT);ctx.lineTo(x,PT+pH);ctx.stroke();
      ctx.fillStyle='#4a5f8a';ctx.font='10px Rajdhani,sans-serif';ctx.textAlign='center';
      ctx.fillText((i*2000).toLocaleString(),x,PT+pH+16);
    }
    // Separator
    ctx.strokeStyle='rgba(255,255,255,0.06)';ctx.lineWidth=1;ctx.setLineDash([4,6]);
    ctx.beginPath();ctx.moveTo(PL,PT+pH*0.47);ctx.lineTo(PL+pW,PT+pH*0.47);ctx.stroke();ctx.setLineDash([]);
    // Y labels
    ctx.textAlign='right';
    ctx.fillStyle='#05e89a';ctx.font='bold 11px Rajdhani,sans-serif';ctx.fillText('GENUINE',PL-5,PT+pH*0.22+4);
    ctx.fillStyle='#f0366a';ctx.fillText('FAKE',PL-5,PT+pH*0.72+4);
    // Dots
    const pts=[];
    raw.forEach(([f,fake])=>{
      const x=PL+(Math.min(f,maxF)/maxF)*pW;
      const by=fake===0?PT+pH*0.22:PT+pH*0.72;
      const y=by+(rnd()-0.5)*pH*0.28;
      pts.push({x,y,fake,f});
      // Glow
      ctx.beginPath();ctx.arc(x,y,7,0,Math.PI*2);
      ctx.fillStyle=fake===0?'rgba(5,232,154,0.06)':'rgba(240,54,106,0.06)';ctx.fill();
      // Dot
      ctx.beginPath();ctx.arc(x,y,4,0,Math.PI*2);
      ctx.fillStyle=fake===0?'rgba(5,232,154,0.75)':'rgba(240,54,106,0.75)';
      ctx.shadowColor=fake===0?'#05e89a':'#f0366a';ctx.shadowBlur=8;ctx.fill();ctx.shadowBlur=0;
      // Ring
      ctx.beginPath();ctx.arc(x,y,4,0,Math.PI*2);
      ctx.strokeStyle=fake===0?'rgba(5,232,154,0.9)':'rgba(240,54,106,0.9)';ctx.lineWidth=1;ctx.stroke();
    });
    canvas._pts=pts;canvas._W=W;canvas._H=H;
  }
  draw();window.addEventListener('resize',draw);
  canvas.addEventListener('mousemove',e=>{
    const r=canvas.getBoundingClientRect();
    const sx=canvas._W/r.width,sy=canvas._H/r.height;
    const mx=(e.clientX-r.left)*sx,my=(e.clientY-r.top)*sy;
    if(!canvas._pts)return;
    let near=null,minD=18;
    canvas._pts.forEach(p=>{const d=Math.hypot(p.x-mx,p.y-my);if(d<minD){minD=d;near=p;}});
    if(near){
      tt.innerHTML=`<span style="color:${near.fake?'#f0366a':'#05e89a'}">${near.fake?'● FAKE':'● GENUINE'}</span> &nbsp; Followers: <strong style="color:#f0f4ff">${near.f.toLocaleString()}</strong>`;
      tt.style.left=(e.clientX+14)+'px';tt.style.top=(e.clientY-12)+'px';tt.classList.add('on');
    } else tt.classList.remove('on');
  });
  canvas.addEventListener('mouseleave',()=>tt.classList.remove('on'));
})();

// ── FEATURE IMPORTANCE ──
(function(){
  const feats=[
    {n:'#followers',v:63.5,c:'#06d6f5'},{n:'profile pic',v:12.0,c:'#f0366a'},
    {n:'username nums',v:9.0,c:'#9b72ff'},{n:'bio length',v:7.0,c:'#05e89a'},
    {n:'#posts',v:5.5,c:'#ffd166'},{n:'#follows',v:4.0,c:'#06d6f5'},
    {n:'fullname words',v:1.5,c:'#ff9642'},{n:'private',v:1.5,c:'#9b72ff'},
    {n:'external URL',v:0.2,c:'#4a5f8a'},{n:'name==user',v:0.2,c:'#4a5f8a'},{n:'fullname nums',v:0.1,c:'#4a5f8a'},
  ];
  const cont=document.getElementById('featList');
  feats.forEach(f=>{
    const div=document.createElement('div');div.className='feat-row';
    div.innerHTML=`
      <div class="feat-meta">
        <span class="feat-name">${f.n}</span>
        <span class="feat-pct" style="color:${f.c};text-shadow:0 0 8px ${f.c};">${f.v}%</span>
      </div>
      <div class="feat-track">
        <div class="feat-fill" style="background:linear-gradient(90deg,${f.c},${f.c}22);" data-w="${(f.v/63.5)*100}"></div>
      </div>`;
    cont.appendChild(div);
  });
  setTimeout(()=>document.querySelectorAll('.feat-fill[data-w]').forEach(el=>el.style.width=el.dataset.w+'%'),500);
})();

// ── PRIVATE BAR CANVAS ──
(function(){
  const canvas=document.getElementById('privateC');
  function draw(){
    const W=canvas.offsetWidth,H=canvas.offsetHeight;
    if(!W||!H)return;
    canvas.width=W;canvas.height=H;
    const ctx=canvas.getContext('2d');
    const groups=[
      {label:'PUBLIC',fake:242,genuine:197,pct:'55.2% FAKE',xr:0.12},
      {label:'PRIVATE',fake:106,genuine:151,pct:'41.3% FAKE',xr:0.55},
    ];
    const maxV=260,bW=Math.max(Math.floor(W*0.11),32),bGap=6,baseY=H-22;

    // Grid lines
    for(let i=0;i<=3;i++){
      const y=baseY-(i/3)*(H-40);
      ctx.strokeStyle='rgba(30,45,90,0.5)';ctx.lineWidth=1;ctx.setLineDash([3,5]);
      ctx.beginPath();ctx.moveTo(0,y);ctx.lineTo(W,y);ctx.stroke();ctx.setLineDash([]);
      if(i>0){ctx.fillStyle='#4a5f8a';ctx.font='9px Rajdhani,sans-serif';ctx.textAlign='left';ctx.fillText(Math.round(i/3*maxV),2,y-2);}
    }

    groups.forEach(g=>{
      const bx=g.xr*W;
      // Fake bar
      const fH=(g.fake/maxV)*(H-40);
      const gr1=ctx.createLinearGradient(0,baseY-fH,0,baseY);
      gr1.addColorStop(0,'#f0366a');gr1.addColorStop(1,'rgba(240,54,106,0.15)');
      ctx.save();ctx.shadowColor='rgba(240,54,106,0.5)';ctx.shadowBlur=12;
      ctx.fillStyle=gr1;ctx.beginPath();ctx.roundRect(bx,baseY-fH,bW,fH,[4,4,0,0]);ctx.fill();ctx.restore();
      ctx.fillStyle='#f0f4ff';ctx.font='bold 11px Exo 2,sans-serif';ctx.textAlign='center';
      ctx.fillText(g.fake,bx+bW/2,baseY-fH-5);
      // Genuine bar
      const gH=(g.genuine/maxV)*(H-40);
      const gr2=ctx.createLinearGradient(0,baseY-gH,0,baseY);
      gr2.addColorStop(0,'#05e89a');gr2.addColorStop(1,'rgba(5,232,154,0.12)');
      ctx.save();ctx.shadowColor='rgba(5,232,154,0.45)';ctx.shadowBlur=12;
      ctx.fillStyle=gr2;ctx.beginPath();ctx.roundRect(bx+bW+bGap,baseY-gH,bW,gH,[4,4,0,0]);ctx.fill();ctx.restore();
      ctx.fillStyle='#f0f4ff';ctx.font='bold 11px Exo 2,sans-serif';ctx.textAlign='center';
      ctx.fillText(g.genuine,bx+bW+bGap+bW/2,baseY-gH-5);
      // Group label
      ctx.fillStyle='#9ab0d8';ctx.font='bold 11px Rajdhani,sans-serif';
      ctx.fillText(g.label,bx+bW+bGap/2,H-5);
      // Pct callout
      const callX=bx+bW*2+bGap+14,callY=baseY-Math.max(fH,gH)-22;
      ctx.fillStyle='rgba(240,54,106,0.08)';ctx.strokeStyle='rgba(240,54,106,0.25)';ctx.lineWidth=1;
      ctx.beginPath();ctx.roundRect(callX-2,callY-12,66,16,4);ctx.fill();ctx.stroke();
      ctx.fillStyle='#f0366a';ctx.font='bold 10px Exo 2,sans-serif';ctx.textAlign='left';ctx.fillText(g.pct,callX+2,callY);
    });
    // Legend
    ctx.fillStyle='#f0366a';ctx.fillRect(W-100,4,10,8);
    ctx.fillStyle='#9ab0d8';ctx.font='11px Rajdhani,sans-serif';ctx.textAlign='left';ctx.fillText('Fake',W-86,12);
    ctx.fillStyle='#05e89a';ctx.fillRect(W-50,4,10,8);
    ctx.fillStyle='#9ab0d8';ctx.fillText('Real',W-36,12);
  }
  draw();window.addEventListener('resize',draw);
})();

// ── PROFILE PIC BARS ──
setTimeout(()=>document.querySelectorAll('.pp-fill[data-w]').forEach(el=>el.style.width=el.dataset.w+'%'),400);
</script>
</body>
</html>
Uploading instagram_dashboard (3).html…]()

---
