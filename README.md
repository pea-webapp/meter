<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ระบบจัดการมิเตอร์ - การไฟฟ้าส่วนภูมิภาค</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@400;500;600&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Sarabun', sans-serif;
            background-color: #f4f6f9;
            overflow-x: hidden;
        }

        /* Header Customization */
        .header {
            background-color: #ffffff;
            border-bottom: 5px solid #8e24aa; /* สีม่วงเข้ม */
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .logo-section {
            display: flex;
            align-items: center;
        }

        .pea-title {
            color: #8e24aa;
            font-weight: 600;
            font-size: 1.4rem;
            margin: 0;
            letter-spacing: 0.5px;
        }

        /* Sidebar Customization */
        .sidebar {
            background-color: #8e24aa;
            color: white;
            min-height: calc(100vh - 75px);
            width: 280px;
            transition: all 0.3s;
        }

        .toggle-area {
            background-color: #4a148c; /* สีม่วงมืดกว่า */
            padding: 10px 15px;
            text-align: right;
        }

        .sidebar-menu {
            margin-top: 20px;
        }

        .sidebar-menu a {
            color: rgba(255, 255, 255, 0.9);
            text-decoration: none;
            padding: 15px 25px;
            display: block;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 1rem;
            transition: 0.2s;
        }

        .sidebar-menu a:hover {
            background-color: rgba(255, 255, 255, 0.15);
            color: #ffffff;
            padding-left: 30px;
        }

        /* Main Content & Card */
        .main-container {
            background-color: #f8f9fa;
            /* ลายเส้นพื้นหลังจางๆ */
            background-image: radial-gradient(#d1d1d1 0.5px, transparent 0.5px);
            background-size: 20px 20px;
        }

        .login-card {
            border: none;
            border-radius: 8px;
            max-width: 450px;
            width: 90%;
        }

        .btn-submit {
            background-color: #007bff;
            padding: 10px 25px;
            font-weight: 500;
        }

        .sub-label {
            font-size: 0.85rem;
            color: #757575;
            display: block;
            margin-top: 4px;
        }
    </style>
</head>
<body class="d-flex flex-column vh-100">

    <header class="header d-flex justify-content-between align-items-center px-4 py-3 shadow-sm">
        <div class="logo-section">
            <h1 class="pea-title">การไฟฟ้าส่วนภูมิภาค</h1>
        </div>
        <div class="login-link">
            <a href="#" class="text-decoration-none fw-bold" style="color: #007bff;">เข้าสู่ระบบ</a>
        </div>
    </header>

    <div class="d-flex flex-grow-1">
        
        <aside class="sidebar shadow-lg">
            <div class="toggle-area">
                <span style="cursor:pointer; color:white;">☰</span>
            </div>
            <nav class="sidebar-menu">
                <a href="#">พิกัดมิเตอร์และหม้อแปลง</a>
                <a href="#">เช็คสถานะมิเตอร์</a>
                <a href="#">รายงานมิเตอร์ประจำเดือน</a>
                <a href="#">สับเปลี่ยนมิเตอร์ชำรุด</a> </nav>
        </aside>

        <main class="main-content flex-grow-1 d-flex justify-content-center align-items-center main-container">
            <div class="card login-card shadow-lg">
                <div class="card-body p-4 p-md-5">
                    <h2 class="mb-4" style="color: #333; font-weight: 500;">Login</h2>
                    <hr class="mb-4">
                    
                    <form>
                        <div class="mb-4">
                            <label class="form-label fw-bold">Username</label>
                            <input type="text" class="form-control form-control-lg">
                            <small class="sub-label">ใช้รหัสเดียวกับ Windows Logon (รหัสพนักงาน)</small>
                        </div>
                        
                        <div class="mb-4">
                            <label class="form-label fw-bold">Password</label>
                            <input type="password" class="form-control form-control-lg">
                            <small class="sub-label">สามารถเปลี่ยน Password ด้วยการกด Ctrl + Alt + Del เลือก Change a Password</small>
                        </div>
                        
                        <div class="mt-4">
                            <button type="submit" class="btn btn-primary btn-submit shadow-sm">เข้าสู่ระบบ</button>
                        </div>
                    </form>
                </div>
            </div>
        </main>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>r')">พิกัดมิเตอร์และหม้อแปลง</a>
    <a href="#" onclick="showPage('status')">เช็คสถานะมิเตอร์</a>
    <a href="#" onclick="showPage('report')">รายงานมิเตอร์ประจำเดือน</a>
    <a href="#" onclick="showPage('replace')">สับเปลี่ยนมิเตอร์ชำรุด</a>
    <a href="#" onclick="logout()">ออกจากระบบ</a>
  </div>

  <!-- Main Content -->
  <div class="main">
    <div id="meter" class="hidden">
      <h2>พิกัดมิเตอร์และหม้อแปลง</h2>
      <iframe src="https://docs.google.com/spreadsheets/d/1fFobMWKz6YgAvlLhuU-E1uJC05KGUKHZXpjdJtYNd08/edit?usp=sharing" width="100%" height="500"></iframe>
    </div>

    <div id="status" class="hidden">
      <h2>เช็คสถานะมิเตอร์</h2>
      <iframe src="https://docs.google.com/spreadsheets/d/1zW_ViGNyUwLlNuaVkKp58dmNu5W-ftC5g6HCB-OZ5Q8/edit?usp=sharing" width="100%" height="500"></iframe>
    </div>

    <div id="report" class="hidden">
      <h2>รายงานมิเตอร์ประจำเดือน</h2>
      <a href="https://drive.google.com/drive/folders/1xG9IMk-Mo5KqCZq9uoj-fJsezHv3Z7oT" target="_blank" class="btn btn-success">แนบไฟล์รายงาน</a>
    </div>

    <div id="replace" class="hidden">
      <h2>สับเปลี่ยนมิเตอร์ชำรุด</h2>
      <iframe src="https://docs.google.com/spreadsheets/d/1uuwjTLQGH3I02mpmX7-MNaRjahp15SD_c77BoSuow6Q/edit?usp=sharing" width="100%" height="500"></iframe>
    </div>
  </div>

  <script>
    if (sessionStorage.getItem("loggedIn") !== "true") {
      alert("กรุณาเข้าสู่ระบบก่อน");
      window.location.href = "index.html";
    }

    function showPage(pageId) {
      document.querySelectorAll('.main > div').forEach(div => div.classList.add("hidden"));
      document.getElementById(pageId).classList.remove("hidden");
    }

    function logout() {
      sessionStorage.clear();
      window.location.href = "index.html";
    }
  </script>
</body>
</html>
