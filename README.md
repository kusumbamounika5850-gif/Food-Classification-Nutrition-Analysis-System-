<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Food Vision AI</title>

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:'Poppins',sans-serif;
    }

    body{
      background:#0f172a;
      color:white;
      line-height:1.7;
    }

    header{
      background:linear-gradient(135deg,#ff6b6b,#ff914d);
      padding:80px 20px;
      text-align:center;
    }

    header h1{
      font-size:3rem;
      margin-bottom:20px;
    }

    header p{
      max-width:900px;
      margin:auto;
      font-size:1.1rem;
    }

    .container{
      width:90%;
      max-width:1200px;
      margin:auto;
      padding:50px 0;
    }

    .section-title{
      color:#ff914d;
      font-size:2rem;
      margin-bottom:30px;
      border-left:5px solid #ff914d;
      padding-left:15px;
    }

    .card{
      background:#1e293b;
      padding:35px;
      margin-bottom:35px;
      border-radius:20px;
      box-shadow:0 5px 20px rgba(0,0,0,0.3);
    }

    .grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
      gap:20px;
    }

    .feature{
      background:#111827;
      padding:25px;
      border-radius:15px;
      transition:0.3s;
    }

    .feature:hover{
      transform:translateY(-8px);
      background:#1f2937;
    }

    .feature h3{
      color:#ff914d;
      margin-bottom:10px;
    }

    .badge-container{
      display:flex;
      flex-wrap:wrap;
      gap:15px;
      margin-top:20px;
    }

    .badge{
      background:#ff914d;
      padding:10px 18px;
      border-radius:30px;
      font-size:14px;
      font-weight:600;
    }

    .image-box{
      margin-top:25px;
    }

    .image-box img{
      width:100%;
      border-radius:15px;
      border:3px solid #ff914d;
    }

    .code{
      background:black;
      color:#00ff99;
      padding:15px;
      border-radius:10px;
      overflow:auto;
      margin-top:15px;
    }

    ul{
      padding-left:20px;
    }

    li{
      margin-bottom:12px;
    }

    footer{
      background:#020617;
      text-align:center;
      padding:50px 20px;
      margin-top:50px;
    }

    footer h2{
      color:#ff914d;
      margin-bottom:15px;
    }

    @media(max-width:768px){

      header h1{
        font-size:2.2rem;
      }

    }

  </style>
</head>

