<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>EPAZA — School Marks System</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700&family=Outfit:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0f1117;--s1:#181c27;--s2:#1f2436;--s3:#252b3d;
  --bd:#2e3550;--ink:#e8ecf5;--ink2:#9aa3bf;--ink3:#5a6380;
  --gold:#f0b429;--red:#e05252;--green:#3ecf8e;--blue:#4a8fff;--purple:#9f7aea;
}
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'Outfit',sans-serif;background:var(--bg);color:var(--ink);min-height:100vh;}
input,select,textarea,button{font-family:'Outfit',sans-serif;}
::-webkit-scrollbar{width:5px;height:5px;}
::-webkit-scrollbar-track{background:var(--bg);}
::-webkit-scrollbar-thumb{background:var(--bd);border-radius:3px;}
@keyframes slideUp{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:translateY(0)}}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}

/* ── LOGIN ── */
#loginWrap{
  min-height:100vh;display:flex;align-items:center;justify-content:center;
  background:radial-gradient(ellipse at 55% 40%,#1a1f35,#0f1117 70%);
}
.lbox{
  background:var(--s1);border:1px solid var(--bd);border-radius:16px;
  padding:2.4rem;width:100%;max-width:400px;
  box-shadow:0 24px 60px rgba(0,0,0,0.55);
  animation:slideUp .4s cubic-bezier(.16,1,.3,1);
}
.llogo{text-align:center;font-family:'Playfair Display',serif;font-size:2.1rem;letter-spacing:.02em;}
.llogo span{color:var(--gold);}
.lsub{text-align:center;font-size:.7rem;color:var(--ink3);letter-spacing:.1em;text-transform:uppercase;margin-top:4px;}
.lschool{text-align:center;font-size:.88rem;color:var(--ink2);margin-top:6px;min-height:1.2rem;}
.lerr{
  color:var(--red);font-size:.82rem;padding:8px 12px;
  background:rgba(224,82,82,.1);border:1px solid rgba(224,82,82,.2);
  border-radius:6px;margin:1rem 0 .5rem;display:none;
}
.lf{margin-top:1rem;}
.lf label{display:block;font-size:.7rem;font-weight:600;text-transform:uppercase;letter-spacing:.07em;color:var(--ink3);margin-bottom:5px;}
.lf input{
  width:100%;padding:10px 13px;background:var(--s2);border:1px solid var(--bd);
  border-radius:7px;color:var(--ink);font-size:.92rem;outline:none;transition:border .15s;
}
.lf input:focus{border-color:var(--gold);}
.lbtn{
  width:100%;margin-top:1.3rem;padding:11px;background:var(--gold);color:#1a1200;
  border:none;border-radius:8px;font-size:.95rem;font-weight:600;cursor:pointer;
  transition:filter .15s;
}
.lbtn:hover{filter:brightness(1.08);}
.lreset{
  display:block;text-align:center;margin-top:.9rem;
  background:none;border:none;color:var(--ink3);font-size:.73rem;
  cursor:pointer;text-decoration:underline;
}
.lf .pw-wrap{position:relative;}
.lf .pw-wrap input{padding-right:38px;}
.lf .pw-eye{
  position:absolute;right:10px;top:50%;transform:translateY(-50%);
  background:none;border:none;color:var(--ink3);cursor:pointer;
  font-size:.88rem;padding:2px;line-height:1;
}
.lf .pw-eye:hover{color:var(--ink);}
.tcls-tag{
  display:inline-flex;align-items:center;gap:4px;
  background:rgba(74,143,255,.12);color:var(--blue);
  border:1px solid rgba(74,143,255,.25);
  border-radius:10px;padding:2px 8px;font-size:.72rem;font-weight:500;
  margin:2px;
}
.teacher-avatar{
  width:32px;height:32px;border-radius:50%;
  background:linear-gradient(135deg,var(--blue),#2a5fcf);
  color:#fff;display:inline-flex;align-items:center;justify-content:center;
  font-size:.72rem;font-weight:700;flex-shrink:0;
}
.pw-wrap-modal{position:relative;}
.pw-wrap-modal input{padding-right:38px;}
.pw-wrap-modal .pw-eye-m{
  position:absolute;right:10px;top:50%;transform:translateY(-50%);
  background:none;border:none;color:var(--ink3);cursor:pointer;
  font-size:.88rem;padding:2px;line-height:1;
}
.pw-wrap-modal .pw-eye-m:hover{color:var(--ink);}

/* ── APP ── */
#appWrap{display:none;flex-direction:column;height:100vh;}

/* TOPBAR */
.topbar{
  height:54px;background:var(--s1);border-bottom:1px solid var(--bd);
  display:flex;align-items:center;justify-content:space-between;
  padding:0 1.4rem;position:sticky;top:0;z-index:100;flex-shrink:0;
}
.tlogo{font-family:'Playfair Display',serif;font-size:1.25rem;}
.tlogo span{color:var(--gold);}
.tschool{font-size:.66rem;color:var(--ink3);margin-top:1px;}
.tright{display:flex;align-items:center;gap:10px;}
.tsaving{font-size:.72rem;color:var(--ink3);}
.upill{
  display:flex;align-items:center;gap:8px;
  background:var(--s2);border:1px solid var(--bd);border-radius:20px;padding:4px 11px 4px 4px;
}
.uav{width:27px;height:27px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:.68rem;font-weight:700;}
.uav.admin{background:linear-gradient(135deg,var(--gold),#d09010);color:#1a1200;}
.uav.teacher{background:linear-gradient(135deg,var(--blue),#2a5fcf);color:#fff;}
.uname{font-size:.82rem;font-weight:500;}
.urole{font-size:.63rem;font-weight:700;text-transform:uppercase;letter-spacing:.06em;padding:2px 6px;border-radius:10px;}
.urole.admin{background:rgba(240,180,41,.15);color:var(--gold);}
.urole.teacher{background:rgba(74,143,255,.15);color:var(--blue);}
.tbtn{background:none;border:1px solid var(--bd);color:var(--ink3);padding:5px 11px;border-radius:6px;cursor:pointer;font-size:.77rem;transition:all .15s;}
.tbtn:hover{border-color:var(--red);color:var(--red);}

/* LAYOUT */
.layout{display:flex;flex:1;overflow:hidden;}

/* SIDEBAR */
.sidebar{width:215px;background:var(--s1);border-right:1px solid var(--bd);padding:1rem 0;overflow-y:auto;flex-shrink:0;}
.navgrp{font-size:.6rem;font-weight:700;text-transform:uppercase;letter-spacing:.1em;color:var(--ink3);padding:.75rem 1.1rem .25rem;}
.navbtn{
  display:flex;align-items:center;gap:9px;width:100%;padding:8px 1.1rem;
  background:none;border:none;border-left:3px solid transparent;
  color:var(--ink2);font-size:.85rem;cursor:pointer;text-align:left;transition:all .12s;
}
.navbtn:hover{background:var(--s2);color:var(--ink);}
.navbtn.active{background:var(--s2);color:var(--gold);border-left-color:var(--gold);font-weight:600;}
.navicon{width:17px;text-align:center;flex-shrink:0;}

/* MAIN */
.main{flex:1;overflow-y:auto;padding:1.6rem;background:var(--bg);}
.page{display:none;}
.page.on{display:block;animation:fadeIn .18s ease;}

/* PAGE HEADER */
.ph{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:1.4rem;padding-bottom:.9rem;border-bottom:1px solid var(--bd);}
.phtitle{font-family:'Playfair Display',serif;font-size:1.55rem;}
.phsub{font-size:.78rem;color:var(--ink3);margin-top:3px;}
.phact{display:flex;gap:7px;flex-wrap:wrap;}

/* STATS */
.sgrid{display:grid;grid-template-columns:repeat(4,1fr);gap:.9rem;margin-bottom:1.3rem;}
.scard{background:var(--s1);border:1px solid var(--bd);border-radius:10px;padding:1.1rem;position:relative;overflow:hidden;}
.scard::after{content:'';position:absolute;bottom:0;left:0;right:0;height:2px;}
.scard.gold::after{background:var(--gold);}
.scard.blue::after{background:var(--blue);}
.scard.green::after{background:var(--green);}
.scard.purple::after{background:var(--purple);}
.snum{font-size:1.9rem;font-weight:600;}
.slbl{font-size:.7rem;text-transform:uppercase;letter-spacing:.07em;color:var(--ink3);margin-top:2px;}

/* CARD */
.card{background:var(--s1);border:1px solid var(--bd);border-radius:10px;padding:1.3rem;margin-bottom:.9rem;}
.ctitle{font-size:.82rem;font-weight:600;color:var(--ink2);margin-bottom:.9rem;text-transform:uppercase;letter-spacing:.05em;}

/* BUTTONS */
.btn{display:inline-flex;align-items:center;gap:5px;padding:7px 14px;border-radius:7px;border:none;font-size:.83rem;font-weight:500;cursor:pointer;transition:all .13s;}
.btn.gold{background:var(--gold);color:#1a1200;}
.btn.gold:hover{filter:brightness(1.07);}
.btn.ghost{background:var(--s2);color:var(--ink2);border:1px solid var(--bd);}
.btn.ghost:hover{color:var(--ink);}
.btn.green{background:rgba(62,207,142,.14);color:var(--green);border:1px solid rgba(62,207,142,.3);}
.btn.red{background:rgba(224,82,82,.12);color:var(--red);border:1px solid rgba(224,82,82,.2);}
.btn.sm{padding:4px 9px;font-size:.74rem;}
.brow{display:flex;gap:7px;flex-wrap:wrap;}

/* FORMS */
.fg{display:flex;flex-direction:column;gap:4px;}
.fg label{font-size:.69rem;font-weight:600;text-transform:uppercase;letter-spacing:.07em;color:var(--ink3);}
.fg input,.fg select,.fg textarea{
  padding:8px 11px;background:var(--s2);border:1px solid var(--bd);
  border-radius:7px;color:var(--ink);font-size:.86rem;outline:none;transition:border .13s;width:100%;
}
.fg input:focus,.fg select:focus,.fg textarea:focus{border-color:var(--gold);}
.fg select option{background:var(--s2);}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:.9rem;}
.g3{display:grid;grid-template-columns:repeat(3,1fr);gap:.9rem;}
.g4{display:grid;grid-template-columns:repeat(4,1fr);gap:.9rem;}
.span2{grid-column:span 2;}

/* TABLE */
.tw{overflow-x:auto;}
table{width:100%;border-collapse:collapse;font-size:.85rem;}
thead tr{border-bottom:1px solid var(--bd);}
th{padding:9px 11px;text-align:left;font-size:.66rem;font-weight:700;text-transform:uppercase;letter-spacing:.08em;color:var(--ink3);}
td{padding:9px 11px;border-bottom:1px solid rgba(46,53,80,.45);vertical-align:middle;}
tr:hover td{background:var(--s2);}

/* MARK INPUTS */
.mkin{width:68px;padding:5px 7px;background:var(--s3);border:1px solid var(--bd);border-radius:5px;color:var(--ink);font-size:.86rem;text-align:center;outline:none;}
.mkin:focus{border-color:var(--gold);}
.mksel{width:84px;padding:5px 7px;background:var(--s3);border:1px solid var(--bd);border-radius:5px;color:var(--ink);font-size:.86rem;outline:none;}
.mksel:focus{border-color:var(--gold);}

/* GRADE BADGES */
.gb{display:inline-flex;align-items:center;justify-content:center;padding:2px 8px;border-radius:11px;font-size:.73rem;font-weight:600;}
.gb.A{background:rgba(62,207,142,.15);color:var(--green);}
.gb.B{background:rgba(74,143,255,.15);color:var(--blue);}
.gb.C{background:rgba(240,180,41,.15);color:var(--gold);}
.gb.D{background:rgba(159,122,234,.15);color:var(--purple);}
.gb.F{background:rgba(224,82,82,.15);color:var(--red);}
.gb.dash{color:var(--ink3);}
.pok{color:var(--green);font-size:.77rem;font-weight:600;}
.pfail{color:var(--red);font-size:.77rem;font-weight:600;}

/* ALERTS */
.al{padding:9px 13px;border-radius:7px;font-size:.81rem;margin-bottom:.9rem;display:flex;align-items:center;gap:8px;}
.al.ok{background:rgba(62,207,142,.1);color:var(--green);border:1px solid rgba(62,207,142,.25);}
.al.info{background:rgba(74,143,255,.1);color:var(--blue);border:1px solid rgba(74,143,255,.25);}
.al.warn{background:rgba(224,82,82,.1);color:var(--red);border:1px solid rgba(224,82,82,.25);}

/* MODAL */
.mbg{position:fixed;inset:0;background:rgba(0,0,0,.75);z-index:200;display:none;align-items:center;justify-content:center;backdrop-filter:blur(4px);}
.mbg.open{display:flex;}
.modal{background:var(--s1);border:1px solid var(--bd);border-radius:12px;padding:1.5rem;width:90%;max-width:500px;max-height:88vh;overflow-y:auto;animation:slideUp .22s cubic-bezier(.16,1,.3,1);}
.mhead{display:flex;justify-content:space-between;align-items:center;margin-bottom:1.1rem;}
.mtitle{font-family:'Playfair Display',serif;font-size:1.1rem;}
.mx{background:none;border:none;color:var(--ink3);font-size:1.1rem;cursor:pointer;padding:3px 7px;border-radius:4px;}
.mx:hover{background:var(--s2);}

/* SEARCH */
.srow{display:flex;gap:7px;margin-bottom:.9rem;}
.srow input,.srow select{padding:7px 11px;background:var(--s1);border:1px solid var(--bd);border-radius:7px;color:var(--ink);font-size:.84rem;outline:none;}
.srow input:focus,.srow select:focus{border-color:var(--gold);}
.srow input{flex:1;}

/* DROP ZONE */
.dzone{border:2px dashed var(--bd);border-radius:9px;padding:2.2rem;text-align:center;cursor:pointer;transition:all .18s;background:var(--s1);}
.dzone:hover,.dzone.drag{border-color:var(--gold);background:rgba(240,180,41,.04);}

/* PROCLAMATION */
.pcard{background:var(--s1);border:1px solid var(--bd);border-radius:10px;padding:1.1rem 1.4rem;margin-bottom:.6rem;display:flex;align-items:center;gap:1.1rem;transition:border-color .13s;}
.pcard:hover{border-color:var(--gold);}
.rcirc{width:44px;height:44px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:1.05rem;flex-shrink:0;}
.r1{background:linear-gradient(135deg,#FFD700,#d09010);color:#1a1200;box-shadow:0 4px 14px rgba(255,215,0,.3);}
.r2{background:linear-gradient(135deg,#C0C0C0,#888);color:#111;}
.r3{background:linear-gradient(135deg,#CD7F32,#9a5a20);color:#fff;}
.rn{background:var(--s3);color:var(--ink2);font-size:.84rem;}

/* REPORT */
.rpaper{background:#fff;color:#111;border-radius:10px;padding:2.2rem;max-width:660px;font-family:'Outfit',sans-serif;}
.rphd{text-align:center;border-bottom:2px solid #111;padding-bottom:.9rem;margin-bottom:1.3rem;}
.rpschool{font-family:'Playfair Display',serif;font-size:1.45rem;}
.rpsub{font-size:.83rem;color:#555;margin-top:3px;}
.rpinfo{display:flex;justify-content:space-between;font-size:.83rem;margin-bottom:1.1rem;background:#f5f5f0;padding:9px 13px;border-radius:6px;}
.rptbl{width:100%;border-collapse:collapse;font-size:.83rem;margin-bottom:.9rem;}
.rptbl th,.rptbl td{border:1px solid #ddd;padding:7px 9px;}
.rptbl th{background:#f0ede4;font-size:.7rem;text-transform:uppercase;letter-spacing:.05em;}
.rpsum{background:#f5f5f0;border-radius:6px;padding:9px 13px;font-size:.83rem;display:flex;justify-content:space-between;}
.rpsigs{display:flex;justify-content:space-between;font-size:.8rem;margin-top:1.3rem;padding-top:.9rem;border-top:1px solid #ddd;}

/* EMPTY */
.empty{text-align:center;padding:2.2rem;color:var(--ink3);}
.ei{font-size:2.3rem;margin-bottom:.5rem;}

/* TYPE BADGE */
.tbadge{font-size:.73rem;font-weight:600;padding:2px 8px;border-radius:11px;background:rgba(255,255,255,.07);}

@media print{
  #loginWrap,.topbar,.sidebar,.phact,.btn,.srow,.brow,.mbg,.noprint{display:none!important;}
  .layout{display:block;}
  .main{padding:0;}
  .page{display:block!important;}
}
</style>
<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
</head>
<body>

<!-- ══ LOGIN ══════════════════════════════════════ -->
<div id="loginWrap">
  <div class="lbox">
    <div class="llogo">E<span>PAZA</span></div>
    <div class="lsub">School Marks Management System</div>
    <div class="lschool" id="lschool"></div>
    <div class="lerr" id="lerr">❌ Invalid username or password.</div>
    <div class="lf"><label>Username</label><input type="text" id="luser" placeholder="Enter username" autocomplete="username"></div>
    <div class="lf"><label>Password</label><div class="pw-wrap"><input type="password" id="lpass" placeholder="Enter password" autocomplete="current-password"><button class="pw-eye" type="button" onclick="toggleLoginPw(this)" title="Show/hide password">👁</button></div></div>
    <button class="lbtn" id="loginBtn">Sign In →</button>
    <button class="lreset" id="resetBtn">Can't login? Reset to defaults</button>
  </div>
</div>

<!-- ══ APP ════════════════════════════════════════ -->
<div id="appWrap">

  <!-- TOPBAR -->
  <div class="topbar">
    <div>
      <div class="tlogo">E<span>PAZA</span></div>
      <div class="tschool" id="tschool"></div>
    </div>
    <div class="tright">
      <span class="tsaving" id="tsaving" style="display:none">💾 Saving…</span>
      <div class="upill">
        <div class="uav" id="uav"></div>
        <span class="uname" id="uname"></span>
        <span class="urole" id="urole"></span>
      </div>
      <button class="tbtn" id="logoutBtn">⏻ Sign Out</button>
    </div>
  </div>

  <div class="layout">
    <!-- SIDEBAR -->
    <div class="sidebar" id="sidebar"></div>

    <!-- MAIN -->
    <div class="main">

      <!-- DASHBOARD -->
      <div class="page" id="p-dashboard">
        <div class="ph"><div><div class="phtitle">Dashboard</div><div class="phsub" id="dwelcome"></div></div></div>
        <div class="sgrid">
          <div class="scard gold"><div class="snum" id="ds0">0</div><div class="slbl">Students</div></div>
          <div class="scard blue"><div class="snum" id="ds1">0</div><div class="slbl">Classes</div></div>
          <div class="scard green"><div class="snum" id="ds2">0</div><div class="slbl">Subjects</div></div>
          <div class="scard purple"><div class="snum" id="ds3">0</div><div class="slbl">Marks Recorded</div></div>
        </div>
        <div class="card"><div class="ctitle">Recent Activity</div><div id="dact"></div></div>
      </div>

      <!-- TEACHERS -->
      <div class="page" id="p-teachers">
        <div class="ph"><div><div class="phtitle">Teachers</div><div class="phsub">Manage staff accounts</div></div><div class="phact"><button class="btn gold" onclick="om('mt')">+ Add Teacher</button></div></div>
        <div class="card"><div class="tw"><table><thead><tr><th>#</th><th>Teacher</th><th>Password</th><th>⭐ Class Teacher Of</th><th>🏫 Assigned Classes</th><th>📚 Assigned Subjects</th><th>Action</th></tr></thead><tbody id="tbt"></tbody></table></div></div>
      </div>

      <!-- CLASSES -->
      <div class="page" id="p-classes">
        <div class="ph"><div><div class="phtitle">Classes</div><div class="phsub">Manage class groups</div></div><div class="phact" id="clsbtn"></div></div>
        <div class="card"><div class="tw"><table><thead><tr><th>#</th><th>Class Name</th><th>Students</th><th id="clsacth"></th></tr></thead><tbody id="tbc"></tbody></table></div></div>
      </div>

      <!-- TERMS -->
      <div class="page" id="p-terms">
        <div class="ph"><div><div class="phtitle">Terms &amp; Periods</div><div class="phsub">Manage assessment periods</div></div><div class="phact"><button class="btn gold" onclick="om('mterm')">+ Add Term</button></div></div>
        <div class="card"><div class="tw"><table><thead><tr><th>#</th><th>Name</th><th>Type</th><th>Active</th><th>Action</th></tr></thead><tbody id="tbterm"></tbody></table></div></div>
      </div>

      <!-- SUBJECTS -->
      <div class="page" id="p-subjects">
        <div class="ph"><div><div class="phtitle">Subjects</div><div class="phsub">Manage subjects &amp; grading scales</div></div><div class="phact" id="subjbtn"></div></div>
        <div class="card"><div class="tw"><table><thead><tr><th>#</th><th>Subject</th><th>Scale</th><th>Promotion Mark</th><th>Grade Thresholds</th><th id="subacth"></th></tr></thead><tbody id="tbs"></tbody></table></div></div>
      </div>

      <!-- STUDENTS -->
      <div class="page" id="p-students">
        <div class="ph"><div><div class="phtitle">Students</div><div class="phsub">Student roster</div></div><div class="phact" id="stbtn"></div></div>
        <div class="srow">
          <input type="text" id="stSearch" placeholder="Search by name or number…" oninput="renderStudents()">
          <select id="stCls" onchange="renderStudents()"><option value="">All Classes</option></select>
        </div>
        <div class="card"><div class="tw"><table><thead><tr><th>#</th><th>Name</th><th>No.</th><th>Class</th><th id="stacth"></th></tr></thead><tbody id="tbst"></tbody></table></div></div>
      </div>

      <!-- MARKS -->
      <div class="page" id="p-marks">
        <div class="ph"><div><div class="phtitle">Enter Marks</div><div class="phsub">Record student grades</div></div><div class="phact"><button class="btn green" onclick="saveAllMarks()">💾 Save Marks</button></div></div>
        <div class="card">
          <div class="g3" style="margin-bottom:1rem;">
            <div class="fg"><label>Class</label><select id="mkCls" onchange="loadMkTable()"><option value="">— Select Class —</option></select></div>
            <div class="fg"><label>Subject</label><select id="mkSub" onchange="loadMkTable()"><option value="">— Select Subject —</option></select></div>
            <div class="fg"><label>Term</label><select id="mkTerm" onchange="loadMkTable()"></select></div>
          </div>
          <div id="mkWrap"><div class="empty"><div class="ei">✏️</div><p>Select class and subject to enter marks.</p></div></div>
        </div>
      </div>

      <!-- IMPORT -->
      <div class="page" id="p-import">
        <div class="ph"><div><div class="phtitle">Import Students</div><div class="phsub">Upload CSV or paste data</div></div></div>
        <div class="card">
          <div class="al info">ℹ️ CSV format: <strong>Name, StudentNumber, ClassName</strong> — first row can be a header</div>
          <div class="dzone" id="dzone" onclick="document.getElementById('csvf').click()"
            ondragover="event.preventDefault();this.classList.add('drag')"
            ondragleave="this.classList.remove('drag')"
            ondrop="this.classList.remove('drag');event.preventDefault();handleDrop(event)">
            <div style="font-size:2rem;margin-bottom:.5rem;">📂</div>
            <div style="font-size:.86rem;color:var(--ink2);"><strong style="color:var(--gold);">Click to browse</strong> or drag &amp; drop a CSV file</div>
          </div>
          <input type="file" id="csvf" accept=".csv,.txt" style="display:none" onchange="handleFile(event)">
          <div id="impres" style="margin-top:.9rem;"></div>
        </div>
        <div class="card">
          <div class="ctitle">Paste CSV Data</div>
          <div class="fg" style="margin-bottom:.8rem;"><label>Paste here</label>
            <textarea id="csvpaste" rows="5" style="resize:vertical;font-family:monospace;font-size:.81rem;" placeholder="Name,Number,Class&#10;Alice Johnson,1,Grade 2A&#10;Bob Smith,2,Grade 2A"></textarea>
          </div>
          <button class="btn gold" onclick="importPaste()">Import</button>
        </div>
      </div>

      <!-- REPORTS -->
      <div class="page" id="p-reports">
        <div class="ph"><div><div class="phtitle">Report Cards</div><div class="phsub">Official Academic Bridge report card</div></div><div class="phact"><button class="btn ghost" onclick="window.print()">&#128438; Print</button></div></div>
        <div class="card noprint">
          <div class="g3">
            <div class="fg"><label>Student</label><select id="rpSt" onchange="genReport()"><option value="">&#8212; Select Student &#8212;</option></select></div>
            <div class="fg"><label>Term</label><select id="rpTerm" onchange="genReport()"></select></div>
            <div class="fg"><label>Class Teacher Remarks</label><input type="text" id="rpRemark" placeholder="e.g. Excellent effort this term&#8230;" oninput="genReport()"></div>
          </div>
        </div>
        <div id="rpOut"><div class="empty"><div class="ei">&#128196;</div><p>Select a student to preview their report card.</p></div></div>
      </div>

      <!-- ANALYTICS -->
      <div class="page" id="p-analytics">
        <div class="ph"><div><div class="phtitle">Performance Analytics</div><div class="phsub">Visual academic performance overview</div></div></div>
        <div class="card noprint" style="margin-bottom:1rem;">
          <div class="g3">
            <div class="fg"><label>Class</label><select id="anCls" onchange="renderAnalytics()"><option value="">All Classes</option></select></div>
            <div class="fg"><label>Term</label><select id="anTerm" onchange="renderAnalytics()"></select></div>
            <div class="fg"><label>Subject</label><select id="anSub" onchange="renderAnalytics()"><option value="">All Subjects</option></select></div>
          </div>
        </div>
        <div id="anOut"><div class="empty"><div class="ei">&#128202;</div><p>Select filters above to see analytics.</p></div></div>
      </div>

      <!-- PROCLAMATION -->
      <div class="page" id="p-proclamation">
        <div class="ph"><div><div class="phtitle">Proclamation List</div><div class="phsub">Honours &amp; student ranking</div></div><div class="phact"><button class="btn ghost" onclick="window.print()">🖨️ Print</button></div></div>
        <div class="card noprint">
          <div class="g2">
            <div class="fg"><label>Class</label><select id="prCls" onchange="genProcl()"><option value="">All Classes</option></select></div>
            <div class="fg"><label>Term</label><select id="prTerm" onchange="genProcl()"></select></div>
          </div>
        </div>
        <div id="prOut"><div class="empty"><div class="ei">🏆</div><p>Enter marks first to see rankings.</p></div></div>
      </div>

      <!-- SETTINGS -->
      <div class="page" id="p-settings">
        <div class="ph"><div><div class="phtitle">Settings</div><div class="phsub">Account &amp; system configuration</div></div></div>
        <div class="card" id="schoolCard">
          <div class="ctitle">School Information</div>
          <div id="schal"></div>
          <div class="fg" style="max-width:400px;margin-bottom:.9rem;"><label>School Name</label><input type="text" id="schin" placeholder="e.g. Greenfield Primary School"></div>
          <button class="btn gold" onclick="saveSchool()">Save School Name</button>
        </div>
        <div class="card" style="max-width:450px;">
          <div class="ctitle">Change My Password</div>
          <div id="pwal"></div>
          <div style="display:flex;flex-direction:column;gap:.75rem;margin-bottom:.9rem;">
            <div class="fg"><label>Current Password</label><input type="password" id="pwold"></div>
            <div class="fg"><label>New Password</label><input type="password" id="pwnew"></div>
            <div class="fg"><label>Confirm New Password</label><input type="password" id="pwcf"></div>
          </div>
          <button class="btn gold" onclick="changePw()">Update Password</button>
        </div>
        <div class="card" id="gradeCard">
          <div class="ctitle">Default Grade Thresholds (%)</div>
          <div style="font-size:.76rem;color:var(--ink3);margin-bottom:.7rem;">These are the global defaults. Each subject can override these in the Subjects page.</div>
          <div id="gral"></div>
          <div class="g4" style="margin-bottom:.6rem;">
            <div class="fg"><label>A — from %</label><input type="number" id="grA"></div>
            <div class="fg"><label>B — from %</label><input type="number" id="grB"></div>
            <div class="fg"><label>C — from %</label><input type="number" id="grC"></div>
            <div class="fg"><label>D — from %</label><input type="number" id="grD"></div>
          </div>
          <div style="font-size:.72rem;color:var(--ink3);margin-bottom:.8rem;">
            A = 80%+ &nbsp;|&nbsp; B = 70–79% &nbsp;|&nbsp; C = 60–69% &nbsp;|&nbsp; D = 50–59% &nbsp;|&nbsp; F = below 50%
          </div>
          <button class="btn gold" onclick="saveGrades()">Save</button>
        </div>
        <div class="card" id="dataCard">
          <div class="ctitle" style="color:var(--red);">⚠️ Data Management</div>
          <div class="brow">
            <button class="btn ghost" onclick="exportData()">📤 Export Backup</button>
            <button class="btn ghost" onclick="document.getElementById('bkf').click()">📥 Import Backup</button>
            <button class="btn red" onclick="clearAll()">🗑️ Clear All Data</button>
          </div>
          <input type="file" id="bkf" accept=".json" style="display:none" onchange="loadBackup(event)">
        </div>
      </div>

    </div><!-- /main -->
  </div><!-- /layout -->
</div><!-- /appWrap -->

<!-- ══ MODALS ══════════════════════════════════════ -->

<!-- Add Teacher -->
<div class="mbg" id="mt"><div class="modal">
  <div class="mhead"><div class="mtitle">➕ Add Teacher</div><button class="mx" onclick="cm('mt')">✕</button></div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg"><label>Full Name</label><input type="text" id="mtn" placeholder="Mrs. Johnson"></div>
    <div class="fg"><label>Username</label><input type="text" id="mtu" placeholder="johnson"></div>
    <div class="fg"><label>Password</label><div class="pw-wrap-modal"><input type="password" id="mtp" placeholder="••••••"><button class="pw-eye-m" type="button" onclick="togglePwField('mtp',this)">👁</button></div></div>
    <div class="fg"><label>⭐ Class Teacher Of <span style="color:var(--ink3);font-weight:400;">(reports & proclamation)</span></label><select id="mtct"><option value="">— None —</option></select></div>
    <div class="fg span2"><label>🏫 Assigned Classes <span style="color:var(--ink3);font-weight:400;">(can enter marks for)</span></label><select id="mtc" multiple style="height:90px;"></select></div>
    <div class="fg span2"><label>📚 Assigned Subjects <span style="color:var(--ink3);font-weight:400;">(subjects they teach)</span></label><select id="mts" multiple style="height:90px;"></select></div>
  </div>
  <div style="font-size:.72rem;color:var(--ink3);margin-bottom:.9rem;">Hold Ctrl/Cmd to select multiple items</div>
  <button class="btn gold" onclick="addTeacher()">Add Teacher</button>
</div></div>

<!-- Edit Teacher -->
<div class="mbg" id="met"><div class="modal">
  <div class="mhead"><div class="mtitle">✏️ Edit Teacher</div><button class="mx" onclick="cm('met')">✕</button></div>
  <input type="hidden" id="metid">
  <div style="margin-bottom:.8rem;padding:9px 12px;background:var(--s2);border-radius:7px;font-size:.86rem;color:var(--ink2);">Editing: <strong id="metname" style="color:var(--ink);"></strong></div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg"><label>Full Name</label><input type="text" id="metn" placeholder="Mrs. Johnson"></div>
    <div class="fg"><label>Username</label><input type="text" id="metu" placeholder="johnson"></div>
    <div class="fg"><label>New Password <span style="color:var(--ink3);font-weight:400;">(leave blank to keep)</span></label><div class="pw-wrap-modal"><input type="password" id="metp" placeholder="Leave blank to keep"><button class="pw-eye-m" type="button" onclick="togglePwField('metp',this)">👁</button></div></div>
    <div class="fg"><label>⭐ Class Teacher Of <span style="color:var(--ink3);font-weight:400;">(reports & proclamation)</span></label><select id="metct"><option value="">— None —</option></select></div>
    <div class="fg span2"><label>🏫 Assigned Classes <span style="color:var(--ink3);font-weight:400;">(can enter marks for)</span></label><select id="metc" multiple style="height:90px;"></select></div>
    <div class="fg span2"><label>📚 Assigned Subjects <span style="color:var(--ink3);font-weight:400;">(subjects they teach)</span></label><select id="mets" multiple style="height:90px;"></select></div>
  </div>
  <div style="font-size:.72rem;color:var(--ink3);margin-bottom:.9rem;">Hold Ctrl/Cmd to select multiple items</div>
  <button class="btn gold" onclick="saveEditTeacher()">Save Changes</button>
</div></div>

<!-- Add Class -->
<div class="mbg" id="mc"><div class="modal">
  <div class="mhead"><div class="mtitle">Add Class</div><button class="mx" onclick="cm('mc')">✕</button></div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg span2"><label>Class Name</label><input type="text" id="mcn" placeholder="e.g. Grade 3A"></div>
  </div>
  <button class="btn gold" onclick="addClass()">Add Class</button>
</div></div>

<!-- Edit Class -->
<div class="mbg" id="mec"><div class="modal">
  <div class="mhead"><div class="mtitle">✏️ Edit Class</div><button class="mx" onclick="cm('mec')">✕</button></div>
  <input type="hidden" id="mecid">
  <div style="margin-bottom:.8rem;padding:9px 12px;background:var(--s2);border-radius:7px;font-size:.86rem;color:var(--ink2);">Editing: <strong id="mecname" style="color:var(--ink);"></strong></div>
  <div class="fg" style="margin-bottom:.9rem;"><label>Class Name</label><input type="text" id="mecn" placeholder="e.g. Grade 3A"></div>
  <button class="btn gold" onclick="saveEditClass()">Save Changes</button>
</div></div>

<!-- Add Term -->
<div class="mbg" id="mterm"><div class="modal">
  <div class="mhead"><div class="mtitle">Add Term / Period</div><button class="mx" onclick="cm('mterm')">✕</button></div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg"><label>Term Name</label><input type="text" id="mtrn" placeholder="e.g. Mid Term, Period 1…"></div>
    <div class="fg"><label>Type</label><select id="mtrt">
      <option value="term">Term</option><option value="period">Period</option><option value="midterm">Mid Term</option>
      <option value="exam">Exam</option><option value="trimester">Trimester</option><option value="semester">Semester</option><option value="other">Other</option>
    </select></div>
  </div>
  <button class="btn gold" onclick="addTerm()">Add Term</button>
</div></div>

<!-- Edit Term -->
<div class="mbg" id="meterm"><div class="modal">
  <div class="mhead"><div class="mtitle">✏️ Edit Term</div><button class="mx" onclick="cm('meterm')">✕</button></div>
  <input type="hidden" id="metrmid">
  <div style="margin-bottom:.8rem;padding:9px 12px;background:var(--s2);border-radius:7px;font-size:.86rem;color:var(--ink2);">Editing: <strong id="metrmname" style="color:var(--ink);"></strong></div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg"><label>Term Name</label><input type="text" id="metrn" placeholder="e.g. Mid Term, Period 1…"></div>
    <div class="fg"><label>Type</label><select id="metrt">
      <option value="term">Term</option><option value="period">Period</option><option value="midterm">Mid Term</option>
      <option value="exam">Exam</option><option value="trimester">Trimester</option><option value="semester">Semester</option><option value="other">Other</option>
    </select></div>
  </div>
  <button class="btn gold" onclick="saveEditTerm()">Save Changes</button>
</div></div>

<!-- Add Subject -->
<div class="mbg" id="ms"><div class="modal" style="max-width:580px;">
  <div class="mhead"><div class="mtitle">Add Subject</div><button class="mx" onclick="cm('ms')">✕</button></div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg span2"><label>Subject Name</label><input type="text" id="msn" placeholder="e.g. Mathematics"></div>
    <div class="fg"><label>Grading Type</label><select id="mssc" onchange="toggleSubForm('ms')">
      <option value="number">Numeric (out of max mark)</option>
      <option value="letter">Letter (A/B/C/D/F)</option>
    </select></div>
    <div class="fg" id="ms-maxmark"><label>Max Mark</label><input type="number" id="msmax" value="100" min="1" placeholder="e.g. 100"></div>
    <div class="fg" id="ms-pass"><label>Promotion Mark</label><input type="number" id="msp" value="50" min="0" placeholder="e.g. 50"></div>
  </div>
  <div id="ms-grades" style="margin-bottom:.9rem;">
    <div class="ctitle" style="margin-bottom:.6rem;">Grade Thresholds (% of max mark)</div>
    <div class="g4">
      <div class="fg"><label>A — from %</label><input type="number" id="ms-grA" value="80" min="0" max="100"></div>
      <div class="fg"><label>B — from %</label><input type="number" id="ms-grB" value="70" min="0" max="100"></div>
      <div class="fg"><label>C — from %</label><input type="number" id="ms-grC" value="60" min="0" max="100"></div>
      <div class="fg"><label>D — from %</label><input type="number" id="ms-grD" value="50" min="0" max="100"></div>
    </div>
  </div>
  <button class="btn gold" onclick="addSubject()">Add Subject</button>
</div></div>

<!-- Edit Subject -->
<div class="mbg" id="mes"><div class="modal" style="max-width:580px;">
  <div class="mhead"><div class="mtitle">✏️ Edit Subject</div><button class="mx" onclick="cm('mes')">✕</button></div>
  <input type="hidden" id="mesid">
  <div style="margin-bottom:.8rem;padding:9px 12px;background:var(--s2);border-radius:7px;font-size:.86rem;color:var(--ink2);">Editing: <strong id="mesname" style="color:var(--ink);"></strong></div>
  <div class="al info" style="margin-bottom:.9rem;">ℹ️ Changes here affect how all existing marks are calculated and graded.</div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg span2"><label>Subject Name</label><input type="text" id="mesn" placeholder="e.g. Mathematics"></div>
    <div class="fg"><label>Grading Type</label><select id="messc" onchange="toggleSubForm('mes')">
      <option value="number">Numeric (out of max mark)</option>
      <option value="letter">Letter (A/B/C/D/F)</option>
    </select></div>
    <div class="fg" id="mes-maxmark"><label>Max Mark</label><input type="number" id="mesmax" value="100" min="1" placeholder="e.g. 100"></div>
    <div class="fg" id="mes-pass"><label>Promotion Mark</label><input type="number" id="mesp" value="50" min="0" placeholder="e.g. 50"></div>
  </div>
  <div id="mes-grades" style="margin-bottom:.9rem;">
    <div class="ctitle" style="margin-bottom:.6rem;">Grade Thresholds (% of max mark)</div>
    <div class="g4">
      <div class="fg"><label>A — from %</label><input type="number" id="mes-grA" min="0" max="100"></div>
      <div class="fg"><label>B — from %</label><input type="number" id="mes-grB" min="0" max="100"></div>
      <div class="fg"><label>C — from %</label><input type="number" id="mes-grC" min="0" max="100"></div>
      <div class="fg"><label>D — from %</label><input type="number" id="mes-grD" min="0" max="100"></div>
    </div>
  </div>
  <button class="btn gold" onclick="saveEditSubject()">Save Changes</button>
</div></div>

<!-- Add Student -->
<div class="mbg" id="mst"><div class="modal">
  <div class="mhead"><div class="mtitle">Add Student</div><button class="mx" onclick="cm('mst')">✕</button></div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg"><label>Full Name</label><input type="text" id="mstn" placeholder="e.g. Alice Johnson"></div>
    <div class="fg"><label>Student Number</label><input type="number" id="mstnum" placeholder="Auto if empty"></div>
    <div class="fg span2"><label>Class</label><select id="mstcls"><option value="">— Select Class —</option></select></div>
  </div>
  <button class="btn gold" onclick="addStudent()">Add Student</button>
</div></div>

<!-- Edit Student -->
<div class="mbg" id="mest"><div class="modal">
  <div class="mhead"><div class="mtitle">✏️ Edit Student</div><button class="mx" onclick="cm('mest')">✕</button></div>
  <input type="hidden" id="mestid">
  <div style="margin-bottom:.8rem;padding:9px 12px;background:var(--s2);border-radius:7px;font-size:.86rem;color:var(--ink2);">Editing: <strong id="mestname" style="color:var(--ink);"></strong></div>
  <div class="g2" style="margin-bottom:.9rem;">
    <div class="fg"><label>Full Name</label><input type="text" id="mestn" placeholder="e.g. Alice Johnson"></div>
    <div class="fg"><label>Student Number</label><input type="text" id="mestnum"></div>
    <div class="fg span2"><label>Class</label><select id="mestcls"><option value="">— Select Class —</option></select></div>
  </div>
  <button class="btn gold" onclick="saveEditStudent()">Save Changes</button>
</div></div>

<script>

// ===== SUPABASE CONNECTION =====
const SUPABASE_URL = "https://xtaakpqxbgkojqbygewc.supabase.co";
const SUPABASE_KEY = "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Inh0YWFrcHF4Ymdrb2pxYnlnZXdjIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NzMzODQ1ODMsImV4cCI6MjA4ODk2MDU4M30.sTAoFf3d4OLIAYY0UYH-BVCGOMdQpkx28Z2hYNIN8c0";

const supabaseClient = window.supabase.createClient(SUPABASE_URL, SUPABASE_KEY);

// Save whole DB to Supabase — ONLY if we have real data
async function supabaseSave(){
  // Safety check: never overwrite Supabase with empty data
  if(!DB.users || DB.users.length === 0) return;
  if(!DB.classes && !DB.subjects && !DB.students) return;
  try{
    await supabaseClient.from("epaza_data").upsert({
      id: "main",
      data: DB
    });
    console.log("Saved to Supabase");
  }catch(e){ console.error(e); }
}

// Load DB from Supabase — merges carefully, never loses data
async function supabaseLoad(){
  try{
    const { data } = await supabaseClient
      .from("epaza_data")
      .select("*")
      .eq("id","main")
      .single();

    if(data && data.data){
      var remote = data.data;
      // Only override each field if remote has MORE or EQUAL data
      if(Array.isArray(remote.users) && remote.users.length >= DB.users.length) DB.users = remote.users;
      if(Array.isArray(remote.teachers) && remote.teachers.length >= DB.teachers.length) DB.teachers = remote.teachers;
      if(Array.isArray(remote.classes) && remote.classes.length >= DB.classes.length) DB.classes = remote.classes;
      if(Array.isArray(remote.subjects) && remote.subjects.length >= DB.subjects.length) DB.subjects = remote.subjects;
      if(Array.isArray(remote.students) && remote.students.length >= DB.students.length) DB.students = remote.students;
      if(remote.marks && Object.keys(remote.marks).length >= Object.keys(DB.marks).length) DB.marks = remote.marks;
      if(remote.settings && typeof remote.settings==='object') DB.settings = Object.assign(DB.settings, remote.settings);
      if(Array.isArray(remote.activity) && remote.activity.length) DB.activity = remote.activity;
      if(Array.isArray(remote.terms) && remote.terms.length) DB.terms = remote.terms;
      console.log("Loaded from Supabase");
    }
  }catch(e){
    console.log("No remote data yet, using local.");
  }
}

// ═══════════════════════════════════════
//  DATA MODEL
// ═══════════════════════════════════════
var DB = {
  users:[{id:'admin',username:'admin',password:'admin123',role:'admin',name:'Administrator'}],
  teachers:[],classes:[],subjects:[],students:[],marks:{},
  settings:{grA:80,grB:70,grC:60,grD:50,schoolName:''},
  activity:[],
  terms:[
    {id:'T1',name:'Term 1',type:'term',active:true},
    {id:'T2',name:'Term 2',type:'term',active:true},
    {id:'T3',name:'Term 3',type:'term',active:true},
    {id:'Final',name:'Final Exam',type:'exam',active:true}
  ]
};
var ME = null;
var saveTimer = null;
var TCLR = {term:'var(--blue)',period:'var(--purple)',midterm:'var(--gold)',exam:'var(--red)',trimester:'var(--green)',semester:'var(--green)',other:'var(--ink3)'};
var TLBL = {term:'Term',period:'Period',midterm:'Mid Term',exam:'Exam',trimester:'Trimester',semester:'Semester',other:'Other'};

// ═══════════════════════════════════════
//  STORAGE
// ═══════════════════════════════════════
function dbSave(){
  clearTimeout(saveTimer);
  saveTimer = setTimeout(function(){
    document.getElementById('tsaving').style.display = 'inline';
    try{ localStorage.setItem('epaza_db', JSON.stringify(DB)); supabaseSave(); }catch(e){}
    setTimeout(function(){ document.getElementById('tsaving').style.display = 'none'; }, 700);
  }, 350);
}

// ═══════════════════════════════════════
//  AUTH
// ═══════════════════════════════════════
document.getElementById('loginBtn').addEventListener('click', doLogin);
document.getElementById('lpass').addEventListener('keydown', function(e){ if(e.key==='Enter') doLogin(); });
document.getElementById('logoutBtn').addEventListener('click', doLogout);
document.getElementById('resetBtn').addEventListener('click', function(){
  if(confirm('Clear all data and reset to defaults? This cannot be undone.')){
    localStorage.clear();
    location.reload();
  }
});

function doLogin(){
  var u = document.getElementById('luser').value.trim();
  var p = document.getElementById('lpass').value;
  var err = document.getElementById('lerr');
  if(!u || !p){ err.style.display='flex'; err.textContent='❌ Please enter username and password.'; return; }
  var user = null;
  for(var i=0;i<DB.users.length;i++){
    if(DB.users[i].username===u && DB.users[i].password===p){ user=DB.users[i]; break; }
  }
  if(!user){ err.style.display='flex'; err.textContent='❌ Invalid username or password.'; return; }
  err.style.display='none';
  ME = user;
  // Show app
  document.getElementById('loginWrap').style.display = 'none';
  document.getElementById('appWrap').style.display = 'flex';
  // Setup topbar
  var initials = ME.name.split(' ').map(function(w){return w[0]||'';}).join('').slice(0,2).toUpperCase();
  var av = document.getElementById('uav');
  av.textContent = initials;
  av.className = 'uav ' + (ME.role==='admin'?'admin':'teacher');
  document.getElementById('uname').textContent = ME.name;
  var rt = document.getElementById('urole');
  rt.textContent = ME.role==='admin'?'Admin':'Teacher';
  rt.className = 'urole ' + (ME.role==='admin'?'admin':'teacher');
  applySchool();
  buildSidebar();
  showPage('dashboard');
  addLog('Signed in: '+ME.name);
  dbSave();
}

function doLogout(){
  ME = null;
  document.getElementById('appWrap').style.display = 'none';
  document.getElementById('loginWrap').style.display = 'flex';
  document.getElementById('luser').value = '';
  document.getElementById('lpass').value = '';
}

function isAdmin(){ return ME && ME.role==='admin'; }
function myClasses(){
  if(isAdmin()) return DB.classes;
  // Teacher only sees their assigned classes
  if(!ME.classes||!ME.classes.length) return [];
  return DB.classes.filter(function(c){ return ME.classes.indexOf(c.id)>=0; });
}
function activeTerms(){ return DB.terms.filter(function(t){ return t.active; }); }
function termLabel(id){
  for(var i=0;i<DB.terms.length;i++) if(DB.terms[i].id===id) return DB.terms[i].name;
  return id;
}
function addLog(txt){
  var t = new Date().toLocaleTimeString('en-GB',{hour:'2-digit',minute:'2-digit'});
  DB.activity.push({text:txt,time:t});
  if(DB.activity.length>60) DB.activity=DB.activity.slice(-60);
}

// ═══════════════════════════════════════
//  SIDEBAR / NAVIGATION
// ═══════════════════════════════════════
function buildSidebar(){
  var admin = isAdmin();
  var html = '';
  function grp(label,items){
    html += '<div class="navgrp">'+label+'</div>';
    items.forEach(function(it){
      html += '<button class="navbtn" id="nb-'+it.id+'" onclick="showPage(\''+it.id+'\')"><span class="navicon">'+it.icon+'</span>'+it.label+'</button>';
    });
  }
  grp('Overview',[{id:'dashboard',icon:'📊',label:'Dashboard'}]);
  if(admin){
    grp('Setup',[
      {id:'teachers',icon:'👩‍🏫',label:'Teachers'},
      {id:'classes',icon:'🏫',label:'Classes'},
      {id:'terms',icon:'📅',label:'Terms & Periods'},
      {id:'subjects',icon:'📚',label:'Subjects'},
      {id:'students',icon:'👨‍🎓',label:'Students'},
    ]);
  } else {
    grp('My Classes',[{id:'students',icon:'👨‍🎓',label:'Students'}]);
  }
  grp('Marking',admin?[{id:'marks',icon:'✏️',label:'Enter Marks'},{id:'import',icon:'📥',label:'Import Data'}]:[{id:'marks',icon:'✏️',label:'Enter Marks'}]);
  grp('Output',[{id:'reports',icon:'📄',label:'Report Cards'},{id:'analytics',icon:'📊',label:'Analytics'},{id:'proclamation',icon:'🏆',label:'Proclamation'}]);
  grp('Account',[{id:'settings',icon:'⚙️',label:'Settings'}]);
  document.getElementById('sidebar').innerHTML = html;
}
function showPage(id){
  document.querySelectorAll('.page').forEach(function(p){ p.classList.remove('on'); });
  document.querySelectorAll('.navbtn').forEach(function(b){ b.classList.remove('active'); });
  var pg = document.getElementById('p-'+id);
  if(pg) pg.classList.add('on');
  var nb = document.getElementById('nb-'+id);
  if(nb) nb.classList.add('active');
  var fns = {
    dashboard:renderDash, teachers:renderTeachers, classes:renderClasses,
    terms:renderTerms, subjects:renderSubjects, students:setupStudents,
    marks:setupMarks, import:function(){}, reports:setupReports,
    analytics:setupAnalytics,
    proclamation:setupProcl, settings:setupSettings
  };
  if(fns[id]) fns[id]();
}
function applySchool(){
  var n = (DB.settings&&DB.settings.schoolName)||'';
  document.getElementById('tschool').textContent = n;
  document.getElementById('lschool').textContent = n;
}

// ═══════════════════════════════════════
//  MODAL HELPERS
// ═══════════════════════════════════════
function om(id){
  if(id==='mt'){
    var clsOpts=DB.classes.map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');
    var subOpts=DB.subjects.map(function(s){return'<option value="'+s.id+'">'+s.name+'</option>';}).join('');
    document.getElementById('mtc').innerHTML=clsOpts;
    document.getElementById('mtct').innerHTML='<option value="">— None —</option>'+clsOpts;
    document.getElementById('mts').innerHTML=subOpts;
  }
  if(id==='mst') document.getElementById('mstcls').innerHTML = '<option value="">— Select Class —</option>'+DB.classes.map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');
  document.getElementById(id).classList.add('open');
}
function cm(id){ document.getElementById(id).classList.remove('open'); }
document.querySelectorAll('.mbg').forEach(function(m){
  m.addEventListener('click',function(e){ if(e.target===m) m.classList.remove('open'); });
});
function flash(id,type,msg){
  var el=document.getElementById(id);
  el.innerHTML='<div class="al '+type+'">'+msg+'</div>';
  setTimeout(function(){ el.innerHTML=''; },3000);
}

// ═══════════════════════════════════════
//  DASHBOARD
// ═══════════════════════════════════════
function renderDash(){
  document.getElementById('dwelcome').textContent = 'Welcome back, '+ME.name;
  document.getElementById('ds0').textContent = DB.students.length;
  document.getElementById('ds1').textContent = DB.classes.length;
  document.getElementById('ds2').textContent = DB.subjects.length;
  document.getElementById('ds3').textContent = Object.keys(DB.marks).length;
  var el = document.getElementById('dact');
  if(!DB.activity.length){
    el.innerHTML='<div class="empty"><div class="ei">📋</div><p>No activity yet.</p></div>';return;
  }
  el.innerHTML = DB.activity.slice(-8).reverse().map(function(a){
    return'<div style="display:flex;gap:10px;align-items:center;padding:8px 0;border-bottom:1px solid var(--bd);"><span style="font-family:monospace;font-size:.7rem;color:var(--ink3);white-space:nowrap;">'+a.time+'</span><span style="font-size:.84rem;">'+a.text+'</span></div>';
  }).join('');
}

// ═══════════════════════════════════════
//  TEACHERS
// ═══════════════════════════════════════
function mySubjects(){
  if(isAdmin()) return DB.subjects;
  if(!ME.subjects||!ME.subjects.length) return DB.subjects; // if no restriction, see all
  return DB.subjects.filter(function(s){ return ME.subjects.indexOf(s.id)>=0; });
}
function addTeacher(){
  var name=document.getElementById('mtn').value.trim();
  var uname=document.getElementById('mtu').value.trim();
  var pass=document.getElementById('mtp').value;
  if(!name||!uname||!pass){alert('Fill all fields.');return;}
  for(var i=0;i<DB.users.length;i++) if(DB.users[i].username===uname){alert('Username already exists.');return;}
  var id='T'+Date.now();
  var clsEl=document.getElementById('mtc');
  var subEl=document.getElementById('mts');
  var cls=Array.from(clsEl.selectedOptions).map(function(o){return o.value;});
  var subs=Array.from(subEl.selectedOptions).map(function(o){return o.value;});
  var classTeacher=document.getElementById('mtct').value;
  DB.users.push({id:id,username:uname,password:pass,role:'teacher',name:name,classes:cls,subjects:subs,classTeacher:classTeacher});
  DB.teachers.push({id:id,name:name,username:uname,classes:cls,subjects:subs,classTeacher:classTeacher});
  addLog('Added teacher: '+name); dbSave(); renderTeachers(); cm('mt');
  document.getElementById('mtn').value='';document.getElementById('mtu').value='';document.getElementById('mtp').value='';
  document.getElementById('mtct').value='';
  Array.from(clsEl.options).forEach(function(o){o.selected=false;});
  Array.from(subEl.options).forEach(function(o){o.selected=false;});
}
function openEditTeacher(id){
  var t=DB.teachers.find(function(x){return x.id===id;});if(!t)return;
  document.getElementById('metid').value=id;
  document.getElementById('metname').textContent=t.name;
  document.getElementById('metn').value=t.name;
  document.getElementById('metu').value=t.username;
  document.getElementById('metp').value='';
  var ctOpts='<option value="">— None —</option>'+DB.classes.map(function(c){return'<option value="'+c.id+'"'+(t.classTeacher===c.id?' selected':'')+'>'+c.name+'</option>';}).join('');
  document.getElementById('metct').innerHTML=ctOpts;
  var clsOpts=DB.classes.map(function(c){
    var sel=(t.classes&&t.classes.indexOf(c.id)>=0)?'selected':'';
    return'<option value="'+c.id+'" '+sel+'>'+c.name+'</option>';
  }).join('');
  document.getElementById('metc').innerHTML=clsOpts;
  var subOpts=DB.subjects.map(function(s){
    var sel=(t.subjects&&t.subjects.indexOf(s.id)>=0)?'selected':'';
    return'<option value="'+s.id+'" '+sel+'>'+s.name+'</option>';
  }).join('');
  document.getElementById('mets').innerHTML=subOpts;
  document.getElementById('met').classList.add('open');
}
function saveEditTeacher(){
  var id=document.getElementById('metid').value;
  var t=DB.teachers.find(function(x){return x.id===id;});if(!t)return;
  var u=DB.users.find(function(x){return x.id===id;});
  var name=document.getElementById('metn').value.trim();
  var uname=document.getElementById('metu').value.trim();
  var pass=document.getElementById('metp').value;
  if(!name||!uname){alert('Name and username are required.');return;}
  for(var i=0;i<DB.users.length;i++) if(DB.users[i].username===uname&&DB.users[i].id!==id){alert('Username already taken.');return;}
  var cls=Array.from(document.getElementById('metc').selectedOptions).map(function(o){return o.value;});
  var subs=Array.from(document.getElementById('mets').selectedOptions).map(function(o){return o.value;});
  var classTeacher=document.getElementById('metct').value;
  t.name=name;t.username=uname;t.classes=cls;t.subjects=subs;t.classTeacher=classTeacher;
  if(u){u.name=name;u.username=uname;u.classes=cls;u.subjects=subs;u.classTeacher=classTeacher;if(pass)u.password=pass;}
  addLog('Updated teacher: '+name);dbSave();renderTeachers();cm('met');
  if(ME&&ME.id===id){
    ME.name=name;ME.username=uname;ME.classes=cls;ME.subjects=subs;ME.classTeacher=classTeacher;
    if(pass)ME.password=pass;
    document.getElementById('uname').textContent=name;
  }
}
function renderTeachers(){
  var tb=document.getElementById('tbt');
  if(!DB.teachers.length){tb.innerHTML='<tr><td colspan="7"><div class="empty"><p>No teachers yet.</p></div></td></tr>';return;}
  tb.innerHTML=DB.teachers.map(function(t,i){
    var initials=t.name.split(' ').map(function(w){return w[0]||'';}).join('').slice(0,2).toUpperCase();
    var assignedClasses=t.classes&&t.classes.length
      ?t.classes.map(function(cid){var c=DB.classes.find(function(x){return x.id===cid;});return c||null;}).filter(Boolean):[];
    var clsList=assignedClasses.length
      ?assignedClasses.map(function(c){return'<span class="tcls-tag">🏫 '+c.name+'</span>';}).join('')
      :'<span style="color:var(--ink3);font-size:.78rem;">None</span>';
    var assignedSubs=t.subjects&&t.subjects.length
      ?t.subjects.map(function(sid){var s=DB.subjects.find(function(x){return x.id===sid;});return s?'<span class="tcls-tag" style="background:rgba(62,207,142,.1);color:var(--green);border-color:rgba(62,207,142,.25);">📚 '+s.name+'</span>':'';}).join('')
      :'<span style="color:var(--ink3);font-size:.78rem;">All subjects</span>';
    var ctCls=t.classTeacher?DB.classes.find(function(c){return c.id===t.classTeacher;}):null;
    var ctBadge=ctCls
      ?'<span style="background:rgba(240,180,41,.15);color:var(--gold);border:1px solid rgba(240,180,41,.3);border-radius:10px;padding:2px 9px;font-size:.74rem;font-weight:600;">⭐ '+ctCls.name+'</span>'
      :'<span style="color:var(--ink3);font-size:.78rem;">—</span>';
    var studentCount=assignedClasses.reduce(function(sum,c){return sum+DB.students.filter(function(s){return s.classId===c.id;}).length;},0);
    var userRec=DB.users.find(function(u){return u.id===t.id;});
    var pwDisplay=userRec?userRec.password:'—';
    return'<tr>'
      +'<td>'+(i+1)+'</td>'
      +'<td><div style="display:flex;align-items:center;gap:9px;"><div class="teacher-avatar">'+initials+'</div><div><div style="font-weight:600;">'+t.name+'</div><div style="font-size:.7rem;color:var(--ink3);">'+t.username+'</div></div></div></td>'
      +'<td><div style="display:flex;align-items:center;gap:6px;">'
        +'<span id="pw-mask-'+t.id+'" style="font-family:monospace;font-size:.81rem;letter-spacing:.1em;">••••••</span>'
        +'<span id="pw-val-'+t.id+'" style="font-family:monospace;font-size:.81rem;display:none;">'+pwDisplay+'</span>'
        +'<button class="btn sm ghost" style="padding:2px 7px;font-size:.68rem;" onclick="toggleTeacherPw(\''+t.id+'\',this)">Show</button>'
      +'</div></td>'
      +'<td>'+ctBadge+'</td>'
      +'<td><div style="display:flex;flex-wrap:wrap;gap:3px;">'+clsList+'</div></td>'
      +'<td><div style="display:flex;flex-wrap:wrap;gap:3px;">'+assignedSubs+'</div></td>'
      +'<td><div class="brow"><button class="btn sm ghost" onclick="openEditTeacher(\''+t.id+'\')">✏️ Edit</button><button class="btn sm red" onclick="delTeacher(\''+t.id+'\')">Remove</button></div></td>'
      +'</tr>';
  }).join('');
}
function toggleTeacherPw(tid,btn){
  var mask=document.getElementById('pw-mask-'+tid);
  var val=document.getElementById('pw-val-'+tid);
  if(val.style.display==='none'){val.style.display='inline';mask.style.display='none';btn.textContent='Hide';}
  else{val.style.display='none';mask.style.display='inline';btn.textContent='Show';}
}
function delTeacher(id){
  if(!confirm('Remove this teacher?'))return;
  DB.teachers=DB.teachers.filter(function(t){return t.id!==id;});
  DB.users=DB.users.filter(function(u){return u.id!==id;});
  dbSave();renderTeachers();
}

// ═══════════════════════════════════════
//  CLASSES
// ═══════════════════════════════════════
function renderClasses(){
  var admin=isAdmin();
  document.getElementById('clsbtn').innerHTML=admin?'<button class="btn gold" onclick="om(\'mc\')">+ Add Class</button>':'';
  document.getElementById('clsacth').textContent=admin?'Action':'';
  var tb=document.getElementById('tbc');
  var list=myClasses();
  if(!list.length){tb.innerHTML='<tr><td colspan="4"><div class="empty"><p>No classes yet.</p></div></td></tr>';return;}
  tb.innerHTML=list.map(function(c,i){
    var cnt=DB.students.filter(function(s){return s.classId===c.id;}).length;
    return'<tr><td>'+(i+1)+'</td><td><strong>'+c.name+'</strong></td><td>'+cnt+'</td><td>'+(admin?'<div class="brow"><button class="btn sm ghost" onclick="openEditClass(\''+c.id+'\')">✏️ Edit</button><button class="btn sm red" onclick="delClass(\''+c.id+'\')">Delete</button></div>':'—')+'</td></tr>';
  }).join('');
}
function openEditClass(id){
  var c=DB.classes.find(function(x){return x.id===id;});if(!c)return;
  document.getElementById('mecid').value=id;
  document.getElementById('mecname').textContent=c.name;
  document.getElementById('mecn').value=c.name;
  document.getElementById('mec').classList.add('open');
}
function saveEditClass(){
  var id=document.getElementById('mecid').value;
  var c=DB.classes.find(function(x){return x.id===id;});if(!c)return;
  var name=document.getElementById('mecn').value.trim();
  if(!name){alert('Enter a class name.');return;}
  c.name=name;
  addLog('Updated class: '+name);dbSave();renderClasses();syncAll();syncClassSelects();cm('mec');
}
function addClass(){
  var name=document.getElementById('mcn').value.trim();
  if(!name){alert('Enter a class name.');return;}
  DB.classes.push({id:'C'+Date.now(),name:name});
  addLog('Added class: '+name);dbSave();renderClasses();syncAll();syncClassSelects();cm('mc');
  document.getElementById('mcn').value='';
}
function delClass(id){
  if(!confirm('Delete class?'))return;
  DB.classes=DB.classes.filter(function(c){return c.id!==id;});
  dbSave();renderClasses();syncAll();syncClassSelects();
}
// Sync all class selects across the app (marks, teacher modals, student modals, reports)
function syncClassSelects(){
  // Teacher add/edit modals class lists
  var teacherClassOpts=DB.classes.map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');
  var mtcEl=document.getElementById('mtc');if(mtcEl)mtcEl.innerHTML=teacherClassOpts;
  var metcEl=document.getElementById('metc');if(metcEl)metcEl.innerHTML=teacherClassOpts;
  // Student class select in marks page
  var mkCls=document.getElementById('mkCls');
  if(mkCls){mkCls.innerHTML='<option value="">— Select Class —</option>'+myClasses().map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');}
  // Proclamation class filter
  var prCls=document.getElementById('prCls');
  if(prCls){var pv=prCls.value;prCls.innerHTML='<option value="">All Classes</option>'+DB.classes.map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');prCls.value=pv;}
}

// ═══════════════════════════════════════
//  TERMS
// ═══════════════════════════════════════
function renderTerms(){
  var tb=document.getElementById('tbterm');
  if(!DB.terms.length){tb.innerHTML='<tr><td colspan="5"><div class="empty"><p>No terms yet.</p></div></td></tr>';return;}
  tb.innerHTML=DB.terms.map(function(t,i){
    return'<tr><td>'+(i+1)+'</td><td><strong>'+t.name+'</strong></td>'
    +'<td><span class="tbadge" style="color:'+(TCLR[t.type]||'var(--ink2)')+';">'+(TLBL[t.type]||t.type)+'</span></td>'
    +'<td><label style="display:flex;align-items:center;gap:7px;cursor:pointer;"><input type="checkbox" '+(t.active?'checked':'')
    +' onchange="toggleTerm(\''+t.id+'\')" style="accent-color:var(--gold);width:15px;height:15px;"><span style="font-size:.81rem;color:'+(t.active?'var(--green)':'var(--ink3)')+';">'+(t.active?'Active':'Hidden')+'</span></label></td>'
    +'<td><div class="brow"><button class="btn sm ghost" onclick="openEditTerm(\''+t.id+'\')">✏️ Edit</button><button class="btn sm red" onclick="delTerm(\''+t.id+'\')">Delete</button></div></td></tr>';
  }).join('');
}
function openEditTerm(id){
  var t=DB.terms.find(function(x){return x.id===id;});if(!t)return;
  document.getElementById('metrmid').value=id;
  document.getElementById('metrmname').textContent=t.name;
  document.getElementById('metrn').value=t.name;
  document.getElementById('metrt').value=t.type;
  document.getElementById('meterm').classList.add('open');
}
function saveEditTerm(){
  var id=document.getElementById('metrmid').value;
  var t=DB.terms.find(function(x){return x.id===id;});if(!t)return;
  var name=document.getElementById('metrn').value.trim();
  if(!name){alert('Enter a term name.');return;}
  t.name=name;t.type=document.getElementById('metrt').value;
  addLog('Updated term: '+name);dbSave();renderTerms();syncTerms();cm('meterm');
}
function addTerm(){
  var name=document.getElementById('mtrn').value.trim();
  if(!name){alert('Enter a term name.');return;}
  for(var i=0;i<DB.terms.length;i++) if(DB.terms[i].name.toLowerCase()===name.toLowerCase()){alert('Term already exists.');return;}
  DB.terms.push({id:'TR'+Date.now(),name:name,type:document.getElementById('mtrt').value,active:true});
  addLog('Added term: '+name);dbSave();renderTerms();syncTerms();cm('mterm');
  document.getElementById('mtrn').value='';
}
function toggleTerm(id){
  for(var i=0;i<DB.terms.length;i++) if(DB.terms[i].id===id){DB.terms[i].active=!DB.terms[i].active;break;}
  dbSave();renderTerms();syncTerms();
}
function delTerm(id){
  if(!confirm('Delete this term?'))return;
  DB.terms=DB.terms.filter(function(t){return t.id!==id;});
  dbSave();renderTerms();syncTerms();
}

// ═══════════════════════════════════════
//  SUBJECTS
// ═══════════════════════════════════════
function toggleSubForm(prefix){
  var sc=document.getElementById(prefix+'sc').value;
  var isLetter=sc==='letter';
  document.getElementById(prefix+'-maxmark').style.display=isLetter?'none':'';
  document.getElementById(prefix+'-pass').style.display=isLetter?'none':'';
  document.getElementById(prefix+'-grades').style.display=isLetter?'none':'';
}
function renderSubjects(){
  var admin=isAdmin();
  document.getElementById('subjbtn').innerHTML=admin?'<button class="btn gold" onclick="om(\'ms\')">+ Add Subject</button>':'';
  document.getElementById('subacth').textContent=admin?'Actions':'';
  var tb=document.getElementById('tbs');
  if(!DB.subjects.length){tb.innerHTML='<tr><td colspan="7"><div class="empty"><p>No subjects yet.</p></div></td></tr>';return;}
  tb.innerHTML=DB.subjects.map(function(s,i){
    var isL=s.scale==='letter';
    var gradeInfo=isL?'—':'A≥'+s.grA+'% B≥'+s.grB+'% C≥'+s.grC+'% D≥'+s.grD+'%';
    return'<tr>'
      +'<td>'+(i+1)+'</td>'
      +'<td><strong>'+s.name+'</strong></td>'
      +'<td>'+(isL?'Letter (A–F)':'Out of '+s.scale)+'</td>'
      +'<td>'+(isL?'—':s.pass)+'</td>'
      +'<td style="font-size:.75rem;color:var(--ink2);">'+gradeInfo+'</td>'
      +'<td>'+(admin?'<div class="brow"><button class="btn sm ghost" onclick="openEditSub(\''+s.id+'\')">✏️ Edit</button><button class="btn sm red" onclick="delSubject(\''+s.id+'\')">Delete</button></div>':'—')+'</td>'
      +'</tr>';
  }).join('');
}
function addSubject(){
  var name=document.getElementById('msn').value.trim();
  if(!name){alert('Enter a subject name.');return;}
  var sc=document.getElementById('mssc').value;
  var isL=sc==='letter';
  var maxMark=isL?'letter':parseFloat(document.getElementById('msmax').value)||100;
  var pass=isL?0:parseFloat(document.getElementById('msp').value)||50;
  var grA=isL?80:parseFloat(document.getElementById('ms-grA').value)||80;
  var grB=isL?70:parseFloat(document.getElementById('ms-grB').value)||70;
  var grC=isL?60:parseFloat(document.getElementById('ms-grC').value)||60;
  var grD=isL?50:parseFloat(document.getElementById('ms-grD').value)||50;
  DB.subjects.push({id:'S'+Date.now(),name:name,scale:maxMark,pass:pass,grA:grA,grB:grB,grC:grC,grD:grD});
  addLog('Added subject: '+name);dbSave();renderSubjects();cm('ms');
  document.getElementById('msn').value='';
  document.getElementById('msmax').value='100';document.getElementById('msp').value='50';
  document.getElementById('ms-grA').value='80';document.getElementById('ms-grB').value='70';
  document.getElementById('ms-grC').value='60';document.getElementById('ms-grD').value='50';
  document.getElementById('mssc').value='number';toggleSubForm('ms');
}
function openEditSub(id){
  var s=DB.subjects.find(function(x){return x.id===id;});if(!s)return;
  document.getElementById('mesid').value=id;
  document.getElementById('mesname').textContent=s.name;
  document.getElementById('mesn').value=s.name;
  document.getElementById('mesc').value=s.code||'';
  var isL=s.scale==='letter';
  document.getElementById('messc').value=isL?'letter':'number';
  document.getElementById('mesmax').value=isL?'100':s.scale;
  document.getElementById('mesp').value=s.pass||50;
  document.getElementById('mes-grA').value=s.grA||85;
  document.getElementById('mes-grB').value=s.grB||70;
  document.getElementById('mes-grC').value=s.grC||55;
  document.getElementById('mes-grD').value=s.grD||40;
  toggleSubForm('mes');
  document.getElementById('mes').classList.add('open');
}
function saveEditSubject(){
  var id=document.getElementById('mesid').value;
  var s=DB.subjects.find(function(x){return x.id===id;});if(!s)return;
  var sc=document.getElementById('messc').value;
  var isL=sc==='letter';
  s.name=document.getElementById('mesn').value.trim()||s.name;
  s.scale=isL?'letter':parseFloat(document.getElementById('mesmax').value)||100;
  s.pass=isL?0:parseFloat(document.getElementById('mesp').value)||50;
  s.grA=isL?80:parseFloat(document.getElementById('mes-grA').value)||80;
  s.grB=isL?70:parseFloat(document.getElementById('mes-grB').value)||70;
  s.grC=isL?60:parseFloat(document.getElementById('mes-grC').value)||60;
  s.grD=isL?50:parseFloat(document.getElementById('mes-grD').value)||50;
  addLog('Updated subject: '+s.name);dbSave();renderSubjects();cm('mes');
}
function delSubject(id){
  if(!confirm('Delete subject?'))return;
  DB.subjects=DB.subjects.filter(function(s){return s.id!==id;});
  dbSave();renderSubjects();
}

// ═══════════════════════════════════════
//  STUDENTS
// ═══════════════════════════════════════
function setupStudents(){
  var admin=isAdmin();
  document.getElementById('stbtn').innerHTML=admin?'<button class="btn gold" onclick="om(\'mst\')">+ Add Student</button>':'';
  document.getElementById('stacth').textContent=admin?'Action':'';
  var cl=document.getElementById('stCls');
  cl.innerHTML='<option value="">All Classes</option>'+myClasses().map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');
  renderStudents();
}
function renderStudents(){
  var admin=isAdmin();
  var q=document.getElementById('stSearch').value.toLowerCase();
  var cf=document.getElementById('stCls').value;
  var list=admin?DB.students:DB.students.filter(function(s){return myClasses().some(function(c){return c.id===s.classId;});});
  if(q) list=list.filter(function(s){return s.name.toLowerCase().includes(q)||s.sid.includes(q);});
  if(cf) list=list.filter(function(s){return s.classId===cf;});
  var tb=document.getElementById('tbst');
  if(!list.length){tb.innerHTML='<tr><td colspan="5"><div class="empty"><p>No students found.</p></div></td></tr>';return;}
  tb.innerHTML=list.map(function(s,i){
    var c=DB.classes.find(function(x){return x.id===s.classId;});
    return'<tr><td>'+(i+1)+'</td><td><strong>'+s.name+'</strong></td><td>'+s.sid+'</td><td>'+(c?c.name:'—')+'</td><td>'+(admin?'<div class="brow"><button class="btn sm ghost" onclick="openEditStudent(\''+s.id+'\')">✏️ Edit</button><button class="btn sm red" onclick="delStudent(\''+s.id+'\')">Delete</button></div>':'—')+'</td></tr>';
  }).join('');
}
function openEditStudent(id){
  var s=DB.students.find(function(x){return x.id===id;});if(!s)return;
  document.getElementById('mestid').value=id;
  document.getElementById('mestname').textContent=s.name;
  document.getElementById('mestn').value=s.name;
  document.getElementById('mestnum').value=s.sid;
  document.getElementById('mestcls').innerHTML='<option value="">— Select Class —</option>'+DB.classes.map(function(c){return'<option value="'+c.id+'"'+(c.id===s.classId?' selected':'')+'>'+c.name+'</option>';}).join('');
  document.getElementById('mest').classList.add('open');
}
function saveEditStudent(){
  var id=document.getElementById('mestid').value;
  var s=DB.students.find(function(x){return x.id===id;});if(!s)return;
  var name=document.getElementById('mestn').value.trim();
  var sid=document.getElementById('mestnum').value.trim();
  var cid=document.getElementById('mestcls').value;
  if(!name||!cid){alert('Name and class are required.');return;}
  s.name=name;s.sid=sid||s.sid;s.classId=cid;
  addLog('Updated student: '+name);dbSave();renderStudents();renderClasses();cm('mest');
  // Propagate to reports dropdown
  var rpSt=document.getElementById('rpSt');
  if(rpSt){var opt=rpSt.querySelector('option[value="'+id+'"]');if(opt)opt.textContent=name;}
}
function addStudent(){
  var name=document.getElementById('mstn').value.trim();
  var cid=document.getElementById('mstcls').value;
  if(!name||!cid){alert('Fill name and class.');return;}
  var sid=document.getElementById('mstnum').value||String(DB.students.length+1);
  DB.students.push({id:'ST'+Date.now(),name:name,sid:sid,classId:cid});
  addLog('Added student: '+name);dbSave();renderStudents();renderClasses();cm('mst');
  document.getElementById('mstn').value='';document.getElementById('mstnum').value='';
}
function delStudent(id){
  if(!confirm('Delete student?'))return;
  DB.students=DB.students.filter(function(s){return s.id!==id;});
  dbSave();renderStudents();renderClasses();
}

// ═══════════════════════════════════════
//  MARKS
// ═══════════════════════════════════════
function calcGrade(v,sub){
  if(v===''||v==null)return'—';
  if(sub.scale==='letter')return v;
  var pct=(parseFloat(v)/parseFloat(sub.scale))*100;
  // Use per-subject thresholds if set, else fall back to global settings
  var grA=sub.grA!=null?sub.grA:DB.settings.grA;
  var grB=sub.grB!=null?sub.grB:DB.settings.grB;
  var grC=sub.grC!=null?sub.grC:DB.settings.grC;
  var grD=sub.grD!=null?sub.grD:DB.settings.grD;
  if(pct>=grA)return'A';if(pct>=grB)return'B';if(pct>=grC)return'C';if(pct>=grD)return'D';
  return'F';
}
function checkPass(v,sub){
  if(v===''||v==null)return false;
  if(sub.scale==='letter')return['A','B','C','D'].indexOf(v)>=0;
  return parseFloat(v)>=sub.pass;
}
function setupMarks(){
  document.getElementById('mkCls').innerHTML='<option value="">— Select Class —</option>'+myClasses().map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');
  document.getElementById('mkSub').innerHTML='<option value="">— Select Subject —</option>'+mySubjects().map(function(s){return'<option value="'+s.id+'">'+s.name+'</option>';}).join('');
  syncTerms();
}
function loadMkTable(){
  var cid=document.getElementById('mkCls').value;
  var sid=document.getElementById('mkSub').value;
  var term=document.getElementById('mkTerm').value;
  var wrap=document.getElementById('mkWrap');
  if(!cid||!sid){wrap.innerHTML='<div class="empty"><div class="ei">✏️</div><p>Select class and subject to enter marks.</p></div>';return;}
  var students=DB.students.filter(function(s){return s.classId===cid;});
  var sub=DB.subjects.find(function(s){return s.id===sid;});
  if(!students.length){wrap.innerHTML='<div class="empty"><p>No students in this class.</p></div>';return;}
  var isL=sub.scale==='letter';
  var rows=students.map(function(s,i){
    var key=s.id+'_'+sid+'_'+term;
    var val=DB.marks[key]||'';
    var gr=calcGrade(val,sub);
    var ps=checkPass(val,sub);
    var inp=isL
      ?'<select class="mksel" id="mk_'+s.id+'" onchange="prevMark(\''+s.id+'\',\''+sid+'\')"><option value="">—</option>'+['A','B','C','D','F'].map(function(l){return'<option value="'+l+'"'+(val===l?' selected':'')+'>'+l+'</option>';}).join('')+'</select>'
      :'<input class="mkin" type="number" id="mk_'+s.id+'" min="0" max="'+sub.scale+'" step="0.5" value="'+val+'" oninput="prevMark(\''+s.id+'\',\''+sid+'\')">';
    return'<tr><td>'+(i+1)+'</td><td>'+s.name+'</td><td>'+s.sid+'</td><td>'+inp+'</td>'
      +'<td id="gr_'+s.id+'"><span class="gb '+gr+'">'+(gr==='—'?'—':gr)+'</span></td>'
      +'<td id="ps_'+s.id+'">'+(val!==''?(ps?'<span class="pok">✓ Pass</span>':'<span class="pfail">✗ Fail</span>'):'—')+'</td></tr>';
  }).join('');
  wrap.innerHTML='<div class="tw"><table><thead><tr><th>#</th><th>Student</th><th>No.</th><th>Mark'+(isL?'':' / '+sub.scale)+'</th><th>Grade</th><th>Status</th></tr></thead><tbody>'+rows+'</tbody></table></div>';
}
function prevMark(stid,subid){
  var sub=DB.subjects.find(function(s){return s.id===subid;});
  var el=document.getElementById('mk_'+stid);
  if(!el)return;
  var v=el.value;
  var gr=calcGrade(v,sub);var ps=checkPass(v,sub);
  document.getElementById('gr_'+stid).innerHTML='<span class="gb '+gr+'">'+(gr==='—'?'—':gr)+'</span>';
  document.getElementById('ps_'+stid).innerHTML=v!==''?(ps?'<span class="pok">✓ Pass</span>':'<span class="pfail">✗ Fail</span>'):'—';
}
function saveAllMarks(){
  var cid=document.getElementById('mkCls').value;
  var sid=document.getElementById('mkSub').value;
  var term=document.getElementById('mkTerm').value;
  if(!cid||!sid){alert('Select class and subject first.');return;}
  var students=DB.students.filter(function(s){return s.classId===cid;});
  var cnt=0;
  students.forEach(function(s){
    var el=document.getElementById('mk_'+s.id);
    if(el&&el.value!==''){DB.marks[s.id+'_'+sid+'_'+term]=el.value;cnt++;}
  });
  var sn=DB.subjects.find(function(s){return s.id===sid;});
  addLog('Saved '+cnt+' marks — '+(sn?sn.name:'')+' ('+termLabel(term)+')');
  dbSave();renderDash();
  alert('✅ '+cnt+' marks saved!');
}

// ═══════════════════════════════════════
//  IMPORT
// ═══════════════════════════════════════
function handleDrop(e){var f=e.dataTransfer.files[0];if(f)readCSV(f);}
function handleFile(e){var f=e.target.files[0];if(f)readCSV(f);}
function readCSV(f){var r=new FileReader();r.onload=function(e){processCSV(e.target.result);};r.readAsText(f);}
function importPaste(){var t=document.getElementById('csvpaste').value.trim();if(!t){alert('Paste CSV data first.');return;}processCSV(t);}
function processCSV(text){
  var lines=text.split('\n').map(function(l){return l.trim();}).filter(Boolean);
  var isH=lines[0]&&lines[0].toLowerCase().indexOf('name')>=0;
  var data=isH?lines.slice(1):lines;
  var added=0,skipped=0;
  data.forEach(function(line){
    var p=line.split(',').map(function(x){return x.trim().replace(/^["']|["']$/g,'');});
    if(!p[0]){skipped++;return;}
    var name=p[0],sid=p[1]||String(DB.students.length+added+1),cname=p[2]||'';
    var classId='';
    if(cname){
      var cls=DB.classes.find(function(c){return c.name.toLowerCase()===cname.toLowerCase();});
      if(!cls){cls={id:'C'+Date.now()+Math.random(),name:cname,level:cname};DB.classes.push(cls);}
      classId=cls.id;
    }
    if(DB.students.find(function(s){return s.sid===sid;})){skipped++;return;}
    DB.students.push({id:'ST'+Date.now()+Math.random(),name:name,sid:sid,classId:classId});
    added++;
  });
  addLog('Imported '+added+' students');dbSave();renderStudents();renderClasses();syncAll();
  document.getElementById('impres').innerHTML='<div class="al ok">✅ Imported <strong>'+added+'</strong> students. ('+skipped+' skipped)</div>';
}

// ═══════════════════════════════════════
//  REPORTS
// ═══════════════════════════════════════
function setupReports(){
  var list;
  if(isAdmin()){
    list=DB.students;
  } else {
    // Teacher only sees report cards for students in their ONE class teacher class
    var ct=ME.classTeacher;
    if(!ct){
      document.getElementById('rpSt').innerHTML='<option value="">— No class assigned —</option>';
      document.getElementById('rpOut').innerHTML='<div class="empty"><div class="ei">🔒</div><p>You are not assigned as a class teacher of any class.</p></div>';
      syncTerms();return;
    }
    list=DB.students.filter(function(s){return s.classId===ct;});
  }
  document.getElementById('rpSt').innerHTML='<option value="">— Select Student —</option>'+list.map(function(s){return'<option value="'+s.id+'">'+s.name+'</option>';}).join('');
  syncTerms();
  genReport();
}
function genReport(){
  var stid=document.getElementById('rpSt').value;
  var term=document.getElementById('rpTerm').value;
  var remark=document.getElementById('rpRemark')?document.getElementById('rpRemark').value:'';
  var out=document.getElementById('rpOut');
  if(!stid){out.innerHTML='<div class="empty"><div class="ei">&#128196;</div><p>Select a student to preview their report card.</p></div>';return;}
  var st=DB.students.find(function(s){return s.id===stid;});
  if(!st){out.innerHTML='';return;}
  var cls=DB.classes.find(function(c){return c.id===st.classId;});
  var school=DB.settings.schoolName||'Academic Bridge School';
  var tl=termLabel(term);
  var date=new Date().toLocaleDateString('en-GB',{day:'numeric',month:'long',year:'numeric'});
  var rows=DB.subjects.map(function(sub){var v=DB.marks[stid+'_'+sub.id+'_'+term]||'';return{sub:sub,v:v,gr:calcGrade(v,sub),ps:checkPass(v,sub)};});
  var filled=rows.filter(function(r){return r.v!=='';});
  var tot=0,cnt=0,passes=0,fails=0;
  filled.forEach(function(r){
    if(r.sub.scale!=='letter'){tot+=(parseFloat(r.v)/parseFloat(r.sub.scale))*100;cnt++;}
    if(r.v!==''){r.ps?passes++:fails++;}
  });
  var avg=cnt?(tot/cnt):null;
  var avgStr=avg!==null?avg.toFixed(1)+'%':'—';
  var g=DB.settings;
  var overallGrade=avg!==null?(avg>=g.grA?'A':avg>=g.grB?'B':avg>=g.grC?'C':avg>=g.grD?'D':'F'):'—';
  var gradeColor={'A':'#1a7a4a','B':'#1a4a8a','C':'#7a5a00','D':'#5a3a7a','F':'#8a1a1a','—':'#555'};
  var gradeLabel={'A':'Distinction','B':'Merit','C':'Credit','D':'Pass','F':'Fail','—':''};
  var promotion=fails===0&&filled.length>0?'PROMOTED':'REFERRED FOR REVIEW';
  var promColor=fails===0&&filled.length>0?'#1a5c30':'#7a1a1a';

  // Mini bar chart SVG for each subject
  function miniBar(v,max){
    if(!v||!max||isNaN(parseFloat(v))||isNaN(parseFloat(max)))return'';
    var pct=Math.min(100,Math.round((parseFloat(v)/parseFloat(max))*100));
    var barColor=pct>=80?'#1a7a4a':pct>=60?'#1a4a8a':pct>=50?'#7a5a00':'#8a1a1a';
    return '<div style="display:flex;align-items:center;gap:5px;min-width:80px;">'
      +'<div style="flex:1;height:6px;background:#e0ddd4;border-radius:3px;overflow:hidden;">'
      +'<div style="width:'+pct+'%;height:100%;background:'+barColor+';border-radius:3px;"></div></div>'
      +'<span style="font-size:.67rem;color:#666;width:26px;text-align:right;">'+pct+'%</span></div>';
  }

  out.innerHTML='<div class="rpaper" style="max-width:720px;">'

    // ── HEADER ──
    +'<div style="border-bottom:3px double #2a2215;padding-bottom:1rem;margin-bottom:1rem;text-align:center;">'
    +'<div style="font-size:.65rem;letter-spacing:.18em;text-transform:uppercase;color:#888;margin-bottom:4px;font-family:Georgia,serif;">Official Academic Record</div>'
    +'<div style="font-family:Georgia,serif;font-size:1.8rem;font-weight:700;color:#1a1a1a;letter-spacing:.02em;">'+school+'</div>'
    +'<div style="font-size:.78rem;color:#666;margin-top:4px;letter-spacing:.06em;">STUDENT ACADEMIC REPORT — '+tl.toUpperCase()+'</div>'
    +'<div style="display:flex;justify-content:center;gap:6px;margin-top:8px;">'
    +'<span style="display:inline-block;width:30px;height:2px;background:#c8a000;border-radius:2px;"></span>'
    +'<span style="display:inline-block;width:60px;height:2px;background:#2a2215;border-radius:2px;"></span>'
    +'<span style="display:inline-block;width:30px;height:2px;background:#c8a000;border-radius:2px;"></span>'
    +'</div></div>'

    // ── STUDENT INFO ──
    +'<div style="display:grid;grid-template-columns:1fr 1fr;gap:0;margin-bottom:1rem;border:1px solid #ccc;border-radius:4px;overflow:hidden;">'
    +'<div style="padding:8px 14px;background:#f7f4ec;border-right:1px solid #ccc;"><span style="font-size:.62rem;text-transform:uppercase;letter-spacing:.08em;color:#888;">Full Name</span><br><strong style="font-size:.95rem;">'+st.name+'</strong></div>'
    +'<div style="padding:8px 14px;background:#f7f4ec;"><span style="font-size:.62rem;text-transform:uppercase;letter-spacing:.08em;color:#888;">Student No.</span><br><strong style="font-size:.95rem;font-family:monospace;">'+st.sid+'</strong></div>'
    +'<div style="padding:8px 14px;border-top:1px solid #ccc;border-right:1px solid #ccc;"><span style="font-size:.62rem;text-transform:uppercase;letter-spacing:.08em;color:#888;">Class</span><br><strong style="font-size:.95rem;">'+(cls?cls.name:'—')+'</strong></div>'
    +'<div style="padding:8px 14px;border-top:1px solid #ccc;"><span style="font-size:.62rem;text-transform:uppercase;letter-spacing:.08em;color:#888;">Date Issued</span><br><strong style="font-size:.95rem;">'+date+'</strong></div>'
    +'</div>'

    // ── MARKS TABLE ──
    +'<table class="rptbl" style="margin-bottom:1rem;">'
    +'<thead><tr style="background:#2a2215;color:#f5f0e0;">'
    +'<th style="background:#2a2215;color:#f5f0e0;padding:9px 10px;">Subject</th>'
    +'<th style="background:#2a2215;color:#f5f0e0;text-align:center;">Mark</th>'
    +'<th style="background:#2a2215;color:#f5f0e0;text-align:center;">Out of</th>'
    +'<th style="background:#2a2215;color:#f5f0e0;text-align:center;">%</th>'
    +'<th style="background:#2a2215;color:#f5f0e0;text-align:center;">Grade</th>'
    +'<th style="background:#2a2215;color:#f5f0e0;text-align:center;">Performance</th>'
    +'<th style="background:#2a2215;color:#f5f0e0;text-align:center;">Result</th>'
    +'</tr></thead><tbody>'
    +rows.map(function(r,i){
      var pct=r.v!==''&&r.sub.scale!=='letter'?((parseFloat(r.v)/parseFloat(r.sub.scale))*100).toFixed(1):'—';
      var gc=gradeColor[r.gr]||'#555';
      return'<tr style="background:'+(i%2===0?'#fff':'#f7f4ec')+';">'
        +'<td style="font-weight:500;">'+r.sub.name+'</td>'
        +'<td style="text-align:center;font-family:monospace;font-weight:600;">'+(r.v||'—')+'</td>'
        +'<td style="text-align:center;color:#888;">'+(r.sub.scale==='letter'?'Letter':r.sub.scale)+'</td>'
        +'<td style="text-align:center;font-family:monospace;">'+(pct==='—'?'—':pct+'%')+'</td>'
        +'<td style="text-align:center;"><span style="display:inline-block;padding:2px 10px;border-radius:10px;font-weight:700;font-size:.8rem;background:'+gc+'22;color:'+gc+';border:1px solid '+gc+'44;">'+r.gr+'</span></td>'
        +'<td>'+miniBar(r.v,r.sub.scale)+'</td>'
        +'<td style="text-align:center;font-weight:600;font-size:.82rem;color:'+(r.v!==''?(r.ps?'#1a7a4a':'#8a1a1a'):'#aaa')+'">'+(r.v!==''?(r.ps?'PASS':'FAIL'):'—')+'</td>'
        +'</tr>';
    }).join('')
    +'</tbody></table>'

    // ── SUMMARY ROW ──
    +'<div style="display:grid;grid-template-columns:repeat(4,1fr);gap:0;border:1px solid #ccc;border-radius:4px;overflow:hidden;margin-bottom:1rem;">'
    +'<div style="padding:10px;text-align:center;background:#f7f4ec;border-right:1px solid #ccc;">'
    +'<div style="font-size:.62rem;text-transform:uppercase;letter-spacing:.08em;color:#888;">Average</div>'
    +'<div style="font-size:1.4rem;font-weight:700;color:#2a2215;font-family:Georgia,serif;">'+avgStr+'</div></div>'
    +'<div style="padding:10px;text-align:center;background:#f7f4ec;border-right:1px solid #ccc;">'
    +'<div style="font-size:.62rem;text-transform:uppercase;letter-spacing:.08em;color:#888;">Overall Grade</div>'
    +'<div style="font-size:1.4rem;font-weight:700;color:'+(gradeColor[overallGrade]||'#555')+';font-family:Georgia,serif;">'+overallGrade+'</div>'
    +'<div style="font-size:.65rem;color:#888;">'+( gradeLabel[overallGrade]||'')+'</div></div>'
    +'<div style="padding:10px;text-align:center;background:#f7f4ec;border-right:1px solid #ccc;">'
    +'<div style="font-size:.62rem;text-transform:uppercase;letter-spacing:.08em;color:#888;">Subjects</div>'
    +'<div style="font-size:1.4rem;font-weight:700;color:#2a2215;font-family:Georgia,serif;">'+filled.length+' / '+rows.length+'</div></div>'
    +'<div style="padding:10px;text-align:center;background:#f7f4ec;">'
    +'<div style="font-size:.62rem;text-transform:uppercase;letter-spacing:.08em;color:#888;">Status</div>'
    +'<div style="font-size:.78rem;font-weight:800;color:'+promColor+';margin-top:4px;letter-spacing:.04em;">'+promotion+'</div></div>'
    +'</div>'

    // ── GRADE SCALE ──
    +'<div style="margin-bottom:1rem;padding:8px 12px;background:#f0ece0;border:1px solid #ddd;border-radius:4px;font-size:.72rem;color:#666;">'
    +'<strong style="color:#2a2215;">Grade Scale:</strong>&nbsp;&nbsp;'
    +'<strong style="color:#1a7a4a;">A</strong> = '+g.grA+'%+ (Distinction)&nbsp;&nbsp;'
    +'<strong style="color:#1a4a8a;">B</strong> = '+g.grB+'–'+(g.grA-1)+'% (Merit)&nbsp;&nbsp;'
    +'<strong style="color:#7a5a00;">C</strong> = '+g.grC+'–'+(g.grB-1)+'% (Credit)&nbsp;&nbsp;'
    +'<strong style="color:#5a3a7a;">D</strong> = '+g.grD+'–'+(g.grC-1)+'% (Pass)&nbsp;&nbsp;'
    +'<strong style="color:#8a1a1a;">F</strong> = Below '+g.grD+'% (Fail)'
    +'</div>'

    // ── REMARKS ──
    +'<div style="margin-bottom:1rem;padding:10px 14px;background:#fffef7;border:1px solid #d8d0b8;border-left:4px solid #c8a000;border-radius:0 4px 4px 0;">'
    +'<div style="font-size:.65rem;text-transform:uppercase;letter-spacing:.1em;color:#888;margin-bottom:4px;">Class Teacher\'s Remarks</div>'
    +'<div style="font-style:italic;color:#333;font-size:.88rem;">'+(remark||'_____________________________________________')+'</div>'
    +'</div>'

    // ── SIGNATURES ──
    +'<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:1.5rem;padding-top:1rem;border-top:1px solid #ccc;font-size:.78rem;color:#555;">'
    +'<div><div style="border-bottom:1px solid #aaa;margin-bottom:4px;height:28px;"></div>Class Teacher</div>'
    +'<div><div style="border-bottom:1px solid #aaa;margin-bottom:4px;height:28px;"></div>Headteacher / Principal</div>'
    +'<div><div style="border-bottom:1px solid #aaa;margin-bottom:4px;height:28px;"></div>Parent / Guardian</div>'
    +'</div>'

    +'</div>';
}

// ═══════════════════════════════════════
//  ANALYTICS
// ═══════════════════════════════════════
function setupAnalytics(){
  var clsEl=document.getElementById('anCls');
  var subEl=document.getElementById('anSub');
  if(clsEl) clsEl.innerHTML='<option value="">All Classes</option>'+DB.classes.map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');
  if(subEl) subEl.innerHTML='<option value="">All Subjects</option>'+DB.subjects.map(function(s){return'<option value="'+s.id+'">'+s.name+'</option>';}).join('');
  syncTerms();
  renderAnalytics();
}
function renderAnalytics(){
  var cid=document.getElementById('anCls')?document.getElementById('anCls').value:'';
  var term=document.getElementById('anTerm')?document.getElementById('anTerm').value:'';
  var sid=document.getElementById('anSub')?document.getElementById('anSub').value:'';
  var out=document.getElementById('anOut');
  if(!out) return;

  var students=cid?DB.students.filter(function(s){return s.classId===cid;}):DB.students;
  var subjects=sid?DB.subjects.filter(function(s){return s.id===sid;}):DB.subjects;
  var g=DB.settings;

  if(!students.length||!subjects.length||!term){
    out.innerHTML='<div class="empty"><div class="ei">&#128202;</div><p>No data to display yet. Add students, subjects, and marks first.</p></div>';return;
  }

  // Grade distribution
  var gradeCount={A:0,B:0,C:0,D:0,F:0};
  var allAvgs=[];
  var subjectAvgs={};

  students.forEach(function(st){
    var tot=0,cnt=0;
    subjects.forEach(function(sub){
      if(sub.scale==='letter') return;
      var v=DB.marks[st.id+'_'+sub.id+'_'+term];
      if(v===undefined||v==='') return;
      var pct=(parseFloat(v)/parseFloat(sub.scale))*100;
      tot+=pct;cnt++;
      if(!subjectAvgs[sub.id]) subjectAvgs[sub.id]={name:sub.name,tot:0,cnt:0};
      subjectAvgs[sub.id].tot+=pct;subjectAvgs[sub.id].cnt++;
    });
    if(cnt){var avg=tot/cnt;allAvgs.push({name:st.name,avg:avg});
      var gr=avg>=g.grA?'A':avg>=g.grB?'B':avg>=g.grC?'C':avg>=g.grD?'D':'F';
      gradeCount[gr]++;
    }
  });

  if(!allAvgs.length){out.innerHTML='<div class="empty"><div class="ei">&#128202;</div><p>No numeric marks recorded for the selected filters.</p></div>';return;}

  allAvgs.sort(function(a,b){return b.avg-a.avg;});
  var classAvg=allAvgs.reduce(function(s,x){return s+x.avg;},0)/allAvgs.length;
  var highest=allAvgs[0];
  var lowest=allAvgs[allAvgs.length-1];
  var passing=allAvgs.filter(function(x){return x.avg>=g.grD;}).length;

  // Color helpers
  var gradeColors={A:'#1a7a4a',B:'#1a4a8a',C:'#7a5a00',D:'#5a3a7a',F:'#8a1a1a'};
  var gradeLabels={A:'Distinction',B:'Merit',C:'Credit',D:'Pass',F:'Fail'};
  var total=allAvgs.length;

  // Build SVG bar chart for grade distribution
  function gradeBar(g,count,total){
    var pct=total?Math.round((count/total)*100):0;
    var barH=pct*1.2;
    return'<div style="display:flex;flex-direction:column;align-items:center;gap:4px;flex:1;">'
      +'<div style="font-size:.78rem;font-weight:700;color:var(--ink);">'+count+'</div>'
      +'<div style="width:100%;height:120px;display:flex;align-items:flex-end;justify-content:center;">'
      +'<div style="width:70%;background:'+gradeColors[g]+';height:'+Math.max(4,barH)+'px;border-radius:4px 4px 0 0;min-height:4px;transition:height .4s;"></div></div>'
      +'<div style="font-size:.88rem;font-weight:700;color:'+gradeColors[g]+';">'+g+'</div>'
      +'<div style="font-size:.65rem;color:var(--ink3);">'+pct+'%</div>'
      +'</div>';
  }

  // Subject performance bars
  var subBars=Object.values(subjectAvgs).map(function(s){
    var a=s.cnt?s.tot/s.cnt:0;
    var w=Math.round(a);
    var bc=a>=g.grA?'#1a7a4a':a>=g.grB?'#1a4a8a':a>=g.grC?'#7a5a00':a>=g.grD?'#5a3a7a':'#8a1a1a';
    return'<div style="margin-bottom:.7rem;">'
      +'<div style="display:flex;justify-content:space-between;margin-bottom:3px;">'
      +'<span style="font-size:.81rem;color:var(--ink);">'+s.name+'</span>'
      +'<span style="font-size:.78rem;font-weight:600;color:'+bc+';">'+a.toFixed(1)+'%</span></div>'
      +'<div style="background:var(--s3);border-radius:4px;height:8px;overflow:hidden;">'
      +'<div style="width:'+w+'%;height:100%;background:'+bc+';border-radius:4px;"></div></div>'
      +'</div>';
  }).join('');

  // Top students list
  var topList=allAvgs.slice(0,5).map(function(s,i){
    var medals=['🥇','🥈','🥉','4.','5.'];
    var bc=s.avg>=g.grA?'#1a7a4a':s.avg>=g.grB?'#1a4a8a':s.avg>=g.grC?'#7a5a00':s.avg>=g.grD?'#5a3a7a':'#8a1a1a';
    return'<div style="display:flex;align-items:center;gap:10px;padding:7px 0;border-bottom:1px solid var(--bd);">'
      +'<span style="font-size:1rem;width:24px;text-align:center;">'+medals[i]+'</span>'
      +'<span style="flex:1;font-size:.83rem;color:var(--ink);font-weight:500;">'+s.name+'</span>'
      +'<span style="font-size:.85rem;font-weight:700;color:'+bc+';">'+s.avg.toFixed(1)+'%</span>'
      +'</div>';
  }).join('');

  out.innerHTML=
    // Summary stats
    '<div style="display:grid;grid-template-columns:repeat(4,1fr);gap:.8rem;margin-bottom:1rem;">'
    +'<div class="scard gold"><div class="snum">'+classAvg.toFixed(1)+'%</div><div class="slbl">Class Average</div></div>'
    +'<div class="scard green"><div class="snum">'+passing+'</div><div class="slbl">Passing Students</div></div>'
    +'<div class="scard blue"><div class="snum">'+total+'</div><div class="slbl">Total Students</div></div>'
    +'<div class="scard purple"><div class="snum">'+Math.round((passing/total)*100)+'%</div><div class="slbl">Pass Rate</div></div>'
    +'</div>'

    // Grade distribution chart + Top students
    +'<div style="display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-bottom:1rem;">'

    +'<div class="card"><div class="ctitle">Grade Distribution</div>'
    +'<div style="display:flex;gap:.5rem;align-items:flex-end;padding:0 .5rem;">'
    +['A','B','C','D','F'].map(function(gr){return gradeBar(gr,gradeCount[gr],total);}).join('')
    +'</div></div>'

    +'<div class="card"><div class="ctitle">Top 5 Students</div>'
    +topList
    +'</div></div>'

    // Subject averages
    +(Object.keys(subjectAvgs).length?
    '<div class="card"><div class="ctitle">Subject Averages</div>'+subBars+'</div>':'')

    // Highest & Lowest
    +'<div style="display:grid;grid-template-columns:1fr 1fr;gap:1rem;">'
    +'<div class="card"><div class="ctitle">Highest Performer</div>'
    +'<div style="font-size:1.1rem;font-weight:600;color:var(--ink);">'+highest.name+'</div>'
    +'<div style="font-size:1.5rem;font-weight:700;color:#1a7a4a;margin-top:4px;">'+highest.avg.toFixed(1)+'%</div>'
    +'<div style="font-size:.72rem;color:var(--ink3);margin-top:2px;">Distinction</div></div>'

    +'<div class="card"><div class="ctitle">Needs Support</div>'
    +'<div style="font-size:1.1rem;font-weight:600;color:var(--ink);">'+lowest.name+'</div>'
    +'<div style="font-size:1.5rem;font-weight:700;color:'+(lowest.avg>=g.grD?'#5a3a7a':'#8a1a1a')+';margin-top:4px;">'+lowest.avg.toFixed(1)+'%</div>'
    +'<div style="font-size:.72rem;color:var(--ink3);margin-top:2px;">'+(lowest.avg>=g.grD?'Passing':'Below Pass Mark')+'</div></div>'
    +'</div>';
}

// ═══════════════════════════════════════
//  PROCLAMATION
// ═══════════════════════════════════════
function setupProcl(){
  if(isAdmin()){
    document.getElementById('prCls').innerHTML='<option value="">All Classes</option>'+DB.classes.map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');
  } else {
    var ct=ME.classTeacher;
    if(!ct){
      document.getElementById('prCls').innerHTML='<option value="">— No class assigned —</option>';
      document.getElementById('prOut').innerHTML='<div class="empty"><div class="ei">🔒</div><p>You are not assigned as a class teacher of any class.</p></div>';
      syncTerms();return;
    }
    var ctCls=DB.classes.find(function(c){return c.id===ct;});
    document.getElementById('prCls').innerHTML=ctCls?'<option value="'+ctCls.id+'">'+ctCls.name+'</option>':'<option value="">—</option>';
  }
  syncTerms();
  genProcl();
}
function genProcl(){
  var cid=document.getElementById('prCls').value;
  var term=document.getElementById('prTerm').value;
  var out=document.getElementById('prOut');
  if(!cid){out.innerHTML='<div class="empty"><div class="ei">🏆</div><p>No class selected.</p></div>';return;}
  if(!isAdmin()&&ME.classTeacher&&cid!==ME.classTeacher){
    out.innerHTML='<div class="empty"><div class="ei">🔒</div><p>Access denied.</p></div>';return;
  }
  var list=DB.students.filter(function(s){return s.classId===cid;});
  var g=DB.settings;
  var ranked=list.map(function(s){
    var tot=0,cnt=0;
    DB.subjects.forEach(function(sub){var v=DB.marks[s.id+'_'+sub.id+'_'+term];if(v!==undefined&&v!==''&&sub.scale!=='letter'){tot+=(parseFloat(v)/parseFloat(sub.scale))*100;cnt++;}});
    return Object.assign({},s,{avg:cnt?(tot/cnt):null,cnt:cnt});
  }).filter(function(s){return s.avg!==null;}).sort(function(a,b){return b.avg-a.avg;});
  if(!ranked.length){out.innerHTML='<div class="empty"><div class="ei">🏆</div><p>No marks recorded for this term yet.</p></div>';return;}
  var tl=termLabel(term);
  var cn=(DB.classes.find(function(c){return c.id===cid;})||{}).name||'—';
  out.innerHTML='<div style="text-align:center;padding:1.1rem;background:var(--s1);border:1px solid var(--bd);border-radius:10px;margin-bottom:1rem;">'
    +'<div style="font-family:\'Playfair Display\',serif;font-size:1.25rem;">🏆 Proclamation List</div>'
    +'<div style="font-size:.78rem;color:var(--ink3);margin-top:3px;">'+tl+' — '+cn+'</div></div>'
    +ranked.map(function(s,i){
      var cls=DB.classes.find(function(c){return c.id===s.classId;});
      var grade=s.avg>=g.grA?'A':s.avg>=g.grB?'B':s.avg>=g.grC?'C':s.avg>=g.grD?'D':'F';
      var medal=i===0?'🥇':i===1?'🥈':i===2?'🥉':String(i+1);
      var rc=i===0?'r1':i===1?'r2':i===2?'r3':'rn';
      return'<div class="pcard"><div class="rcirc '+rc+'">'+medal+'</div>'
        +'<div style="flex:1;"><div style="font-weight:600;">'+s.name+'</div>'
        +'<div style="font-size:.76rem;color:var(--ink3);margin-top:2px;">No. '+s.sid+' · '+(cls?cls.name:'—')+' · '+s.cnt+' subject'+(s.cnt!==1?'s':'')+'</div></div>'
        +'<div style="text-align:right;"><div style="font-size:1.35rem;font-weight:600;color:var(--gold);">'+s.avg.toFixed(1)+'%</div>'
        +'<div style="font-size:.7rem;color:var(--ink3);">Grade '+grade+'</div></div></div>';
    }).join('');
}

// ═══════════════════════════════════════
//  SETTINGS
// ═══════════════════════════════════════
function setupSettings(){
  var admin=isAdmin();
  document.getElementById('schoolCard').style.display=admin?'block':'none';
  document.getElementById('gradeCard').style.display=admin?'block':'none';
  document.getElementById('dataCard').style.display=admin?'block':'none';
  document.getElementById('schin').value=DB.settings.schoolName||'';
  document.getElementById('grA').value=DB.settings.grA;
  document.getElementById('grB').value=DB.settings.grB;
  document.getElementById('grC').value=DB.settings.grC;
  document.getElementById('grD').value=DB.settings.grD;
}
function saveGrades(){
  DB.settings.grA=+document.getElementById('grA').value;
  DB.settings.grB=+document.getElementById('grB').value;
  DB.settings.grC=+document.getElementById('grC').value;
  DB.settings.grD=+document.getElementById('grD').value;
  dbSave();flash('gral','ok','✅ Grade thresholds saved.');
}
function changePw(){
  var old=document.getElementById('pwold').value;
  var nw=document.getElementById('pwnew').value;
  var cf=document.getElementById('pwcf').value;
  if(ME.password!==old){flash('pwal','warn','❌ Current password incorrect.');return;}
  if(nw.length<4){flash('pwal','warn','❌ Password too short (min 4 chars).');return;}
  if(nw!==cf){flash('pwal','warn','❌ Passwords do not match.');return;}
  ME.password=nw;
  DB.users=DB.users.map(function(u){return u.id===ME.id?Object.assign({},u,{password:nw}):u;});
  dbSave();flash('pwal','ok','✅ Password updated.');
  document.getElementById('pwold').value='';document.getElementById('pwnew').value='';document.getElementById('pwcf').value='';
}
function exportData(){
  var b=new Blob([JSON.stringify(DB,null,2)],{type:'application/json'});
  var a=document.createElement('a');a.href=URL.createObjectURL(b);
  a.download='epaza_backup_'+new Date().toISOString().slice(0,10)+'.json';a.click();
}
function loadBackup(e){
  var f=e.target.files[0];if(!f)return;
  var r=new FileReader();
  r.onload=function(ev){try{DB=JSON.parse(ev.target.result);dbSave();location.reload();}catch(e){alert('Invalid backup file.');}};
  r.readAsText(f);
}
function clearAll(){
  if(!confirm('⚠️ Delete ALL data? This cannot be undone.'))return;
  if(!confirm('Are you absolutely sure?'))return;
  localStorage.clear();location.reload();
}

// ═══════════════════════════════════════
//  SYNC HELPERS
// ═══════════════════════════════════════
function syncTerms(){
  var at=activeTerms();
  var opts=at.map(function(t){return'<option value="'+t.id+'">'+t.name+'</option>';}).join('');
  if(!opts) opts='<option value="">No active terms</option>';
  ['mkTerm','rpTerm','prTerm','anTerm'].forEach(function(id){
    var el=document.getElementById(id);if(!el)return;
    var cur=el.value;el.innerHTML=opts;
    if(at.find(function(t){return t.id===cur;})) el.value=cur;
  });
}
function syncAll(){
  syncTerms();
  var cl=document.getElementById('stCls');
  if(cl){cl.innerHTML='<option value="">All Classes</option>'+myClasses().map(function(c){return'<option value="'+c.id+'">'+c.name+'</option>';}).join('');}
  syncClassSelects();
}

// ═══════════════════════════════════════
//  INIT — load data then show login
// ═══════════════════════════════════════
// ═══════════════════════════════════════
//  PASSWORD TOGGLE HELPERS
// ═══════════════════════════════════════
function toggleLoginPw(btn){
  var inp=document.getElementById('lpass');
  if(inp.type==='password'){inp.type='text';btn.textContent='🙈';}
  else{inp.type='password';btn.textContent='👁';}
}
function togglePwField(fieldId,btn){
  var inp=document.getElementById(fieldId);
  if(inp.type==='password'){inp.type='text';btn.textContent='🙈';}
  else{inp.type='password';btn.textContent='👁';}
}

// ═══════════════════════════════════════
//  ADMIN PROPAGATION — school name syncs everywhere
// ═══════════════════════════════════════
function saveSchool(){
  var v=document.getElementById('schin').value.trim();
  if(!v){flash('schal','warn','Enter a school name.');return;}
  DB.settings.schoolName=v;dbSave();applySchool();
  // Also re-render dashboard sub to reflect new school
  var dw=document.getElementById('dwelcome');if(dw&&ME)dw.textContent='Welcome back, '+ME.name;
  flash('schal','ok','✅ School name saved and updated everywhere.');
}

async function initApp(){
  // Show loading overlay while we fetch data
  var overlay = document.createElement('div');
  overlay.id = 'loadOverlay';
  overlay.style.cssText = 'position:fixed;inset:0;background:var(--bg);display:flex;flex-direction:column;align-items:center;justify-content:center;z-index:99999;gap:14px;';
  overlay.innerHTML = '<div style="font-family:\'Playfair Display\',serif;font-size:2rem;font-weight:700;">E<span style="color:var(--gold)">PAZA</span></div>'
    + '<div style="font-size:.88rem;color:var(--ink3);">Loading data…</div>'
    + '<div style="width:48px;height:4px;background:var(--s3);border-radius:4px;overflow:hidden;"><div id="loadBar" style="height:100%;width:0%;background:var(--gold);border-radius:4px;transition:width .4s;"></div></div>';
  document.body.appendChild(overlay);
  document.getElementById('loadBar').style.width = '40%';

  // Load from localStorage first
  var raw = null;
  var keys = ['epaza_db','em3_db','edumark_v4','edumark_db'];
  for(var i=0;i<keys.length;i++){
    raw = localStorage.getItem(keys[i]);
    if(raw) break;
  }
  if(raw){
    try{
      var d = JSON.parse(raw);
      if(d && typeof d === 'object'){
        if(Array.isArray(d.users) && d.users.length) DB.users = d.users;
        if(Array.isArray(d.teachers)) DB.teachers = d.teachers;
        if(Array.isArray(d.classes)) DB.classes = d.classes;
        if(Array.isArray(d.subjects)) DB.subjects = d.subjects;
        if(Array.isArray(d.students)) DB.students = d.students;
        if(d.marks && typeof d.marks==='object') DB.marks = d.marks;
        if(d.settings && typeof d.settings==='object') DB.settings = Object.assign(DB.settings, d.settings);
        if(Array.isArray(d.activity)) DB.activity = d.activity;
        if(Array.isArray(d.terms) && d.terms.length) DB.terms = d.terms;
      }
    }catch(e){}
  }
  document.getElementById('loadBar').style.width = '70%';

  // Then Supabase overrides (master data)
  await supabaseLoad();
  document.getElementById('loadBar').style.width = '100%';

  // Guarantee admin exists
  var adminExists = DB.users.some(function(u){ return u.id==='admin'; });
  if(!adminExists){
    DB.users.unshift({id:'admin',username:'admin',password:'admin123',role:'admin',name:'Administrator'});
  }

  // Save merged result back to localStorage
  try{ localStorage.setItem('epaza_db', JSON.stringify(DB)); }catch(e){}

  applySchool();

  // Remove loading overlay and show login
  setTimeout(function(){
    overlay.remove();
    document.getElementById('loginWrap').style.display = 'flex';
  }, 300);
}

// Hide login until data is ready
document.getElementById('loginWrap').style.display = 'none';
initApp();
</script>

</body>
</html>
