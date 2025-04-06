<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Infinity Tours and Travels</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background: #f1f3f6;
      color: #333;
      padding: 20px;
    }

    h1 {
      text-align: center;
      margin-bottom: 20px;
      color: #1e2a38;
    }

    .container {
      max-width: 800px;
      margin: auto;
    }

    .card {
      background: white;
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.08);
      margin-bottom: 20px;
    }

    .card img {
      width: 100%;
      border-radius: 12px;
      margin-bottom: 10px;
    }

    .card h2 {
      font-size: 1.3rem;
      margin-bottom: 10px;
      color: #173e6d;
    }

    .card p {
      margin-bottom: 10px;
    }

    .card button {
      background: #007f5f;
      color: white;
      padding: 10px 15px;
      border: none;
      border-radius: 10px;
      font-size: 1rem;
      cursor: pointer;
      width: 100%;
    }

    .card button:hover {
      background: #006747;
    }

    .cost {
      font-weight: bold;
      color: #d97706;
    }

    .whatsapp-btn {
      display: block;
      text-align: center;
      background: #25d366;
      color: white;
      padding: 14px;
      border-radius: 12px;
      font-size: 1.2rem;
      text-decoration: none;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }

    .whatsapp-btn:hover {
      background: #1ebe5d;
    }

    input[type="number"] {
      width: 100%;
      padding: 10px;
      border-radius: 10px;
      border: 1px solid #ccc;
      font-size: 1rem;
      margin-top: 10px;
      margin-bottom: 10px;
    }

    @media (max-width: 600px) {
      h1 {
        font-size: 1.5rem;
      }

      .card h2 {
        font-size: 1.1rem;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Infinity Tours and Travels</h1>

    <!-- Custom Trip -->
    <div class="card">
      <h2>Calculate Custom Trip</h2>
      <input type="number" id="customDistance" placeholder="Enter distance in km" />
      <button onclick="customCalculate()">Calculate</button>
      <p>Estimated Cost: <span class="cost" id="customCost">₹0</span></p>
    </div>

    <!-- Destination Cards -->
    <div class="card">
      <h2>Lonavala</h2>
      <img src="https://upload.wikimedia.org/wikipedia/commons/2/2b/Lonavla_view.jpg" alt="Lonavala" />
      <p>Distance: 65 km</p>
      <p>Estimated Cost: <span class="cost" id="cost1">₹0</span></p>
      <button onclick="calculateCost(65, 'cost1')">Calculate</button>
    </div>

    <div class="card">
      <h2>Mahabaleshwar</h2>
      <img src="https://upload.wikimedia.org/wikipedia/commons/7/7e/Mahabaleshwar.jpg" alt="Mahabaleshwar" />
      <p>Distance: 120 km</p>
      <p>Estimated Cost: <span class="cost" id="cost2">₹0</span></p>
      <button onclick="calculateCost(120, 'cost2')">Calculate</button>
    </div>

    <div class="card">
      <h2>Lavasa</h2>
      <img src="https://upload.wikimedia.org/wikipedia/commons/b/bf/Lavasa_City_View.jpg" alt="Lavasa" />
      <p>Distance: 60 km</p>
      <p>Estimated Cost: <span class="cost" id="cost3">₹0</span></p>
      <button onclick="calculateCost(60, 'cost3')">Calculate</button>
    </div>

    <div class="card">
      <h2>Matheran</h2>
      <img src="https://upload.wikimedia.org/wikipedia/commons/4/43/Matheran_Valley_View.jpg" alt="Matheran" />
      <p>Distance: 125 km</p>
      <p>Estimated Cost: <span class="cost" id="cost4">₹0</span></p>
      <button onclick="calculateCost(125, 'cost4')">Calculate</button>
    </div>

    <div class="card">
      <h2>Alibaug</h2>
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/34/Alibaug_Beach.jpg" alt="Alibaug" />
      <p>Distance: 143 km</p>
      <p>Estimated Cost: <span class="cost" id="cost5">₹0</span></p>
      <button onclick="calculateCost(143, 'cost5')">Calculate</button>
    </div>

    <a class="whatsapp-btn" href="https://wa.me/917769889009" target="_blank">Book Now on WhatsApp</a>
  </div>

  <script>
    function calculateCost(distance, elementId) {
      const rate = 13;
      const cost = distance * rate;
      document.getElementById(elementId).textContent = `₹${cost}`;
    }

    function customCalculate() {
      const distance = parseFloat(document.getElementById("customDistance").value);
      const rate = 13;
      if (!isNaN(distance) && distance > 0) {
        const cost = distance * rate;
        document.getElementById("customCost").textContent = `₹${cost}`;
      } else {
        alert("Please enter a valid distance in kilometers.");
      }
    }
  </script>
</body>
</html>
