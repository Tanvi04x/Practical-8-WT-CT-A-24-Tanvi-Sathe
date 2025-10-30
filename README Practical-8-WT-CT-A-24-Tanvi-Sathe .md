# Practical-8-WT-CT-A-24-Tanvi-Sathe
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript Loops, Conditional Statements, and Functions</title>
  <style>
    body {
      font-family: "Poppins", sans-serif;
      background: linear-gradient(135deg, #a1c4fd, #c2e9fb);
      padding: 20px;
      line-height: 1.6;
    }
    h2 {
      color: #2c3e50;
    }
    button {
      background-color: #4CAF50;
      color: white;
      border: none;
      padding: 10px 15px;
      margin: 5px 0;
      border-radius: 5px;
      cursor: pointer;
      transition: 0.3s;
    }
    button:hover {
      background-color: #45a049;
    }
    .output {
      background: #fff;
      padding: 15px;
      border-radius: 8px;
      margin-top: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
  </style>
</head>
<body>

  <h1>JavaScript Example</h1>

  <h2>[A] While and For Loop</h2>
  <p>This program takes a number from the user and prints numbers up to that limit using <b>while</b> and <b>for</b> loops.</p>
  <button onclick="demoLoops()">Run Loop Example</button>
  <div id="loopOutput" class="output"></div>

  <hr>


  <h2>[B] Conditional Statements and Functions </h2>
  <p>This program takes marks from the user and displays the grade using <b>conditional statements</b> inside a <b>function</b>.</p>
  <button onclick="demoCondition()">Run Conditional Example</button>
  <div id="condOutput" class="output"></div>

  <script>
    
    function demoLoops() {
      let limit = prompt("Enter the number up to which you want to print:");
      limit = parseInt(limit);
      if (isNaN(limit) || limit <= 0) {
        document.getElementById("loopOutput").innerHTML = "❌ Please enter a valid positive number.";
        return;
      }

      let output = "<b>Using While Loop:</b><br>";
      let i = 1;

      while (i <= limit) {
        output += "Number (while): " + i + "<br>";
        i++;
      }

      output += "<br><b>Using For Loop:</b><br>";
      for (let j = 1; j <= limit; j++) {
        output += "Number (for): " + j + "<br>";
      }

      document.getElementById("loopOutput").innerHTML = output;
    }

    function checkGrade(marks) {
      if (marks >= 90) {
        return "Grade A (Excellent)";
      } else if (marks >= 75) {
        return "Grade B (Good)";
      } else if (marks >= 50) {
        return "Grade C (Average)";
      } else {
        return "Fail (Needs Improvement)";
      }
    }

    function demoCondition() {
      let marks = prompt("Enter your marks (0-100):");
      marks = parseInt(marks);

      if (isNaN(marks) || marks < 0 || marks > 100) {
        document.getElementById("condOutput").innerHTML = "❌ Please enter a valid mark between 0 and 100.";
        return;
      }

      let result = checkGrade(marks);
      document.getElementById("condOutput").innerHTML =
        "You entered: " + marks + "<br>Your Result: <b>" + result + "</b>";
    }
  </script>

</body>
</html>
