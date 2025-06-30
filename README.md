# alex-portfolio
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Alex Styles Portfolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Alex Styles</h1>
    <p>Web Developer | Designer | Coder</p>
  </header>

  <main class="container">
    <section class="portfolio-item" title="Project 1: Personal Website">
      <h2>Project 1</h2>
      <p>Responsive personal website using HTML, CSS and Copilot enhancements.</p>
      <button onclick="showModal()">View Details</button>
    </section>
  </main>

  <!-- Modal -->
  <div id="modal" class="modal">
    <div class="modal-content">
      <span onclick="closeModal()" class="close">&times;</span>
      <h2>Project 1 Details</h2>
      <p>This site demonstrates the use of GitHub Copilot in responsive and polished web design.</p>
    </div>
  </div>

  <script>
    function showModal() {
      document.getElementById('modal').style.display = 'block';
    }
    function closeModal() {
      document.getElementById('modal').style.display = 'none';
    }
  </script>
</body>
</html>

/* CSS: style.css */
body {
  font-family: 'Poppins', sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f8f9fa;
  color: #333;
}

header {
  background: linear-gradient(to right, #4e54c8, #8f94fb);
  padding: 20px;
  text-align: center;
  color: white;
}

.container {
  display: flex;
  justify-content: center;
  padding: 20px;
  gap: 20px;
}

.portfolio-item {
  background-color: white;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  transition: transform 0.2s;
  max-width: 300px;
}

.portfolio-item:hover {
  transform: scale(1.05);
}

.modal {
  display: none;
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-content {
  background-color: white;
  margin: 10% auto;
  padding: 20px;
  width: 80%;
  max-width: 500px;
  border-radius: 8px;
}

.close {
  float: right;
  font-size: 24px;
  cursor: pointer;
}

@media screen and (max-width: 768px) {
  .container {
    flex-direction: column;
    align-items: center;
  }
  header {
    font-size: 18px;
  }
  .portfolio-item {
    width: 90%;
  }
}
