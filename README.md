<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portfolio Login</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f2f2f2;
      margin: 0;
      padding: 0;
    }
    .container {
      max-width: 400px;
      margin: 100px auto;
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    input[type="text"], input[type="password"] {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    button {
      width: 100%;
      padding: 10px;
      background: #4CAF50;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    button:hover {
      background: #45a049;
    }
    .error {
      color: red;
      margin-top: 10px;
    }
    .dashboard {
      display: none;
      max-width: 800px;
      margin: 50px auto;
      background: #fff;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    table {
      width: 100%;
      border-collapse: collapse;
    }
    table, th, td {
      border: 1px solid #ccc;
    }
    th, td {
      padding: 10px;
      text-align: center;
    }
    th {
      background-color: #f4f4f4;
    }
  </style>
</head>
<body>
  <div class="container" id="login-box">
    <h2>Login</h2>
    <input type="text" id="username" placeholder="Username">
    <input type="password" id="password" placeholder="Password">
    <button onclick="login()">Login</button>
    <div class="error" id="error-msg"></div>
  </div>  <div class="dashboard" id="dashboard">
    <h2>Work Score Table</h2>
    <table>
      <tr>
        <th>Name</th>
        <th>Date</th>
        <th>No. of ACC</th>
        <th>Payment</th>
      </tr>
      <tr>
        <td>John Doe</td>
        <td>2025-03-30</td>
        <td>10</td>
        <td>$100</td>
      </tr>
      <tr>
        <td>Jane Smith</td>
        <td>2025-03-29</td>
        <td>8</td>
        <td>$80</td>
      </tr>
    </table>
  </div>  <script>
    const users = {
      "akash": "1234",
      "admin": "admin123"
    };

    function login() {
      const user = document.getElementById("username").value;
      const pass = document.getElementById("password").value;
      const errorMsg = document.getElementById("error-msg");

      if (users[user] && users[user] === pass) {
        document.getElementById("login-box").style.display = "none";
        document.getElementById("dashboard").style.display = "block";
      } else {
        errorMsg.textContent = "Invalid username or password.";
      }
    }
  </script></body>
</html>