<body>

  <!-- HERO SECTION -->

  <header>

    <h1>🍔 Food Vision AI</h1>

    <p>
      Deep Learning Powered Food Classification & Nutrition Analysis System using 
      <strong>Custom CNN</strong>, 
      <strong>VGG16</strong>, and 
      <strong>ResNet50</strong>.
    </p>

  </header>

  <div class="container">

    <!-- PROJECT OVERVIEW -->

    <section class="card">

      <h2 class="section-title">📌 Project Overview</h2>

      <p>
        Food Vision AI is an intelligent AI-powered food classification and nutrition analysis system 
        developed using Deep Learning and Computer Vision technologies.
      </p>

      <br>

      <p>
        The system predicts food categories from uploaded images and displays nutrition information,
        prediction confidence scores, and AI analytics through a modern responsive dashboard.
      </p>

      <br>

      <h3 style="color:#ff914d;">🚀 Practical Applications</h3>

      <ul>
        <li>Computer Vision</li>
        <li>Transfer Learning</li>
        <li>Deep Learning Deployment</li>
        <li>Flask Backend Development</li>
        <li>Redis Integration</li>
      </ul>

    </section>

    <!-- FEATURES -->

    <section class="card">

      <h2 class="section-title">🚀 Features</h2>

      <div class="grid">

        <div class="feature">
          <h3>🍕 Food Classification</h3>
          <p>AI-powered food image recognition system.</p>
        </div>

        <div class="feature">
          <h3>📊 Confidence Score</h3>
          <p>Displays prediction confidence in real time.</p>
        </div>

        <div class="feature">
          <h3>🥗 Nutrition Analysis</h3>
          <p>Shows calories, protein, fat, and nutrition data.</p>
        </div>

        <div class="feature">
          <h3>⚡ Redis Integration</h3>
          <p>Fast nutrition data retrieval using Redis.</p>
        </div>

        <div class="feature">
          <h3>🧠 Multiple Models</h3>
          <p>Custom CNN, VGG16, and ResNet50 support.</p>
        </div>

        <div class="feature">
          <h3>📸 Instant Upload</h3>
          <p>Upload and analyze food images instantly.</p>
        </div>

      </div>

    </section>

    <!-- MODELS -->

    <section class="card">

      <h2 class="section-title">🧠 Deep Learning Models</h2>

      <div class="grid">

        <div class="feature">
          <h3>🔹 Custom CNN</h3>
          <p>
            Custom-built Convolutional Neural Network trained specifically for food image classification.
          </p>
        </div>

        <div class="feature">
          <h3>🔹 VGG16</h3>
          <p>
            Transfer Learning model using pretrained ImageNet weights for high-accuracy prediction.
          </p>
        </div>

        <div class="feature">
          <h3>🔹 ResNet50</h3>
          <p>
            Advanced Residual Neural Network architecture for deep feature learning and better performance.
          </p>
        </div>

      </div>

    </section>

    <!-- TECHNOLOGIES -->

    <section class="card">

      <h2 class="section-title">💻 Technologies Used</h2>

      <div class="badge-container">

        <div class="badge">Python</div>
        <div class="badge">Flask</div>
        <div class="badge">TensorFlow</div>
        <div class="badge">Keras</div>
        <div class="badge">OpenCV</div>
        <div class="badge">Redis</div>
        <div class="badge">HTML5</div>
        <div class="badge">CSS3</div>
        <div class="badge">JavaScript</div>

      </div>

    </section>

    <!-- APPLICATION PREVIEW -->

    <section class="card">

      <h2 class="section-title">📸 Application Preview</h2>

      <h3 style="color:#ff914d;">🔹 Before Prediction</h3>

      <div class="image-box">
        <img src="before.png" alt="Before Prediction">
      </div>

      <br><br>

      <h3 style="color:#ff914d;">🔹 Prediction Results</h3>

      <div class="image-box">
        <img src="after.png" alt="Prediction Results">
      </div>

    </section>

    <!-- HOW IT WORKS -->

    <section class="card">

      <h2 class="section-title">⚙️ How It Works</h2>

      <ol style="padding-left:20px;">

        <li>Upload food image</li>
        <li>AI model processes image</li>
        <li>Food category gets predicted</li>
        <li>Nutrition data fetched from Redis</li>
        <li>Confidence score generated</li>
        <li>Results displayed on dashboard</li>

      </ol>

    </section>

    <!-- INSTALLATION -->

    <section class="card">

      <h2 class="section-title">📦 Installation</h2>

      <h3>1️⃣ Clone Repository</h3>

      <div class="code">
git clone https://github.com/your-username/food-vision-ai.git
cd food-vision-ai
      </div>

      <br>

      <h3>2️⃣ Create Virtual Environment</h3>

      <div class="code">
python -m venv .venv
      </div>

      <br>

      <h3>3️⃣ Activate Environment</h3>

      <div class="code">
.venv\Scripts\activate
      </div>

      <br>

      <h3>4️⃣ Install Dependencies</h3>

      <div class="code">
pip install -r requirements.txt
      </div>

      <br>

      <h3>5️⃣ Run Application</h3>

      <div class="code">
python app.py
      </div>

    </section>

    <!-- FUTURE -->

    <section class="card">

      <h2 class="section-title">🎯 Future Improvements</h2>

      <ul>

        <li>Real-time webcam prediction</li>
        <li>Mobile application support</li>
        <li>Multi-food detection</li>
        <li>Cloud deployment</li>
        <li>Voice assistant integration</li>
        <li>Calorie tracking system</li>

      </ul>

    </section>

  </div>

  <!-- FOOTER -->

  <footer>

    <h2>👨‍💻 Developer</h2>

    <p><strong>Mounika Kusumba</strong></p>

    <p>
      AI Engineer & Deep Learning Developer
    </p>

    <br>

    <p>
      Computer Vision | TensorFlow | OpenCV | Deep Learning
    </p>

  </footer>

</body>
</html>
