<!DOCTYPE html>
<html lang="th">
<head>
  <meta charset="UTF-8">
  <title>PEA Dashboard</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body { font-family: 'Sarabun', sans-serif; background-color: #f4f6f9; }
    .sidebar { background-color: #8e24aa; color: white; min-height: 100vh; width: 250px; }
    .sidebar a { color: white; display: block; padding: 12px; text-decoration: none; }
    .sidebar a:hover { background-color: #6a1b9a; }
    .main { flex-grow: 1; padding: 20px; }
    .hidden { display: none; }
  </style>
</head>
<body class="d-flex">

  <!-- Sidebar -->
  <div class="sidebar">
    <h4 class="p-3">การไฟฟ้าส่วนภูมิภาค</h4>
    <a href="#" onclick="showPage('meter')">พิกัดมิเตอร์และหม้อแปลง</a>
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
