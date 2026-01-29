<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>School Management System</title>
  <style>
    * {
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      margin: 0;
      background: #f4f6f8;
    }

    header {
      background: #2c3e50;
      color: white;
      padding: 15px;
      text-align: center;
      font-size: 22px;
    }

    nav {
      background: #34495e;
      padding: 10px;
      display: flex;
      justify-content: center;
      gap: 15px;
    }

    nav button {
      padding: 10px 15px;
      border: none;
      background: #1abc9c;
      color: white;
      cursor: pointer;
      border-radius: 5px;
    }

    nav button:hover {
      background: #16a085;
    }

    .container {
      padding: 20px;
    }

    .section {
      display: none;
      background: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    .section.active {
      display: block;
    }

    h2 {
      margin-top: 0;
      color: #2c3e50;
    }

    input, select {
      padding: 8px;
      width: 100%;
      margin: 8px 0;
    }

    button.add {
      background: #3498db;
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 5px;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
    }

    table, th, td {
      border: 1px solid #ccc;
    }

    th, td {
      padding: 10px;
      text-align: center;
    }

    footer {
      text-align: center;
      padding: 10px;
      margin-top: 20px;
      color: #777;
    }
  </style>
</head>
<body>

<header>School Management System</header>

<nav>
  <button onclick="showSection('dashboard')">Dashboard</button>
  <button onclick="showSection('students')">Students</button>
  <button onclick="showSection('teachers')">Teachers</button>
  <button onclick="showSection('attendance')">Attendance</button>
</nav>

<div class="container">

  <div id="dashboard" class="section active">
    <h2>Dashboard</h2>
    <p>Welcome to the School Management System project.</p>
    <ul>
      <li>Manage Students</li>
      <li>Manage Teachers</li>
      <li>Track Attendance</li>
    </ul>
  </div>

  <div id="students" class="section">
    <h2>Student Management</h2>
    <input type="text" id="studentName" placeholder="Student Name">
    <input type="text" id="studentClass" placeholder="Class">
    <button class="add" onclick="addStudent()">Add Student</button>

    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Class</th>
        </tr>
      </thead>
      <tbody id="studentTable"></tbody>
    </table>
  </div>

  <div id="teachers" class="section">
    <h2>Teacher Management</h2>
    <input type="text" id="teacherName" placeholder="Teacher Name">
    <input type="text" id="teacherSubject" placeholder="Subject">
    <button class="add" onclick="addTeacher()">Add Teacher</button>

    <table>
      <thead>
        <tr>
          <th>Name</th>
          <th>Subject</th>
        </tr>
      </thead>
      <tbody id="teacherTable"></tbody>
    </table>
  </div>

  <div id="attendance" class="section">
    <h2>Attendance</h2>
    <select id="attendanceStatus">
      <option value="Present">Present</option>
      <option value="Absent">Absent</option>
    </select>
    <button class="add" onclick="markAttendance()">Mark Attendance</button>

    <table>
      <thead>
        <tr>
          <th>Status</th>
        </tr>
      </thead>
      <tbody id="attendanceTable"></tbody>
    </table>
  </div>

</div>

<footer>© 2026 School Management Project</footer>

<script>
  function showSection(id) {
    document.querySelectorAll('.section').forEach(sec => {
      sec.classList.remove('active');
    });
    document.getElementById(id).classList.add('active');
  }

  function addStudent() {
    let name = document.getElementById('studentName').value;
    let cls = document.getElementById('studentClass').value;

    if (name === '' || cls === '') {
      alert('Please fill all fields');
      return;
    }

    let row = `<tr><td>${name}</td><td>${cls}</td></tr>`;
    document.getElementById('studentTable').innerHTML += row;

    document.getElementById('studentName').value = '';
    document.getElementById('studentClass').value = '';
  }

  function addTeacher() {
    let name = document.getElementById('teacherName').value;
    let subject = document.getElementById('teacherSubject').value;

    if (name === '' || subject === '') {
      alert('Please fill all fields');
      return;
    }

    let row = `<tr><td>${name}</td><td>${subject}</td></tr>`;
    document.getElementById('teacherTable').innerHTML += row;

    document.getElementById('teacherName').value = '';
    document.getElementById('teacherSubject').value = '';
  }

  function markAttendance() {
    let status = document.getElementById('attendanceStatus').value;
    let row = `<tr><td>${status}</td></tr>`;
    document.getElementById('attendanceTable').innerHTML += row;
  }
</script>

</body>
</html>
