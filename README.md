<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Scientific Number Checker</title>
<style>
    body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
  }
  
  header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 20px 0;
  }
  
  nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    text-align: center;
  }
  
  nav ul li {
    display: inline;
    margin-right: 20px;
  }
  
  nav ul li a {
    text-decoration: none;
    color: #333;
  }
  
  .container {
    margin: 20px auto;
    width: 80%;
    text-align: center;
  }
  
  form {
    margin-bottom: 20px;
  }
  
  input[type="text"] {
    padding: 8px;
    width: 200px;
  }
  
  button {
    padding: 8px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #45a049;
  }
  
  #result {
    font-size: 18px;
    font-weight: bold;
  }
  
  footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 0;
    position: fixed;
    bottom: 0;
    width: 100%;
  }
</style>
<link rel="stylesheet" href="styles.css">
</head>
<body>
<header>
    <h1>Scientific Number Checker</h1>
    <script>
document.getElementById('scientificForm').addEventListener('submit', function(event) {
  event.preventDefault();
  var input = document.getElementById('scientificNumber').value;
  var result = document.getElementById('result');

  if (isScientificNumber(input)) {
    result.textContent = "Yes, it is a scientific number.";
  } else {
    result.textContent = "No, it is not a scientific number.";
  }
});

function isScientificNumber(input) {
  var scientificNumberRegex = /^[-+]?[0-9]*\.?[0-9]+([eE][-+]?[0-9]+)?$/;
  return scientificNumberRegex.test(input);
}
    </script>
</header>
<nav>
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About Us</a></li>
        <li><a href="#upload">Upload</a></li>
        <li><a href="#edit">Edit</a></li>
        <li><a href="#run">Run</a></li>
    </ul>
</nav>
<div class="container" id="home">
    <form id="scientificForm">
        <label for="scientificNumber">INPUT STRING:</label>
        <input type="text" id="scientificNumber" name="scientificNumber" required>
        <button type="submit">Check</button>
    </form>
    <div id="result"></div>
</div>
<div class="container" id="about">
    <h2>About Us</h2>
    <p>This is the about us page. You can add information about your team here.</p>
</div>
<div class="container" id="upload">
    <h2>Upload File</h2>
    <!-- Form for uploading files -->
</div>
<div class="container" id="edit">
    <h2>Edit File</h2>
    <!-- Form for editing files -->
</div>
<div class="container" id="run">
    <h2>Run File</h2>
    <!-- Button to run the file -->
</div>
<footer>
    <p>&copy; 2024 Scientific Number Checker</p>
</footer>
<script src="script.js"></script>
</body>
</html>
