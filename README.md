<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Anthony's Tech Universe</title>
  <style>
    body {
      background-color: #121212; /* Dark background */
      color: #00ff00; /* Neon green text */
      font-family: 'Courier New', Courier, monospace; 
      text-align: center;
    }
    a {
      color: #00ffff; /* Cyan links */
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }
    .container {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
    }
    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .card {
      background-color: rgba(0, 255, 0, 0.1); /* Neon green card background */
      border: 2px solid #00ff00;
      border-radius: 10px;
      padding: 20px;
      transition: all 0.3s ease;
    }
    .card:hover {
      box-shadow: 0 0 20px #00ff00;
      transform: translateY(-5px);
    }
    .skill-bar {
      height: 30px;
      background-color: #333;
      border-radius: 5px;
      margin-bottom: 10px;
      overflow: hidden;
    }
    .skill-level {
      height: 100%;
      background-color: #00ff00;
      width: 0%; /* Initial width 0% */
      transition: width 0.5s ease-in-out;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1><span style="color: #00ffff;">Anthony's</span> Tech Universe</h1> 

   <div class="grid">
      <div class="card">
        <h2><span style="color: #ff00ff;">// </span>Coding Arsenal</h2>
        <div class="skill-bar">
          <div class="skill-level" style="width: 90%;" data-skill="JavaScript"></div>
        </div>
        JavaScript (90%)
        <div class="skill-bar">
          <div class="skill-level" style="width: 80%;" data-skill="Python"></div>
        </div>
        Python (80%)
        <div class="skill-bar">
          <div class="skill-level" style="width: 75%;" data-skill="React"></div>
        </div>
        React (75%)
        <!-- Add more skills here -->
      </div>

    <div class="card">
        <h2><span style="color: #ff00ff;">// </span>Project Gallery</h2>
        <!-- Project links here -->
        <a href="#">Project 1</a><br>
        <a href="#">Project 2</a><br>
        <a href="#">Project 3</a>
      </div>

      <div class="card">
        <h2><span style="color: #ff00ff;">// </span>Connect</h2>
        <!-- Contact links here -->
        <a href="#">GitHub</a><br>
        <a href="#">LinkedIn</a><br>
        <a href="#">Email</a>
      </div>
    </div>
  </div>

  <script>
    // Optional: Add JavaScript for interactive elements like tooltips on skill bars
    const skillBars = document.querySelectorAll('.skill-bar');
    skillBars.forEach(bar => {
      bar.addEventListener('mouseover', () => {
        const skillLevel = bar.querySelector('.skill-level');
        const skillName = skillLevel.dataset.skill;
        // You could display a tooltip here with the skill name
      });
    });
  </script>
</body>
</html>
