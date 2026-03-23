<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>EduBuild — School Platform</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Merriweather:ital,wght@0,700;0,900;1,400&display=swap');
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --navy:#0D2B5E;--blue:#1565C0;--sky:#2196F3;--teal:#00838F;
  --green:#2E7D32;--orange:#E65100;--purple:#6A1B9A;--red:#B71C1C;
  --bg:#F0F4FF;--surface:#fff;--surface2:#F5F7FF;--border:#DDE3F0;
  --text:#1A2340;--muted:#5A6B8A;--r:10px;
  --shadow:0 4px 24px rgba(13,43,94,0.10);
}
html{scroll-behavior:smooth}
body{font-family:'Nunito','Segoe UI',Arial,sans-serif;background:var(--bg);color:var(--text);line-height:1.65;overflow-x:hidden}
a{color:var(--blue);text-decoration:none}
h1,h2,h3{font-family:'Merriweather','Georgia',serif}

/* ══ SCREENS ══ */
.screen{display:none;min-height:100vh}
.screen.active{display:block}

/* ══════════════════════════
   LOGIN SCREEN
══════════════════════════ */
#loginScreen{
  min-height:100vh;
  background:linear-gradient(135deg,#0D2B5E 0%,#1565C0 55%,#006064 100%);
  display:flex;align-items:center;justify-content:center;padding:2rem;
}
#loginScreen.active{display:flex}
.login-box{
  background:#fff;border-radius:16px;padding:2.5rem 2rem;
  width:100%;max-width:420px;box-shadow:0 20px 60px rgba(0,0,0,0.25);
  animation:fadeUp 0.5s ease both;
}
.login-logo{text-align:center;margin-bottom:1.8rem}
.login-logo h1{font-size:1.8rem;color:var(--navy);margin-bottom:0.3rem}
.login-logo h1 b{color:var(--blue)}
.login-logo p{font-size:0.82rem;color:var(--muted)}
.login-tabs{display:flex;gap:0;background:var(--bg);border-radius:8px;padding:4px;margin-bottom:1.5rem}
.ltab{
  flex:1;padding:0.5rem;text-align:center;font-size:0.75rem;font-weight:700;
  border-radius:6px;cursor:pointer;transition:all 0.2s;color:var(--muted);
}
.ltab.on{background:#fff;color:var(--navy);box-shadow:var(--shadow)}
.login-role-icon{text-align:center;font-size:2.2rem;margin-bottom:0.8rem}
.login-form-title{font-size:1rem;font-weight:800;color:var(--navy);text-align:center;margin-bottom:1.2rem}
.field{margin-bottom:1rem}
.field label{display:block;font-size:0.75rem;font-weight:700;color:var(--muted);margin-bottom:0.3rem;text-transform:uppercase;letter-spacing:0.05em}
.field input{
  width:100%;padding:0.7rem 0.9rem;border:2px solid var(--border);
  border-radius:8px;font-size:0.9rem;font-family:inherit;
  outline:none;transition:border-color 0.2s;
}
.field input:focus{border-color:var(--blue)}
.login-btn{
  width:100%;padding:0.85rem;background:var(--blue);color:#fff;
  border:none;border-radius:8px;font-size:0.9rem;font-weight:800;
  cursor:pointer;transition:background 0.2s,transform 0.1s;
  font-family:inherit;margin-top:0.5rem;
}
.login-btn:hover{background:#0D47A1;transform:translateY(-1px)}
.login-btn:active{transform:translateY(0)}
.login-error{
  background:#FFEBEE;color:var(--red);border:1px solid #FFCDD2;
  border-radius:7px;padding:0.6rem 0.9rem;font-size:0.8rem;
  font-weight:700;text-align:center;margin-top:0.8rem;display:none;
}
.login-hint{
  background:var(--bg);border-radius:7px;padding:0.6rem 0.9rem;
  font-size:0.72rem;color:var(--muted);margin-top:1rem;text-align:center;
}
.login-hint b{color:var(--navy)}

/* ══════════════════════════
   SUPERADMIN DASHBOARD
══════════════════════════ */
#adminScreen{background:var(--bg)}
#adminScreen.active{display:block}
.admin-nav{
  background:var(--navy);padding:0 1.5rem;height:58px;
  display:flex;align-items:center;justify-content:space-between;
  position:sticky;top:0;z-index:999;
}
.admin-nav-brand{font-family:'Merriweather',serif;color:#fff;font-size:1rem;font-style:italic}
.admin-nav-brand b{font-style:normal;color:#64B5F6}
.admin-nav-right{display:flex;align-items:center;gap:1rem}
.admin-badge{
  background:rgba(100,181,246,0.18);color:#90CAF9;
  border:1px solid rgba(100,181,246,0.3);border-radius:100px;
  padding:0.2rem 0.75rem;font-size:0.68rem;font-weight:700;
}
.signout-btn{
  background:rgba(255,255,255,0.1);color:#fff;border:1px solid rgba(255,255,255,0.2);
  border-radius:7px;padding:0.3rem 0.75rem;font-size:0.72rem;font-weight:700;
  cursor:pointer;transition:background 0.2s;font-family:inherit;
}
.signout-btn:hover{background:rgba(255,255,255,0.2)}
.admin-layout{display:flex;min-height:calc(100vh - 58px)}
.admin-sidebar{
  width:220px;background:#fff;border-right:1px solid var(--border);
  padding:1rem 0;flex-shrink:0;position:sticky;top:58px;height:calc(100vh - 58px);overflow-y:auto;
}
.sidebar-section{padding:0.4rem 1rem 0.2rem;font-size:0.65rem;font-weight:800;text-transform:uppercase;letter-spacing:0.15em;color:var(--muted)}
.sidebar-item{
  display:flex;align-items:center;gap:0.7rem;
  padding:0.6rem 1rem;font-size:0.8rem;color:var(--muted);
  cursor:pointer;transition:all 0.15s;border-left:3px solid transparent;
  font-weight:600;
}
.sidebar-item:hover{background:var(--bg);color:var(--navy)}
.sidebar-item.on{background:var(--bg);color:var(--blue);border-left-color:var(--blue);font-weight:800}
.admin-main{flex:1;padding:2rem;overflow-y:auto}
.admin-page{display:none}
.admin-page.on{display:block}
.page-title{font-size:1.4rem;font-weight:900;color:var(--navy);margin-bottom:0.3rem}
.page-sub{font-size:0.85rem;color:var(--muted);margin-bottom:1.8rem}

/* stat cards */
.stat-cards{display:grid;grid-template-columns:repeat(auto-fill,minmax(160px,1fr));gap:1rem;margin-bottom:2rem}
.stat-card{
  background:#fff;border:1px solid var(--border);border-radius:var(--r);
  padding:1.2rem;display:flex;flex-direction:column;gap:0.3rem;
}
.sc-icon{font-size:1.6rem}
.sc-num{font-size:1.8rem;font-weight:900;color:var(--navy)}
.sc-label{font-size:0.74rem;color:var(--muted);font-weight:600}

/* tables */
.tbl-wrap{background:#fff;border-radius:var(--r);border:1px solid var(--border);overflow:hidden;margin-bottom:1.5rem}
.tbl-head{padding:1rem 1.2rem;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid var(--border)}
.tbl-head h3{font-size:0.9rem;font-weight:800;color:var(--navy)}
table{width:100%;border-collapse:collapse;font-size:0.8rem}
th{background:var(--navy);color:#fff;padding:0.65rem 1rem;text-align:left;font-size:0.74rem;font-weight:700}
td{padding:0.65rem 1rem;border-bottom:1px solid var(--border);color:var(--text);vertical-align:middle}
tr:last-child td{border-bottom:none}
tr:nth-child(even) td{background:var(--surface2)}
tr:hover td{background:#EEF4FF}

/* badges */
.badge{display:inline-block;padding:0.18rem 0.55rem;border-radius:100px;font-size:0.68rem;font-weight:700}
.badge-green{background:#E8F5E9;color:var(--green)}
.badge-blue{background:#E3F2FD;color:var(--blue)}
.badge-orange{background:#FFF3E0;color:var(--orange)}
.badge-red{background:#FCE4EC;color:var(--red)}
.badge-purple{background:#EDE7F6;color:var(--purple)}

/* forms / modals */
.modal-overlay{
  display:none;position:fixed;inset:0;background:rgba(0,0,0,0.45);
  z-index:9000;align-items:center;justify-content:center;padding:1rem;
}
.modal-overlay.open{display:flex}
.modal{
  background:#fff;border-radius:14px;padding:2rem;width:100%;max-width:440px;
  box-shadow:0 20px 60px rgba(0,0,0,0.2);animation:fadeUp 0.25s ease both;
}
.modal h3{font-size:1.1rem;font-weight:800;color:var(--navy);margin-bottom:1.2rem}
.mfield{margin-bottom:1rem}
.mfield label{display:block;font-size:0.73rem;font-weight:700;color:var(--muted);margin-bottom:0.3rem;text-transform:uppercase}
.mfield input,.mfield select{
  width:100%;padding:0.62rem 0.85rem;border:2px solid var(--border);
  border-radius:7px;font-size:0.85rem;font-family:inherit;outline:none;
  transition:border-color 0.2s;
}
.mfield input:focus,.mfield select:focus{border-color:var(--blue)}
.modal-btns{display:flex;gap:0.7rem;margin-top:1.2rem;justify-content:flex-end}
.btn{padding:0.55rem 1.2rem;border-radius:7px;font-size:0.8rem;font-weight:700;cursor:pointer;border:none;font-family:inherit;transition:all 0.2s}
.btn-primary{background:var(--blue);color:#fff}
.btn-primary:hover{background:#0D47A1}
.btn-danger{background:var(--red);color:#fff}
.btn-danger:hover{background:#880E1B}
.btn-ghost{background:var(--bg);color:var(--muted);border:1px solid var(--border)}
.btn-ghost:hover{color:var(--navy);border-color:var(--navy)}
.add-btn{
  background:var(--blue);color:#fff;border:none;border-radius:7px;
  padding:0.45rem 1rem;font-size:0.76rem;font-weight:700;cursor:pointer;
  font-family:inherit;transition:background 0.2s;
}
.add-btn:hover{background:#0D47A1}
.action-ico{cursor:pointer;padding:0.2rem 0.4rem;border-radius:4px;transition:background 0.15s;font-size:0.9rem}
.action-ico:hover{background:var(--bg)}

/* callout */
.callout{border-radius:var(--r);padding:1rem 1.2rem;margin-bottom:1.2rem;display:flex;gap:0.8rem;font-size:0.84rem;border-left:4px solid}
.callout p{margin:0;line-height:1.6}
.callout strong{font-weight:800}
.c-tip{background:#E8F5E9;border-color:var(--green)}
.c-info{background:#E3F2FD;border-color:var(--sky)}
.c-warn{background:#FFF3E0;border-color:var(--orange)}

/* progress bars */
.prog-row{display:flex;align-items:center;gap:0.8rem;margin-bottom:0.6rem;font-size:0.78rem}
.prog-lbl{width:100px;color:var(--muted);flex-shrink:0}
.prog-track{flex:1;height:8px;background:#E0E0E0;border-radius:4px;overflow:hidden}
.prog-fill{height:100%;border-radius:4px}
.prog-pct{width:35px;text-align:right;font-weight:800;color:var(--navy)}

/* report card */
.report-card{
  background:#fff;border:2px solid var(--border);border-radius:var(--r);
  padding:1.5rem;margin-bottom:1rem;
}
.report-header{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:1rem;padding-bottom:1rem;border-bottom:1px solid var(--border)}
.report-school{font-size:1rem;font-weight:900;color:var(--navy)}
.report-term{font-size:0.75rem;color:var(--muted)}
.report-student{font-size:0.85rem}
.report-student b{color:var(--navy)}
.report-grades{width:100%;border-collapse:collapse;font-size:0.8rem;margin-bottom:0.8rem}
.report-grades th{background:var(--navy);color:#fff;padding:0.5rem 0.8rem;text-align:left;font-size:0.72rem}
.report-grades td{padding:0.5rem 0.8rem;border-bottom:1px solid var(--border)}
.report-footer{font-size:0.75rem;color:var(--muted);border-top:1px solid var(--border);padding-top:0.8rem;margin-top:0.5rem}
.print-btn{
  background:var(--navy);color:#fff;border:none;border-radius:7px;
  padding:0.5rem 1.2rem;font-size:0.78rem;font-weight:700;cursor:pointer;
  font-family:inherit;transition:background 0.2s;
}
.print-btn:hover{background:#1565C0}

/* section heading */
.sec-h{font-size:1rem;font-weight:800;color:var(--navy);margin:1.5rem 0 0.8rem;display:flex;align-items:center;gap:0.5rem}

/* grid 2 col */
.g2{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-bottom:1rem}
.g3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:1rem;margin-bottom:1rem}

/* announcement */
.announce{background:#fff;border:1px solid var(--border);border-radius:var(--r);padding:1rem 1.2rem;margin-bottom:0.75rem;border-left:4px solid var(--blue)}
.announce-title{font-size:0.88rem;font-weight:800;color:var(--navy);margin-bottom:0.2rem}
.announce-meta{font-size:0.72rem;color:var(--muted)}
.announce-body{font-size:0.82rem;color:var(--text);margin-top:0.4rem}

/* ══ ANIMATIONS ══ */
@keyframes fadeUp{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:none}}
.reveal{opacity:0;transform:translateY(12px);transition:opacity 0.45s,transform 0.45s}
.reveal.vis{opacity:1;transform:none}

/* ══ RESPONSIVE ══ */
@media(max-width:768px){
  .admin-sidebar{display:none}
  .g2,.g3{grid-template-columns:1fr}
  .stat-cards{grid-template-columns:1fr 1fr}
}
@media print{
  .admin-nav,.admin-sidebar,.add-btn,.print-btn,.action-ico,
  .sidebar-item,.modal-overlay{display:none!important}
  .admin-main{padding:0}
  .report-card{border:2px solid #000}
}
</style>
</head>
<body>

<!-- ══════════════════════════════════════
     SCREEN 1: LOGIN
══════════════════════════════════════ -->
<div id="loginScreen" class="screen active">
  <div class="login-box">
    <div class="login-logo">
      <h1><b>Edu</b>Build</h1>
      <p>School Management Platform</p>
    </div>

    <!-- Role tabs -->
    <div class="login-tabs">
      <div class="ltab on" onclick="setRole('superadmin')">👑 SuperAdmin</div>
      <div class="ltab" onclick="setRole('teacher')">👩‍🏫 Teacher</div>
      <div class="ltab" onclick="setRole('student')">👨‍🎓 Student</div>
      <div class="ltab" onclick="setRole('parent')">👪 Parent</div>
    </div>

    <div class="login-role-icon" id="roleIcon">👑</div>
    <div class="login-form-title" id="roleTitle">SuperAdmin Sign In</div>

    <div class="field">
      <label>Username / Email</label>
      <input type="text" id="loginUser" placeholder="Enter your username" autocomplete="username"/>
    </div>
    <div class="field">
      <label>Password</label>
      <input type="password" id="loginPass" placeholder="Enter your password" autocomplete="current-password"/>
    </div>

    <button class="login-btn" onclick="doLogin()">Sign In →</button>
    <div class="login-error" id="loginError">❌ Incorrect username or password. Please try again.</div>

    <div class="login-hint" id="loginHint">
      SuperAdmin: <b>Michel@2005</b> / <b>Michel@4321</b>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════
     SCREEN 2: SUPERADMIN DASHBOARD
══════════════════════════════════════ -->
<div id="adminScreen" class="screen">

  <!-- Top Nav -->
  <nav class="admin-nav">
    <div class="admin-nav-brand"><b>Edu</b>Build Admin</div>
    <div class="admin-nav-right">
      <span class="admin-badge">👑 SuperAdmin — Michel</span>
      <button class="signout-btn" onclick="signOut()">⬅ Sign Out</button>
    </div>
  </nav>

  <div class="admin-layout">

    <!-- Sidebar -->
    <aside class="admin-sidebar">
      <div class="sidebar-section">Overview</div>
      <div class="sidebar-item on" onclick="showPage('dashboard',this)">📊 Dashboard</div>
      <div class="sidebar-item" onclick="showPage('announcements',this)">📢 Announcements</div>

      <div class="sidebar-section" style="margin-top:0.5rem">Users</div>
      <div class="sidebar-item" onclick="showPage('users',this)">👥 All Users</div>
      <div class="sidebar-item" onclick="showPage('teachers',this)">👩‍🏫 Teachers</div>
      <div class="sidebar-item" onclick="showPage('students',this)">👨‍🎓 Students</div>
      <div class="sidebar-item" onclick="showPage('parents',this)">👪 Parents</div>

      <div class="sidebar-section" style="margin-top:0.5rem">Academics</div>
      <div class="sidebar-item" onclick="showPage('subjects',this)">📚 Subjects</div>
      <div class="sidebar-item" onclick="showPage('classes',this)">🏫 Classes</div>
      <div class="sidebar-item" onclick="showPage('lessons',this)">📖 Lessons</div>
      <div class="sidebar-section" style="margin-top:0.5rem">Progress</div>
      <div class="sidebar-item" onclick="showPage('grades',this)">📝 Grades</div>
      <div class="sidebar-item" onclick="showPage('attendance',this)">✅ Attendance</div>
      <div class="sidebar-item" onclick="showPage('reports',this)">📋 Reports</div>
      <div class="sidebar-section" style="margin-top:0.5rem">Settings</div>
      <div class="sidebar-item" onclick="showPage('settings',this)">⚙️ Settings</div>
    </aside>

    <!-- Main Content -->
    <main class="admin-main">

      <!-- ── DASHBOARD ── -->
      <div class="admin-page on" id="page-dashboard">
        <div class="page-title">Welcome back, Michel 👑</div>
        <div class="page-sub">Here's what's happening at your school today — Monday, 23 March 2026</div>

        <div class="stat-cards">
          <div class="stat-card reveal"><div class="sc-icon">👨‍🎓</div><div class="sc-num" id="totalStudents">247</div><div class="sc-label">Total Students</div></div>
          <div class="stat-card reveal"><div class="sc-icon">👩‍🏫</div><div class="sc-num" id="totalTeachers">18</div><div class="sc-label">Teachers</div></div>
          <div class="stat-card reveal"><div class="sc-icon">📚</div><div class="sc-num">8</div><div class="sc-label">Subjects</div></div>
          <div class="stat-card reveal"><div class="sc-icon">🏫</div><div class="sc-num">12</div><div class="sc-label">Classes</div></div>
          <div class="stat-card reveal"><div class="sc-icon">✅</div><div class="sc-num">91%</div><div class="sc-label">Attendance Today</div></div>
          <div class="stat-card reveal"><div class="sc-icon">📋</div><div class="sc-num">43</div><div class="sc-label">Reports Generated</div></div>
        </div>

        <div class="g2">
          <div class="tbl-wrap reveal">
            <div class="tbl-head"><h3>📊 School Average by Subject</h3></div>
            <div style="padding:1.2rem">
              <div class="prog-row"><div class="prog-lbl">Science</div><div class="prog-track"><div class="prog-fill" style="width:82%;background:#1565C0"></div></div><div class="prog-pct">82%</div></div>
              <div class="prog-row"><div class="prog-lbl">Mathematics</div><div class="prog-track"><div class="prog-fill" style="width:74%;background:#2E7D32"></div></div><div class="prog-pct">74%</div></div>
              <div class="prog-row"><div class="prog-lbl">Research</div><div class="prog-track"><div class="prog-fill" style="width:88%;background:#6A1B9A"></div></div><div class="prog-pct">88%</div></div>
              <div class="prog-row"><div class="prog-lbl">English</div><div class="prog-track"><div class="prog-fill" style="width:70%;background:#E65100"></div></div><div class="prog-pct">70%</div></div>
              <div class="prog-row"><div class="prog-lbl">History</div><div class="prog-track"><div class="prog-fill" style="width:77%;background:#00838F"></div></div><div class="prog-pct">77%</div></div>
              <div class="prog-row"><div class="prog-lbl">Geography</div><div class="prog-track"><div class="prog-fill" style="width:65%;background:#F57F17"></div></div><div class="prog-pct">65%</div></div>
            </div>
          </div>
          <div class="tbl-wrap reveal">
            <div class="tbl-head"><h3>🔔 Recent Activity</h3></div>
            <table>
              <thead><tr><th>Action</th><th>User</th><th>Time</th></tr></thead>
              <tbody>
                <tr><td>Grade submitted</td><td>Mrs. Okonkwo</td><td>9:12 AM</td></tr>
                <tr><td>New student registered</td><td>Admin</td><td>8:55 AM</td></tr>
                <tr><td>Report generated</td><td>Mr. Dlamini</td><td>8:40 AM</td></tr>
                <tr><td>Lesson uploaded</td><td>Ms. Patel</td><td>8:22 AM</td></tr>
                <tr><td>Attendance marked</td><td>Mrs. Okonkwo</td><td>7:58 AM</td></tr>
              </tbody>
            </table>
          </div>
        </div>

        <div class="callout c-tip reveal">
          <span style="font-size:1.2rem">💡</span>
          <p><strong>Quick Tip:</strong> Use the sidebar to manage users, view grades, generate reports, and post announcements. As SuperAdmin you have full access to every feature.</p>
        </div>
      </div>

      <!-- ── ANNOUNCEMENTS ── -->
      <div class="admin-page" id="page-announcements">
        <div class="page-title">📢 Announcements</div>
        <div class="page-sub">Post school-wide news visible to all users</div>
        <button class="add-btn" onclick="openModal('addAnnounce')">+ New Announcement</button>
        <div style="margin-top:1.2rem" id="announceList">
          <div class="announce"><div class="announce-title">Term 2 Exam Schedule Released</div><div class="announce-meta">Posted by Michel · 22 Mar 2026 · 📌 Pinned</div><div class="announce-body">Term 2 examinations will run from 15–25 April 2026. Please check the school calendar for your specific timetable. All students must arrive 15 minutes before their exam.</div></div>
          <div class="announce" style="border-left-color:var(--green)"><div class="announce-title">Science Fair Registration Open</div><div class="announce-meta">Posted by Michel · 20 Mar 2026</div><div class="announce-body">Students in Grades 8–12 are invited to register for the Annual Science Fair. Submissions close 5 April 2026. Contact your Science teacher for more details.</div></div>
          <div class="announce" style="border-left-color:var(--orange)"><div class="announce-title">School Closure — Public Holiday</div><div class="announce-meta">Posted by Michel · 18 Mar 2026</div><div class="announce-body">The school will be closed on Friday 27 March 2026 for a public holiday. Normal classes resume Monday 30 March 2026.</div></div>
        </div>
      </div>

      <!-- ── ALL USERS ── -->
      <div class="admin-page" id="page-users">
        <div class="page-title">👥 All Users</div>
        <div class="page-sub">View and manage every account on the platform</div>
        <div class="tbl-wrap reveal">
          <div class="tbl-head"><h3>User Accounts</h3><button class="add-btn" onclick="openModal('addUser')">+ Add User</button></div>
          <table>
            <thead><tr><th>Name</th><th>Username</th><th>Role</th><th>Status</th><th>Actions</th></tr></thead>
            <tbody id="userTable">
              <tr><td><b>Michel</b></td><td>Michel@2005</td><td><span class="badge badge-purple">👑 SuperAdmin</span></td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" title="Edit">✏️</span></td></tr>
              <tr><td>Sarah Okonkwo</td><td>s.okonkwo</td><td><span class="badge badge-blue">👩‍🏫 Teacher</span></td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)" title="Delete">🗑️</span> <span class="action-ico" title="Edit">✏️</span></td></tr>
              <tr><td>James Mokoena</td><td>j.mokoena</td><td><span class="badge" style="background:#E8F5E9;color:#1B5E20">👨‍🎓 Student</span></td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)" title="Delete">🗑️</span> <span class="action-ico" title="Edit">✏️</span></td></tr>
              <tr><td>Priya Patel</td><td>p.patel</td><td><span class="badge badge-blue">👩‍🏫 Teacher</span></td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)" title="Delete">🗑️</span> <span class="action-ico" title="Edit">✏️</span></td></tr>
              <tr><td>Lebo Dlamini</td><td>l.dlamini</td><td><span class="badge" style="background:#E8F5E9;color:#1B5E20">👨‍🎓 Student</span></td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)" title="Delete">🗑️</span> <span class="action-ico" title="Edit">✏️</span></td></tr>
              <tr><td>Mrs. Dlamini</td><td>parent.dlamini</td><td><span class="badge badge-orange">👪 Parent</span></td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)" title="Delete">🗑️</span> <span class="action-ico" title="Edit">✏️</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── TEACHERS ── -->
      <div class="admin-page" id="page-teachers">
        <div class="page-title">👩‍🏫 Teachers</div>
        <div class="page-sub">Manage teacher accounts and subject assignments</div>
        <div class="tbl-wrap reveal">
          <div class="tbl-head"><h3>Teaching Staff</h3><button class="add-btn" onclick="openModal('addTeacher')">+ Add Teacher</button></div>
          <table>
            <thead><tr><th>Name</th><th>Subject</th><th>Classes</th><th>Students</th><th>Status</th><th>Actions</th></tr></thead>
            <tbody id="teacherTable">
              <tr><td><b>Mrs. Sarah Okonkwo</b></td><td>Science</td><td>Gr 8A, 9B, 10A</td><td>87</td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Mr. David Nkosi</b></td><td>Mathematics</td><td>Gr 8B, 9A, 11A</td><td>92</td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Ms. Priya Patel</b></td><td>Research</td><td>Gr 10B, 11B, 12A</td><td>68</td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Mr. John Dlamini</b></td><td>English</td><td>Gr 8A, 9A, 10A</td><td>84</td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Mrs. Grace Moyo</b></td><td>History</td><td>Gr 9B, 10B</td><td>52</td><td><span class="badge badge-orange">On Leave</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── STUDENTS ── -->
      <div class="admin-page" id="page-students">
        <div class="page-title">👨‍🎓 Students</div>
        <div class="page-sub">Manage student enrolment and progress</div>
        <div class="tbl-wrap reveal">
          <div class="tbl-head"><h3>Student Register</h3><button class="add-btn" onclick="openModal('addStudent')">+ Enrol Student</button></div>
          <table>
            <thead><tr><th>Name</th><th>Grade</th><th>Class</th><th>Avg Score</th><th>Attendance</th><th>Actions</th></tr></thead>
            <tbody id="studentTable">
              <tr><td><b>James Mokoena</b></td><td>Grade 10</td><td>10A</td><td><span class="badge badge-green">78%</span></td><td>92%</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Lebo Dlamini</b></td><td>Grade 10</td><td>10B</td><td><span class="badge badge-blue">85%</span></td><td>96%</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Amara Osei</b></td><td>Grade 9</td><td>9A</td><td><span class="badge badge-orange">61%</span></td><td>78%</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Thabo Nkosi</b></td><td>Grade 11</td><td>11A</td><td><span class="badge badge-green">90%</span></td><td>98%</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Zanele Moyo</b></td><td>Grade 8</td><td>8B</td><td><span class="badge badge-red">55%</span></td><td>72%</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Sipho Ndlovu</b></td><td>Grade 12</td><td>12A</td><td><span class="badge badge-green">82%</span></td><td>94%</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── PARENTS ── -->
      <div class="admin-page" id="page-parents">
        <div class="page-title">👪 Parents</div>
        <div class="page-sub">Manage parent accounts linked to students</div>
        <div class="tbl-wrap reveal">
          <div class="tbl-head"><h3>Parent Accounts</h3><button class="add-btn" onclick="openModal('addParent')">+ Add Parent</button></div>
          <table>
            <thead><tr><th>Parent Name</th><th>Child</th><th>Child Grade</th><th>Contact</th><th>Actions</th></tr></thead>
            <tbody>
              <tr><td><b>Mrs. Mokoena</b></td><td>James Mokoena</td><td>Grade 10</td><td>parent.mokoena@email.com</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Mr. Dlamini Sr.</b></td><td>Lebo Dlamini</td><td>Grade 10</td><td>parent.dlamini@email.com</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Mrs. Osei</b></td><td>Amara Osei</td><td>Grade 9</td><td>parent.osei@email.com</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Mr. Nkosi Sr.</b></td><td>Thabo Nkosi</td><td>Grade 11</td><td>parent.nkosi@email.com</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── SUBJECTS ── -->
      <div class="admin-page" id="page-subjects">
        <div class="page-title">📚 Subjects</div>
        <div class="page-sub">All subjects offered at the school</div>
        <button class="add-btn" onclick="openModal('addSubject')">+ Add Subject</button>
        <div class="tbl-wrap reveal" style="margin-top:1rem">
          <table>
            <thead><tr><th>Subject</th><th>Teacher</th><th>Classes</th><th>Students</th><th>Avg Score</th><th>Actions</th></tr></thead>
            <tbody id="subjectTable">
              <tr><td><b>🔬 Science</b></td><td>Mrs. Okonkwo</td><td>6</td><td>87</td><td><span class="badge badge-green">82%</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>➕ Mathematics</b></td><td>Mr. Nkosi</td><td>6</td><td>92</td><td><span class="badge badge-blue">74%</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>🔍 Research</b></td><td>Ms. Patel</td><td>4</td><td>68</td><td><span class="badge badge-green">88%</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>📖 English</b></td><td>Mr. Dlamini</td><td>6</td><td>84</td><td><span class="badge badge-orange">70%</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>🌍 History</b></td><td>Mrs. Moyo</td><td>4</td><td>52</td><td><span class="badge badge-blue">77%</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>🗺️ Geography</b></td><td>TBA</td><td>3</td><td>44</td><td><span class="badge badge-orange">65%</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── CLASSES ── -->
      <div class="admin-page" id="page-classes">
        <div class="page-title">🏫 Classes</div>
        <div class="page-sub">Manage class groups and enrolments</div>
        <button class="add-btn" onclick="openModal('addClass')">+ Add Class</button>
        <div class="tbl-wrap reveal" style="margin-top:1rem">
          <table>
            <thead><tr><th>Class</th><th>Grade</th><th>Teacher</th><th>Students</th><th>Actions</th></tr></thead>
            <tbody id="classTable">
              <tr><td><b>Class 8A</b></td><td>Grade 8</td><td>Mr. Dlamini</td><td>22</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Class 8B</b></td><td>Grade 8</td><td>Mr. Nkosi</td><td>21</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Class 9A</b></td><td>Grade 9</td><td>Mr. Nkosi</td><td>24</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Class 9B</b></td><td>Grade 9</td><td>Mrs. Okonkwo</td><td>23</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Class 10A</b></td><td>Grade 10</td><td>Mrs. Okonkwo</td><td>25</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Class 10B</b></td><td>Grade 10</td><td>Ms. Patel</td><td>24</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Class 11A</b></td><td>Grade 11</td><td>Mr. Nkosi</td><td>22</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
              <tr><td><b>Class 12A</b></td><td>Grade 12</td><td>Ms. Patel</td><td>20</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── LESSONS ── -->
      <div class="admin-page" id="page-lessons">
        <div class="page-title">📖 Lessons</div>
        <div class="page-sub">All uploaded lessons and learning materials</div>
        <button class="add-btn" onclick="openModal('addLesson')">+ Upload Lesson</button>
        <div class="tbl-wrap reveal" style="margin-top:1rem">
          <table>
            <thead><tr><th>Lesson Title</th><th>Subject</th><th>Grade</th><th>Teacher</th><th>Date</th><th>Actions</th></tr></thead>
            <tbody id="lessonTable">
              <tr><td><b>Introduction to Cell Biology</b></td><td>Science</td><td>Grade 10</td><td>Mrs. Okonkwo</td><td>20 Mar 2026</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>Quadratic Equations</b></td><td>Mathematics</td><td>Grade 11</td><td>Mr. Nkosi</td><td>19 Mar 2026</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>Research Methodology — Part 2</b></td><td>Research</td><td>Grade 12</td><td>Ms. Patel</td><td>18 Mar 2026</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>Shakespeare — Hamlet Overview</b></td><td>English</td><td>Grade 10</td><td>Mr. Dlamini</td><td>17 Mar 2026</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>World War II Causes</b></td><td>History</td><td>Grade 9</td><td>Mrs. Moyo</td><td>16 Mar 2026</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
              <tr><td><b>Photosynthesis Lab Report</b></td><td>Science</td><td>Grade 9</td><td>Mrs. Okonkwo</td><td>15 Mar 2026</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── GRADES ── -->
      <div class="admin-page" id="page-grades">
        <div class="page-title">📝 Grades</div>
        <div class="page-sub">View and manage student grades across all subjects</div>
        <button class="add-btn" onclick="openModal('addGrade')">+ Enter Grade</button>
        <div class="tbl-wrap reveal" style="margin-top:1rem">
          <table>
            <thead><tr><th>Student</th><th>Subject</th><th>Grade</th><th>Assignment</th><th>Score</th><th>Teacher</th></tr></thead>
            <tbody id="gradeTable">
              <tr><td>James Mokoena</td><td>Science</td><td>10A</td><td>Cell Biology Test</td><td><span class="badge badge-green">84%</span></td><td>Mrs. Okonkwo</td></tr>
              <tr><td>James Mokoena</td><td>Mathematics</td><td>10A</td><td>Algebra Quiz</td><td><span class="badge badge-blue">72%</span></td><td>Mr. Nkosi</td></tr>
              <tr><td>Lebo Dlamini</td><td>Research</td><td>10B</td><td>Research Paper 1</td><td><span class="badge badge-green">90%</span></td><td>Ms. Patel</td></tr>
              <tr><td>Amara Osei</td><td>English</td><td>9A</td><td>Essay Assignment</td><td><span class="badge badge-orange">61%</span></td><td>Mr. Dlamini</td></tr>
              <tr><td>Thabo Nkosi</td><td>Mathematics</td><td>11A</td><td>Calculus Test</td><td><span class="badge badge-green">93%</span></td><td>Mr. Nkosi</td></tr>
              <tr><td>Zanele Moyo</td><td>Science</td><td>8B</td><td>Lab Report</td><td><span class="badge badge-red">55%</span></td><td>Mrs. Okonkwo</td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── ATTENDANCE ── -->
      <div class="admin-page" id="page-attendance">
        <div class="page-title">✅ Attendance</div>
        <div class="page-sub">Daily attendance records for all students</div>
        <div class="callout c-info" style="margin-bottom:1.2rem">
          <span style="font-size:1.1rem">ℹ️</span>
          <p><strong>Today's attendance rate: 91%</strong> — 225 of 247 students present. 22 absences recorded. 3 parents have been notified automatically.</p>
        </div>
        <div class="tbl-wrap reveal">
          <div class="tbl-head"><h3>Attendance Register — 23 Mar 2026</h3></div>
          <table>
            <thead><tr><th>Student</th><th>Class</th><th>Status</th><th>Days Present</th><th>Attendance %</th></tr></thead>
            <tbody>
              <tr><td>James Mokoena</td><td>10A</td><td><span class="badge badge-green">✓ Present</span></td><td>42/46</td><td>91%</td></tr>
              <tr><td>Lebo Dlamini</td><td>10B</td><td><span class="badge badge-green">✓ Present</span></td><td>44/46</td><td>96%</td></tr>
              <tr><td>Amara Osei</td><td>9A</td><td><span class="badge badge-red">✗ Absent</span></td><td>36/46</td><td>78%</td></tr>
              <tr><td>Thabo Nkosi</td><td>11A</td><td><span class="badge badge-green">✓ Present</span></td><td>45/46</td><td>98%</td></tr>
              <tr><td>Zanele Moyo</td><td>8B</td><td><span class="badge badge-orange">⚠ Late</span></td><td>33/46</td><td>72%</td></tr>
              <tr><td>Sipho Ndlovu</td><td>12A</td><td><span class="badge badge-green">✓ Present</span></td><td>43/46</td><td>93%</td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- ── REPORTS ── -->
      <div class="admin-page" id="page-reports">
        <div class="page-title">📋 Reports</div>
        <div class="page-sub">Generate and view student term reports</div>
        <button class="print-btn" onclick="window.print()">🖨️ Print This Report</button>

        <div class="report-card reveal" style="margin-top:1.2rem">
          <div class="report-header">
            <div>
              <div class="report-school">🏫 EduBuild Academy</div>
              <div class="report-term">Term 1 · January – March 2026</div>
            </div>
            <div style="text-align:right" class="report-student">
              <b>James Mokoena</b><br>
              Grade 10A · Student ID: EB-2026-047<br>
              <span style="font-size:0.72rem;color:var(--muted)">DOB: 14 Jun 2010</span>
            </div>
          </div>
          <table class="report-grades">
            <thead><tr><th>Subject</th><th>Teacher</th><th>Term Mark</th><th>Exam</th><th>Final %</th><th>Grade</th></tr></thead>
            <tbody>
              <tr><td>Science</td><td>Mrs. Okonkwo</td><td>82%</td><td>86%</td><td><b>84%</b></td><td><span class="badge badge-green">A</span></td></tr>
              <tr><td>Mathematics</td><td>Mr. Nkosi</td><td>70%</td><td>74%</td><td><b>72%</b></td><td><span class="badge badge-blue">B</span></td></tr>
              <tr><td>Research</td><td>Ms. Patel</td><td>88%</td><td>92%</td><td><b>90%</b></td><td><span class="badge badge-green">A</span></td></tr>
              <tr><td>English</td><td>Mr. Dlamini</td><td>66%</td><td>70%</td><td><b>68%</b></td><td><span class="badge badge-blue">B</span></td></tr>
              <tr><td>History</td><td>Mrs. Moyo</td><td>75%</td><td>79%</td><td><b>77%</b></td><td><span class="badge badge-blue">B</span></td></tr>
            </tbody>
          </table>
          <div style="display:flex;gap:2rem;font-size:0.82rem;padding:0.5rem 0">
            <div><strong>Overall Average:</strong> 78.2%</div>
            <div><strong>Attendance:</strong> 92%</div>
            <div><strong>Conduct:</strong> <span class="badge badge-green">Excellent</span></div>
            <div><strong>Position:</strong> 12 of 25</div>
          </div>
          <div class="report-footer">
            <strong>Teacher Comment:</strong> James has shown excellent progress this term, particularly in Research and Science. Mathematics needs more focused practice. Keep up the good work.<br>
            <strong>Principal:</strong> Michel (SuperAdmin) &nbsp;&nbsp; <strong>Date:</strong> 23 March 2026
          </div>
        </div>
      </div>

      <!-- ── SETTINGS ── -->
      <div class="admin-page" id="page-settings">
        <div class="page-title">⚙️ Settings</div>
        <div class="page-sub">Configure your school platform</div>

        <div class="g2">
          <div class="tbl-wrap reveal">
            <div class="tbl-head"><h3>School Information</h3></div>
            <div style="padding:1.2rem;display:flex;flex-direction:column;gap:0.9rem">
              <div class="mfield"><label>School Name</label><input type="text" value="EduBuild Academy"/></div>
              <div class="mfield"><label>School Address</label><input type="text" value="123 Education Street, Johannesburg"/></div>
              <div class="mfield"><label>Principal / SuperAdmin</label><input type="text" value="Michel" readonly/></div>
              <div class="mfield"><label>Contact Email</label><input type="text" value="admin@edubuild.school"/></div>
              <div class="mfield"><label>Current Term</label><input type="text" value="Term 1 · Jan – Mar 2026"/></div>
              <button class="btn btn-primary" style="align-self:flex-start" onclick="alert('Settings saved successfully!')">Save Changes</button>
            </div>
          </div>
          <div class="tbl-wrap reveal">
            <div class="tbl-head"><h3>SuperAdmin Account</h3></div>
            <div style="padding:1.2rem;display:flex;flex-direction:column;gap:0.9rem">
              <div class="mfield"><label>Username</label><input type="text" value="Michel@2005" readonly/></div>
              <div class="mfield"><label>Display Name</label><input type="text" value="Michel"/></div>
              <div class="mfield"><label>Email</label><input type="text" value="michel@edubuild.school"/></div>
              <div class="mfield"><label>New Password</label><input type="password" placeholder="Leave blank to keep current"/></div>
              <div class="callout c-warn" style="margin:0"><span>⚠️</span><p style="font-size:0.76rem">Changing your password will require you to sign in again.</p></div>
              <button class="btn btn-primary" style="align-self:flex-start" onclick="alert('Account updated successfully!')">Update Account</button>
            </div>
          </div>
        </div>
      </div>

    </main>
  </div>
</div>

<!-- ══════════════════════════════════════
     MODALS
══════════════════════════════════════ -->

<!-- Add User Modal -->
<div class="modal-overlay" id="modal-addUser">
  <div class="modal">
    <h3>➕ Add New User</h3>
    <div class="mfield"><label>Full Name</label><input type="text" id="nu-name" placeholder="e.g. John Smith"/></div>
    <div class="mfield"><label>Username</label><input type="text" id="nu-user" placeholder="e.g. j.smith"/></div>
    <div class="mfield"><label>Role</label><select id="nu-role"><option>👩‍🏫 Teacher</option><option>👨‍🎓 Student</option><option>👪 Parent</option></select></div>
    <div class="mfield"><label>Password</label><input type="password" id="nu-pass" placeholder="Set initial password"/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addUser')">Cancel</button>
      <button class="btn btn-primary" onclick="addUser()">Add User</button>
    </div>
  </div>
</div>

<!-- Add Teacher Modal -->
<div class="modal-overlay" id="modal-addTeacher">
  <div class="modal">
    <h3>👩‍🏫 Add Teacher</h3>
    <div class="mfield"><label>Full Name</label><input type="text" id="nt-name" placeholder="e.g. Mr. John Smith"/></div>
    <div class="mfield"><label>Subject</label><input type="text" id="nt-subject" placeholder="e.g. Mathematics"/></div>
    <div class="mfield"><label>Classes</label><input type="text" id="nt-classes" placeholder="e.g. Gr 9A, 10B"/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addTeacher')">Cancel</button>
      <button class="btn btn-primary" onclick="addTeacher()">Add Teacher</button>
    </div>
  </div>
</div>

<!-- Add Student Modal -->
<div class="modal-overlay" id="modal-addStudent">
  <div class="modal">
    <h3>👨‍🎓 Enrol Student</h3>
    <div class="mfield"><label>Full Name</label><input type="text" id="ns-name" placeholder="e.g. Sipho Dlamini"/></div>
    <div class="mfield"><label>Grade</label><select id="ns-grade"><option>Grade 8</option><option>Grade 9</option><option>Grade 10</option><option>Grade 11</option><option>Grade 12</option></select></div>
    <div class="mfield"><label>Class</label><input type="text" id="ns-class" placeholder="e.g. 10A"/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addStudent')">Cancel</button>
      <button class="btn btn-primary" onclick="addStudent()">Enrol Student</button>
    </div>
  </div>
</div>

<!-- Add Parent Modal -->
<div class="modal-overlay" id="modal-addParent">
  <div class="modal">
    <h3>👪 Add Parent</h3>
    <div class="mfield"><label>Parent Name</label><input type="text" id="np-name" placeholder="e.g. Mrs. Dlamini"/></div>
    <div class="mfield"><label>Child's Name</label><input type="text" id="np-child" placeholder="e.g. Lebo Dlamini"/></div>
    <div class="mfield"><label>Email</label><input type="text" id="np-email" placeholder="e.g. parent@email.com"/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addParent')">Cancel</button>
      <button class="btn btn-primary" onclick="addParent()">Add Parent</button>
    </div>
  </div>
</div>

<!-- Add Subject Modal -->
<div class="modal-overlay" id="modal-addSubject">
  <div class="modal">
    <h3>📚 Add Subject</h3>
    <div class="mfield"><label>Subject Name</label><input type="text" id="nsub-name" placeholder="e.g. Physical Science"/></div>
    <div class="mfield"><label>Assigned Teacher</label><input type="text" id="nsub-teacher" placeholder="e.g. Mrs. Okonkwo"/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addSubject')">Cancel</button>
      <button class="btn btn-primary" onclick="addSubject()">Add Subject</button>
    </div>
  </div>
</div>

<!-- Add Class Modal -->
<div class="modal-overlay" id="modal-addClass">
  <div class="modal">
    <h3>🏫 Add Class</h3>
    <div class="mfield"><label>Class Name</label><input type="text" id="ncl-name" placeholder="e.g. Class 12B"/></div>
    <div class="mfield"><label>Grade</label><select id="ncl-grade"><option>Grade 8</option><option>Grade 9</option><option>Grade 10</option><option>Grade 11</option><option>Grade 12</option></select></div>
    <div class="mfield"><label>Teacher</label><input type="text" id="ncl-teacher" placeholder="e.g. Mr. Nkosi"/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addClass')">Cancel</button>
      <button class="btn btn-primary" onclick="addClass()">Add Class</button>
    </div>
  </div>
</div>

<!-- Add Lesson Modal -->
<div class="modal-overlay" id="modal-addLesson">
  <div class="modal">
    <h3>📖 Upload Lesson</h3>
    <div class="mfield"><label>Lesson Title</label><input type="text" id="nl-title" placeholder="e.g. Introduction to Genetics"/></div>
    <div class="mfield"><label>Subject</label><input type="text" id="nl-sub" placeholder="e.g. Science"/></div>
    <div class="mfield"><label>Grade</label><select id="nl-grade"><option>Grade 8</option><option>Grade 9</option><option>Grade 10</option><option>Grade 11</option><option>Grade 12</option></select></div>
    <div class="mfield"><label>Teacher</label><input type="text" id="nl-teacher" placeholder="e.g. Mrs. Okonkwo"/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addLesson')">Cancel</button>
      <button class="btn btn-primary" onclick="addLesson()">Upload Lesson</button>
    </div>
  </div>
</div>

<!-- Add Grade Modal -->
<div class="modal-overlay" id="modal-addGrade">
  <div class="modal">
    <h3>📝 Enter Grade</h3>
    <div class="mfield"><label>Student Name</label><input type="text" id="ng-student" placeholder="e.g. James Mokoena"/></div>
    <div class="mfield"><label>Subject</label><input type="text" id="ng-sub" placeholder="e.g. Science"/></div>
    <div class="mfield"><label>Assignment</label><input type="text" id="ng-assign" placeholder="e.g. Chapter 3 Test"/></div>
    <div class="mfield"><label>Score (%)</label><input type="number" id="ng-score" placeholder="e.g. 85" min="0" max="100"/></div>
    <div class="mfield"><label>Teacher</label><input type="text" id="ng-teacher" placeholder="e.g. Mrs. Okonkwo"/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addGrade')">Cancel</button>
      <button class="btn btn-primary" onclick="addGrade()">Save Grade</button>
    </div>
  </div>
</div>

<!-- Add Announcement Modal -->
<div class="modal-overlay" id="modal-addAnnounce">
  <div class="modal">
    <h3>📢 New Announcement</h3>
    <div class="mfield"><label>Title</label><input type="text" id="na-title" placeholder="Announcement title"/></div>
    <div class="mfield"><label>Message</label><input type="text" id="na-body" placeholder="Write your announcement here..."/></div>
    <div class="modal-btns">
      <button class="btn btn-ghost" onclick="closeModal('addAnnounce')">Cancel</button>
      <button class="btn btn-primary" onclick="addAnnounce()">Post Announcement</button>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════
     JAVASCRIPT
══════════════════════════════════════ -->
<script>
/* ──────────────────────────────────────
   AUTH — CREDENTIALS
   SuperAdmin: Michel@2005 / Michel@4321
────────────────────────────────────── */
const CREDENTIALS = {
  superadmin: { user: 'Michel@2005', pass: 'Michel@4321', role: 'superadmin' },
  teacher:    { user: 'teacher',     pass: 'teacher123',  role: 'teacher' },
  student:    { user: 'student',     pass: 'student123',  role: 'student' },
  parent:     { user: 'parent',      pass: 'parent123',   role: 'parent' }
};

const ROLE_META = {
  superadmin: { icon:'👑', title:'SuperAdmin Sign In', hint:'Username: <b>Michel@2005</b> &nbsp;|&nbsp; Password: <b>Michel@4321</b>' },
  teacher:    { icon:'👩‍🏫', title:'Teacher Sign In',    hint:'Username: <b>teacher</b> &nbsp;|&nbsp; Password: <b>teacher123</b>' },
  student:    { icon:'👨‍🎓', title:'Student Sign In',    hint:'Username: <b>student</b> &nbsp;|&nbsp; Password: <b>student123</b>' },
  parent:     { icon:'👪',  title:'Parent Sign In',     hint:'Username: <b>parent</b> &nbsp;|&nbsp; Password: <b>parent123</b>' }
};

let currentRole = 'superadmin';

function setRole(role) {
  currentRole = role;
  document.querySelectorAll('.ltab').forEach(t => t.classList.remove('on'));
  const idx = {superadmin:0,teacher:1,student:2,parent:3}[role];
  document.querySelectorAll('.ltab')[idx].classList.add('on');
  document.getElementById('roleIcon').textContent = ROLE_META[role].icon;
  document.getElementById('roleTitle').textContent = ROLE_META[role].title;
  document.getElementById('loginHint').innerHTML = ROLE_META[role].hint;
  document.getElementById('loginError').style.display = 'none';
  document.getElementById('loginUser').value = '';
  document.getElementById('loginPass').value = '';
}

function doLogin() {
  const u = document.getElementById('loginUser').value.trim();
  const p = document.getElementById('loginPass').value;
  const cred = CREDENTIALS[currentRole];
  const err = document.getElementById('loginError');

  if (u === cred.user && p === cred.pass) {
    err.style.display = 'none';
    if (currentRole === 'superadmin') {
      document.getElementById('loginScreen').classList.remove('active');
      document.getElementById('adminScreen').classList.add('active');
      initReveal();
    } else {
      // Other roles — show coming soon message
      err.style.display = 'block';
      err.style.background = '#E8F5E9';
      err.style.color = '#2E7D32';
      err.style.border = '1px solid #C8E6C9';
      err.textContent = '✅ Login successful! ' + currentRole.charAt(0).toUpperCase() + currentRole.slice(1) + ' dashboard coming soon.';
    }
  } else {
    err.style.display = 'block';
    err.style.background = '#FFEBEE';
    err.style.color = '#B71C1C';
    err.style.border = '1px solid #FFCDD2';
    err.textContent = '❌ Incorrect username or password. Please try again.';
    document.getElementById('loginPass').value = '';
    document.getElementById('loginPass').focus();
  }
}

// Allow Enter key on password field
document.addEventListener('DOMContentLoaded', () => {
  document.getElementById('loginPass').addEventListener('keydown', e => {
    if (e.key === 'Enter') doLogin();
  });
  document.getElementById('loginUser').addEventListener('keydown', e => {
    if (e.key === 'Enter') document.getElementById('loginPass').focus();
  });
});

function signOut() {
  document.getElementById('adminScreen').classList.remove('active');
  document.getElementById('loginScreen').classList.add('active');
  setRole('superadmin');
  document.getElementById('loginUser').value = '';
  document.getElementById('loginPass').value = '';
}

/* ──────────────────────────────────────
   SIDEBAR NAVIGATION
────────────────────────────────────── */
function showPage(name, el) {
  document.querySelectorAll('.admin-page').forEach(p => p.classList.remove('on'));
  document.querySelectorAll('.sidebar-item').forEach(s => s.classList.remove('on'));
  document.getElementById('page-' + name).classList.add('on');
  if (el) el.classList.add('on');
  initReveal();
}

/* ──────────────────────────────────────
   MODALS
────────────────────────────────────── */
function openModal(id) {
  document.getElementById('modal-' + id).classList.add('open');
}
function closeModal(id) {
  document.getElementById('modal-' + id).classList.remove('open');
}
// Close modal on overlay click
document.querySelectorAll('.modal-overlay').forEach(o => {
  o.addEventListener('click', e => { if (e.target === o) o.classList.remove('open'); });
});

/* ──────────────────────────────────────
   ADD FUNCTIONS — insert rows into tables
────────────────────────────────────── */
function todayStr() {
  const d = new Date();
  return d.toLocaleDateString('en-GB',{day:'numeric',month:'short',year:'numeric'});
}

function addUser() {
  const n = document.getElementById('nu-name').value.trim();
  const u = document.getElementById('nu-user').value.trim();
  const r = document.getElementById('nu-role').value;
  if (!n || !u) { alert('Please fill in all fields.'); return; }
  const roleMap = {'👩‍🏫 Teacher':'badge-blue','👨‍🎓 Student':'badge-green','👪 Parent':'badge-orange'};
  const tbody = document.getElementById('userTable');
  const row = tbody.insertRow();
  row.innerHTML = `<td><b>${n}</b></td><td>${u}</td><td><span class="badge ${roleMap[r]}">${r}</span></td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td>`;
  closeModal('addUser');
  document.getElementById('nu-name').value=''; document.getElementById('nu-user').value='';
  updateCount('totalStudents', r.includes('Student') ? 1 : 0);
  updateCount('totalTeachers', r.includes('Teacher') ? 1 : 0);
}

function addTeacher() {
  const n = document.getElementById('nt-name').value.trim();
  const s = document.getElementById('nt-subject').value.trim();
  const c = document.getElementById('nt-classes').value.trim();
  if (!n || !s) { alert('Please fill name and subject.'); return; }
  const tbody = document.getElementById('teacherTable');
  const row = tbody.insertRow();
  row.innerHTML = `<td><b>${n}</b></td><td>${s}</td><td>${c||'TBA'}</td><td>0</td><td><span class="badge badge-green">Active</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td>`;
  closeModal('addTeacher');
  document.getElementById('nt-name').value=''; document.getElementById('nt-subject').value=''; document.getElementById('nt-classes').value='';
  updateCount('totalTeachers', 1);
}

function addStudent() {
  const n = document.getElementById('ns-name').value.trim();
  const g = document.getElementById('ns-grade').value;
  const c = document.getElementById('ns-class').value.trim();
  if (!n) { alert('Please enter student name.'); return; }
  const tbody = document.getElementById('studentTable');
  const row = tbody.insertRow();
  row.innerHTML = `<td><b>${n}</b></td><td>${g}</td><td>${c||'TBA'}</td><td><span class="badge badge-blue">N/A</span></td><td>N/A</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td>`;
  closeModal('addStudent');
  document.getElementById('ns-name').value=''; document.getElementById('ns-class').value='';
  updateCount('totalStudents', 1);
}

function addParent() {
  const n = document.getElementById('np-name').value.trim();
  const ch = document.getElementById('np-child').value.trim();
  const em = document.getElementById('np-email').value.trim();
  if (!n || !ch) { alert('Please fill parent name and child name.'); return; }
  const rows = document.querySelectorAll('#page-parents tbody tr');
  const tbody = document.querySelector('#page-parents tbody');
  const row = tbody.insertRow();
  row.innerHTML = `<td><b>${n}</b></td><td>${ch}</td><td>—</td><td>${em||'—'}</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td>`;
  closeModal('addParent');
  document.getElementById('np-name').value=''; document.getElementById('np-child').value=''; document.getElementById('np-email').value='';
}

function addSubject() {
  const n = document.getElementById('nsub-name').value.trim();
  const t = document.getElementById('nsub-teacher').value.trim();
  if (!n) { alert('Please enter subject name.'); return; }
  const tbody = document.getElementById('subjectTable');
  const row = tbody.insertRow();
  row.innerHTML = `<td><b>📘 ${n}</b></td><td>${t||'TBA'}</td><td>0</td><td>0</td><td><span class="badge badge-blue">N/A</span></td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td>`;
  closeModal('addSubject');
  document.getElementById('nsub-name').value=''; document.getElementById('nsub-teacher').value='';
}

function addClass() {
  const n = document.getElementById('ncl-name').value.trim();
  const g = document.getElementById('ncl-grade').value;
  const t = document.getElementById('ncl-teacher').value.trim();
  if (!n) { alert('Please enter class name.'); return; }
  const tbody = document.getElementById('classTable');
  const row = tbody.insertRow();
  row.innerHTML = `<td><b>${n}</b></td><td>${g}</td><td>${t||'TBA'}</td><td>0</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span> <span class="action-ico">✏️</span></td>`;
  closeModal('addClass');
  document.getElementById('ncl-name').value=''; document.getElementById('ncl-teacher').value='';
}

function addLesson() {
  const title = document.getElementById('nl-title').value.trim();
  const sub = document.getElementById('nl-sub').value.trim();
  const gr = document.getElementById('nl-grade').value;
  const t = document.getElementById('nl-teacher').value.trim();
  if (!title) { alert('Please enter a lesson title.'); return; }
  const tbody = document.getElementById('lessonTable');
  const row = tbody.insertRow(0);
  row.innerHTML = `<td><b>${title}</b></td><td>${sub||'—'}</td><td>${gr}</td><td>${t||'—'}</td><td>${todayStr()}</td><td><span class="action-ico" onclick="delRow(this)">🗑️</span></td>`;
  closeModal('addLesson');
  document.getElementById('nl-title').value=''; document.getElementById('nl-sub').value=''; document.getElementById('nl-teacher').value='';
}

function addGrade() {
  const st = document.getElementById('ng-student').value.trim();
  const sb = document.getElementById('ng-sub').value.trim();
  const as = document.getElementById('ng-assign').value.trim();
  const sc = document.getElementById('ng-score').value;
  const t = document.getElementById('ng-teacher').value.trim();
  if (!st || !sc) { alert('Please enter student name and score.'); return; }
  const grade = parseInt(sc);
  const cls = grade >= 80 ? 'badge-green' : grade >= 60 ? 'badge-blue' : grade >= 50 ? 'badge-orange' : 'badge-red';
  const tbody = document.getElementById('gradeTable');
  const row = tbody.insertRow(0);
  row.innerHTML = `<td>${st}</td><td>${sb||'—'}</td><td>—</td><td>${as||'Assessment'}</td><td><span class="badge ${cls}">${sc}%</span></td><td>${t||'—'}</td>`;
  closeModal('addGrade');
  document.getElementById('ng-student').value=''; document.getElementById('ng-sub').value=''; document.getElementById('ng-assign').value=''; document.getElementById('ng-score').value=''; document.getElementById('ng-teacher').value='';
}

function addAnnounce() {
  const ti = document.getElementById('na-title').value.trim();
  const bo = document.getElementById('na-body').value.trim();
  if (!ti) { alert('Please enter an announcement title.'); return; }
  const colors = [
    'var(--blue)','var(--green)','var(--orange)','var(--purple)','var(--teal)'
  ];
  const col = colors[Math.floor(Math.random()*colors.length)];
  const list = document.getElementById('announceList');
  const div = document.createElement('div');
  div.className = 'announce';
  div.style.borderLeftColor = col;
  div.innerHTML = `<div class="announce-title">${ti}</div><div class="announce-meta">Posted by Michel · ${todayStr()} · 📌 New</div><div class="announce-body">${bo||''}</div>`;
  list.insertBefore(div, list.firstChild);
  closeModal('addAnnounce');
  document.getElementById('na-title').value=''; document.getElementById('na-body').value='';
}

/* ──────────────────────────────────────
   DELETE ROW
────────────────────────────────────── */
function delRow(el) {
  if (confirm('Are you sure you want to delete this record?')) {
    el.closest('tr').remove();
  }
}

/* ──────────────────────────────────────
   UPDATE STAT COUNTERS
────────────────────────────────────── */
function updateCount(id, delta) {
  const el = document.getElementById(id);
  if (el && delta !== 0) el.textContent = parseInt(el.textContent) + delta;
}

/* ──────────────────────────────────────
   SCROLL REVEAL
────────────────────────────────────── */
function initReveal() {
  setTimeout(() => {
    document.querySelectorAll('.reveal').forEach(el => {
      el.classList.add('vis');
    });
  }, 50);
}
</script>
</body>
</html>
